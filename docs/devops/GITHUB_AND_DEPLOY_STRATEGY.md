# GitHub And Deploy Strategy - Lost Frontier

## Repository Model

Lost Frontier should use two associated repositories:

- `WildPoxx/lost-frontier`: private matrix repository for canon, planning, project governance, Foundry notes, and selected OLF production documents.
- `WildPoxx/masterquest-fvtt-dev`: module repository for MasterQuest / `olf-fql-campaign-ops`, including tests, packaging, GitHub Actions, and Foundry server deploy.

MasterQuest is an associated module/tooling project, not the canonical source for Lost Frontier lore.

## Local Paths

- Lost Frontier root:
  `C:\Users\amari\source\OLF\Lost Frontier`

- MasterQuest local repository:
  `C:\Users\amari\source\OLF\Lost Frontier\12. IA e Foundry Tools\Modulo FQL - OLF - Hack\olf-fql-campaign-ops`

## GitHub Access

GitHub CLI is installed locally, but may not be available in every PowerShell session through `PATH`.

Known executable:

```powershell
C:\Users\amari\AppData\Local\Microsoft\WinGet\Packages\GitHub.cli_Microsoft.Winget.Source_8wekyb3d8bbwe\bin\gh.exe
```

Known authenticated account:

```text
WildPoxx
```

Required scopes for repository and workflow work:

```text
repo, workflow
```

## MasterQuest Deploy

MasterQuest has a validated manual GitHub Actions deploy workflow:

```text
.github/workflows/manual-foundry-deploy.yml
```

Supported modes:

- `package-only`: run deploy-safe tests and build the package.
- `dry-run`: build package and verify SSH/server path without changing server files.
- `deploy`: back up the existing module folder and replace it on the Foundry server.

Manual deploy is intentional because the Foundry server is live campaign infrastructure.

## Foundry Server Facts

Non-secret operational values:

```text
FOUNDRY_HOST=168.75.93.69
FOUNDRY_USER=ubuntu
FOUNDRY_PORT=22
FOUNDRY_MODULES_PATH=/home/ubuntu/.local/share/FoundryVTT/Data/modules
```

Do not commit private keys or GitHub secrets. The private SSH key belongs only in GitHub Actions secrets or the local `.ssh` folder.

## Safety Rules

Do not commit:

- private SSH keys;
- GitHub tokens;
- `.env` files;
- Foundry license keys;
- server passwords;
- raw private campaign logs;
- live-world snapshots with secrets;
- sourcebooks, third-party modules, vendor ZIPs, or commercial assets;
- generated/heavy media unless deliberately handled through Git LFS or releases.

## Recommended First GitHub Flow

1. Keep `WildPoxx/masterquest-fvtt-dev` as the module repository.
2. Create private `WildPoxx/lost-frontier` as the matrix repository.
3. Push only the curated baseline first.
4. Connect the Claude project to `WildPoxx/lost-frontier`.
5. Add more files by curated topic, not with a blind `git add .`.

