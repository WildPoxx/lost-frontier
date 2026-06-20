# Asimovian Magic — Technomancer Edge Tree

Projeto: Outsiders — Lost Frontier  
Sistema: Savage Worlds Adventure Edition / Foundry VTT 13 / SWADE 5.2.6

## Estrutura da árvore

```text
Arcane Background (Technomancer)
└── Asimovian Mage
    ├── Strain Specialist
    ├── Mirage Protocol
    └── Asimovian Channeler
        └── Improved Asimovian Channeler
            ├── Master Asimovian Channeler
            └── Aetheric Channeler
                └── Portal Engineer
                    └── Chrono-Displacement Theorist

Hashmonn-Bound Stabilization = GM Permission / Dominic-style forbidden Edge
```

## Design

- **Arcane Background (Technomancer)** cria a base da Magia Asimoviana.
- **Asimovian Mage** é o equivalente funcional de Wizard: altera Trappings por custo extra.
- **Asimovian Channeler** abre o uso de células de Teleritha como fonte externa de Power Points.
- **Improved/Master Asimovian Channeler** ampliam capacidade de slots, sobrecarga e estabilidade.
- **Aetheric Channeler**, **Portal Engineer** e **Chrono-Displacement Theorist** formam o ramo dimensional/Aethera.
- **Mirage Protocol** forma o ramo de ilusão/Nexyra.
- **Hashmonn-Bound Stabilization** é proibida por padrão e serve como base mecânica para Dominic Nimbus Mirage.

## Itens incluídos

### Arcane Background (Technomancer)

<p>Technomancers are practitioners of Asimovian Magic: arcane effects engineered through Teleritha resonance, field instruments, occult computation, and machine-assisted ritual. They do not treat magic as a supernatural gift, but as a dangerous material process that can be measured, amplified, corrupted, and stabilized.</p><ul><li><strong>Requirements:</strong> Novice, Smarts d6+</li><li><strong>Arcane Skill:</strong> Focus (Spirit)</li><li><strong>Starting Powers:</strong> Any two available powers from the list below.</li><li><strong>Power Points:</strong> 15</li><li><strong>Available Powers:</strong> <em>Arcane protection, barrier, blast, bolt, boost/lower Trait, burst, confusion, deflection, detect/conceal arcana, dispel, environmental protection, farsight, havoc, illusion, invisibility, light/darkness, object reading, protection, sloth/speed, sound/silence, stun, telekinesis, teleport.</em></li><li><strong>Asimovian Magic:</strong> Technomancers may take Edges that require Arcane Background (Gifted) or Arcane Background (Weird Science), at the GM's discretion, when the effect is justified through Teleritha-based technology.</li><li><strong>Teleritha Strain:</strong> When a technomancer Critically Fails a Focus roll, the GM may introduce strain backlash, device failure, a Teleritha anomaly, or a temporary increase in Tension Charge.</li></ul>

**Requirements:** Novice, Smarts d6+

---

### Asimovian Mage

<p>The technomancer has learned to translate arcane formulae into modular Teleritha procedures. By spending additional energy, the character can alter how a power manifests, replacing inherited occult forms with engineered trappings.</p><p>When activating a power, the technomancer may spend <strong>1 additional Power Point</strong> to change the power's Trapping to another calibrated Teleritha strain or technological expression. The new Trapping must still make sense for the power and may have consequences if it interacts with a target's resistance, vulnerability, or environmental condition.</p><p>If the technomancer has access to a compatible Teleritha Cell, the GM may allow the altered Trapping to match that cell's strain. Incompatible or unstable trappings may generate Tension Charge at the GM's discretion.</p>

**Requirements:** Seasoned, Arcane Background (Technomancer), Focus d6+

---

### Strain Specialist

<p>The technomancer specializes in one Teleritha strain: Magyon, Dhuron, Osmerion, Veyra, Aethera, Kinethea, Quantara, Stravon, Axyron, or Nexyra.</p><p>Choose one strain when this Edge is taken. When the character activates a power with a compatible Trapping for that strain, she may ignore up to <strong>1 point of Focus penalties</strong> from Multi-Action, unstable devices, environmental interference, or Teleritha conversion. This does not ignore Wound or Fatigue penalties unless the GM rules the penalty comes from the strain interaction itself.</p><p>This Edge may be taken multiple times, choosing a different strain each time.</p>

**Requirements:** Seasoned, Arcane Background (Technomancer), Focus d8+

---

### Asimovian Channeler

<p>The technomancer can operate a Teleritha Converter and use refined Teleritha Cells as external Power Point sources.</p><p>The character may maintain <strong>one active Teleritha Cell slot</strong>. When activating a power with a compatible Trapping, she may spend Power Points from that cell instead of her personal Power Points. Each use generates <strong>+1 Tension Charge</strong>.</p><p>The character may also use an action to convert cell energy into personal Power Points: roll Focus. On a success, restore 5 personal Power Points. On a raise, restore 10. On a failure, the cell loses 5 Power Points and the character restores nothing. On a Critical Failure, trigger strain backlash. This cannot restore Power Points above the character's normal maximum.</p>

**Requirements:** Seasoned, Arcane Background (Technomancer), Asimovian Mage, Focus d8+, Electronics d8+

---

### Improved Asimovian Channeler

<p>The technomancer has improved her converter architecture and can handle stronger or mismatched Teleritha flows.</p><p>The character may maintain <strong>two active Teleritha Cell slots</strong>. She may attempt to power a spell with a mismatched cell, but the Focus roll suffers <strong>-2</strong> and the use generates <strong>+1 extra Tension Charge</strong>.</p><p><strong>Asimovian Overcharge:</strong> Once per encounter, the character may consume one full Teleritha Cell and roll Focus at -2. On a success, she gains 10 temporary Power Points. On a raise, she gains 15 temporary Power Points. On a failure, the cell is consumed and she suffers Fatigue. On a Critical Failure, trigger strain backlash. Temporary Power Points vanish at the end of the encounter.</p>

**Requirements:** Veteran, Asimovian Channeler, Focus d10+, Electronics d10+

---

### Master Asimovian Channeler

<p>The technomancer has mastered high-load Teleritha conversion and can sustain multiple external reservoirs without immediate collapse.</p><p>The character may maintain <strong>three active Teleritha Cell slots</strong>. Once per encounter, after gaining Tension Charge from a compatible cell use, she may reduce the gained Tension Charge by 1, to a minimum of 0. This reduction cannot be applied to Aethera Surge or Critical Failure consequences.</p><p>When using Teleritha Cell Conversion to restore personal Power Points, a raise restores 10 Power Points and also removes 1 Tension Charge if the cell was compatible with the last power the character activated.</p>

**Requirements:** Legendary, Improved Asimovian Channeler, Focus d12, Science d10+, Electronics d10+

---

### Aetheric Channeler

<p>The technomancer has learned to survive limited contact with Aethera, the Teleritha strain of space-time, non-locality, folds, and thresholds.</p><p>The character may safely mount refined Aethera Cells in a Teleritha Converter. Aethera is compatible with <em>teleport</em>, portal effects, time-slip effects, dimensional concealment, non-local perception, and similar powers approved by the GM.</p><p><strong>Aethera Surge:</strong> Once per session, the character may consume one refined Aethera Cell to gain 20 temporary Power Points. Roll Focus at -2. On a failure, the character suffers Fatigue and temporal displacement. On a Critical Failure, trigger Aethera Backlash. These temporary Power Points last until the end of the encounter.</p>

**Requirements:** Heroic, Improved Asimovian Channeler, Focus d10+, Science d10+, Teleport or dimensional power

---

### Portal Engineer

<p>The technomancer can force short-lived dimensional apertures instead of merely teleporting herself.</p><p>When using <em>teleport</em>, the character may open a small portal instead of simply moving. This can move the caster and up to one adjacent willing target, or allow a single object/person-sized passage for one round. The Focus roll is made at <strong>-2</strong>.</p><p>On a failure, the portal opens but drifts, depositing the target 1d6 x 2 inches away from the intended location or in a dangerous adjacent position. On a Critical Failure, the GM introduces dimensional backlash, an unstable echo, environmental damage, or something briefly looking through the portal.</p>

**Requirements:** Veteran, Aetheric Channeler, Focus d10+, Teleport

---

### Mirage Protocol

<p>The technomancer blends illusion, phase displacement, and techno-occult decoys into a single evasive protocol.</p><p>When the character successfully uses <em>illusion</em> or <em>invisibility</em> with a raise, attackers suffer <strong>-2 to Tests and attacks</strong> against her until they correctly identify the real target with Notice or Smarts opposed by her Focus.</p><p>This Edge is especially common among technomancers who specialize in Nexyra, perception interference, semiotic mirages, and false positional data.</p>

**Requirements:** Seasoned, Arcane Background (Technomancer), Focus d8+, Illusion or Invisibility

---

### Chrono-Displacement Theorist

<p>The technomancer can perform brief, unstable tactical displacements through Aethera. This is not true control over time; it is a dangerous non-local correction that looks, to observers, as if the character had already moved.</p><p><strong>Unreliable Time-Slip:</strong> Once per encounter, after initiative is dealt, the character may attempt a Focus roll at -2. On a success, she may reposition up to 12 inches as if she had already been there a moment before. On a raise, she also gains +2 Parry until her next turn. On a failure, she gains Fatigue. On a Critical Failure, she vanishes until the end of the next round and returns in a GM-chosen compromised position.</p>

**Requirements:** Legendary, Aetheric Channeler, Portal Engineer, Focus d12, Science d10+

---

### Hashmonn-Bound Stabilization

<p><strong>GM Permission Only.</strong> The character has integrated a hostile demonic, extra-dimensional, or alien-organic limb or organ into her body and uses cybernetic stabilizers to keep it from consuming her.</p><p>The character gains <strong>+2 to resist possession, corruption, demonic influence, and hostile dimensional intrusion</strong>. The integrated limb may also count as a magical or dimensional natural weapon if the GM approves.</p><p>However, when the character rolls a Critical Failure on a Focus roll involving Aethera, teleportation, illusion, or the integrated limb, the limb rebels. The character becomes Shaken and must immediately roll Spirit at -2. On a failure, the GM may trigger dimensional backlash, loss of control, or unwanted action by the limb.</p>

**Requirements:** Legendary, Arcane Background (Technomancer), Focus d10+, Spirit d10+, Vigor d8+, GM permission

---

