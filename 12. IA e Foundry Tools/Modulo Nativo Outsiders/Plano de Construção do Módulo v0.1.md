
# 1. Plano de Construção do Módulo v0.1

A versão **v0.1** deve ser simples, funcional e controlada.

Ela não precisa automatizar tudo. Ela precisa provar que o módulo existe, aparece no Foundry, organiza o conteúdo corretamente e oferece o primeiro pacote jogável de **Outsiders — Lost Frontier**.

## Objetivo da v0.1

> Fazer o módulo aparecer no Foundry VTT v13 e conter o núcleo jogável inicial de Outsiders — Lost Frontier para SWADE, sem alterar o sistema-base.

---

# 2. Identidade do módulo

## 2.1. Nome exibido no Foundry

```text
Outsiders — Lost Frontier
```

Esse é o nome que aparecerá na lista de módulos.

## 2.2. ID técnico

```text
outsiders-lost-frontier
```

Esse nome será usado internamente pelo Foundry.

Regras importantes:

```text
sem acentos
sem espaços
sem letras maiúsculas
sem travessão especial
```

## 2.3. Versão inicial

```text
0.1.0
```

Significado:

```text
0 = ainda não é versão final
1 = primeiro pacote funcional
0 = sem revisão corretiva ainda
```

## 2.4. Sistema-base

```text
swade
```

O módulo dependerá do sistema SWADE.

## 2.5. Foundry-alvo

```text
Foundry VTT v13
```

A compatibilidade deve ser pensada para v13, porque é a versão da mesa.

---

# 3. Descrição curta do módulo

Sugestão de descrição:

```text
Conteúdo de cenário, ancestralidades, Edges, Hindrances, regras de Teleritha, Sincrisólise e suporte inicial para a campanha Outsiders — Lost Frontier usando SWADE no Foundry VTT.
```

Versão mais curta:

```text
Módulo de cenário para Outsiders — Lost Frontier, com conteúdo SWADE, Teleritha, Sincrisólise, ancestralidades e suporte inicial para Rust Hollow.
```

Eu prefiro a segunda: mais limpa para manifesto.

---

# 4. Estrutura inicial de pastas

A versão v0.1 deve ter esta estrutura:

```text
outsiders-lost-frontier/
│
├── module.json
│
├── packs/
│
├── lang/
│   └── pt-BR.json
│
├── scripts/
│
├── styles/
│
└── assets/
    └── icons/
```

## Função de cada pasta

|Pasta/arquivo|Função|Entra na v0.1?|
|---|---|--:|
|`module.json`|Manifesto do módulo|Sim|
|`packs/`|Compêndios do módulo|Sim|
|`lang/`|Tradução/localização|Sim, básico|
|`scripts/`|Macros e scripts futuros|Sim, vazia ou mínima|
|`styles/`|CSS futuro|Sim, vazia ou mínima|
|`assets/icons/`|Ícones próprios futuros|Sim, vazia ou mínima|

Mesmo que algumas pastas fiquem vazias no começo, é útil criá-las para manter a organização.

---

# 5. Compêndios iniciais

A v0.1 deve criar poucos compêndios, mas bem definidos.

## 5.1. Lista de compêndios v0.1

|Nome do compêndio|Tipo|Conteúdo|
|---|---|---|
|`OLF — Ancestralidades`|Item|Humanos, Krohminitas, Orunai, Kitanos|
|`OLF — Edges`|Item|Edges próprios do cenário|
|`OLF — Hindrances`|Item|Hindrances próprios do cenário|
|`OLF — Teleritha e Powers`|Item ou Journal|Cepas, trappings e poderes especiais|
|`OLF — Journals do Cenário`|JournalEntry|Rust Hollow, Companhia, Segunda Trilha etc.|
|`OLF — Facções`|JournalEntry|Facções do primeiro arco|
|`OLF — NPCs e Criaturas`|Actor|Floyd, Dentinho, Synthas, Lorna etc.|
|`OLF — Tabelas`|RollTable|Sobrecarga, prospecção, reações etc.|
|`OLF — Macros`|Macro|Entrará depois; pode ficar preparado|

## 5.2. Decisão prática

Para a v0.1, eu criaria os seguintes compêndios no manifesto:

```text
olf-ancestries
olf-edges
olf-hindrances
olf-teleritha
olf-journals
olf-factions
olf-actors
olf-tables
olf-macros
```

Esses nomes são os IDs técnicos dos compêndios.

---

# 6. Documentos que devem ser criados primeiro

Agora precisamos ordenar. Nem tudo deve ser escrito ao mesmo tempo.

## 6.1. Primeiro bloco — base de personagem

Este é o primeiro bloco funcional.

```text
Ancestry: Humano
Ancestry: Krohminita
Ancestry: Orunai
Ancestry: Kitano
```

Critério: sem isso, o jogador ainda não consegue criar personagem do cenário.

---

## 6.2. Segundo bloco — Hindrances

```text
Dependência — Teleritha
Vulnerabilidade — Vibração
Cognição Alienígena
Rigidez de Padrão
Ciclo Biológico Krohminita
Fraqueza Ambiental — Atmosfera Rarefeita
Vulnerabilidade ao Frio
Ressonância Instável
```

Critério: as desvantagens precisam existir antes das ancestralidades serem finalizadas, porque algumas serão concedidas por elas.

---

## 6.3. Terceiro bloco — Edges

```text
Sintonia com Teleritha
Iniciado em Sincrisólise
Ressonador Orunai
Condutor de Bondak
Condutor de Tal’Bondak
Interface Neural de Rastro
Prospector de Rust Hollow
```

Critério: estes Edges dão identidade mecânica ao cenário.

---

## 6.4. Quarto bloco — Teleritha

```text
Pyra
Gravis
Fluxa
Veyra
Aethera
Pulvis
Osmério
```

Cada entrada deve ter:

```text
descrição
uso tecnológico
uso mecânico
risco
exemplo de trapping
facções interessadas
```

---

## 6.5. Quinto bloco — Sincrisólise

```text
Journal: Regra de Sincrisólise
Edge: Iniciado em Sincrisólise
Hindrance: Ressonância Instável
RollTable: Sobrecarga de Teleritha
```

Critério: Sincrisólise precisa ser ensinável em mesa antes de ser automatizada.

---

## 6.6. Sexto bloco — Rust Hollow

```text
Journal: Rust Hollow
Journal: Companhia Bask-Callico
Journal: Programa Segunda Trilha
Journal: Bondaks
Journal: Tal’Bondaks
Journal: Fragmento SWIX
```

---

## 6.7. Sétimo bloco — Facções

```text
Companhia Bask-Callico
Stargazers
Expedicionários
Guilda de Ferro
Cyberdome
LMT
Abutres de Aço
```

---

## 6.8. Oitavo bloco — NPCs e criaturas

```text
Floyd Merian
Dentinho
Synthas Abi
Lorna Kamen
Bondak comum
Tal’Bondak comum
Agente da Guilda
Técnico Cyberdome
Cepador LMT
```

---

## 6.9. Nono bloco — Tabelas

```text
Sobrecarga de Teleritha
Reação de Tal’Bondak
Complicações de Prospecção
Fenômenos do Campo das Estrelas Cadentes
Interesse de Facção
```

---

# 7. Ordem de trabalho recomendada

Esta deve ser a sequência real.

## Etapa 1 — Criar a carcaça do módulo

Resultado esperado:

```text
O Foundry reconhece o módulo.
O módulo aparece na lista de módulos.
O módulo pode ser ativado no mundo.
```

Arquivos envolvidos:

```text
module.json
pastas básicas
```

Nada de conteúdo ainda.

---

## Etapa 2 — Criar compêndios vazios

Resultado esperado:

```text
Os compêndios aparecem no Foundry.
Eles estão separados por categoria.
Ainda podem estar vazios.
```

Compêndios:

```text
Ancestralidades
Edges
Hindrances
Teleritha
Journals
Facções
NPCs/Criaturas
Tabelas
Macros
```

---

## Etapa 3 — Criar documentos manuais dentro do Foundry

Como você não programa, o caminho mais seguro no começo é:

```text
1. criar os itens pelo Foundry;
2. preencher os campos pela interface;
3. testar se aparecem corretamente;
4. exportar para compêndio;
5. só depois transformar em arquivo distribuível.
```

Isso evita você ter que escrever JSON manualmente.

Você não precisa começar escrevendo código.

---

## Etapa 4 — Consolidar os primeiros itens

Primeira meta de conteúdo:

```text
4 Ancestralidades
8 Hindrances
7 Edges
7 entradas de Teleritha
1 regra de Sincrisólise
```

Esse é o primeiro pacote mecânico.

---

## Etapa 5 — Testar criação de personagem

Teste prático:

```text
Criar personagem Orunai
Criar personagem Krohminita
Criar personagem Kitano
Criar personagem Humano
Verificar se Edges e Hindrances fazem sentido
Verificar se grants/concessões funcionam ou precisam ser manuais
```

Aqui descobriremos se vale automatizar concessões ou deixar instrução manual.

---

## Etapa 6 — Criar material de campanha inicial

Depois da mecânica base:

```text
Rust Hollow
Companhia
Bondaks
Tal’Bondaks
Floyd
Dentinho
SWIX
Facções do primeiro arco
```

---

## Etapa 7 — Criar tabelas

Só depois do núcleo de campanha.

Tabelas devem servir a cenas reais:

```text
quando alguém testa Sincrisólise;
quando um Tal’Bondak reage;
quando uma prospecção dá errado;
quando uma facção percebe o SWIX.
```

---

# 8. Critério de pronto da v0.1

A versão v0.1 estará pronta quando:

```text
1. O módulo aparece e ativa no Foundry v13.
2. Os compêndios aparecem organizados.
3. As quatro ancestralidades iniciais existem.
4. Os Hindrances centrais existem.
5. Os Edges centrais existem.
6. A regra textual de Teleritha existe.
7. A regra textual de Sincrisólise existe.
8. Rust Hollow possui journal inicial.
9. O fragmento SWIX possui journal ou item inicial.
10. Ao menos uma tabela de Sobrecarga existe.
```

Critério extra, mas recomendado:

```text
11. Um personagem Orunai pode ser criado usando apenas material do módulo.
12. Um personagem Krohminita pode ser criado usando apenas material do módulo.
13. Um personagem ligado a Rust Hollow pode ser criado usando apenas material do módulo.
```

---

# 9. O que eu recomendo não fazer ainda

## Não criar macros agora

Ainda não.

Motivo: se a regra de Sincrisólise mudar, a macro quebra ou fica errada.

## Não criar Active Effects complexos agora

Ainda não.

Motivo: primeiro precisamos saber quais efeitos serão fixos e quais serão interpretativos.

## Não importar centenas de journals

Ainda não.

Motivo: muito conteúdo sem uso imediato atrapalha mais do que ajuda.

## Não modificar o sistema SWADE

Definitivamente não agora.

Motivo: é arriscado, difícil de manter e provavelmente desnecessário.

---

# 10. Documento de controle da v0.1

Sugiro manter um documento chamado:

```text
OLF — Controle do Módulo v0.1
```

Com esta estrutura:

```markdown
# OLF — Controle do Módulo v0.1

## Status geral

- Foundry-alvo: v13
- Sistema: SWADE
- Versão do módulo: 0.1.0
- Estado: em construção

## Compêndios

| Compêndio | Criado? | Testado? | Observações |
|---|---:|---:|---|
| OLF — Ancestralidades | Não | Não | |
| OLF — Edges | Não | Não | |
| OLF — Hindrances | Não | Não | |
| OLF — Teleritha e Powers | Não | Não | |
| OLF — Journals do Cenário | Não | Não | |
| OLF — Facções | Não | Não | |
| OLF — NPCs e Criaturas | Não | Não | |
| OLF — Tabelas | Não | Não | |
| OLF — Macros | Não | Não | |

## Conteúdo mínimo

| Documento | Tipo | Criado? | Testado? | Observações |
|---|---|---:|---:|---|
| Humano | Ancestry | Não | Não | |
| Krohminita | Ancestry | Não | Não | |
| Orunai | Ancestry | Não | Não | |
| Kitano | Ancestry | Não | Não | |
| Iniciado em Sincrisólise | Edge | Não | Não | |
| Ressonância Instável | Hindrance | Não | Não | |
| Sobrecarga de Teleritha | RollTable | Não | Não | |
| Rust Hollow | Journal | Não | Não | |
| Fragmento SWIX | Journal/Item | Não | Não | |

## Testes obrigatórios

- [ ] Módulo aparece no Foundry.
- [ ] Módulo ativa sem erro.
- [ ] Compêndios aparecem.
- [ ] Ancestralidade pode ser arrastada para ficha.
- [ ] Edge pode ser arrastado para ficha.
- [ ] Hindrance pode ser arrastado para ficha.
- [ ] RollTable pode ser rolada.
- [ ] Journal abre corretamente.
```

Esse documento é simples, mas é o que impede o projeto de virar neblina.

---

# 11. Próximo passo real

Agora podemos seguir para a primeira execução prática:

[Task] : IMPLEMENTAÇÃO : manifesto inicial : módulo Foundry/SWADE : Outsiders — Lost Frontier

O próximo produto deve ser o **rascunho do `module.json`**, em versão explicada linha por linha, para você entender o que cada parte faz.

Eu vou escrever de um jeito em que você não precise entender JSON de antemão: primeiro mostro a versão final, depois explico cada bloco em português claro.