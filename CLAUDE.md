# Claude Project Instructions - Lost Frontier

Use this file as the first orientation point for Claude sessions working with **OutsiderS - Lost Frontier**.

## Required Reading

Read these before giving project-level answers:

1. `README.md`
2. `AI_COLLABORATION.md`
3. `docs/ai/CLAUDE_SKILLS_INDEX.md`

If the environment exposes `.claude/skills/`, use those files as the executable Claude Code skills. If the environment is Claude Project Knowledge and does not expose hidden directories, use `docs/ai/CLAUDE_SKILLS_INDEX.md` as the non-hidden mirror of the same protocols.

## Core Rules

- Respond in Portuguese by default.
- Treat Mario as the creative director.
- Preserve canon, tone, continuity, and table-facing intent.
- Do not invent lore, mechanics, names, facts, repository state, or Foundry behavior not supported by files.
- Explain code, JSON, Git, Foundry manifests, packs, and SWADE/FVTT behavior in plain language when they matter.
- Separate what exists today, what is inferred, and what still needs Mario's decision.

## Project Baseline

- Project: **OutsiderS - Lost Frontier**.
- Foundry module id: `outsiders-lost-frontier`.
- Target Foundry: v13 Stable build 351 unless Mario says otherwise.
- Target system: SWADE 5.2.6 unless Mario says otherwise.
- Treat Forien's Quest Log as a recommended integration, not as a mandatory dependency for all OLF work.
- Treat `WildPoxx/masterquest-fvtt-dev` as an associated module/tooling repository, not as the canonical home of Lost Frontier lore.

## Skill Routing

- Use `lost-frontier-foundry-dev` for general OLF, Foundry module, repository, canon-production, pack, macro, asset, and GitHub workflow work.
- Use `fql-olf-quest-ops-architecture` for FQL legacy payloads, quest trees, TAM logs/macros, migration, diagnostics, patch plans, backups, or GM operations panels.
- Use `swade-fvtt-mechanics-model` for SWADE 5.2.6 rules, Foundry implementation questions, actor/item/combat/journal JSON, and adventure mechanics.

When a task touches more than one area, combine the relevant protocols and say which ones are being used.
