# OLF Bestiary Individual Actor JSON Export

Generated as individual Actor JSON files for Foundry import. This is not a .db and not a single combined JSON.

## Critical implementation rules applied

- `system.stats.size` is populated from the OLF Bestiary v0.3 matrix.
- Natural Armor is represented as a functional `type: armor` Gear item derived from the working Dragon armor pattern.
- `system.stats.toughness.armor` is also populated for verification.
- `system.stats.toughness.modifier` records the gap between Foundry auto calculation and the v0.3 listed Toughness.
- The Sandworm Adult portrait and token paths are preserved from the corrected export supplied by the user.

## Files

| File | Actor | Scale | Size | Armor | Toughness | Modifier | Portrait | Token |
|---|---|---:|---:|---:|---:|---:|---|---|
| `bondak.json` | Bondak | Normal | 1 | 1 | 7 | -1 | `icons/creatures/mammals/bull-horns-eyes-glowin-orange.webp` | `icons/creatures/mammals/bull-horns-eyes-glowin-orange.webp` |
| `talbondak.json` | Tal'Bondak | Normal | 3 | 1 | 10 | -1 | `icons/creatures/mammals/bull-horns-eyes-glowin-orange.webp` | `icons/creatures/mammals/bull-horns-eyes-glowin-orange.webp` |
| `cocara.json` | Cocara | Large | 4 | 1 | 11 | 0 | `icons/creatures/birds/corvid-call-sound-blue.webp` | `icons/creatures/birds/corvid-call-sound-blue.webp` |
| `urakhshor.json` | Urakhshor | Large | 5 | 3 | 16 | 0 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
| `thraggor.json` | Thrag'gor | Huge | 8 | 4 | 22 | 2 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
| `sandworm-juvenile.json` | Sandworm, Juvenile | Huge | 8 | 4 | 20 | 0 | `icons/creatures/tentacles/tentacle-earth-toned.webp` | `icons/creatures/tentacles/tentacle-earth-toned.webp` |
| `sandworm-adult.json` | Sandworm, Adult | Huge | 11 | 5 | 25 | 1 | `worlds/outsiders-lost-frontier/imgs/bestiary/sandworm-trans.webp` | `worlds/outsiders-lost-frontier/imgs/bestiary/beast-tokens/token_sandworm.webp` |
| `sandworm-ancilar.json` | Sandworm, Ancilar | Gargantuan | 12 | 6 | 28 | 2 | `icons/creatures/tentacles/tentacle-earth-toned.webp` | `icons/creatures/tentacles/tentacle-earth-toned.webp` |
| `kryll-dragon.json` | Kryll Dragon | Huge | 8 | 5 | 23 | 2 | `icons/creatures/reptiles/dragon-horned-blue.webp` | `icons/creatures/reptiles/dragon-horned-blue.webp` |
| `vharu-kesh.json` | Vharu-Kesh | Normal | 0 | 0 | 6 | 0 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
| `kharbasil.json` | Khar'Basil | Large | 5 | 4 | 18 | 1 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
| `drakhar-veyl.json` | Drakhar Veyl | Normal | 3 | 2 | 11 | -1 | `icons/creatures/reptiles/dragon-horned-blue.webp` | `icons/creatures/reptiles/dragon-horned-blue.webp` |
| `zharikarn.json` | Zharikarn | Normal | 2 | 1 | 9 | 0 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
| `nhar-sul-verme-cuspidor-de-pulvis.json` | Nhar-Sul, Verme Cuspidor de Pulvis | Normal | 0 | 0 | 6 | 0 | `icons/creatures/tentacles/tentacle-earth-toned.webp` | `icons/creatures/tentacles/tentacle-earth-toned.webp` |
| `enxame-karveth-vermes-fura-casco.json` | Enxame Karveth, Vermes Fura-Casco | Swarm | 0 | 0 | 7 | 0 | `icons/creatures/tentacles/tentacle-earth-toned.webp` | `icons/creatures/tentacles/tentacle-earth-toned.webp` |
| `veylkhar-aranha-morcego-do-abismo.json` | Veyl'Khar, Aranha-Morcego do Abismo | Small | -2 | 0 | 4 | 1 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
| `caranguejo-de-casco-morto.json` | Caranguejo de Casco Morto | Large | 4 | 4 | 15 | 0 | `icons/creatures/invertebrates/crab-spider-red.webp` | `icons/creatures/invertebrates/crab-spider-red.webp` |
| `cardume-de-ossos.json` | Cardume de Ossos | Swarm | 0 | 1 | 8 | 0 | `icons/creatures/invertebrates/wasp-swarm-movement.webp` | `icons/creatures/invertebrates/wasp-swarm-movement.webp` |
| `besouro-arco-de-dhuron.json` | Besouro Arco de Dhuron | Normal | 2 | 3 | 11 | 0 | `icons/creatures/invertebrates/beetle-stag-horned-blue.webp` | `icons/creatures/invertebrates/beetle-stag-horned-blue.webp` |
| `filhote-de-bruma-veyshal.json` | Filhote de Bruma Vey'Shal | Normal | 0 | 1 | 7 | 0 | `icons/svg/mystery-man.svg` | `icons/svg/mystery-man.svg` |
