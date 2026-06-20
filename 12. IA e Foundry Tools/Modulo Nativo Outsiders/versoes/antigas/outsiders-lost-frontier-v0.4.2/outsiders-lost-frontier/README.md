# OutsiderS - Lost Frontier Companion v0.3

Foundry VTT module for SWADE v13.

## v0.3 focus

- Rebuilds the custom actor sheet using SWADE CharacterSheet as the only runtime base.
- Reproduces the visual polygon architecture inspired by the Super Powers Companion internally.
- Does not require the Super Powers Companion module.
- Uses `dist/index.js` and `dist/style.css`, matching the structural pattern of official SWADE companion modules.
- Registers the sheet as optional only: `makeDefault: false`.
- Removes the Pinnacle/Savage branding from the custom sheet and inserts only `olf-logo.webp`.
- Keeps compendiums grouped through `packFolders`.

## Expected layout assets

Place these in `assets/layout/` if you replace the bundled versions:

- olf-logo.webp
- rust-metal-texture.webp
- background-header-new.webp
- condition-hex-small.webp
- hex-decoration-med.webp
- metal-compass-square.webp
- sand-texture.webp
- BossBar.webp

## Installation

Delete the previous `outsiders-lost-frontier` folder from Foundry's Data/modules directory, then upload this folder.


## v0.3.2

Visual tuning for the Lost Frontier sheet. Layout folder intentionally ships empty; user-managed assets must be placed in assets/layout/.
