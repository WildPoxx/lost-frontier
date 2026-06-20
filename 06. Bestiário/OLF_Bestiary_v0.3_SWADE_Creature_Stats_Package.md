# OLF Bestiary v0.3 — SWADE Creature Stats Package

**Projeto:** Outsiders — Lost Frontier  
**Sistema:** Savage Worlds Adventure Edition (SWADE)  
**Finalidade:** pacote de design mecânico para construir stat blocks de criaturas em Foundry VTT / SBI.

---

## 1. Escala SWADE adotada

| Categoria SWADE | Faixa de Size | Scale Modifier | Wounds adicionais | Uso em OLF |
|---|---:|---:|---:|---|
| Tiny | -4 | -6 | 0 | insetos mínimos, roedores, microfauna |
| Very Small | -3 | -4 | 0 | batspiders pequenos, parasitas maiores |
| Small | -2 | -2 | 0 | aranhas ósseas, predadores pequenos |
| Normal | -1 a 3 | — | 0 | humanos, lobos, montarias, Bondaks, animais grandes |
| Large | 4 a 7 | +2 | +1 | Khar'Basil, Urakhshor grande, caranguejos de casco |
| Huge | 8 a 11 | +4 | +2 | Sandworms jovens/adultas, Kryll Dragons, Thrag'gor |
| Gargantuan | 12+ | +6 | +3 | Sandworms ancilares, megafauna de set piece |

**Regra de mesa:** criaturas `Gargantuan` deixam de ser apenas inimigos e passam a funcionar como **ameaças de cena**, quase Hazards vivos. Elas podem ser combatidas, mas a cena deve girar em torno de posição, cobertura, veículos, fuga, ritual, armadilhas, iscas ou objetivos paralelos.

---

## 2. Convenções deste pacote

| Campo | Uso |
|---|---|
| **Role** | função tática da criatura em mesa |
| **Scale** | categoria SWADE |
| **Size** | valor de Size proposto |
| **Extra/Wild Card** | forma padrão de uso |
| **Attributes** | valores sugeridos, não importação final obrigatória |
| **Skills** | perícias principais para stat block |
| **Pace** | movimento em terra, voo, nado ou burrow |
| **Toughness** | valor já incluindo Size e Armor |
| **Wounds** | Wounds extras por escala e/ou Resilient |
| **Attacks** | armas naturais ou efeitos diretos |
| **Special Abilities** | habilidades SWADE ou custom compatíveis |
| **Design Notes** | observações para balanceamento e uso |

---


# 3. Creature Stat Design Matrix

## Bondak
| Campo | Valor |
|---|---|
| **Role** | animal domesticado, rastreador de fungos e carga leve |
| **Base actor** | Mule + Bull |
| **Scale** | Normal |
| **Size** | 1 |
| **Default use** | Extra |
| **Attributes** | Agility d4, Smarts d4 (A), Spirit d6, Strength d8, Vigor d8 |
| **Skills** | Athletics d4, Fighting d4, Notice d8, Survival d6, Stealth d4 |
| **Pace** | 6; Running d6 |
| **Parry** | 4 |
| **Toughness** | 7 (1) |
| **Wounds** | 0 |
| **Attacks** | Horns/Headbutt: Str+d4; Bite: Str+d4 |

**Special Abilities**

- **Armor +1:** thick hide and dorsal plates.
- **Teleritha Scent:** +2 to Notice or Survival to locate energy-fed fungi, leaking cells, contaminated soil, or active salvage residue.
- **Ornery:** riders or handlers suffer -1 when forcing the animal into danger unless trained or bonded.

**Design Notes:** Bondak comum não deve ser um combatente relevante. Sua função é exploração, logística e alerta ambiental.

---
## Tal'Bondak
| Campo | Valor |
|---|---|
| **Role** | rastreador pesado bioengenheirado, escavador e animal de expedição |
| **Base actor** | Bull + Bear + Mule |
| **Scale** | Normal |
| **Size** | 3 |
| **Default use** | Extra; Wild Card apenas para Dentinho ou espécimes narrativamente centrais |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d8, Strength d12+2, Vigor d10 |
| **Skills** | Athletics d6, Fighting d6, Notice d10, Survival d8, Stealth d4 |
| **Pace** | 6; Running d6; Burrow 2 in soft soil or fungal beds only |
| **Parry** | 5 |
| **Toughness** | 10 (1) |
| **Wounds** | 0 |
| **Attacks** | Horns: Str+d6; Bite: Str+d4; Charge: Str+d8 if it moves at least 6'' before attacking |

**Special Abilities**

- **Armor +1:** thick hide and plates.
- **Enhanced Teleritha Scent:** +2 to track Osmérion, micelial saturation, energy residues, and calibrated signatures; +4 with a functioning Arreio de Rastro.
- **Sensitive Nose:** Aethera, dimensional noise, or corrupted Teleritha may force a Spirit roll or the Tal'Bondak becomes Distracted or Shaken.
- **Stubborn Bond:** +2 to resist commands that separate it from a bonded handler.

**Design Notes:** Tal'Bondaks são tecnologia viva. Não devem virar simples montarias; o risco de sobrecarga precisa aparecer em jogo.

---
## Cocara
| Campo | Valor |
|---|---|
| **Role** | predador aéreo psíquico, controlador de posição e caçador de vítimas atordoadas |
| **Base actor** | Raptor + Aerial Stalker + Darkraptor |
| **Scale** | Large |
| **Size** | 4 |
| **Default use** | Extra para espécime comum; Wild Card para alfa, matriarca ou cena-chefe |
| **Attributes** | Agility d8, Smarts d8, Spirit d10, Strength d12+1, Vigor d8 |
| **Skills** | Athletics d10, Fighting d8, Intimidation d10, Notice d10, Psionics d10, Stealth d8 |
| **Pace** | Ground 3; Flight 24; Running d6 |
| **Parry** | 6 |
| **Toughness** | 11 (1) |
| **Wounds** | +1 por Large; Wild Card usa Wounds normais + escala conforme Foundry |
| **Attacks** | Bite: Str+d6; Claws: Str+d6; Talon Snatch: opposed Athletics to Grapple during a flyby |

**Special Abilities**

- **Flight 24:** uses Athletics for aerial maneuvering.
- **Fear -1:** the humanoid skull, psychic pressure, and hunting cry disturb witnesses.
- **Psychic Daze:** Psionics vs Spirit. On success, target becomes Distracted and Vulnerable. On a raise, target is Stunned.
- **Mental Scream:** Cone Template or Medium Blast Template, Psionics vs Spirit. Targets who fail are Stunned; success leaves them Distracted until the end of their next turn. After using this ability, the Cocara must roll Spirit. Failure causes one level of Fatigue; Critical Failure causes Fatigue and Shaken.
- **Predatory Suggestion:** once per scene, a Cocara may use Psionics vs Spirit to make a confused target move its Pace toward an exposed, high, or isolated position. This is not full mind control; obvious self-destruction grants +2 to resist.
- **Psychic Feeding:** if a Cocara Incapacitates or maintains a Stunned target for a full round, it may remove one level of Fatigue caused by Mental Scream.
- **Light Frame:** despite Large scale, the Cocara is not heavily armored; called shots to wings are viable.

**Design Notes:** A Cocara deve atacar depois de abalar a presa. O dano físico é secundário; a ameaça real é Stun, queda, isolamento e The Drop.

---
## Urakhshor
| Campo | Valor |
|---|---|
| **Role** | predador territorial mineralizado, emboscador pesado de fendas |
| **Base actor** | Bear + Darkraptor + Drake |
| **Scale** | Large |
| **Size** | 5 |
| **Default use** | Extra de elite ou Wild Card |
| **Attributes** | Agility d6, Smarts d6 (A), Spirit d10, Strength d12+5, Vigor d12 |
| **Skills** | Athletics d8, Fighting d10, Intimidation d10, Notice d10, Stealth d8, Survival d8 |
| **Pace** | 7; Running d6; Climb 4 in rock/fissures |
| **Parry** | 7 |
| **Toughness** | 16 (3) |
| **Wounds** | +1 por Large; considerar Resilient para Extras de elite |
| **Attacks** | Vibro-Claws: Str+d8, AP 4 vs stone, metal, armor, or Teleritha composites; Bite: Str+d6 |

**Special Abilities**

- **Armor +3:** mineralized hide.
- **Hardy:** a second Shaken result does not cause a Wound.
- **Ambush Pattern:** +2 to Stealth and Notice when hunting near known routes, fendas, passes, or repeated trails.
- **Vibration Reader:** halves penalties from darkness or concealment if the target is moving on stone, metal, or packed ground.
- **Territorial Patience:** gains +2 on the first Fighting roll against prey that enters a prepared kill zone.
- **Environmental Weakness - Sonic Overload:** takes +4 damage or -4 resistance against intense sonic/Veyra-disruptive effects.

**Design Notes:** Urakhshor não é perseguidor infinito. Ele vence quando prevê a rota. Jogadores inteligentes devem poder contorná-lo, distraí-lo ou quebrar seu padrão.

---
## Thrag'gor
| Campo | Valor |
|---|---|
| **Role** | colosso destruidor, ameaça de infraestrutura e fera reativa a Veyra |
| **Base actor** | Stomper + Drake + Dragon |
| **Scale** | Huge |
| **Size** | 8 |
| **Default use** | Extra de elite; Wild Card para encontro central |
| **Attributes** | Agility d4, Smarts d4 (A), Spirit d10, Strength d12+8, Vigor d12 |
| **Skills** | Athletics d8, Fighting d8, Intimidation d10, Notice d6 |
| **Pace** | 5; Running d6 |
| **Parry** | 6 |
| **Toughness** | 22 (4) |
| **Wounds** | +2 por Huge |
| **Attacks** | Stomp: Str+d10; Slam: Str+d8; Multi-Limb Strike: two Fighting attacks with forelimbs as one action, MAP applies normally unless using only limb actions by GM ruling |

**Special Abilities**

- **Armor +4:** plates, mass, and mineralized hide.
- **Hardy.:**
- **Siege Body:** +4 to Athletics or Strength rolls to break structures, gates, scaffolds, or industrial machinery.
- **Crushing Advance:** once per round, may move through Normal-scale obstacles and creatures. Targets must Evade or suffer Str+d8 damage and fall prone.
- **Veyra-Drawn:** intense Veyra emissions, refineries, resonance engines, or sonic pulses may redirect or enrage it. Use opposed Science/Repair/Performance vs Spirit to lure it.
- **Swat:** ignores up to 4 points of Scale penalties when using Stomp or Slam against smaller targets.

**Design Notes:** Thrag'gor é evento móvel. A cena deve ser sobre escapar, redirecionar, derrubar, prender ou proteger uma instalação.

---
## Sandworm, Juvenile
| Campo | Valor |
|---|---|
| **Role** | verme jovem de areia, predador subterrâneo pesado |
| **Base actor** | Giant Worm + Death Worm |
| **Scale** | Huge |
| **Size** | 8 |
| **Default use** | Extra |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d8, Strength d12+8, Vigor d12 |
| **Skills** | Athletics d6, Fighting d8, Notice d10, Stealth d8 |
| **Pace** | Ground 4; Burrow 16 in sand; Running d6 |
| **Parry** | 6 |
| **Toughness** | 20 (4) |
| **Wounds** | +2 por Huge |
| **Attacks** | Bite: Str+d8; Body Slam: Str+d6 in a Small Blast Template line/area chosen by GM |

**Special Abilities**

- **Armor +4:** vitrified plates.
- **Burrow 16:** sand, soft mineral soil, dunes, and Pulvis beds.
- **Tremor Sense:** detects walking targets at long range through sand or packed ground; ignores visual darkness against moving grounded prey.
- **Erupt:** if hidden underground, opposed Stealth vs Notice; on success target is Vulnerable to the worm only; on raise the worm has The Drop.
- **Sand Wake:** emergence creates Difficult Ground in a Small or Medium Blast Template.

**Design Notes:** Esta é a versão que os PCs podem enfrentar cedo sem virar catástrofe regional.

---
## Sandworm, Adult
| Campo | Valor |
|---|---|
| **Role** | megafauna adulta, ameaça de barcaça e travessia |
| **Base actor** | Giant Worm + Deep Space Worm |
| **Scale** | Huge |
| **Size** | 11 |
| **Default use** | Hazard vivo; Extra apenas se a cena for de caça |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d10, Strength d12+11, Vigor d12 |
| **Skills** | Athletics d6, Fighting d8, Notice d10, Stealth d8 |
| **Pace** | Ground 4; Burrow 20 in sand; Running d6 |
| **Parry** | 6 |
| **Toughness** | 25 (5) |
| **Wounds** | +2 por Huge |
| **Attacks** | Bite: Str+d10; Body Crush: Str+d8, area by footprint; Sand Breach: opposed Athletics vs Agility to avoid being knocked prone |

**Special Abilities**

- **Armor +5:** massive vitrified plates.
- **Burrow 20.:**
- **Hardy.:**
- **Swat:** ignores up to 4 points of Scale penalties with Bite, Body Crush, or Sand Breach.
- **Devour Vehicle:** on a raise against a vehicle-scale target, may inflict collision/crushing consequences at GM discretion rather than only personal damage.
- **Attracted to Vibration:** poorly tuned engines, marching columns, and Gravis resonance tests may draw it from miles away.
- **Swallow Whole:** use only for Adult+ specimens; targets hit by Bite must Evade or be swallowed. At the end of the worm's turns, swallowed victims roll Vigor at -2 or suffer a Wound. Escape requires cutting, explosive force, or a Dramatic Task.

**Design Notes:** Adult Sandworm deve ser tratada como problema de navegação, não só saco de HP.

---
## Sandworm, Ancilar
| Campo | Valor |
|---|---|
| **Role** | verme ancestral de escala Gargantuan, set piece e catástrofe viva |
| **Base actor** | Deep Space Worm |
| **Scale** | Gargantuan |
| **Size** | 12 |
| **Default use** | Hazard vivo / boss ambiental; raramente combate direto |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d12, Strength d12+12, Vigor d12 |
| **Skills** | Athletics d6, Fighting d8, Notice d10, Stealth d6 |
| **Pace** | Ground 4; Burrow 16 through sand, glassed dunes, or soft stone |
| **Parry** | 6 |
| **Toughness** | 28 (6) |
| **Wounds** | +3 por Gargantuan |
| **Attacks** | Bite: Str+d10, Heavy Weapon; Stomp/Body Drop: Strength damage in a GM-defined footprint template; Sandquake: special area hazard |

**Special Abilities**

- **Gargantuan:** Heavy Armor, attacks count as Heavy Weapons, +3 Wounds, Stomp available.
- **Armor +6:** Heavy Armor; ancient vitrified shell.
- **Hardy.:**
- **Unstoppable:** takes a maximum of one Wound from a single damaging attack after Soak unless the attacker acts on a Joker or uses a prepared set-piece weakness.
- **Tremor Sovereign:** detects vehicles, herds, engines, or explosions through sand at extreme distances.
- **Sandquake:** when it emerges or dives, all grounded targets in a large zone must roll Athletics or Agility or fall prone and become Vulnerable.
- **Swallow Whole:** as Adult, but escape should be a Dramatic Task unless the group uses heavy weapons, explosives, cutting rigs, or internal hazards.
- **Ancient Ossuary:** its remains are locations, not loot piles.

**Design Notes:** Relatos de ossadas acima de Size 12 devem existir como locais de aventura: túneis ósseos, cidades-carcaça, rotas de contrabando, minas de osso ressonante.

---
## Kryll Dragon
| Campo | Valor |
|---|---|
| **Role** | megafauna blindada do Mar de Areia, destruidor de barcas e recurso estratégico |
| **Base actor** | Dragon + Drake + Omega Crab |
| **Scale** | Huge |
| **Size** | 8 |
| **Default use** | Extra de elite; Wild Card para elder ou caçada épica |
| **Attributes** | Agility d6, Smarts d6 (A), Spirit d10, Strength d12+8, Vigor d12 |
| **Skills** | Athletics d8, Fighting d10, Intimidation d10, Notice d8, Stealth d6 |
| **Pace** | Ground 6; Burrow/Sand Swim 10; Running d6 |
| **Parry** | 7 |
| **Toughness** | 23 (5) |
| **Wounds** | +2 por Huge |
| **Attacks** | Bite: Str+d10; Claws: Str+d8, AP 2; Tail Lash: Str+d6 in a sweep arc |

**Special Abilities**

- **Armor +5:** vitrified teleritic carapace.
- **Hardy.:**
- **Hull Breaker:** attacks against vehicles, barcas, platforms, or hulls gain AP 4 and count as Heavy Weapons only against objects/vehicles if using prepared momentum or emergence.
- **Resonance Wake:** movement through sand imposes -2 to Driving/Piloting rolls of nearby barcas until end of next round unless stabilized.
- **Multi-Limb Assault:** may make two claw attacks as one action; MAP applies normally.
- **Teleritha Bones:** carcass is a strategic resource; harvesting attracts predators, Guild agents, or bone-swarms.

**Design Notes:** Kryll Dragons são menos sísmicos que Sandworms e mais combativos. Use-os para caça, território e conflito econômico.

---
## Vharu-Kesh
| Campo | Valor |
|---|---|
| **Role** | rastreador de túnel, cão-esporo de Krom'Vathra |
| **Base actor** | Dog/Wolf + Cyber Dog |
| **Scale** | Normal |
| **Size** | 0 |
| **Default use** | Extra; matilhas de 3-6 |
| **Attributes** | Agility d8, Smarts d6 (A), Spirit d6, Strength d8, Vigor d8 |
| **Skills** | Athletics d8, Fighting d6, Intimidation d6, Notice d10, Stealth d8, Survival d8 |
| **Pace** | 10; Running d10 |
| **Parry** | 5 |
| **Toughness** | 6 |
| **Wounds** | 0 |
| **Attacks** | Bite: Str+d6 |

**Special Abilities**

- **Spore Scent:** +2 Notice/Survival to track sweat, fear, blood, infection, micelial disturbance, or fungal disease; +4 inside living Krom'Vathra tunnels.
- **Pack Hunter:** +1 damage when gaining Gang Up bonus; this does not stack beyond normal Gang Up limits unless GM wants elite packs.
- **Tunnel Runner:** ignores Difficult Ground from fungal mats, roots, slick organic passages, or cramped tunnels.
- **War Variant:** add Armor +1, Size 1, and Paralytic Spores: target Shaken or Wounded by Bite must roll Vigor or become Stunned.

**Design Notes:** Use Vharu-Kesh como alarme vivo e perseguidor, não como dano bruto.

---
## Khar'Basil
| Campo | Valor |
|---|---|
| **Role** | trono de guerra vivo, plataforma de cerco e bloqueio de galeria |
| **Base actor** | Omega Crab + Stomper + Drake |
| **Scale** | Large |
| **Size** | 5 |
| **Default use** | Extra de elite; Wild Card para exemplar real/ritual |
| **Attributes** | Agility d4, Smarts d4 (A), Spirit d10, Strength d12+5, Vigor d12 |
| **Skills** | Athletics d8, Fighting d8, Intimidation d10, Notice d6 |
| **Pace** | 5; Running d6 |
| **Parry** | 6 |
| **Toughness** | 18 (4) |
| **Wounds** | +1 por Large; considerar Very Resilient para plataformas de guerra importantes |
| **Attacks** | Mandibles: Str+d8; Trample/Stomp: Str+d10; Bone Ram: Str+d8, AP 2 vs structures |

**Special Abilities**

- **Armor +4:** mineralized carapace with low-purity Teleritha.
- **Living Platform:** can carry 4-6 riders or a light organic weapon platform without penalty.
- **Siege Mount:** may mount one organic projector, bone ram, archer platform, or spore emitter as Gear/Vehicle attachment.
- **Ground Sense:** halves penalties from darkness or cover when detecting moving grounded targets.
- **Slow Bulk:** -2 to attempts requiring sudden turns, leaps, or narrow maneuvering.
- **Commanded Beast:** without handler, rider, pheromone command, or trained pilot, it follows simple defensive instincts.

**Design Notes:** Khar'Basil não é só criatura: é interface entre animal, veículo e fortificação.

---
## Drakhar Veyl
| Campo | Valor |
|---|---|
| **Role** | montaria aérea de Krom'Vathra, predador de precisão e patrulha de abismo |
| **Base actor** | Darkraptor + Dragon + Haze Dragon |
| **Scale** | Normal |
| **Size** | 3 |
| **Default use** | Extra; Wild Card para montaria nomeada |
| **Attributes** | Agility d8, Smarts d6 (A), Spirit d8, Strength d12+2, Vigor d10 |
| **Skills** | Athletics d10, Fighting d8, Notice d8, Stealth d8 |
| **Pace** | Ground 4; Flight 18; Running d6 |
| **Parry** | 6 |
| **Toughness** | 11 (2) |
| **Wounds** | 0 |
| **Attacks** | Bite: Str+d6; Claws: Str+d6; Dive Claw: Str+d8 after descending at least 6'' |

**Special Abilities**

- **Flight 18:** adapted to vertical currents, caves, and abyssal shafts.
- **Armor +2:** organic plates.
- **Low Light Vision.:**
- **Bonded Mount:** -2 to Riding/Piloting-equivalent handling rolls unless the rider is bonded, trained, or recognized by pheromone/metabolic pattern.
- **Defensive Spores:** once per encounter, creates a Small Blast Template cloud. Targets inside roll Vigor or become Distracted; on a Critical Failure they are Stunned.
- **Cable Ripper:** +2 to attacks against ropes, cables, exposed rigging, and light aircraft control surfaces.

**Design Notes:** Não tratar como dragão clássico. É montaria predatória, útil em passadiços verticais e combate aéreo curto.

---
## Zharikarn
| Campo | Valor |
|---|---|
| **Role** | predador cavernícola de abismo, caçador de parede/teto |
| **Base actor** | Darkraptor + Bone Spider + Giant Spider |
| **Scale** | Normal |
| **Size** | 2 |
| **Default use** | Extra de elite |
| **Attributes** | Agility d10, Smarts d6 (A), Spirit d8, Strength d12, Vigor d8 |
| **Skills** | Athletics d10, Fighting d8, Intimidation d8, Notice d8, Stealth d10 |
| **Pace** | 8; Wall Pace 8; Running d6 |
| **Parry** | 6 |
| **Toughness** | 9 (1) |
| **Wounds** | 0 |
| **Attacks** | Claws: Str+d6; Bite: Str+d6 |

**Special Abilities**

- **Armor +1:** fungal-bone plates.
- **Wall Walker.:**
- **Ceiling Ambush:** +2 Stealth when above or behind targets; if it gains Surprise, first attack has The Drop.
- **Spore-Mask Hide:** ignores up to 2 points of penalties from dim light, mist, spores, or fungal haze.
- **Rending Leap:** if it moves at least 4'' before attacking from above, +2 damage on a raise.

**Design Notes:** Mantido como criatura provisória até canonização final. Sua lacuna útil é predador selvagem de Krom'Vathra/Nexo.

---
## Nhar-Sul, Verme Cuspidor de Pulvis
| Campo | Valor |
|---|---|
| **Role** | predador médio de deserto, cuspidor de toxina mineral |
| **Base actor** | Spit Worm |
| **Scale** | Normal |
| **Size** | 0 |
| **Default use** | Extra |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d8, Strength d8, Vigor d8 |
| **Skills** | Athletics d6, Fighting d6, Intimidation d8, Notice d8, Shooting d6, Stealth d6 |
| **Pace** | 6; Burrow 4 in soft sand; Running d6 |
| **Parry** | 5 |
| **Toughness** | 6 |
| **Wounds** | 0 |
| **Attacks** | Bite: Str+d6; Spit Pulvis Bile: Range 3/6/12, Vigor roll or Stunned; sealed suits grant +2 to resist |

**Special Abilities**

- **Infravision.:**
- **Pulvis Metabolism:** immune to minor Pulvis irritation and +4 to resist Pulvis-based Hazards.
- **Mineral Paralysis:** targets hit by Spit Pulvis Bile roll Vigor; failure causes Stunned, raise on attack or Critical Failure on resistance causes Stunned and one level of Fatigue.
- **Residue Cloud:** after spitting, leaves a faint Pulvis haze; Notice or Survival can track it.

**Design Notes:** Boa ameaça intermediária. Não substitui Sandworms; anuncia que a areia está viva.

---
## Enxame Karveth, Vermes Fura-Casco
| Campo | Valor |
|---|---|
| **Role** | enxame perfurador, ameaça de carne, filtros, armaduras e veículos |
| **Base actor** | Swarm, Bore Worm |
| **Scale** | Swarm |
| **Size** | 0 |
| **Default use** | Hazard vivo / Swarm |
| **Attributes** | Agility d10, Smarts d4 (A), Spirit d12, Strength d8, Vigor d10 |
| **Skills** | Notice d6, Stealth d8 |
| **Pace** | 10; Running d6; can enter gaps, vents, fabric and exposed joints |
| **Parry** | 4 |
| **Toughness** | 7 |
| **Wounds** | Swarm rules |
| **Attacks** | Bites: automatic swarm damage to targets in template unless Shaken |

**Special Abilities**

- **Swarm:** +2 to recover from Shaken; area-effect attacks are most effective; normal weapons have limited effect by SWADE swarm rules.
- **Split:** when Wounded, may split into two smaller swarms at GM discretion.
- **Infection:** if it causes Shaken or Wounded, victim rolls Vigor. Failure means embedded larvae cause one automatic Wound per day until treated by Healing/Science in proper conditions.
- **Hull-Borer:** may attack exposed equipment, filters, armor seams, vehicle intakes, or energy cells; treat as a Complication or Repair penalty rather than simple damage when dramatically useful.
- **Heat-Seeking:** attracted by body heat, engines, batteries and leaking Teleritha.

**Design Notes:** A vitória contra o enxame deve cobrar manutenção. Use para destruir confiança em equipamento.

---
## Veyl'Khar, Aranha-Morcego do Abismo
| Campo | Valor |
|---|---|
| **Role** | pequeno predador vertical, venenoso e furtivo |
| **Base actor** | Batspider |
| **Scale** | Small |
| **Size** | -2 |
| **Default use** | Extra; grupos de 2-8 |
| **Attributes** | Agility d10, Smarts d6 (A), Spirit d8, Strength d4, Vigor d6 |
| **Skills** | Athletics d8, Fighting d6, Notice d8, Stealth d10 |
| **Pace** | Ground 4; Flight 8; Wall Pace 4 |
| **Parry** | 5 |
| **Toughness** | 4 |
| **Wounds** | 0 |
| **Attacks** | Poison Bite: minimal damage; target hit on exposed skin rolls Vigor -2 or gains Fatigue; Critical Failure causes Stunned |

**Special Abilities**

- **Flight 8.:**
- **Wall Walker.:**
- **Backbiter:** if it has Surprise, it lands on the target's back with The Drop. Victim suffers -2 to attack it until it is Shaken or Wounded.
- **Poison Bite -2:** cannot penetrate sealed armor; seeks exposed skin or light clothing via Called Shot.
- **Tiny Target:** attackers use appropriate Scale rules; area attacks are efficient.

**Design Notes:** O perigo é queda, distração e pânico em pontes, não dano direto.

---
## Caranguejo de Casco Morto
| Campo | Valor |
|---|---|
| **Role** | necrófago blindado de salvage, caranguejo que usa sucata como concha |
| **Base actor** | Omega Crab |
| **Scale** | Large |
| **Size** | 4 |
| **Default use** | Extra de elite |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d8, Strength d12+4, Vigor d10 |
| **Skills** | Athletics d8, Fighting d8, Notice d8, Stealth d8 |
| **Pace** | 6; Running d6; Climb 3 over wreckage |
| **Parry** | 6 |
| **Toughness** | 15 (4) |
| **Wounds** | +1 por Large |
| **Attacks** | Claws: Str+d8, AP 4; Crushing Grip: +2 to Grapple and crushing damage against Bound/Entangled prey |

**Special Abilities**

- **Armor +4:** scrap shell and natural carapace.
- **Scrap Camouflage:** +2 Stealth while hidden among wreckage, hull plates, or scrapyards.
- **Shell Scavenger:** if given time after combat, may improve or replace damaged shell with nearby salvage; GM may restore Armor or create new weakness based on material.
- **Data-Shell:** its shell may contain old markings, plates, serials, or clues from fallen craft.

**Design Notes:** Serve como ameaça e pista ambulante no Campo das Estrelas Cadentes.

---
## Cardume de Ossos
| Campo | Valor |
|---|---|
| **Role** | enxame necrófago de carcaças de megafauna |
| **Base actor** | Bore Worm Swarm + Bone Spider |
| **Scale** | Swarm |
| **Size** | 0 |
| **Default use** | Swarm/Hazard |
| **Attributes** | Agility d8, Smarts d4 (A), Spirit d10, Strength d6, Vigor d10 |
| **Skills** | Notice d8, Stealth d8 |
| **Pace** | 8; Burrow 4 through bone dust, marrow tunnels, and carcass cavities |
| **Parry** | 4 |
| **Toughness** | 8 (1) |
| **Wounds** | Swarm rules |
| **Attacks** | Bone Bites: automatic swarm damage; against unarmored targets may trigger Vigor roll or Fatigue |

**Special Abilities**

- **Swarm.:**
- **Armor +1:** bone shards and teleritic fragments dispersed through the mass.
- **Split.:**
- **Carcass Defense:** +2 Stealth and +2 damage inside ossuaries, carcasses, Sandworm bones, or Kryll remains.
- **Marrow Infection:** Shaken or Wounded targets roll Vigor; failure causes Fatigue from bone-dust infection until treated.
- **Resource Guardian:** harvesting a megafauna carcass without precautions triggers the swarm.

**Design Notes:** Impede que uma carcaça seja apenas tesouro. O monstro continua depois da morte do monstro maior.

---
## Besouro Arco de Dhuron
| Campo | Valor |
|---|---|
| **Role** | inseto blindado com descarga bioelétrica/telerítica |
| **Base actor** | Arc Beetle |
| **Scale** | Normal |
| **Size** | 2 |
| **Default use** | Extra |
| **Attributes** | Agility d6, Smarts d4 (A), Spirit d8, Strength d10, Vigor d8 |
| **Skills** | Athletics d8, Fighting d6, Notice d6, Shooting d8, Stealth d4 |
| **Pace** | 6; Running d6 |
| **Parry** | 5 |
| **Toughness** | 11 (3) |
| **Wounds** | 0 |
| **Attacks** | Bite: Str+d4; Arc Discharge: Range 6/12/24, Damage 3d6, AP 2 |

**Special Abilities**

- **Armor +3:** thick Dhuron-rich shell.
- **Environmental Resistance - Electricity:** reduces electrical damage by 4 and +4 to resist matching Hazards.
- **Static Draw:** active generators, Veyra conduits, or exposed cells may attract it.
- **Overcharge Death:** on Incapacitation near unstable electronics, GM may call for Repair/Electronics or create a minor electrical Hazard.

**Design Notes:** Bom para laboratórios, refinarias e túneis energizados.

---
## Filhote de Bruma Vey'Shal
| Campo | Valor |
|---|---|
| **Role** | pequeno dragonoide fúngico, dispersor de esporos psicoativos |
| **Base actor** | Haze Dragon |
| **Scale** | Normal |
| **Size** | 0 |
| **Default use** | Extra |
| **Attributes** | Agility d4, Smarts d6 (A), Spirit d6, Strength d8, Vigor d8 |
| **Skills** | Athletics d6, Fighting d4, Intimidation d6, Notice d6, Stealth d6 |
| **Pace** | 6; Running d6 |
| **Parry** | 4 |
| **Toughness** | 7 (1) |
| **Wounds** | 0 |
| **Attacks** | Bite: Str+d4; Spore Breath: Cone Template, Vigor roll or Fatigue/Distracted depending on scene |

**Special Abilities**

- **Armor +1:** scaly fungal hide.
- **Spore Breath:** takes full turn; targets may Evade. On hit, Vigor roll or Distracted and Fatigued. On Critical Failure, Stunned.
- **Fungal Symbiosis:** +2 Stealth and Vigor recovery in Khromicélio-rich areas.
- **Environmental Weakness - Dry Sterile Air:** -2 to Vigor and recovery rolls in dry, sterile, filtered or anti-fungal environments.

**Design Notes:** Não é dragão de fantasia. É vetor biológico de esporos estruturados.

---

# 4. Abilities padronizadas para OLF

## Psychic Daze
**Uso:** Cocara e criaturas psíquicas de Veyra/Aethera.  
**Regra:** Psionics vs Spirit. Success: target becomes Distracted and Vulnerable. Raise: target is Stunned.  
**Custo recomendado:** se usado em área ou como grito, a criatura rola Spirit após o uso; failure causes Fatigue.

## Mental Scream
**Uso:** Cocara alfa, enxames psíquicos, horrores do Véu.  
**Regra:** Cone Template or Medium Blast Template. Targets resist with Spirit. Failure causes Stunned; success may still leave Distracted. The creature must roll Spirit after use or suffer Fatigue.

## Teleritha Scent
**Uso:** Bondaks, Tal'Bondaks, criaturas do Campo.  
**Regra:** +2 to Notice/Survival involving energy-fed fungi, leaking cells, Pulvis residue, Osmérion, or calibrated signatures. Dangerous signatures may force Spirit or Vigor rolls.

## Tremor Sense
**Uso:** Sandworms, Kryll Dragons, Urakhshor.  
**Regra:** ignores visual penalties to detect grounded moving targets through sand, stone, metal, or packed soil. Does not detect motionless targets automatically.

## Vitrified Plates
**Uso:** Sandworms, Kryll Dragons, Mar de Areia.  
**Regra:** Armor +4 to +6 depending on scale. Heavy Armor should be reserved for Gargantuan creatures or explicit vehicle-scale carapace.

## Siege Body
**Uso:** Thrag'gor, Khar'Basil, Kryll Dragon.  
**Regra:** +4 to break structures or damage objects when fiction supports mass and leverage. Avoid making all attacks Heavy Weapons unless the creature is Gargantuan or explicitly attacking vehicles/structures.

## Hull-Borer / Hull Breaker
**Uso:** Karveth, Kryll Dragon, Caranguejo de Casco Morto.  
**Regra:** instead of direct Wounds, may impose Complications on equipment, vehicles, filters, armor seams, or power cells. Good for Quick Encounters and Dramatic Tasks.

---

# 5. Design warnings

1. **Não usar Gargantuan cedo demais.** Em SWADE, Gargantuan não é apenas “muito grande”; ele altera a natureza do encontro com Heavy Armor, Heavy Weapons, +3 Wounds e Stomp.
2. **Não inflar Toughness sem função.** Se a criatura já tem Size alto, Armor alto e Hardy, cada ponto extra de Toughness pesa muito.
3. **Usar Fatigue como custo de poderes fortes.** Isso é especialmente importante para Cocara e efeitos psíquicos recorrentes.
4. **Separar criatura de Hazard.** Sandworm adulta e ancilar podem ter stat block, mas a cena deve funcionar como Hazard vivo.
5. **Manter Special Abilities curtas.** Para SBI/Foundry, blocos limpos são mais úteis que parágrafos bonitos.
6. **Heavy Armor é exceção.** Por regra, Gargantuan concede Heavy Armor automaticamente. Fora disso, use apenas se a ficção exigir escala veicular ou carapaça excepcional.
7. **Scale não substitui Called Shot.** Tamanho do alvo e escala da parte atingida importam. Olho, junta, antena, asa ou placa exposta podem ter escala menor que o corpo inteiro.

---

# 6. Próxima fase

Este pacote ainda é uma matriz de design. A próxima etapa é gerar, criatura por criatura, blocos SBI-safe em inglês, com estrutura:

```text
Name
Rank Gender Ancestry

Attributes: ...
Skills: ...
Pace: X; Parry: X; Toughness: X (Y)
Hindrances: ...
Edges: ...
Gear: ...
```

Special Abilities customizadas devem entrar preferencialmente como itens manuais pós-importação ou como Gear/Attack textual simples, conforme estabilidade do SWADE Stat Block Importer.
