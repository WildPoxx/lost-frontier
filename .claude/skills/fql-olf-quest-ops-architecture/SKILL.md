---
name: fql-olf-quest-ops-architecture
description: Engineer, diagnose, migrate, or extend Lost Frontier quest operations built from Forien's Quest Log concepts. Use when working with FQL legacy payloads, JournalEntry quest trees, flags["forien-quest-log"].json, TAM logs/macros, quest and subquest topology, GM control panels, dry-run patch plans, backup-safe updates, or OLF replacements for FQL internals.
---

# FQL OLF Quest Ops Architecture

Use this skill when Lost Frontier work touches quest operations, Forien's Quest Log, TAM diagnostics, or migration from legacy FQL behavior into OLF-owned workflows.

## Core Stance

- Treat Mario as the creative director and as a non-specialist in code and JSON.
- Explain technical terms in plain Portuguese when they matter.
- Treat FQL as a useful legacy base, not as a design ceiling.
- Prefer a bridge-first rewrite: preserve existing campaign data while moving validation, migration, diagnostics, GM confirmation, and write safety into OLF code.

## Read Order

Start from the current repository, not from memory.

Some FQL/MasterQuest files below live in the associated repository `WildPoxx/masterquest-fvtt-dev`, locally nested at `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops`. If they are not visible in Claude Project Knowledge, ask Mario to connect or attach the associated MasterQuest repository.

Read first when they exist:

1. `README.md`
2. `AI_COLLABORATION.md`
3. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/16_Internal_Workplan_And_Skills.md`
4. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/20_FQL_TAM_Logs_And_Architecture_Assessment.md`

Read when relevant:

- `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/17_SWADE_5_2_6_FVTT_Baseline.md`
- `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/19_ChatGPT_Backup_Analysis.md`
- `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/12_Legacy_Scripts_Inventory.md`
- `03. Aventuras/Aventura 1 - Ferrugem e Estrelas/FQL/Arquitetura de Transposição de Módulo de Aventura para FQL - Plano e Modelos de Script.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes de Atualizacao de Relogios - Rust under the Stars.md`
- `docs/devops/GITHUB_AND_DEPLOY_STRATEGY.md` for GitHub, MasterQuest, deploy, or repository boundaries.

If a needed file is not available through Claude's current GitHub/project context, say that clearly and ask Mario to attach it or expose the associated repository.

## Legacy Contract

Assume this baseline unless the files prove otherwise:

- FQL stores quests as `JournalEntry`.
- The canonical FQL payload lives in `flags["forien-quest-log"].json`.
- FQL often anchors quest entries under the `_fql_quests` folder.
- OLF/TAM macros may add parallel metadata under `flags["outsiders-lost-frontier"]`.

Preserve at minimum:

- `tasks`
- `rewards`
- `gmnotes`
- `playernotes`
- `status`
- `parent`
- `subquests`
- unknown fields that are not proven disposable.

Do not strip unknown fields unless there is an explicit validated migration rule.

## Architecture Rule

Separate quest operations into layers:

1. legacy read layer
2. validated OLF read model
3. diagnostic layer
4. patch-plan layer
5. GM confirmation layer
6. write/apply layer
7. post-apply validation and refresh layer

Do not jump from raw legacy payload directly to mutation.

## Write Safety

For any write-capable operation:

1. Inspect current payloads first.
2. Produce a dry-run or patch preview first.
3. Create a backup before mutation.
4. Sanitize only what is justified by an explicit rule.
5. Apply idempotent updates.
6. Re-validate quest tree consistency.
7. Refresh affected views only after data integrity checks.

Default to non-destructive behavior: archive over delete, preserve traceability, and avoid hard deletion unless Mario explicitly requests it.

## Failure Patterns

Watch for:

- invalid `rewards` payloads causing FQL rendering/enrichment failures;
- invalid or partial `tasks` payloads;
- duplicate quests or subquests linked to the wrong parent;
- drift between Journal state and FQL in-memory state;
- Foundry v13 compatibility warnings that are noise rather than the actual OLF problem.

Separate core Foundry warnings, third-party module warnings, SWADE warnings, FQL payload issues, and OLF mutation bugs before diagnosing root cause.

## Output

Be direct. Distinguish clearly between what exists today, what FQL legacy does, what the OLF target should do, and what still needs GM confirmation.
