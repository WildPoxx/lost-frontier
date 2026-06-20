# Diretrizes de Criação de Criaturas SWADE/FVTT — OutsiderS: Lost Frontier

**Projeto:** OutsiderS — Lost Frontier Companion  
**Sistema:** Savage Worlds Adventure Edition  
**Foundry VTT:** v13  
**SWADE:** 5.2.6  
**Escopo:** criação, correção, importação e consolidação de criaturas para o compendium `OLF - Bestiary`  
**Arquivo-alvo final:** `packs/olf-bestiary.db`  
**Status:** diretriz técnica consolidada após testes operacionais com `Sandworm, Adult`  
**Última revisão:** 2026-05-19

---

# 1. Princípio central

Criatura de bestiário para Foundry/SWADE não é apenas um stat block textual.

Ela deve funcionar como **Actor mecânico operacional**.

Portanto, a IA deve distinguir rigidamente entre:

| Camada | Função | Fonte de verdade |
|---|---|---|
| Design SWADE | define Scale, Size, Armor, Toughness, Wounds, ataques e habilidades | documento de bestiário |
| Actor Foundry | executa os campos mecânicos no sistema SWADE | JSON exportado/importado |
| Apresentação textual | descreve a criatura para o Mestre | Biography, Special Abilities, Notes |
| Asset visual | portrait/token usados em ficha e cena | `img` e `prototypeToken.texture.src` |

Regra operacional:

> Se o Foundry não computa, não está implementado.

Exemplo: escrever `Armor +5` como Special Ability descritiva não basta. A Armor só está correta quando o valor aparece mecanicamente na ficha, especialmente no escudo de Toughness.

---

# 2. Ordem correta de trabalho

A criação ou correção de criaturas deve seguir esta ordem:

```text
1. Ler a matriz mecânica da criatura.
2. Definir Scale e Size.
3. Definir Vigor, Armor e Toughness esperada.
4. Verificar Wounds por escala.
5. Criar ou corrigir o Actor JSON.
6. Inserir Armor natural como item funcional, se houver.
7. Preservar portrait e token se já existirem.
8. Importar no Foundry.
9. Conferir visualmente Size, Toughness, Armor e Gear.
10. Exportar o Actor corrigido.
11. Só então consolidar no .db.
```

A IA não deve gerar novo `.db` final enquanto houver incerteza sobre o comportamento dos Actors no Foundry.

---

# 3. Scale, Size e Wounds

## 3.1. Scale e Size

O campo `system.stats.size` é obrigatório.

Não basta escrever “Huge”, “Large” ou “Gargantuan” na descrição. O valor numérico precisa estar no Actor.

Modelo:

```json
"system": {
  "stats": {
    "size": 11
  }
}
```

## 3.2. Matriz recomendada

| Categoria SWADE | Faixa Size | Uso no OLF | Wounds adicionais esperadas |
|---|---:|---|---:|
| Tiny | -4 | microfauna, insetos mínimos | 0 |
| Very Small | -3 | parasitas maiores | 0 |
| Small | -2 | predadores pequenos | 0 |
| Normal | -1 a 3 | humanos, Bondaks, montarias, animais grandes | 0 |
| Large | 4 a 7 | Urakhshor, Khar'Basil, caranguejos de casco | +1 |
| Huge | 8 a 11 | Sandworms jovens/adultas, Kryll Dragons, Thrag'gor | +2 |
| Gargantuan | 12+ | Sandworms ancilares, megafauna de set piece | +3 |

## 3.3. Wounds no Actor

Para Extras de bestiário, o campo deve refletir a durabilidade total esperada:

```json
"wounds": {
  "value": 0,
  "max": 3,
  "ignored": 0
}
```

Exemplo: uma criatura **Huge** Extra costuma aparecer com `wounds.max = 3` quando o projeto está tratando os Wounds adicionais como parte da ficha operacional.

A IA deve conferir isso criatura por criatura. Não presumir.

---

# 4. Toughness em SWADE/FVTT

## 4.1. Cálculo observado no Foundry/SWADE

Com `autoCalcToughness: true`, o Foundry/SWADE calcula Toughness a partir de:

```text
Toughness = contribuição de Vigor + Size + Armor equipada
```

A contribuição básica de Vigor segue a escala:

| Vigor | Contribuição |
|---|---:|
| d4 | 4 |
| d6 | 5 |
| d8 | 6 |
| d10 | 7 |
| d12 | 8 |
| d12+N | 8 + N |

Exemplo confirmado com `Sandworm, Adult`:

```text
Vigor d12 = 8
Size 11 = +11
Armor +5 = +5

Toughness = 24 (5)
```

## 4.2. Toughness final

O campo deve existir no Actor:

```json
"stats": {
  "toughness": {
    "value": 24,
    "armor": 5,
    "modifier": 0
  }
}
```

Mas a IA não deve confiar apenas nesse campo se `autoCalcToughness` estiver ativo. O teste real é a ficha do Foundry.

## 4.3. Modificadores

Não confiar em:

```json
"system.stats.toughness.modifier": 1
```

como solução para divergências enquanto `autoCalcToughness: true`.

Se a Toughness desejada não bate com o cálculo automático, há apenas três caminhos seguros:

```text
1. Corrigir Size, Armor ou Vigor.
2. Criar uma fonte mecânica real e testada que some Toughness.
3. Desligar autoCalcToughness e tratar Toughness manualmente, registrando essa exceção.
```

A opção 3 deve ser exceção, não regra.

---

# 5. Armor natural: regra crítica

## 5.1. Problema identificado

Em Foundry/SWADE, `Armor +X` como Special Ability pode ser apenas texto.

Isso não computa automaticamente.

Exemplo incorreto:

```json
{
  "name": "Armor +5",
  "type": "ability",
  "system": {
    "description": "Armor +5"
  }
}
```

Isso pode servir como descrição, mas não como implementação mecânica.

## 5.2. Forma correta para criaturas OLF

Para criaturas do bestiário, Armor natural deve ser implementada como **Gear do tipo armor**, embutido no Actor:

```json
{
  "name": "Armor +5",
  "type": "armor",
  "img": "systems/swade/assets/icons/armor.svg",
  "system": {
    "armor": 5,
    "description": "<p>Natural armored hide and reinforced plates.</p>",
    "equippable": true,
    "equipStatus": 3,
    "isNaturalArmor": true,
    "locations": {
      "arms": true,
      "head": true,
      "legs": true,
      "torso": true
    },
    "quantity": 1,
    "weight": 0,
    "price": 0,
    "minStr": "",
    "toughness": 0,
    "isHeavyArmor": false
  }
}
```

## 5.3. Campo decisivo: `equipStatus`

Este foi o ponto crítico revelado pelo teste.

| Valor | Comportamento observado | Ícone | Computa Armor? |
|---:|---|---|---|
| `1` | item carregado | bolsa | não |
| `3` | item equipado/vestido | camiseta | sim |

Regra absoluta:

```json
"equipStatus": 3
```

Armor natural embutida em Actor JSON deve vir equipada.

Se aparecer o ícone de bolsa, está errado.

Se aparecer o ícone de camiseta, está correto.

## 5.4. Teste visual obrigatório

Após importar o Actor, verificar:

```text
1. Gear > Armors mostra Armor +X.
2. O ícone do item é uma camiseta, não uma bolsa.
3. O escudo de Toughness mostra X.
4. Tooltip de Toughness inclui Armor: +X.
5. Toughness final bate com Vigor + Size + Armor.
```

Para `Sandworm, Adult`, o resultado esperado é:

```text
Size 11
Armor +5
Toughness 24 (5)
```

---

# 6. Special Abilities

## 6.1. Função correta

Special Abilities devem registrar comportamento, regras especiais e exceções de uso.

Exemplos:

```text
Burrow 20
Hardy
Swat
Swallow Whole
Attracted to Vibration
Devour Vehicle
```

## 6.2. Função incorreta

Special Ability não deve ser usada como substituto de campo mecânico quando o Foundry exige item, efeito ou atributo próprio.

Evitar:

```text
Armor +5 apenas como Special Ability
Size 11 apenas como Special Ability
Flight apenas textual, sem pace.fly quando necessário
```

## 6.3. Quando uma Ability precisa de Active Effect

Se uma habilidade altera um campo mecânico, a IA deve avaliar se precisa de Active Effect.

Exemplo conceitual:

```json
"changes": [
  {
    "key": "system.stats.toughness.armor",
    "mode": 2,
    "value": 4
  }
]
```

Contudo, para o bestiário OLF, a opção preferencial para Armor natural é **item `type: armor` equipado**, não Active Effect.

---

# 7. Imagens, tokens e paths

## 7.1. Preservação obrigatória

Se um Actor exportado já possui `img` e `prototypeToken.texture.src`, a IA deve preservar esses caminhos.

Exemplo:

```json
"img": "worlds/outsiders-lost-frontier/imgs/bestiary/sandworm-trans.webp"
```

```json
"prototypeToken": {
  "texture": {
    "src": "worlds/outsiders-lost-frontier/imgs/bestiary/beast-tokens/token_sandworm.webp"
  }
}
```

Não substituir por ícones genéricos.

## 7.2. Imagens não são embutidas

Exportar Actor JSON não embute a imagem.

O JSON guarda apenas o caminho.

Para portabilidade do módulo, os arquivos de imagem precisam existir exatamente nesses paths ou devem ser migrados para paths de módulo.

## 7.3. Regra para módulo final

Para distribuição do módulo, preferir paths como:

```text
modules/outsiders-lost-frontier/imgs/bestiary/...
```

Para teste em mundo local, preservar paths existentes:

```text
worlds/outsiders-lost-frontier/imgs/bestiary/...
```

Não converter automaticamente sem autorização.

---

# 8. Actor JSON individual versus `.db`

## 8.1. Durante testes

Usar arquivos individuais:

```text
sandworm-adult.json
kryll-dragon.json
urakhshor.json
```

Não usar `.db` enquanto houver correções mecânicas em aberto.

Motivo: o usuário pode importar e testar Actor por Actor sem substituir o compendium inteiro.

## 8.2. Após validação

Somente depois de testar e exportar os Actors corrigidos do Foundry:

```text
1. consolidar os JSONs finais;
2. gerar novo `packs/olf-bestiary.db`;
3. atualizar o módulo;
4. empacotar, se solicitado.
```

## 8.3. Fonte superior

Quando houver divergência entre:

```text
A. arquivo .db gerado previamente
B. Actor corrigido/exportado do Foundry
```

a fonte superior é:

```text
B. Actor corrigido/exportado do Foundry
```

---

# 9. Scripts de correção no Foundry

## 9.1. Regra de segurança

Scripts não devem atualizar Actors apenas por nome.

Motivo:

```text
nomes podem duplicar;
imports podem gerar "(imp)";
o compendium pode conter múltiplas versões;
o mundo pode ter cópias temporárias.
```

## 9.2. Usar Actor ID explícito

Scripts devem exigir ID real do Actor:

```js
const ACTOR_IDS = {
  "Sandworm, Adult": "PASTE_WORLD_ACTOR_ID_HERE"
};
```

O script deve buscar por:

```js
game.actors.get(actorId)
```

Não por:

```js
game.actors.getName("Sandworm, Adult")
```

## 9.3. Confirmar mismatch

Se o ID aponta para Actor com nome diferente, o script deve pedir confirmação ou abortar.

---

# 10. Checklist obrigatório por criatura

Antes de considerar uma criatura pronta:

## 10.1. Identificação

```text
[ ] name correto
[ ] type = npc
[ ] folder correto ou neutro para importação
[ ] flags do projeto preservadas ou atualizadas
```

## 10.2. Imagem

```text
[ ] img preservado
[ ] prototypeToken.texture.src preservado
[ ] token width/height coerente com Size/Scale
[ ] actorLink false, salvo exceção
```

## 10.3. Scale e Size

```text
[ ] Scale registrado em flags ou notes
[ ] system.stats.size correto
[ ] Special Ability de Size, se existir, não contradiz o campo real
```

## 10.4. Toughness

```text
[ ] Vigor conferido
[ ] Size conferido
[ ] Armor conferida
[ ] Toughness final bate no Foundry
[ ] escudo mostra Armor correta
[ ] tooltip de Toughness não contradiz a matriz
```

## 10.5. Armor

```text
[ ] item type = armor
[ ] system.armor = valor correto
[ ] system.equippable = true
[ ] system.equipStatus = 3
[ ] system.isNaturalArmor = true, se for natural
[ ] locations adequadas
[ ] ícone visual = camiseta
[ ] escudo mostra o valor
```

## 10.6. Wounds

```text
[ ] wounds.max coerente com Scale
[ ] Wild Card ou Extra tratado corretamente
[ ] Hardy/Resilient, se houver, implementado ou registrado
```

## 10.7. Skills e Attacks

```text
[ ] Skills com dice corretos
[ ] ataques que precisam rolar dano foram criados como weapon/action, quando necessário
[ ] habilidades apenas narrativas ficaram como ability
[ ] Heavy Weapon/Heavy Armor conferidos quando aplicável
```

---

# 11. Exemplo de referência: Sandworm, Adult

## 11.1. Campos esperados

```text
Name: Sandworm, Adult
Scale: Huge
Size: 11
Vigor: d12
Armor: +5
Toughness automática: 24 (5)
Wounds max: 3
```

## 11.2. Cálculo

```text
Vigor d12 = 8
Size 11 = 11
Armor +5 = 5

8 + 11 + 5 = 24
```

## 11.3. Armor funcional

```json
{
  "name": "Armor +5",
  "type": "armor",
  "img": "systems/swade/assets/icons/armor.svg",
  "system": {
    "armor": 5,
    "equippable": true,
    "equipStatus": 3,
    "isNaturalArmor": true,
    "locations": {
      "arms": true,
      "head": true,
      "legs": true,
      "torso": true
    }
  }
}
```

## 11.4. Resultado visual esperado

```text
Gear > Armors: Armor +5
Ícone: camiseta
Toughness: 24
Escudo: 5
```

---

# 12. Erros proibidos

A IA não deve repetir estes erros:

```text
[ ] Gerar Size 0 para criaturas Large/Huge/Gargantuan.
[ ] Tratar Armor +X apenas como texto.
[ ] Criar Armor em Gear com equipStatus 1.
[ ] Aceitar ícone de bolsa como Armor funcional.
[ ] Trocar portrait/token por paths genéricos.
[ ] Regenerar .db inteiro antes de testar Actor individual.
[ ] Atualizar Actor por nome em script de correção.
[ ] Usar Toughness manual incompatível sem registrar exceção.
[ ] Presumir que item isolado se comporta igual a item embutido no Actor.
```

---

# 13. Fluxo recomendado para próximas correções

## 13.1. Quando o usuário já corrigiu no Foundry

Pedir o export do Actor corrigido.

Usar esse export como matriz principal.

Não reconstruir do zero.

## 13.2. Quando for gerar teste

Gerar um arquivo individual:

```text
nome-da-criatura-tested.json
```

Não gerar `.db`.

## 13.3. Quando vários Actors precisarem de patch

Preferir duas opções:

```text
A. pasta zipada com JSON individual de cada Actor;
B. script de patch por Actor ID explícito.
```

Nunca usar update massivo por nome.

## 13.4. Quando for fechar o bestiário

Somente após todos os Actors importarem corretamente:

```text
1. usuário exporta os Actors corrigidos;
2. IA valida campos críticos;
3. IA gera novo olf-bestiary.db;
4. usuário testa compendium;
5. só então empacotar módulo.
```

---

# 14. Regra final

Para o bestiário OLF, uma criatura só está correta quando:

```text
o design SWADE,
o JSON do Actor,
a ficha visual do Foundry,
o cálculo de Toughness,
a Armor equipada,
as imagens,
o token
e o uso em mesa
dizem a mesma coisa.
```

Se qualquer camada contradiz as demais, o Actor ainda não está pronto.
