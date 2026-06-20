# Plano FQL — Rust under the Stars

## Estrutura recomendada

- Quest principal: `Ferrugem sob as Estrelas`
- Subquests:
  - `Ato I - O Rastro sob a Ferrugem`
  - `Ato II - A Chave de Rastro`
  - `Ato III - A Vespera Quebrada`
  - `Rumores e Pontas Soltas`

## Regra de uso

O Quest Log registra o que os jogadores sabem, perseguem ou podem escolher fazer. Segredos do mestre ficam fora do FQL.

## Estados

- `inactive`: preparado, não revelado aos jogadores.
- `available`: conhecido, mas ainda não assumido.
- `active`: objetivo atual.
- `completed`: resolvido.
- `failed`: perdido, sabotado ou assumido por outra facção.

## Procedimento sugerido

1. Rodar o macro `rust_under_the_stars_fql_seed_macro.js` como GM.
2. Conferir a pasta `_fql_quests` ou abrir o Quest Log.
3. Manter tudo `inactive` até começar a sessão.
4. Mover a quest principal para `available` ou `active` quando os PCs se envolverem com Floyd, Dentinho, Lorna ou o SWIX.
5. Ativar cada subquest por ato.
6. Nunca revelar objetivos ocultos antes da ficção justificar.

## Nota técnica

O macro cria JournalEntries com a flag:

```js
flags: {
  "forien-quest-log": {
    json: { ...questData }
  }
}
```

O FQL usa esses JournalEntries na pasta `_fql_quests` como base de dados interna.
