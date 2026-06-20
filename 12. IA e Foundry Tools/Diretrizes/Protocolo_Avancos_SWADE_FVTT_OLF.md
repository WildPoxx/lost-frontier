---
titulo: Protocolo de Avanços SWADE/FVTT — Outsiders - Lost Frontier
tipo: Diretriz Técnica
projeto: Outsiders - Lost Frontier
sistema: Savage Worlds Adventure Edition
foundry: v13
swade: 5.2.6
status: Consolidado após teste com Helena Brimstone III
data: 2026-05-26
---

# Protocolo de Avanços SWADE/FVTT — Outsiders - Lost Frontier

```markdown
[Task] : PROTOCOLO : Foundry/SWADE : avanços de NPCs e PCs : Outsiders - Lost Frontier
```

## 1. Finalidade

Este protocolo define como scripts de criação/correção de Actors em Foundry VTT devem registrar **Advances** no sistema SWADE 5.2.6 sem quebrar a ficha oficial/customizada.

O objetivo é permitir que NPCs e PCs criados por macro já apareçam com:

- Rank correto;
- quantidade de Advances correta;
- aba nativa de Advances funcional;
- lista auditável de avanços;
- compatibilidade com `CharacterSheet#getAdvances`.

Este protocolo foi consolidado após o erro recorrente identificado em **Helena Brimstone III**, no qual a ficha não abria por causa de valores inválidos em `system.advances.list[].sort`.

---

## 2. Diagnóstico técnico

No SWADE 5.2.6, a ficha processa os avanços pelo método interno:

```js
#getAdvances() {
  const retVal = new Array();
  const advances = this.actor.system.advances.list;

  for (const advance of advances) {
    advance.enrichedNotes = await this.#enrichText(advance.notes);
    const sort = advance.sort;
    const rankIndex = util.getRankFromAdvance(advance.sort);
    const rank = util.getRankFromAdvanceAsString(sort);

    if (!retVal[rankIndex]) {
      retVal.push({ rank, list: [] });
    }

    retVal[rankIndex].list.push(advance);
  }

  return retVal;
}
```

O ponto crítico é:

```js
util.getRankFromAdvance(advance.sort)
```

Portanto, `advance.sort` **não é peso de ordenação Foundry**.

Em `system.advances.list`, `sort` significa o **número real do avanço na trilha**.

---

## 3. Regra principal

Nunca usar:

```js
sort: index * 1000
```

Nunca usar:

```js
sort: 0
```

Sempre usar:

```js
sort: index + 1
```

Exemplo correto para 10 avanços:

```js
sort: 1
sort: 2
sort: 3
sort: 4
sort: 5
sort: 6
sort: 7
sort: 8
sort: 9
sort: 10
```

---

## 4. Estrutura correta de um Advance

Cada entrada de `system.advances.list` deve seguir este formato mínimo:

```js
{
  id: foundry.utils.randomID(8),
  type: 0,
  sort: 1,
  rank: 0,
  planned: false,
  notes: "Arcane Background (Technomancer)"
}
```

### Campos

| Campo | Tipo | Obrigatório | Função |
|---|---:|---:|---|
| `id` | string | sim | identificador interno do avanço |
| `type` | number | sim | tipo de avanço segundo enum SWADE |
| `sort` | number | sim | número real do avanço na trilha |
| `rank` | number | recomendado | rank calculado a partir de `sort` |
| `planned` | boolean | sim | se é avanço planejado |
| `notes` | string | sim | descrição exibida na ficha |

Não persistir manualmente:

```js
enrichedNotes
```

Esse campo é gerado pela ficha para renderização. Não deve ser tratado como fonte de verdade.

---

## 5. Enum de tipos de avanço

No SWADE 5.2.6, os tipos válidos são:

```js
const ADVANCE_TYPE = {
  EDGE: 0,
  SINGLE_SKILL: 1,
  TWO_SKILLS: 2,
  ATTRIBUTE: 3,
  HINDRANCE: 4
};
```

### Regras

- Não existe `type: "power"`.
- Não existe `type: "combat"`.
- Não usar strings em `type`.
- Não inventar enums fora do SWADE.

Quando um avanço representar aquisição de Power, protocolo especial, refinamento narrativo ou pacote de combate, usar normalmente:

```js
type: ADVANCE_TYPE.EDGE
```

ou registrar o detalhe em `notes` e em `Advancement Audit`.

---

## 6. Cálculo de Rank a partir do número do avanço

O SWADE usa o número do avanço para determinar o Rank.

Função canônica para scripts OLF:

```js
function getRankNumberFromAdvanceNumber(n) {
  if (n <= 3) return 0;       // Novice
  if (n <= 7) return 1;       // Seasoned
  if (n <= 11) return 2;      // Veteran
  if (n <= 15) return 3;      // Heroic
  return 4;                   // Legendary
}
```

### Tabela

| Advance | Rank numérico | Rank textual |
|---:|---:|---|
| 1–3 | 0 | Novice |
| 4–7 | 1 | Seasoned |
| 8–11 | 2 | Veteran |
| 12–15 | 3 | Heroic |
| 16+ | 4 | Legendary |

---

## 7. Função padrão para criação de lista de avanços

Todo script OLF que criar Actor com avanços deve usar uma função equivalente a esta:

```js
function buildSwadeAdvanceList(advances) {
  return advances.map((adv, index) => {
    const sort = index + 1;

    return {
      id: foundry.utils.randomID(8),
      type: Number(adv.type),
      sort,
      rank: getRankNumberFromAdvanceNumber(sort),
      planned: Boolean(adv.planned ?? false),
      notes: String(adv.notes ?? "")
    };
  });
}
```

Com a função auxiliar:

```js
function getRankNumberFromAdvanceNumber(n) {
  if (n <= 3) return 0;
  if (n <= 7) return 1;
  if (n <= 11) return 2;
  if (n <= 15) return 3;
  return 4;
}
```

---

## 8. Bloco correto em `actor.update` ou `Actor.create`

Ao criar ou corrigir Actor, usar:

```js
await actor.update({
  "system.advances": {
    mode: "expanded",
    value: advances.length,
    rank: "Veteran",
    details: "Veteran Wild Card NPC with 10 advances.",
    list: buildSwadeAdvanceList(advances)
  }
}, { diff: false });
```

### Observação

Usar `{ diff: false }` quando for substituir o objeto `system.advances` inteiro. Isso evita merge parcial sujo com listas antigas.

---

## 9. Rank textual e quantidade de avanços

Para NPCs criados por script, registrar simultaneamente:

```js
"system.advances.value": 10
"system.advances.rank": "Veteran"
```

E também em flags OLF:

```js
"flags.outsiders-lost-frontier.rank": "Veteran"
"flags.outsiders-lost-frontier.advances": 10
```

### Importante

Flags OLF são úteis para auditoria, mas a ficha do SWADE não usa flags OLF para calcular ou exibir Advances.

A ficha lê:

```js
system.advances.value
system.advances.rank
system.advances.list
```

---

## 10. Advancement Audit obrigatório para NPCs complexos

Para NPCs Wild Card importantes, criar também uma `ability` chamada:

```text
Advancement Audit — [Nome do NPC]
```

Função:

- registrar a intenção mecânica dos avanços;
- facilitar revisão humana;
- preservar rastreabilidade caso a lista nativa seja editada manualmente;
- documentar escolhas que não se traduzem perfeitamente nos enums do SWADE.

Modelo:

```js
{
  name: "Advancement Audit — Helena Brimstone III",
  type: "ability",
  system: {
    description: `
      <h2>Veteran Wild Card — 10 Advances</h2>
      <ol>
        <li>Arcane Background (Technomancer)</li>
        <li>Asimovian Mage</li>
        <li>Focus and Demon Hunter field training</li>
        <li>Alertness</li>
        <li>Asimovian Channeler</li>
        <li>Strain Specialist (Aethera)</li>
        <li>Strain Specialist (Dhuron)</li>
        <li>Combat field refinement</li>
        <li>Improved Asimovian Channeler</li>
        <li>Banish and advanced Warden containment protocols</li>
      </ol>
    `
  }
}
```

---

## 11. Antipadrões proibidos

### 11.1. Usar `sort` como peso Foundry

Proibido:

```js
sort: index * 1000
```

Causa erro em `CharacterSheet#getAdvances`.

---

### 11.2. Usar Rank como string dentro de cada avanço

Proibido:

```js
rank: "Veteran"
```

Correto:

```js
rank: 2
```

---

### 11.3. Usar tipo como string

Proibido:

```js
type: "edge"
type: "skill"
type: "power"
```

Correto:

```js
type: 0
type: 1
type: 2
type: 3
type: 4
```

---

### 11.4. Criar campos de renderização como fonte de verdade

Evitar persistir:

```js
enrichedNotes
```

A ficha gera isso automaticamente.

---

### 11.5. Acreditar que flags bastam

Incorreto:

```js
flags.outsiders-lost-frontier.rank = "Veteran"
flags.outsiders-lost-frontier.advances = 10
```

Isso não atualiza a ficha. É apenas metadado.

---

## 12. Checklist obrigatório pós-criação

Após criar Actor por script, conferir:

```text
[ ] A ficha abre sem erro no console.
[ ] Header mostra o Rank correto.
[ ] Header mostra o total correto de Advances.
[ ] Aba Advances abre.
[ ] Advances estão numerados 1..N.
[ ] Nenhum Advance tem sort 0.
[ ] Nenhum Advance tem sort 1000, 2000 etc.
[ ] Nenhum Advance tem type string.
[ ] Nenhum Advance tem rank string.
[ ] Advancement Audit existe em Abilities para NPCs importantes.
```

---

## 13. Função de validação recomendada

Antes de atualizar um Actor, scripts OLF devem validar a lista:

```js
function validateSwadeAdvanceList(list) {
  const validTypes = new Set([0, 1, 2, 3, 4]);

  for (let i = 0; i < list.length; i++) {
    const adv = list[i];
    const expectedSort = i + 1;

    if (!Number.isFinite(Number(adv.sort))) {
      throw new Error(`Advance ${i + 1}: sort must be a finite number.`);
    }

    if (Number(adv.sort) !== expectedSort) {
      throw new Error(`Advance ${i + 1}: sort must be ${expectedSort}, got ${adv.sort}.`);
    }

    if (!validTypes.has(Number(adv.type))) {
      throw new Error(`Advance ${i + 1}: invalid type ${adv.type}.`);
    }

    if (typeof adv.notes !== "string") {
      throw new Error(`Advance ${i + 1}: notes must be a string.`);
    }
  }

  return true;
}
```

---

## 14. Política para casos instáveis

Se a ficha continuar quebrando mesmo com schema correto:

1. parar de popular `system.advances.list`;
2. mudar `system.advances.mode` para `legacy`;
3. registrar o total em `system.advances.value`;
4. registrar o Rank em `system.advances.rank`;
5. registrar os detalhes em `system.advances.details` e `Advancement Audit`.

Fallback estável:

```js
"system.advances": {
  mode: "legacy",
  value: 10,
  rank: "Veteran",
  details: "Veteran Wild Card NPC with 10 advances. See Advancement Audit.",
  list: []
}
```

Essa solução é aceitável apenas se a lista expandida estiver comprovadamente instável.

---

## 15. Aplicação obrigatória em scripts futuros

Todo script futuro de criação de Actor OLF deve seguir este fluxo:

```text
1. Definir matriz mecânica do NPC.
2. Definir Rank e número de Advances.
3. Criar ADVANCES com tipos válidos SWADE.
4. Gerar system.advances.list com sort 1..N.
5. Validar lista antes de Actor.create/actor.update.
6. Criar Actor.
7. Inserir Skills, Edges, Powers e Gear.
8. Criar Advancement Audit para NPCs Wild Card importantes.
9. Abrir ficha ou orientar teste visual.
10. Exportar Actor validado.
```

---

## 16. Modelo mínimo reutilizável

```js
const ADVANCE_TYPE = {
  EDGE: 0,
  SINGLE_SKILL: 1,
  TWO_SKILLS: 2,
  ATTRIBUTE: 3,
  HINDRANCE: 4
};

function getRankNumberFromAdvanceNumber(n) {
  if (n <= 3) return 0;
  if (n <= 7) return 1;
  if (n <= 11) return 2;
  if (n <= 15) return 3;
  return 4;
}

function buildSwadeAdvanceList(advances) {
  return advances.map((adv, index) => {
    const sort = index + 1;
    return {
      id: foundry.utils.randomID(8),
      type: Number(adv.type),
      sort,
      rank: getRankNumberFromAdvanceNumber(sort),
      planned: Boolean(adv.planned ?? false),
      notes: String(adv.notes ?? "")
    };
  });
}

function validateSwadeAdvanceList(list) {
  const validTypes = new Set([0, 1, 2, 3, 4]);
  for (let i = 0; i < list.length; i++) {
    const adv = list[i];
    const expectedSort = i + 1;
    if (Number(adv.sort) !== expectedSort) throw new Error(`Advance ${i + 1}: invalid sort.`);
    if (!validTypes.has(Number(adv.type))) throw new Error(`Advance ${i + 1}: invalid type.`);
    if (typeof adv.notes !== "string") throw new Error(`Advance ${i + 1}: notes must be string.`);
  }
  return true;
}
```

---

## 17. Status

Este protocolo deve ser tratado como **diretriz obrigatória** para qualquer criação automatizada de Actor em OLF usando Foundry VTT v13 e SWADE 5.2.6.

A falha original de Helena Brimstone III foi resolvida ao substituir:

```js
sort: index * 1000
```

por:

```js
sort: index + 1
```

