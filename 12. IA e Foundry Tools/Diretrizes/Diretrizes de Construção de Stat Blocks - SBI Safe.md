
# Diretrizes de Geração de Stat Blocks — SBI Optimization v3

## I. Identificação

**Projeto:** Outsiders — Lost Frontier  
**Sistema:** Savage Worlds Adventure Edition — SWADE  
**Ambiente:** Foundry VTT 13 / SWADE 5.2.6  
**Módulo-alvo:** SWADE Stat Block Importer (SBI)  
**Uso principal:** conversão de PCs, NPCs e criaturas para Stat Blocks importáveis via SBI  
**Status:** versão consolidada após testes operacionais extensivos

---

# II. Objetivo

Este documento define o padrão obrigatório para geração de Stat Blocks destinados ao SBI.

O objetivo NÃO é produzir texto bonito, narrativo ou completo.

O objetivo é:

- importar sem erro;
- preservar estrutura mecânica;
- minimizar corrupção de parsing;
- evitar duplicação de Active Effects;
- impedir geração de itens inválidos;
- reduzir necessidade de retrabalho;
- estabilizar importações recorrentes.

---

# III. Princípio Central

O SBI NÃO interpreta significado.

Ele opera por:

- parsing linear;
- regex;
- delimitadores;
- padrões textuais;
- nomes reconhecíveis;
- ordem esperada;
- tokens;
- cabeçalhos;
- pontuação.

Portanto:

> O Stat Block deve ser tratado como artefato técnico de importação.

Não como texto narrativo.

---

# IV. Filosofia SBI Optimization

## Regra principal

Entre:

1. importar mais conteúdo automaticamente;
2. importar menos conteúdo com maior estabilidade;

sempre escolher:

> importar menos conteúdo com maior estabilidade.

---

# V. Linguagem obrigatória

Sempre usar inglês.

## Correto

```text
Attributes:
Skills:
Edges:
Hindrances:
Gear:
Powers:
Power Points:
```

## Proibido

```text
Atributos:
Perícias:
Vantagens:
Complicações:
Equipamentos:
```

---

# VI. Estrutura Canônica SBI-safe

## PC / Wild Card

```text
Name
Wild Card
Rank Gender Ancestry

Attributes: ...
Skills: ...
Pace: X; Parry: X; Toughness: X
Bennies: X
Hindrances: ...
Edges: ...
Powers: ...
Power Points: X
Gear: ...
```

---

## Extra

```text
Name
Rank Gender Ancestry

Attributes: ...
Skills: ...
Pace: X; Parry: X; Toughness: X
Hindrances: ...
Edges: ...
Gear: ...
```

---

# VII. Ordem obrigatória

1. Nome
2. Wild Card (se aplicável)
3. Linha de conceito
4. Attributes
5. Skills
6. Pace/Parry/Toughness
7. Bennies
8. Hindrances
9. Edges
10. Powers
11. Power Points
12. Gear

---

# VIII. Campos proibidos

Nunca incluir no bloco principal:

```text
Current Wealth:
Current Load:
Languages:
Languages Known:
Books In Use:
Setting Rules:
Setting Modlines:
Background:
Notes:
Biography:
Arcane Background:
Current Power Points:
Advances:
```

Esses dados devem ir para:

```markdown
## Ajustes manuais pós-importação
```

---

# IX. Nome e conceito

## Nome

Usar nome limpo.

## Correto

```text
Kaelen
```

## Proibido

```text
Player Character: Kaelen
NPC: Kaelen
Kaelen — blind pilot fugitive
```

---

## Linha de conceito

Formato curto:

```text
Novice Male Human
```

Sem lore.

---

# X. Attributes

## Formato obrigatório

```text
Attributes: Agility d8, Smarts d6, Spirit d6, Strength d6, Vigor d6
```

## Ordem obrigatória

1. Agility
2. Smarts
3. Spirit
4. Strength
5. Vigor

---

# XI. Skills

## Formato obrigatório

```text
Skills: Athletics d6, Notice d6, Shooting d8
```

---

## Idiomas

Idiomas devem entrar SOMENTE como perícia.

## Correto

```text
Skills: Language (Native) d8
```

## Proibido

```text
Languages: Native d8
Language:
Languages Known:
```

---

## Modificadores

### Regra

Se o bônus vier de Edge/Hindrance reconhecida:

NÃO embutir na perícia.

## Correto

```text
Skills: Notice d6
Edges: Alertness
```

## Proibido

```text
Skills: Notice d6+2
Edges: Alertness
```

---

## Quando usar +X

Somente quando o bônus for estrutural/custom e NÃO vier de item reconhecido.

---

# XII. Pace, Parry e Toughness

## Formato obrigatório

```text
Pace: 6; Parry: 5; Toughness: 7 (2)
```

---

## Regras

- usar valores finais;
- não recalcular manualmente;
- armor em parênteses.

---

# XIII. Bennies

## Formato

```text
Bennies: 3
```

---

# XIV. Hindrances

## Formato

```text
Hindrances: Blind (Major), Wanted (Minor)
```

---

## Proibido

```text
Hindrances: Secret (minor, arm fused with Campo artifact)
```

Detalhes vão para pós-importação.

---

# XV. Edges

## Formato

```text
Edges: Ace, Alertness, Danger Sense
```

---

## Arcane Background

Sempre em Edges.

## Correto

```text
Edges: Arcane Background (Gifted)
```

---

## Regra anti-duplicação

Nunca duplicar bônus já aplicados por Edge.

---

# XVI. Powers

## Formato seguro

```text
Powers: Boost Trait
Power Points: 15
```

---

## Regra crítica

Usar sempre nome-base do poder.

---

## Proibido

```text
Powers: Boost/Lower Trait
```

---

## Correto

```text
Powers: Boost Trait
```

Renomear manualmente depois.

---

# XVII. Gear

## Formato obrigatório

```text
Gear: Unarmed (Str), Knife (Str+d4), Laser Pistol (Range 15/30/60, Damage 2d6, RoF 1, AP 2)
```

---

## Regra

Usar uma única linha.

---

## Evitar

- subdivisões;
- notas;
- riqueza;
- carga;
- peso;
- descrições longas.

---

# XVIII. SPECIAL ABILITIES — CAMPO DE ALTO RISCO

## REGRA OPERACIONAL

`Special Abilities:` deve ser considerado:

> campo hostil e instável.

---

# XIX. REGRA DE OURO

Para PCs e NPCs humanoides:

> NÃO usar `Special Abilities:`.

---

# XX. Proibição explícita

NUNCA usar `Special Abilities:` para:

- Arcane Background;
- Gifted;
- Powers;
- habilidades humanas simples;
- vantagens customizadas;
- pequenos bônus;
- capacidades de ladrão;
- efeitos passivos leves.

---

# XXI. Casos proibidos

## Proibido

```text
Special Abilities:
Gifted
```

---

## Proibido

```text
Special Abilities:
Resilient
```

---

## Proibido

```text
Special Abilities:
Scuttle
```

---

## Proibido

```text
Special Abilities:
Gifted: Power Points 15
```

---

# XXII. Motivo da proibição

Esses padrões já produziram:

- fragmentação por caracteres;
- itens vazios;
- corrupção de parsing;
- importações quebradas;
- abilities transformadas em letras individuais;
- arrays inválidos.

---

# XXIII. HUMANOID SAFE MODE

Para humanoides comuns, usar SOMENTE:

- Attributes
- Skills
- Pace/Parry/Toughness
- Bennies
- Hindrances
- Edges
- Powers
- Power Points
- Gear

Nada além disso.

---

# XXIV. Como lidar com habilidades customizadas

Adicionar manualmente depois da importação.

Usar:

```markdown
## Ajustes manuais pós-importação
```

---

## Exemplo

```text
Resilient: May suffer 1 Wound before Incapacitation.

Scuttle: Ignore 2 points of difficult terrain penalties in scrap environments.
```

---

# XXV. Uso permitido de Special Abilities

Somente para:

- monstros;
- criaturas;
- ancestrais não humanoides;
- armas naturais;
- armor natural;
- imunidades;
- vulnerabilidades;
- senses especiais.

---

# XXVI. Formato permitido

```text
Special Abilities:
@a Armor +2
@w Bite: Str+d6.
@sa Low Light Vision: Ignore illumination penalties.
```

---

# XXVII. Tags aceitas

```text
@sa = Special Ability
@w  = Weapon
@a  = Armor
@e  = Edge
@h  = Hindrance
```

---

# XXVIII. Regra de segurança absoluta

Se existir dúvida sobre usar `Special Abilities:`:

> NÃO usar.

---

# XXIX. Conversão de JSON → SBI

## Procedimento obrigatório

1. identificar tipo do ator;
2. extrair atributos finais;
3. extrair perícias;
4. identificar bônus derivados;
5. separar bônus automáticos;
6. extrair Hindrances limpas;
7. extrair Edges oficiais;
8. simplificar Powers;
9. extrair Gear essencial;
10. remover lore;
11. remover settings;
12. gerar bloco mínimo estável.

---

# XXX. Dados para pós-importação

Tudo que NÃO for parsing estrutural deve ir para:

```markdown
## Ajustes manuais pós-importação
```

Incluindo:

- lore;
- wealth;
- carga;
- limitações de poder;
- trapping;
- setting rules;
- modlines;
- efeitos customizados;
- observações.

---

# XXXI. Checklist pré-entrega

Antes de entregar um Stat Block:

- cabeçalhos em inglês?
- ordem correta?
- nome limpo?
- sem Languages?
- sem Special Abilities humanoides?
- sem lore?
- sem notas?
- sem duplicação de bônus?
- Powers simplificados?
- Gear em linha única?
- bloco mínimo?
- estabilidade priorizada?

---

# XXXII. Checklist pós-importação

Verificar:

## Traits

- atributos corretos;
- perícias corretas;
- modifiers corretos;
- sem duplicação.

---

## Edges/Hindrances

- itens corretos;
- Active Effects corretos;
- sem itens fragmentados.

---

## Gear

- armas corretas;
- armor correta;
- sem lixo importado.

---

## Powers

- Arcane Background correto;
- PP corretos;
- powers corretos;
- sem duplicações;
- customizações feitas manualmente.

---

# XXXIII. Known Issues

## PP Refresh Bug

O botão refresh pode ultrapassar limite máximo de PP.

Conferir manualmente.

---

## Powers customizados

Precisam de edição manual posterior.

---

## Special Abilities

Campo instável.

Evitar quase sempre.

---

# XXXIV. Regra final

O SBI NÃO deve receber:

- lore;
- automação excessiva;
- criatividade estrutural;
- texto híbrido;
- campos experimentais.

O SBI deve receber:

> apenas estrutura mecânica mínima e estável.

---

# XXXV. Exemplos Canônicos

## PC Wild Card

```text
Kaelen
Wild Card
Novice Male Human

Attributes: Agility d10, Smarts d8, Spirit d4, Strength d4, Vigor d6
Skills: Athletics d4, Driving d8, Electronics d4, Focus d4, Language (Native) d8, Notice d6, Piloting d8, Repair d4, Shooting d6
Pace: 6; Parry: 2; Toughness: 5
Bennies: 3
Hindrances: Blind (Major), Outsider (Minor), Wanted (Minor)
Edges: Ace, Alertness, Danger Sense
Gear: Unarmed (Str)
```

---

## PC com poderes

```text
Jax Vale
Wild Card
Novice Male Human

Attributes: Agility d8, Smarts d6, Spirit d6, Strength d6, Vigor d6
Skills: Athletics d8, Electronics d6, Focus d4, Language (Native) d8, Notice d6, Shooting d6, Stealth d6, Survival d6, Thievery d6+1
Pace: 6; Parry: 2; Toughness: 6 (1)
Bennies: 3
Hindrances: Heroic, Poverty, Secret (Minor)
Edges: Arcane Background (Gifted), Thief
Powers: Boost Trait
Power Points: 15
Gear: Dagger/Knife (Str+d4), Laser Pistol (Range 15/30/60, Damage 2d6, RoF 1, AP 2)
```

---

## Extra humanoide seguro

```text
Nikko Varr
Extra
Novice Male Human

Attributes: Agility d8, Smarts d6, Spirit d6, Strength d4, Vigor d6
Skills: Athletics d8, Driving d8, Fighting d4, Notice d6, Shooting d4, Stealth d10, Taunt d6, Thievery d10
Pace: 6; Parry: 4; Toughness: 5
Gear: Light Pistol (Range 12/24/48, Damage 2d6, RoF 1), Rust Knife (Str+d4)
```

---

# XXXVI. Cláusula metodológica final

Quando o SBI exigir escolha entre:

- completude;
- estabilidade;

sempre escolher:

> estabilidade.