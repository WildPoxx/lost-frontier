# Claude Skills Index - Lost Frontier

This file is the non-hidden mirror for Claude Project Knowledge. The executable Claude Code versions live under:

```text
.claude/skills/lost-frontier-foundry-dev/SKILL.md
.claude/skills/masterquest-quest-ops/SKILL.md
.claude/skills/swade-fvtt-mechanics-model/SKILL.md
```

If `.claude/skills/` is not visible in the current Claude surface, treat the protocols below as the active skill instructions.

Repository coverage note: the matrix repo is `WildPoxx/lost-frontier`. Some FQL/MasterQuest docs referenced below live in the associated repo `WildPoxx/masterquest-fvtt-dev`, locally nested at `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops`. See `docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md` for the current visibility map.

## lost-frontier-foundry-dev

Use for OutsiderS Lost Frontier as a canon, RPG design, and Foundry VTT project. Trigger it when the task involves Lost Frontier files, Foundry VTT v13, SWADE 5.2.6, `module.json`, compendium packs, macros, bestiary, assets, GitHub workflow docs, AI collaboration, or project organization.

Act as a technical, editorial, and organizational collaborator. Mario is the creative director. Preserve his canon authority, explain technical choices in plain Portuguese, and avoid inventing lore, mechanics, names, or structural decisions that the files do not support.

Before substantial work, consult:

- `README.md`
- `AI_COLLABORATION.md`
- `docs/devops/GITHUB_AND_DEPLOY_STRATEGY.md` when the task touches GitHub, deploy, MasterQuest, or repository governance.

For specialized production tasks, consult the relevant fine directive:

- `12. IA e Foundry Tools/Diretrizes/Protocolo_Avancos_SWADE_FVTT_OLF.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes de Construção de Stat Blocks - SBI Safe.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes_Criacao_Criaturas_SWADE_FVTT_OLF.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes de Atualizacao de Relogios - Rust under the Stars.md`
- `03. Aventuras/Aventura 1 - Ferrugem e Estrelas/FQL/Arquitetura de Transposição de Módulo de Aventura para FQL - Plano e Modelos de Script.md`

Baseline:

- Project: **OutsiderS - Lost Frontier**.
- Foundry module id: `outsiders-lost-frontier`.
- Target Foundry: v13 Stable build 351 unless Mario says otherwise.
- Target system: SWADE 5.2.6 unless Mario says otherwise.
- Treat Forien's Quest Log as a recommended integration, not as a mandatory dependency.
- Treat `WildPoxx/masterquest-fvtt-dev` as an associated module/tooling repository, not as the canonical home of Lost Frontier lore.

Workflow:

1. Ground every answer in the current conversation and repository files.
2. Classify the task: canon/editorial, SWADE design, Foundry module, FQL integration, assets, GitHub/deploy, or project organization.
3. Locate relevant files before proposing edits.
4. Before editing, state what will change, why, and how the result will be checked.
5. Keep changes small, reversible, and consistent with existing structure.
6. Preserve installability: do not break `module.json`, pack paths, asset paths, language files, or compatibility metadata.
7. Report what changed, where, how it was validated, and the next concrete step.

Foundry guidance:

- Prefer compendium packs for distributable content.
- Foundry v13 often uses LevelDB pack directories; do not assume a pack is a single `.db` file.
- Preserve existing UUIDs and asset paths unless deliberately migrating them.
- If a macro depends on FQL, check that `forien-quest-log` is active and give a clear GM-facing warning when it is not.
- For portability, prefer name/compendium resolution where practical, while preserving working UUIDs already present.

## masterquest-quest-ops

Use for MasterQuest and Lost Frontier quest operations, Forien's Quest Log, TAM diagnostics, or migration from legacy FQL behavior into OLF-owned workflows. Trigger it for MasterQuest work, FQL legacy payloads, `JournalEntry` quest trees, `flags["forien-quest-log"].json`, TAM logs/macros, quest and subquest topology, GM control panels, dry-run patch plans, backup-safe updates, or OLF replacements for FQL internals.

Core stance:

- Treat Mario as creative director and as a non-specialist in code and JSON.
- Explain technical terms in plain Portuguese.
- Treat FQL as a useful legacy base, not as a design ceiling.
- Prefer a bridge-first rewrite: preserve existing campaign data while moving validation, migration, diagnostics, GM confirmation, and write safety into OLF code.

Some FQL/MasterQuest files below live in the associated repository `WildPoxx/masterquest-fvtt-dev`. If they are not visible in Claude Project Knowledge, ask Mario to connect or attach that repository.

Read first when available:

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
- `docs/devops/GITHUB_AND_DEPLOY_STRATEGY.md`

Legacy contract:

- FQL stores quests as `JournalEntry`.
- The canonical FQL payload lives in `flags["forien-quest-log"].json`.
- FQL often anchors quest entries under `_fql_quests`.
- OLF/TAM macros may add metadata under `flags["outsiders-lost-frontier"]`.

Preserve at minimum `tasks`, `rewards`, `gmnotes`, `playernotes`, `status`, `parent`, `subquests`, and unknown fields that are not proven disposable.

Quest operations should pass through these layers:

1. legacy read layer
2. validated OLF read model
3. diagnostic layer
4. patch-plan layer
5. GM confirmation layer
6. write/apply layer
7. post-apply validation and refresh layer

For writes, inspect payloads, produce dry-run/patch preview, back up first, sanitize only by explicit rule, apply idempotently, and validate tree consistency. Default to archive over delete.

Watch for invalid `rewards`, invalid `tasks`, duplicate quests/subquests, Journal/FQL state drift, and unrelated Foundry v13 warning noise.

## swade-fvtt-mechanics-model

Use for SWADE 5.2.6 rules and Foundry VTT 13.351 implementation in Lost Frontier. Trigger it for Bennies, Wild Die, Support, Fear, Hazards, Quick Encounters, Chases, Dramatic Tasks, Social Conflict, Travel, actors, items, combat, journals, JSON, module integration, or adventure design using SWADE in Foundry.

Work on two linked planes:

- **SWADE as tabletop RPG**: rules, GM procedures, scene design, encounters, and dramatic structure.
- **SWADE as Foundry system**: actors, items, combat, cards, chat, settings, JSON, system documents, and implementation behavior.

Baseline:

- Foundry VTT `13.351`
- SWADE `5.2.6`
- Lost Frontier module id `outsiders-lost-frontier`

Do not import behavior from newer SWADE or Foundry versions without saying that it may differ from the project baseline.

The `olf-fql-campaign-ops` docs and fixtures referenced below live in the associated repository `WildPoxx/masterquest-fvtt-dev`. If they are not visible in Claude Project Knowledge, ask Mario to connect or attach that repository before doing deep SWADE/FVTT implementation work.

Separate three layers:

- **table rule**: what the book or game procedure says;
- **FVTT implementation**: how SWADE represents it in actors, items, combat, chat, settings, hooks, or UI;
- **OLF custom layer**: how Lost Frontier reads, organizes, reports, or updates it.

Read first when available:

1. `README.md`
2. `AI_COLLABORATION.md`
3. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/17_SWADE_5_2_6_FVTT_Baseline.md`
4. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/18_SWADE_FVTT_Skill_Spec.md`
5. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/fixtures/swade_5_2_6/technical.index.json`

For specific production protocols, read:

- `12. IA e Foundry Tools/Diretrizes/Protocolo_Avancos_SWADE_FVTT_OLF.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes de Construção de Stat Blocks - SBI Safe.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes_Criacao_Criaturas_SWADE_FVTT_OLF.md`

For rules questions, explain the mechanic simply, say what the player or GM does at the table, then explain Foundry behavior if useful.

For development questions, identify relevant SWADE document types and data flow, inspect manifests/data models/settings/hooks/JSON examples before proposing code, and prefer observed contracts over memory.

For adventure or encounter design, choose the right SWADE tool before defaulting to combat. Consider Dramatic Tasks, Quick Encounters, Chases, Social Conflict, Travel, Fear, Hazards, Interludes, and Mass Battles.

Guardrails:

- Explain `flags`, `manifest`, `document class`, `data model`, and `pack` when needed.
- Do not confuse a Foundry compendium with a rules sourcebook.
- Do not automate a narrative GM decision.
- Do not write to actors, combats, journals, packs, or settings without preview and approval.
- When the book rule and Foundry behavior diverge, name the difference explicitly.
