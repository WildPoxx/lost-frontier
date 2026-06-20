

# 1. Objetivo do módulo

O módulo deve ser um pacote instalável no Foundry VTT v13 que acrescenta ao sistema SWADE os elementos próprios de **Outsiders — Lost Frontier**, sem alterar diretamente o sistema SWADE.

Em termos simples:

> O SWADE continua sendo o motor.  
> O módulo de Outsiders adiciona o cenário, as regras específicas e as ferramentas da campanha.

# 2. Princípio de organização

O módulo deve ter três camadas.

## Camada 1 — Conteúdo de jogo

Aquilo que aparece para jogadores e mestre como itens, regras e opções.

Entra aqui:

- Ancestralidades;
    
- Edges;
    
- Hindrances;
    
- Powers;
    
- Trappings de Teleritha;
    
- equipamentos;
    
- armas;
    
- armaduras;
    
- criaturas;
    
- NPCs;
    
- facções;
    
- tabelas;
    
- handouts;
    
- journal entries.
    

Essa é a camada mais importante para começar.

## Camada 2 — Automação leve

Aquilo que ajuda a mesa sem tentar substituir o mestre.

Entra aqui:

- macros simples;
    
- rolagens padronizadas;
    
- mensagens no chat;
    
- aplicação de efeitos temporários;
    
- botões de apoio;
    
- tabelas de consequência.
    

Exemplo:

```text
Macro: Testar Sincrisólise
1. pergunta qual cepa será usada;
2. pede a rolagem apropriada;
3. calcula risco;
4. mostra resultado no chat;
5. sugere consequência.
```

O objetivo aqui não é fazer um videogame. É acelerar mesa.

## Camada 3 — Automação avançada

Aquilo que mexe mais fundo no Foundry.

Entra depois, não agora.

Pode incluir:

- hooks;
    
- scripts automáticos;
    
- alteração dinâmica de fichas;
    
- integração com Active Effects;
    
- criação automática de itens;
    
- controle de recursos personalizados;
    
- interfaces próprias.
    

Essa camada só deve ser criada depois que soubermos exatamente quais regras realmente precisam dela.

# 3. O que deve entrar no primeiro módulo

Eu recomendo dividir o módulo inicial em blocos.

## 3.1. Ancestralidades

Primeiro conjunto essencial.

```text
Humanos
Krohminitas
Orunai
Kitanos
Kadiff
Tarekhs
Migma
```

Mas eu sugiro começar apenas com as três ou quatro mais centrais:

```text
Humanos
Krohminitas
Orunai
Kitanos
```

Critério: entra primeiro o que os jogadores podem escolher na criação de personagem.

## 3.2. Hindrances próprios

Entram os Hindrances que expressam as condições do cenário.

Exemplos:

```text
Dependência — Teleritha
Vulnerabilidade — Vibração
Cognição Alienígena
Rigidez de Padrão
Ciclo Biológico Krohminita
Atmosfera Inadequada
Exposição ao Véu
Dívida de Companhia
Marcado por Facção
Ressonância Instável
```

Critério: só entra Hindrance que gere decisão mecânica ou narrativa recorrente.

## 3.3. Edges próprios

Aqui entram opções de progressão e identidade.

Exemplos:

```text
Sintonia com Teleritha
Condutor de Bondak
Condutor de Tal’Bondak
Interface Neural de Rastro
Iniciado em Sincrisólise
Cartógrafo do Véu
Ressonador Orunai
Cepador Aprendiz
Prospector de Rust Hollow
Veterano do Campo das Estrelas Cadentes
```

Critério: Edge precisa fazer algo em mesa. Não basta ser “legal”.

## 3.4. Powers e trappings de Teleritha

Aqui devemos ser cuidadosos.

Não precisamos reinventar todos os Powers de SWADE. Melhor usar os Powers existentes e criar **trappings** por cepa.

Exemplo:

```text
Bolt + Pyra = descarga explosiva instável
Protection + Gravis = campo de ancoragem
Boost Trait + Fluxa = condução sináptica
Speed + Veyra = vibração cinética
Teleport + Aethera = dobra transvelar
```

Critério: o módulo não deve duplicar o livro básico sem necessidade.

## 3.5. Sincrisólise

Este deve ser um subsistema próprio, mas eu não começaria pela automação pesada.

Primeira versão:

```text
Sincrisólise como Edge + regra textual + macro auxiliar.
```

Componentes:

```text
Edge: Iniciado em Sincrisólise
Hindrance opcional: Ressonância Instável
Macro: Teste de Sincrisólise
Tabela: Consequências de Sobrecarga
Journal: Regras de Sincrisólise
```

Depois evoluímos para automação.

## 3.6. Teleritha

A Teleritha precisa entrar como sistema material, não como lore solto.

Primeiro conjunto:

```text
Pyra
Gravis
Fluxa
Veyra
Aethera
Pulvis
Osmério
Occanium
```

Cada entrada deve conter:

```text
Descrição curta
Uso tecnológico
Uso mecânico
Risco
Exemplo de trapping
Facções interessadas
```

Critério: cada cepa precisa gerar decisão, custo ou conflito.

## 3.7. Rust Hollow

Como a campanha inicial parte de Rust Hollow, ela deve entrar no módulo antes de todas as demais colônias.

Entram:

```text
Journal: Rust Hollow
Journal: Companhia Bask-Callico
Journal: Programa Segunda Trilha
Journal: Bondaks
Journal: Tal’Bondaks
Journal: Floyd Merian
Journal: Dentinho
Journal: Fragmento SWIX
```

Isso se conecta diretamente ao plot inicial, no qual Floyd Merian encontra com Dentinho um fragmento SWIX ligado ao Starwalker-IX, Outpost-87 e Victor Walker .

## 3.8. Facções

Aqui eu sugiro começar só com facções que têm função no primeiro arco.

Primeiro pacote:

```text
Companhia Bask-Callico
Stargazers
Expedicionários
Guilda de Ferro
Cyberdome
LMT
Abutres de Aço
Chifres da Areia Baixa
Culto dos Deuses Mortos
```

O documento de facções já dá uma base forte: a Companhia organiza a prospecção e sustenta Rust Hollow, enquanto Guilda, Cyberdome, LMT e outras forças disputam controle, tecnologia e informação .

## 3.9. Macros iniciais

No primeiro módulo, eu colocaria poucas macros.

```text
01 — Teste de Sincrisólise
02 — Risco de Sobrecarga de Teleritha
03 — Reação de Tal’Bondak
04 — Fenômeno do Véu Rasgado
05 — Complicação de Prospecção
```

Critério: macro só entra se economizar tempo real em sessão.

# 4. O que não deve entrar agora

Essa parte é crucial.

## Não entra no primeiro módulo

```text
Alteração do código-fonte do sistema SWADE
Automação completa de todas as regras
Interface visual própria
Todos os NPCs do cenário inteiro
Todas as colônias em detalhe
Todas as facções existentes
Sistema econômico completo
Crafting completo de Teleritha
Bestiário inteiro
Mapas
Músicas
Cenas prontas demais
```

Por quê?

Porque isso transformaria o módulo em um monstro antes de ele ser jogável.

O primeiro objetivo não é fazer uma enciclopédia. É fazer uma base funcional para a mesa.

# 5. Estrutura recomendada do módulo

Em linguagem simples, a pasta do módulo deveria ficar assim:

```text
outsiders-lost-frontier/
│
├── module.json
│
├── scripts/
│   ├── macros/
│   │   ├── sincrisolise.js
│   │   ├── sobrecarga-teleritha.js
│   │   ├── reacao-talbondak.js
│   │   └── fenomeno-veu.js
│
├── packs/
│   ├── ancestries/
│   ├── edges/
│   ├── hindrances/
│   ├── powers/
│   ├── abilities/
│   ├── equipment/
│   ├── npcs/
│   ├── factions/
│   ├── journals/
│   └── tables/
│
├── lang/
│   └── pt-BR.json
│
├── styles/
│   └── outsiders.css
│
└── assets/
    ├── icons/
    ├── portraits/
    ├── tokens/
    └── maps/
```

Você não precisa saber escrever isso ainda. Essa estrutura serve como mapa.

# 6. Faseamento recomendado

## Fase 1 — Módulo mínimo jogável

Objetivo: fazer o módulo aparecer no Foundry e conter o conteúdo essencial.

Entra:

```text
module.json
compêndio de Ancestries
compêndio de Edges
compêndio de Hindrances
journal de regras básicas de Teleritha
journal de Sincrisólise
journal de Rust Hollow
```

Sem automação complexa.

## Fase 2 — Regras próprias

Objetivo: transformar o cenário em mecânica.

Entra:

```text
Powers com trappings
Edges de Teleritha
Hindrances ambientais
tabelas de risco
primeiras macros simples
```

## Fase 3 — Campanha inicial

Objetivo: preparar a aventura de Rust Hollow / SWIX / Outpost-87.

Entra:

```text
NPCs principais
facções do arco inicial
tabelas de encontros
journals de cenas
itens do McGuffin
macros de prospecção
```

## Fase 4 — Automação avançada

Objetivo: melhorar fluidez depois que a regra já foi testada em mesa.

Entra:

```text
Active Effects refinados
macros com botões
hooks
integração com ficha
automação parcial de Sincrisólise
```

# 7. Decisão metodológica inicial

Eu recomendo que o primeiro outline oficial do módulo seja este:

```text
Módulo: Outsiders — Lost Frontier
Sistema-base: SWADE
Foundry-alvo: v13
Função: adicionar conteúdo e regras específicas do cenário sem alterar o sistema-base
Escopo inicial: personagens jogáveis, Teleritha, Sincrisólise, Rust Hollow e primeiro arco
Automação inicial: baixa
Automação futura: progressiva, após teste em mesa
```

# 8. Próximo passo correto

O próximo passo não é programar.

O próximo passo é criar uma tabela de escopo:

```markdown
| Bloco | Entra no módulo? | Entra agora? | Tipo no Foundry | Observações |
|---|---:|---:|---|---|
| Orunai | Sim | Sim | Ancestry | Jogável |
| Krohminitas | Sim | Sim | Ancestry | Jogável |
| Sincrisólise | Sim | Sim | Edge + Journal + Macro | Começar simples |
| Todas as facções | Sim | Não | Journal | Só arco inicial agora |
| Bestiário completo | Sim | Não | Actor/NPC | Fase posterior |
```

Minha recomendação direta: **começamos por essa tabela de escopo**. Ela vira a constituição do módulo. Depois dela, qualquer item novo precisa justificar por que entra agora, por que entra depois ou por que fica fora.