# Arquitetura de Transposição de Módulo de Aventura para FQL

## Procedimento-padrão para _Outsiders — Lost Frontier_

---

## 1. Objetivo do Documento

Este documento estabelece o método-padrão para transpor um módulo de aventura de **Outsiders — Lost Frontier** para o módulo **Forien’s Quest Log** no Foundry VTT.

O objetivo não é transformar o FQL em mero “diário de missões”, mas em um **painel de gerenciamento narrativo, mecânico e metajogável** para o Mestre.

O FQL deve servir para:

1. organizar o módulo como estrutura de jogo;
    
2. acompanhar objetivos, decisões, falhas e recompensas;
    
3. facilitar a condução em mesa por meio de links para Journals e Handouts;
    
4. registrar o progresso real dos jogadores;
    
5. gerar fechamento de sessão;
    
6. gerar fechamento de módulo;
    
7. preservar pontas soltas para continuidade da campanha.
    

---

## 2. Scripts Oficiais do Fluxo FQL

A arquitetura utiliza três scripts principais.

| Script                 | Nome oficial                 | Função                                                                              |
| ---------------------- | ---------------------------- | ----------------------------------------------------------------------------------- |
| Script de transposição | `OLF FQL - TAM`              | Cria ou atualiza a arquitetura inicial de quests de um módulo.                      |
| Script de fechamento   | `OLF FQL Closeout Assistant` | Auxilia o Mestre a registrar progresso, recompensas, consequências e pontas soltas. |
| Script de continuidade | `OLF FQL Continuity Report`  | Gera relatório consolidado para planejamento de módulos futuros.                    |

### 2.1. OLF FQL - TAM

Nome completo:

```text
OLF FQL - TAM
```

Significado:

```text
Transposition Adventure Manager
```

Função:

```text
Transpor a arquitetura de um módulo de aventura para o Forien’s Quest Log.
```

O TAM cria ou atualiza:

- Quest Principal do módulo;
    
- subquests operacionais;
    
- subquests recorrentes por fase;
    
- estrutura de Pontas Soltas;
    
- objetivos;
    
- recompensas;
    
- notas do mestre;
    
- notas dos jogadores iniciais;
    
- correlações entre Objectives e Rewards;
    
- links para Journals;
    
- links para Handouts;
    
- flags auxiliares para uso futuro pelos demais scripts.
    

---

### 2.2. OLF FQL Closeout Assistant

Função:

```text
Auxiliar o Mestre no encerramento de sessões, subquests e módulos.
```

O Closeout Assistant não deve decidir sozinho o que aconteceu. Ele deve:

1. ler o estado atual das quests;
    
2. perguntar ao Mestre se Objectives e Rewards já foram atualizados;
    
3. gerar proposta de texto para Player Notes;
    
4. sugerir pontas soltas a partir de objetivos falhos, ignorados ou não concluídos;
    
5. permitir revisão humana antes de gravar;
    
6. registrar o fechamento confirmado;
    
7. detectar quando todas as subquests relevantes de um módulo foram encerradas;
    
8. oferecer fechamento consolidado da Quest Principal.
    

---

### 2.3. OLF FQL Continuity Report

Função:

```text
Gerar relatório de continuidade após o encerramento de um módulo.
```

Esse relatório deve servir como material de entrada para o planejamento do módulo seguinte.

Ele deve coletar:

- estado final da Quest Principal;
    
- Player Notes consolidadas;
    
- subquests concluídas, falhas ou pendentes;
    
- objetivos cumpridos;
    
- objetivos falhos;
    
- objetivos não concluídos;
    
- recompensas obtidas;
    
- recompensas não obtidas;
    
- pontas soltas;
    
- NPCs relevantes;
    
- facções em vantagem;
    
- facções em perda;
    
- ameaças em movimento;
    
- ganchos para o próximo módulo.
    

---

# 3. Princípio Central da Arquitetura

A transposição para o FQL deve preservar a diferença entre:

```text
Ato = unidade narrativa preparada pelo Mestre.
Quest = unidade metajogável de progresso, agência e consequência.
```

Um Ato pertence à estrutura narrativa da aventura.

Uma Quest pertence à estrutura operacional de jogo.

Portanto:

```text
Journals organizam o texto preparado.
FQL organiza o que está em disputa, o que foi feito e o que continua vivo.
```

---

# 4. Estrutura Geral de um Módulo no FQL

Todo módulo deve ser transposto com a seguinte arquitetura-base:

```text
[Nome do Módulo] [active]
├── [Subquest 1 — vetor inicial] [active]
├── [Subquest 2 — relação / objeto / agente central] [active ou inactive]
├── [Subquest 3 — conflito político / técnico / social] [active ou inactive]
├── [Subquest 4 — crise emergente] [inactive]
├── [Subquest 5 — resolução operacional] [inactive]
└── [Subquest recorrente — Fase N] [active ou inactive]

OLF — Pontas Soltas [inactive]
└── [MN — Nome do Módulo] [inactive]
```

A quantidade de subquests pode variar. O critério não é simetria, mas função.

Uma subquest deve existir quando houver:

- vetor claro de ação dos PCs;
    
- objeto de desejo;
    
- conflito de agência;
    
- NPC ou relação recorrente;
    
- disputa de custódia;
    
- frente política;
    
- risco técnico;
    
- consequência que precisa ser rastreada;
    
- linha de continuidade para módulos futuros.
    

---

# 5. Quest Principal do Módulo

A Quest Principal representa o módulo como capítulo da campanha.

Ela não deve ser usada para microcontrole.

## 5.1. Função

A Quest Principal deve registrar:

- premissa macro do módulo;
    
- objetivos gerais;
    
- recompensas gerais;
    
- política de avanço;
    
- relação entre subquests;
    
- instruções de fechamento;
    
- estado consolidado ao fim do módulo.
    

## 5.2. Status inicial

Normalmente:

```text
active
```

## 5.3. Objectives da Quest Principal

Devem ser poucos e amplos.

Modelo:

```text
☐ Identificar o problema central do módulo.
☐ Impedir que a situação saia completamente do controle dos PCs.
☐ Transformar informação em direção prática.
☐ Resolver quem conduz a próxima etapa.
☐ Encerrar o módulo com consequência clara para o próximo.
```

## 5.4. Rewards da Quest Principal

Devem representar recompensas consolidadas, não microbenefícios.

Exemplos genéricos:

```text
Elegibilidade para Advance do módulo.
Direção para o próximo módulo.
Contato estratégico consolidado.
Recurso operacional obtido.
Reputação local alterada.
Expedição / missão / operação preparada.
```

## 5.5. GM Notes da Quest Principal

Devem conter:

1. função da Quest Principal;
    
2. arquitetura do módulo;
    
3. lista de subquests;
    
4. política de avanço;
    
5. instruções sobre Pontas Soltas;
    
6. critério de fechamento do módulo.
    

Modelo:

```html
<h2>Função desta Quest Principal</h2>
<p>Esta quest registra o módulo como capítulo da campanha. Ela não deve ser usada para microcontrole de sessão.</p>

<h2>Arquitetura do Módulo</h2>
<ul>
  <li><strong>[Subquest 1]:</strong> função.</li>
  <li><strong>[Subquest 2]:</strong> função.</li>
  <li><strong>[Subquest recorrente — Fase N]:</strong> função e continuidade.</li>
</ul>

<h2>Política de Avanço</h2>
<p>Ao completar aproximadamente <strong>4 objetivos significativos</strong>, os personagens ficam elegíveis a <strong>1 Advance</strong>, sempre sujeito à confirmação do Mestre.</p>

<ul>
  <li>Não conceder mais de 1 Advance por sessão.</li>
  <li>Evitar mais de 1 Advance por módulo, salvo decisão consciente do Mestre.</li>
  <li>Objetivos excedentes podem gerar recompensas narrativas, contatos, recursos ou vantagens futuras.</li>
</ul>

<h2>Pontas Soltas</h2>
<p>Ao encerrar subquests, registre pendências em <strong>OLF — Pontas Soltas</strong>, no registro correspondente ao módulo.</p>

<h2>Fechamento do Módulo</h2>
<p>Quando todas as subquests relevantes estiverem <strong>completed</strong> ou <strong>failed</strong>, rode o Closeout Assistant para gerar síntese final.</p>
```

---

# 6. Subquests

As subquests representam vetores de agência, não necessariamente divisões de Ato.

## 6.1. Tipos de Subquest

|Tipo|Função|
|---|---|
|Vetor inicial|Introduz o problema central.|
|Relação viva|Acompanha NPC, criatura, aliado ou vínculo recorrente.|
|Objeto de desejo|Acompanha artefato, dado, tecnologia, pista ou recurso.|
|Crise emergente|Ativa virada dramática específica.|
|Disputa política|Mede controle, influência, legitimidade e soberania.|
|Preparação operacional|Organiza recursos para a próxima etapa.|
|Fase recorrente|Representa parte de uma linha de campanha que retorna em módulos futuros.|

## 6.2. Status inicial das Subquests

Subquests podem começar como:

```text
active
```

quando já estão vivas na ficção desde o começo do módulo.

Ou:

```text
inactive
```

quando dependem de gatilho narrativo posterior.

O status `inactive` não impede que a subquest esteja vinculada à Quest Principal. Ela pode ser ativada manualmente quando a ficção justificar.

## 6.3. Regra de ativação

Uma subquest deve ser ativada quando:

- os PCs entram em contato com o conflito;
    
- o objeto de desejo se torna jogável;
    
- o NPC ou facção passa a agir diretamente;
    
- uma consequência anterior abre nova frente;
    
- o Mestre decide que aquela linha agora precisa ser rastreada.
    

---

# 7. Subquests Recorrentes por Fase

Algumas linhas narrativas não se encerram em um módulo. Elas retornam em fases sucessivas.

Nesse caso, não se recomenda criar uma Quest Principal paralela, salvo necessidade excepcional. O método preferencial é:

```text
Módulo N
└── [Linha Recorrente] — Fase N: [Nome da Fase]
```

Exemplo genérico:

```text
[Nome do Módulo 1]
└── Disputa Política — Fase I: Controle Inicial

[Nome do Módulo 2]
└── Disputa Política — Fase II: Corrida por Recursos

[Nome do Módulo 3]
└── Disputa Política — Fase III: Soberania Final
```

A fase pode ser concluída ao fim do módulo sem encerrar a linha de campanha.

## 7.1. Regra de fechamento

Ao final do módulo:

```text
Concluir a fase.
Não concluir a linha de campanha.
Registrar a continuidade em Pontas Soltas.
```

---

# 8. Objectives

Objectives devem ser concretos o suficiente para orientar decisões, mas não tão estreitos que engessem a narrativa.

## 8.1. Três formas de resultado

Cada Objective pode produzir consequência por:

```text
ação;
falha;
inação.
```

Interpretação:

|Estado|Significado|
|---|---|
|Completed|Os PCs interferiram e produziram efeito relevante.|
|Failed|Os PCs tentaram e falharam, ou uma força adversária ganhou vantagem.|
|Unchecked|Os PCs ignoraram, não perceberam ou deixaram outro agente decidir.|

Essa interpretação deve ser explicitada nas GM Notes quando a subquest for política, investigativa ou de longo prazo.

## 8.2. Formulação recomendada

Prefira:

```text
Decidir ajudar [NPC ou grupo].
Proteger [objeto / pessoa / informação].
Descobrir [pista relevante].
Impedir que [facção] obtenha vantagem decisiva.
Definir quem controla [recurso].
Garantir [recurso operacional].
Registrar consequência de [evento].
```

Evite:

```text
Derrotar vilão X.
Seguir para cena Y.
Ler texto Z.
Fazer a coisa certa.
```

---

# 9. Rewards

Rewards devem registrar mudanças reais de posição na ficção ou no metajogo.

## 9.1. Tipos de Rewards

|Tipo|Exemplo|
|---|---|
|Aliado|`Aliado: [NPC]`|
|Contato|`Contato: [NPC / facção]`|
|Acesso|`Acesso: [local / instalação / rede]`|
|Pista|`Pista: [informação descoberta]`|
|Ferramenta|`Ferramenta: [objeto funcional]`|
|Recurso|`Recurso: [transporte / mantimento / equipamento]`|
|Reputação|`Reputação: [grupo reconhece os PCs como X]`|
|Dívida|`Dívida: [facção/NPC deve ou cobra algo]`|
|Risco|`Risco: [consequência negativa rastreável]`|
|Outcome|`Outcome: [estado político/narrativo]`|
|Advance|`Elegibilidade para Advance — [Quest/Subquest]`|

## 9.2. Rewards como Outcomes

Nem toda Reward é positiva.

Em subquests políticas, uma Reward pode registrar resultado de posição:

```text
Outcome: vantagem provisória da Companhia.
Outcome: Rust Hollow fraturada.
Risco: disputa jurídica futura.
Risco: observador obrigatório de facção.
```

Isso é válido porque o FQL está sendo usado como painel de estado narrativo, não apenas como sistema de prêmio.

---

# 10. Correlação Objectives → Rewards

Sempre que possível, cada subquest deve conter em GM Notes uma seção:

```html
<h2>Correlação Objectives → Rewards</h2>
```

Função:

```text
Orientar o Mestre sobre quais recompensas são sugeridas quando determinados objetivos forem cumpridos, falharem ou gerarem consequência.
```

O FQL não deve conceder automaticamente essas Rewards. O Mestre confirma conforme a ficção.

## Modelo

```html
<h2>Correlação Objectives → Rewards</h2>

<p>Use esta tabela como orientação de julgamento. O FQL não concede rewards automaticamente: o Mestre confirma quando a consequência ocorreu em ficção.</p>

<table>
  <thead>
    <tr>
      <th>Objective</th>
      <th>Rewards sugeridos</th>
      <th>Critério</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Decidir ajudar [NPC].</td>
      <td>
        <ul>
          <li>Aliado: [NPC].</li>
        </ul>
      </td>
      <td>Conceda quando os PCs assumirem responsabilidade real pelo NPC.</td>
    </tr>
  </tbody>
</table>
```

## Flag técnica recomendada

O TAM pode salvar essa correlação também como flag:

```js
flags["outsiders-lost-frontier"].fqlRewardMap
```

Estrutura sugerida:

```js
[
  {
    objective: "Decidir ajudar [NPC].",
    rewards: ["Aliado: [NPC]."],
    note: "Conceda quando houver compromisso real em ficção."
  }
]
```

Essa flag deve ser usada futuramente pelo Closeout Assistant.

---

# 11. Handouts no FQL

O FQL deve funcionar como painel de condução. Por isso, as GM Notes de cada subquest devem conter uma seção final chamada:

```html
<h2>Handouts</h2>
```

Essa seção deve ficar depois de:

```html
<h2>Não Esquecer</h2>
```

ou, quando houver:

```html
<h2>Correlação Objectives → Rewards</h2>
```

## 11.1. Função

A seção `Handouts` deve listar os handouts em ordem aproximada de apresentação.

Ela deve conter:

- cena ou momento;
    
- link UUID do JournalEntryPage;
    
- função do handout;
    
- indicação de quando mostrar.
    

## 11.2. Modelo

```html
<h2>Handouts</h2>

<p>Use estes handouts em ordem aproximada de apresentação. Mostre apenas quando a cena ou a descoberta justificar.</p>

<ol>
  <li><strong>Abertura / Cena Inicial:</strong> @UUID[...]{Handout 01} — apresentar o local como espaço vivo.</li>
  <li><strong>Primeiro contato com NPC:</strong> @UUID[...]{Handout 02} — reforçar vínculo ou conflito.</li>
  <li><strong>Descoberta técnica:</strong> @UUID[...]{Handout 03} — mostrar somente após teste, cena ou revelação.</li>
</ol>
```

## 11.3. Diretriz

Não incluir todos os handouts existentes. Incluir apenas os úteis para aquela subquest.

O Mestre deve poder abrir a subquest e conduzir a cena sem buscar em outra aba.

---

# 12. Pontas Soltas

`OLF — Pontas Soltas` é uma Quest contínua, normalmente inativa, usada como repositório persistente de continuidade.

Ela não representa uma missão ativa para os jogadores.

## 12.1. Arquitetura

```text
OLF — Pontas Soltas [inactive]
├── M01 — [Nome do Módulo 1] [inactive]
├── M02 — [Nome do Módulo 2] [inactive]
└── M03 — [Nome do Módulo 3] [inactive]
```

## 12.2. Função

Registrar:

- ameaças em movimento;
    
- dívidas;
    
- promessas;
    
- NPCs recorrentes;
    
- facções em vantagem;
    
- pistas pendentes;
    
- consequências futuras;
    
- objetivos falhos;
    
- objetivos ignorados;
    
- recompensas não obtidas;
    
- riscos que devem retornar.
    

## 12.3. Player Notes padrão

```html
<h2>Pontas Soltas — [Código do Módulo] — [Nome do Módulo]</h2>

<h3>Ameaças em Movimento</h3>
<ul>
  <li><em>Nenhuma registrada ainda.</em></li>
</ul>

<h3>Dívidas e Promessas</h3>
<ul>
  <li><em>Nenhuma registrada ainda.</em></li>
</ul>

<h3>Pistas Pendentes</h3>
<ul>
  <li><em>Nenhuma registrada ainda.</em></li>
</ul>

<h3>NPCs Recorrentes</h3>
<ul>
  <li><em>Nenhum registrado ainda.</em></li>
</ul>

<h3>Facções com Interesse Ativo</h3>
<ul>
  <li><em>Nenhuma registrada ainda.</em></li>
</ul>

<h3>Consequências Futuras</h3>
<ul>
  <li><em>Nenhuma registrada ainda.</em></li>
</ul>
```

---

# 13. OLF FQL - TAM

## 13.1. Função técnica

O TAM deve:

1. verificar se o usuário é GM;
    
2. verificar se Forien’s Quest Log está ativo;
    
3. localizar ou criar a pasta interna `_fql_quests`;
    
4. criar ou atualizar a Quest Principal;
    
5. criar ou atualizar subquests;
    
6. vincular subquests à Quest Principal;
    
7. criar ou atualizar `OLF — Pontas Soltas`;
    
8. criar ou atualizar a subquest de Pontas Soltas do módulo;
    
9. inserir Objectives;
    
10. inserir Rewards;
    
11. inserir GM Notes;
    
12. inserir Player Notes iniciais;
    
13. inserir flags auxiliares;
    
14. opcionalmente definir a Quest Principal como `primaryQuest`.
    

## 13.2. Estrutura recomendada do script

O script deve ser escrito em inglês.

O conteúdo da aventura pode ficar em português.

Estrutura-base:

```js
(async () => {
  const MODULE_ID = "forien-quest-log";
  const FLAG_KEY = "json";
  const OLF_FLAG_ID = "outsiders-lost-frontier";
  const FQL_FOLDER_NAME = "_fql_quests";

  if (!game.user.isGM) {
    ui.notifications.error("This macro must be executed by a GM.");
    throw new Error("GM user required.");
  }

  if (!game.modules.get(MODULE_ID)?.active) {
    ui.notifications.error("Forien's Quest Log is not active.");
    throw new Error("Forien's Quest Log is not active.");
  }

  // Helper functions:
  // - getQuestData
  // - findQuestByName
  // - createQuestWithFallback
  // - ensureParentChildLink
  // - buildTasks
  // - buildRewards
  // - renderCorrelationTable
  // - renderHandoutList

  // Module architecture:
  const quests = [
    {
      key: "module",
      parentKey: null,
      name: "[Nome do Módulo]",
      status: "active",
      description: "...",
      gmnotes: "...",
      playernotes: "...",
      tasks: [],
      rewards: []
    }
  ];

  // Creation/update loop.
})();
```

## 13.3. Regra de segurança

O TAM deve evitar duplicar quests.

Antes de criar uma quest, deve buscar por nome:

```js
findQuestByName(name)
```

Se existir, deve atualizar ou reaproveitar.

## 13.4. Conteúdo em português, código em inglês

Regra obrigatória:

```text
Código, funções e variáveis em inglês.
Conteúdo de aventura em português.
```

Isso reduz erro de sintaxe e mantém legibilidade técnica.

---

# 14. OLF FQL Closeout Assistant

## 14.1. Função

O Closeout Assistant auxilia o Mestre a encerrar sessão, subquest ou módulo.

Ele não decide sozinho.

Ele pergunta, propõe e grava somente após confirmação.

## 14.2. Fluxo recomendado

```text
1. Selecionar Quest Principal ativa.
2. Listar subquests vinculadas.
3. Identificar subquests em progresso.
4. Perguntar ao Mestre:
   “Todos os objetivos e recompensas desta sessão já foram atualizados?”
5. Se não:
   cancelar operação.
6. Se sim:
   ler Objectives, Rewards, Player Notes e GM Notes.
7. Gerar proposta de Player Notes.
8. Sugerir Pontas Soltas.
9. Abrir preview editável.
10. Gravar após confirmação.
11. Verificar se todas as subquests relevantes foram concluídas ou falharam.
12. Se sim:
   oferecer fechamento consolidado da Quest Principal.
```

## 14.3. Pergunta prévia obrigatória

```text
Todos os objetivos realizados nesta sessão já foram marcados na Quest?
Todas as recompensas recebidas nesta sessão já foram registradas na Quest?
```

Opções:

```text
Sim, continuar.
Não, cancelar para atualizar.
```

Se o Mestre escolher “não”, o script deve parar.

## 14.4. Player Notes de sessão

Modelo:

```html
<hr>
<h2>Fechamento de Sessão — [data]</h2>

<h3>Objetivos Concluídos</h3>
<ul>
  <li>...</li>
</ul>

<h3>Objetivos Falhos ou Perdidos</h3>
<ul>
  <li>...</li>
</ul>

<h3>Recompensas Obtidas</h3>
<ul>
  <li>...</li>
</ul>

<h3>Consequência Narrativa</h3>
<p>...</p>

<h3>Pendências</h3>
<ul>
  <li>...</li>
</ul>
```

## 14.5. Sugestão de Pontas Soltas

O Closeout Assistant deve sugerir pontas soltas a partir de:

- Objectives failed;
    
- Objectives unchecked em subquest encerrada;
    
- Rewards não obtidas;
    
- Outcomes negativos;
    
- riscos registrados;
    
- texto de Player Notes;
    
- comentário adicional do Mestre.
    

Modelo de prompt interno:

```text
Foram detectados os seguintes possíveis itens de continuidade:
- [Objetivo falho]
- [Objetivo não concluído]
- [Reward não obtida]
- [Risco registrado]

Deseja registrar algum desses itens em Pontas Soltas?
```

O Mestre deve poder:

- selecionar itens sugeridos;
    
- editar texto;
    
- adicionar itens próprios;
    
- cancelar.
    

---

# 15. Fechamento da Quest Principal

O fechamento da Quest Principal só ocorre quando:

```text
todas as subquests relevantes estiverem completed ou failed;
```

ou quando o Mestre confirmar manualmente que o módulo terminou.

## 15.1. Estrutura do fechamento consolidado

```html
<hr>
<h2>Fechamento do Módulo — [Nome do Módulo]</h2>

<h3>Resumo do Módulo</h3>
<p>...</p>

<h3>Objetivos Principais Alcançados</h3>
<ul>
  <li>...</li>
</ul>

<h3>Recompensas Consolidadas</h3>
<ul>
  <li>...</li>
</ul>

<h3>Estado Final dos Elementos Centrais</h3>
<ul>
  <li><strong>[Elemento 1]:</strong> ...</li>
  <li><strong>[Elemento 2]:</strong> ...</li>
</ul>

<h3>Pontas Soltas para Continuidade</h3>
<ul>
  <li>...</li>
</ul>
```

---

# 16. OLF FQL Continuity Report

## 16.1. Função

Gerar um relatório copiável em Markdown para planejamento futuro.

Esse script não altera quests.

Ele apenas lê e apresenta.

## 16.2. Entrada

O Mestre seleciona:

```text
Quest Principal encerrada ou em fechamento.
```

O script também lê:

```text
OLF — Pontas Soltas
└── [registro do módulo]
```

## 16.3. Saída esperada

```markdown
# Relatório de Continuidade — [Nome do Módulo]

## Estado Final do Módulo

...

## Subquests

| Subquest | Status | Objetivos Concluídos | Falhos | Pendentes |
|---|---:|---:|---:|---:|

## Recompensas Obtidas

...

## Outcomes Políticos ou Narrativos

...

## Pontas Soltas

### Ameaças em Movimento

...

### Dívidas e Promessas

...

### Pistas Pendentes

...

### NPCs Recorrentes

...

### Facções com Interesse Ativo

...

### Consequências Futuras

...

## Recomendações para o Próximo Módulo

...
```

## 16.4. Uso no planejamento

O relatório deve ser trazido para a IA como base para construir o módulo seguinte.

A IA deve então:

1. ler o estado final;
    
2. identificar pendências relevantes;
    
3. propor quais retornam como subquests;
    
4. propor quais viram ameaças de fundo;
    
5. propor quais devem ser resolvidas, agravadas ou transformadas;
    
6. estruturar o próximo módulo com continuidade real da mesa.
    

---

# 17. Checklist de Transposição de um Novo Módulo

Antes de escrever o TAM de um módulo, a IA deve produzir este checklist.

## 17.1. Leitura estrutural

```text
☐ Ler o módulo completo.
☐ Identificar premissa.
☐ Identificar conflito central.
☐ Identificar objetos de desejo.
☐ Identificar NPCs centrais.
☐ Identificar facções.
☐ Identificar riscos.
☐ Identificar possíveis estados finais.
```

## 17.2. Mapeamento FQL

```text
☐ Definir Quest Principal.
☐ Definir subquests ativas desde o início.
☐ Definir subquests inativas por gatilho.
☐ Definir subquests recorrentes por fase.
☐ Definir Pontas Soltas do módulo.
☐ Definir Objectives por subquest.
☐ Definir Rewards por subquest.
☐ Definir Outcomes quando necessário.
```

## 17.3. GM Notes

```text
☐ Inserir função da quest.
☐ Inserir fluxo sugerido.
☐ Inserir links para Journals.
☐ Inserir sequência recomendada.
☐ Inserir seção Não Esquecer.
☐ Inserir Correlação Objectives → Rewards.
☐ Inserir Handouts.
```

## 17.4. Handouts

```text
☐ Listar handouts existentes.
☐ Identificar handouts faltantes.
☐ Associar cada handout a cena/subquest.
☐ Gerar UUIDs corretos.
☐ Inserir seção Handouts nas GM Notes.
```

## 17.5. Teste no Foundry

```text
☐ Rodar TAM.
☐ Conferir Active Quests.
☐ Conferir Inactive Quests.
☐ Abrir Quest Principal.
☐ Conferir GM Notes.
☐ Conferir Player Notes.
☐ Conferir Objectives.
☐ Conferir Rewards.
☐ Conferir links de Journals.
☐ Conferir links de Handouts.
☐ Corrigir com patch, se necessário.
```

---

# 18. Regra de Ouro

O FQL não substitui o Mestre.

Ele organiza a memória da mesa.

A arquitetura deve sempre preservar:

```text
decisão humana;
rastreabilidade;
consequência;
continuidade;
clareza operacional.
```

O FQL deve responder, a cada módulo:

```text
O que estava em disputa?
O que os PCs fizeram?
O que os PCs falharam em fazer?
O que os PCs ignoraram?
Quem ganhou com isso?
Quem perdeu com isso?
O que mudou na ficção?
O que deve retornar depois?
```

Essa é a função do método.

---

# 19. Nomenclatura-padrão

|Elemento|Nome|
|---|---|
|Script de transposição|`OLF FQL - TAM`|
|Script de fechamento|`OLF FQL Closeout Assistant`|
|Script de relatório|`OLF FQL Continuity Report`|
|Quest de continuidade|`OLF — Pontas Soltas`|
|Subquest de pontas por módulo|`[Código] — [Nome do Módulo]`|
|Seção de recompensas|`Correlação Objectives → Rewards`|
|Seção de handouts|`Handouts`|
|Status inicial do módulo|`active`|
|Status de subquest futura|`inactive`|
|Status de fase encerrada|`completed` ou `failed`|

---

# 20. Forma final do método

```text
1. A aventura é escrita nos Journals.
2. O módulo é transposto para FQL pelo TAM.
3. O FQL vira painel de condução.
4. O Mestre conduz cenas usando Journals, Objectives, Rewards e Handouts.
5. Ao fim da sessão, o Closeout Assistant registra progresso.
6. Ao fim da subquest, o Closeout Assistant registra consequências.
7. Ao fim do módulo, o Closeout Assistant consolida a Quest Principal.
8. As pendências são registradas em OLF — Pontas Soltas.
9. O Continuity Report gera relatório final.
10. O relatório alimenta o planejamento do próximo módulo.
```

Esse é o procedimento-padrão para qualquer transposição futura de módulo de aventura de **Outsiders — Lost Frontier** para o **Forien’s Quest Log**.