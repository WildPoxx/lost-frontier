# Project Knowledge Coverage - Lost Frontier

This file records which Claude-oriented guidance files are expected to be visible from the matrix repository and which require the associated MasterQuest repository.

## Matrix Repository

Repository:

```text
WildPoxx/lost-frontier
```

These files are in the matrix repo and should be visible when Claude syncs `WildPoxx/lost-frontier`:

- `CLAUDE.md`
- `AI_COLLABORATION.md`
- `README.md`
- `docs/ai/CLAUDE_SKILLS_INDEX.md`
- `.claude/skills/lost-frontier-foundry-dev/SKILL.md`
- `.claude/skills/masterquest-quest-ops/SKILL.md`
- `.claude/skills/swade-fvtt-mechanics-model/SKILL.md`
- `docs/devops/GITHUB_AND_DEPLOY_STRATEGY.md`
- `docs/ai/HANDOFF_CLAUDE_SKILLS_AND_GITHUB_FOR_VERACRUCIA.md`

Fine operational directives in the matrix repo:

- `12. IA e Foundry Tools/Diretrizes/Protocolo_Avancos_SWADE_FVTT_OLF.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes de Construção de Stat Blocks - SBI Safe.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes_Criacao_Criaturas_SWADE_FVTT_OLF.md`
- `12. IA e Foundry Tools/Diretrizes/Diretrizes de Atualizacao de Relogios - Rust under the Stars.md`
- `03. Aventuras/Aventura 1 - Ferrugem e Estrelas/FQL/Arquitetura de Transposição de Módulo de Aventura para FQL - Plano e Modelos de Script.md`

## Associated MasterQuest Repository

Repository:

```text
WildPoxx/masterquest-fvtt-dev
```

Local nested path:

```text
12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops
```

These files are referenced by the Lost Frontier skills but belong to the associated MasterQuest repository:

- `docs/12_Legacy_Scripts_Inventory.md`
- `docs/16_Internal_Workplan_And_Skills.md`
- `docs/17_SWADE_5_2_6_FVTT_Baseline.md`
- `docs/18_SWADE_FVTT_Skill_Spec.md`
- `docs/19_ChatGPT_Backup_Analysis.md`
- `docs/20_FQL_TAM_Logs_And_Architecture_Assessment.md`
- `fixtures/swade_5_2_6/technical.index.json`

If Claude cannot see these files in a Lost Frontier project chat, connect `WildPoxx/masterquest-fvtt-dev` as an additional GitHub source or attach the relevant files for that task.

## Interpretation Rule

Do not treat missing MasterQuest files as missing Lost Frontier canon. Treat them as associated technical context that may need a second repository connection.
