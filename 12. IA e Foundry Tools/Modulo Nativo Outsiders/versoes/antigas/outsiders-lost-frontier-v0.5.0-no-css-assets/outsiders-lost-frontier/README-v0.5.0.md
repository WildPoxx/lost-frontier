# OLF Companion v0.5.0

This version restructures the module around the Science Fiction Companion-style architecture:

- module title: `OLF Companion`;
- compendium packs are grouped under the module title in Foundry;
- packs use v13-style LevelDB folders, not flat `.db` files;
- typed packs: `book`, `teleritha`, `ancestries`, `abilities`, `edges`, `hindrances`, `powers`, `vehicles`, `actors`, etc.

## Included content

- Danahimm ancestry package.
- Teleritha / Resonance / Syncrisalysis / Technosynthesis / Metacatalysis / Harmurgy Journals.
- Initial Harmurgic Formulas as Power items.
- Provisional Harmurgist Edges and Teleritha Hindrances.
- Initial vehicle Actors: Dust Runner, Sandcutter, Veyra Runner, Outrunner.
- Provisional actors: Bondak, Tal'Bondak, Dentinho, Floyd Merian.

## Installation warning

Back up your current module folder before replacing it.

This zip includes `dist/style.css` copied from the latest clean CSS available in the build workspace. It does not include final layout image assets. Place your layout assets in:

`Data/modules/outsiders-lost-frontier/assets/layout/`

Especially:

`olf-logo.webp`

If you have hand-edited CSS on the server, preserve it before installing, or use the packs-only zip instead.
