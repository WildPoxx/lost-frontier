---
name: swade-fvtt-mechanics-model
description: Interpret SWADE 5.2.6 for Foundry VTT 13.351 in Lost Frontier. Use for SWADE rules, Bennies, Wild Die, Support, Fear, Hazards, Quick Encounters, Chases, Dramatic Tasks, Social Conflict, Travel, actors, items, combat, journals, JSON, module integration, or adventure design using the SWADE system in Foundry.
---

# SWADE FVTT Mechanics Model

Use this skill to work on two linked planes:

- **SWADE as tabletop RPG**: rules, GM procedures, scene design, encounters, and dramatic structure.
- **SWADE as Foundry system**: actors, items, combat, cards, chat, settings, JSON, system documents, and implementation behavior.

Always explain in clear Portuguese. Assume Mario does not know code or JSON unless he says otherwise.

## Baseline

Use this default baseline unless the files or Mario specify another one:

- Foundry VTT `13.351`
- SWADE `5.2.6`
- Lost Frontier module id `outsiders-lost-frontier`

Do not import behavior from newer SWADE or Foundry versions without saying that it may differ from the project baseline.

## Separate Three Layers

For every SWADE task, identify the layer:

- **table rule**: what the book or game procedure says;
- **FVTT implementation**: how the SWADE system represents it in actors, items, combat, chat, settings, hooks, or UI;
- **OLF custom layer**: how Lost Frontier reads, organizes, reports, or updates it for the campaign/module.

Do not treat these layers as the same thing.

## Read Order

Start with project sources when available:

1. `README.md`
2. `AI_COLLABORATION.md`
3. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/17_SWADE_5_2_6_FVTT_Baseline.md`
4. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/docs/18_SWADE_FVTT_Skill_Spec.md`
5. `12. IA e Foundry Tools/Modulo FQL - OLF - Hack/olf-fql-campaign-ops/fixtures/swade_5_2_6/technical.index.json`

If local SWADE source code or PDFs are not available in Claude's context, say so rather than pretending to have inspected them. Use official PEG/SWADE sources only when live web or attached files are available.

## Response Modes

For a **rules question**:

- explain the mechanic simply;
- say what the player or GM does at the table;
- then, if useful, explain how it tends to appear in Foundry.

For a **development question**:

- identify the relevant SWADE document types and data flow;
- inspect manifests, data models, settings, hooks, or JSON examples before proposing code;
- prefer observed contracts in files over memory.

For an **adventure or encounter design question**:

- choose the right SWADE tool before defaulting to combat;
- consider Dramatic Tasks, Quick Encounters, Chases, Social Conflict, Travel, Fear, Hazards, Interludes, and Mass Battles;
- translate the creative idea into table procedure, not unnecessary automation.

## Guardrails

- Do not assume Mario understands `flags`, `manifest`, `document class`, `data model`, or `pack`; explain them when needed.
- Do not confuse a Foundry compendium with a rules sourcebook.
- Do not automate a narrative GM decision.
- Do not write to actors, combats, journals, packs, or settings without preview and approval.
- When the book rule and Foundry behavior diverge, name the difference explicitly.

## High-Value Topics

Pay special attention to:

- Bennies and Joker's Wild
- Wild Die and rerolls
- Support
- Quick Encounters
- Chases
- Dramatic Tasks
- Fear
- Hazards
- Interludes
- Mass Battles
- Networking
- Social Conflict
- Travel
- actors, items, effects, journals, and combat subtypes in SWADE
