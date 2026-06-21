# Handoff - Claude Skills, GitHub e replicacao para Veracrucia

Este handoff registra o processo usado no projeto **OutsiderS - Lost Frontier** para criar um repositorio Git/GitHub, conectar o projeto ao Claude e transpor skills do Codex para uma estrutura que o Claude consiga usar. O objetivo e repetir o mesmo procedimento no projeto **Veracrucia**.

## 1. Resultado alcancado no Lost Frontier

Repositorio matriz:

```text
WildPoxx/lost-frontier
```

Repositorio tecnico associado:

```text
WildPoxx/masterquest-fvtt-dev
```

Commits principais do processo:

```text
266375e Document GitHub and deploy strategy
c64530d Add curated Lost Frontier markdown corpus
2dcd509 Add Claude project skills for Lost Frontier
67a50f6 Add visible Claude project instructions
7b2ae5f Document Claude skill coverage
7d5b149 Rename FQL quest ops skill to MasterQuest
```

Arquivos criados para orientar Claude:

```text
CLAUDE.md
AI_COLLABORATION.md
docs/ai/CLAUDE_SKILLS_INDEX.md
docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md
.claude/skills/lost-frontier-foundry-dev/SKILL.md
.claude/skills/masterquest-quest-ops/SKILL.md
.claude/skills/swade-fvtt-mechanics-model/SKILL.md
```

## 2. Problema resolvido

O Codex usa skills locais em `C:\Users\amari\.codex\skills`. Claude Code tambem entende uma estrutura de skills, mas em outro lugar:

```text
.claude/skills/<nome-da-skill>/SKILL.md
```

O Claude Project Knowledge pode nao expor pastas ocultas como `.claude/`. Por isso, a solucao final usa duas camadas:

1. **Skills executaveis para Claude Code**

```text
.claude/skills/<nome-da-skill>/SKILL.md
```

2. **Espelho visivel para Claude Project Knowledge**

```text
CLAUDE.md
docs/ai/CLAUDE_SKILLS_INDEX.md
docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md
```

Assim, se Claude ve `.claude/skills`, ele usa as skills diretamente. Se nao ve, ele usa o indice em `docs/ai/`.

## 3. Metodo usado para transpor skills

1. Inventariar as skills do Codex.
2. Separar skills pessoais de Mario das skills especificas do projeto.
3. Converter apenas as skills realmente necessarias para o projeto.
4. Remover referencias especificas a ferramentas internas do Codex.
5. Preservar:
   - papel da IA no projeto;
   - gatilhos de uso;
   - ordem de leitura;
   - guardrails;
   - criterios de validacao;
   - relacao com documentos de referencia.
6. Criar uma pasta por skill em `.claude/skills/`.
7. Criar `CLAUDE.md` como ponto de entrada.
8. Criar `docs/ai/CLAUDE_SKILLS_INDEX.md` como espelho nao oculto.
9. Criar `docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md` quando houver mais de um repositorio ou fontes externas.
10. Testar no Claude com prompt de leitura dirigida.

## 4. Estrutura recomendada para Veracrucia

Nome sugerido do repositorio:

```text
WildPoxx/veracrucia
```

Visibilidade recomendada:

```text
private
```

Motivo: Veracrucia e um projeto autoral/literario em andamento. O repositorio pode conter rascunhos, notas de continuidade, mapas de personagem, referencias de leitura, arquivos editoriais e material ainda nao publicado.

Estrutura minima recomendada:

```text
README.md
AI_COLLABORATION.md
CLAUDE.md
.gitignore
.gitattributes
docs/ai/CLAUDE_SKILLS_INDEX.md
docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md
.claude/skills/
```

## 5. Skills recomendadas para Veracrucia

Nao copiar todas as skills do Codex. Comecar com um conjunto pequeno e autoral.

Skills de projeto recomendadas:

```text
veracrucia-authorial-style
veracrucia-scene-planner
veracrucia-editorial-diagnostics
veracrucia-reference-decoupage
```

Possiveis fontes Codex para conversao:

```text
C:\Users\amari\.codex\skills\mb-authorial-style
C:\Users\amari\.codex\skills\veracrucia-scene-planner
C:\Users\amari\.codex\skills\mb-literary-critical-editor
C:\Users\amari\.codex\skills\literary-reference-decoupage
C:\Users\amari\.codex\skills\prose-engineering
C:\Users\amari\.codex\skills\rigor-academico-fontes
```

Proposta de roteamento:

- `veracrucia-authorial-style`: voz, estilo, anti-artificialidade, registro autoral, cenas e revisao de prosa.
- `veracrucia-scene-planner`: planejamento de cenas antes da escrita, perguntas de preparacao, POV, promessa/payoff, funcao dramatica.
- `veracrucia-editorial-diagnostics`: parecer critico, problemas de continuidade, superficialidade, artificio, ritmo, estrutura.
- `veracrucia-reference-decoupage`: analise de autores, tecnicas transferiveis, leitura comparativa, sem imitacao direta.

## 6. AI_COLLABORATION.md para Veracrucia

O arquivo deve deixar claro:

- Mario e o autor e diretor criativo.
- A IA nao deve inventar canon, cenas, passado de personagem ou decisao estetica sem base.
- A resposta deve ser em portugues por padrao.
- A IA deve diferenciar:
  - texto canonico;
  - rascunho;
  - nota de planejamento;
  - sugestao editorial;
  - inferencia.
- A IA deve preservar voz, ritmo, ambiguidade e tensao literaria.
- A IA deve evitar prosa generica, sentimentalismo explicativo e conclusoes moralizantes.
- Referencias literarias servem para decupagem tecnica, nao para imitacao.

## 7. CLAUDE.md para Veracrucia

O `CLAUDE.md` deve ser o ponto de entrada do Claude. Modelo:

```text
Leia README.md, AI_COLLABORATION.md e docs/ai/CLAUDE_SKILLS_INDEX.md antes de responder em nivel de projeto.

Use veracrucia-authorial-style para escrita, reescrita, voz e estilo.
Use veracrucia-scene-planner para planejar cenas antes de redigir.
Use veracrucia-editorial-diagnostics para parecer critico e diagnostico.
Use veracrucia-reference-decoupage para trabalhar com autores de referencia sem imitacao.

Responda em portugues. Preserve Mario como autor e diretor criativo. Nao invente canon. Marque incertezas.
```

## 8. Git e GitHub - fluxo recomendado

1. Definir a pasta raiz local de Veracrucia.
2. Criar `.gitignore` antes do primeiro commit.
3. Excluir do Git comum:
   - PDFs comerciais;
   - livros de terceiros;
   - backups brutos;
   - arquivos temporarios;
   - exports pesados;
   - imagens grandes;
   - documentos pessoais sensiveis;
   - chaves, tokens e `.env`.
4. Criar `README.md`.
5. Criar `AI_COLLABORATION.md`.
6. Criar `CLAUDE.md`.
7. Criar `.claude/skills/`.
8. Criar `docs/ai/CLAUDE_SKILLS_INDEX.md`.
9. Criar `docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md`.
10. Fazer commit inicial curado.
11. Criar repositorio GitHub privado.
12. Conectar o repositorio ao Claude pelo conector GitHub.
13. Testar com prompt de leitura dirigida.

Comandos conceituais:

```powershell
git init -b main
git add README.md AI_COLLABORATION.md CLAUDE.md .gitignore .gitattributes docs/ai .claude/skills
git commit -m "Initial Veracrucia project baseline"
git remote add origin https://github.com/WildPoxx/veracrucia.git
git push -u origin main
```

Tambem e possivel fazer a criacao inicial pelo GitHub Desktop, desde que o commit seja curado e nao use `git add .` sem revisao.

## 9. Prompt de teste para Claude

Depois de conectar o GitHub ao projeto Claude:

```text
Leia CLAUDE.md, README.md, AI_COLLABORATION.md e docs/ai/CLAUDE_SKILLS_INDEX.md. Depois explique quais skills do projeto Veracrucia voce encontrou, quando deve usar cada uma e quais arquivos ainda faltam no Project Knowledge.
```

Se Claude nao enxergar `.claude/skills`, testar:

```text
Leia docs/ai/CLAUDE_SKILLS_INDEX.md como espelho das skills do projeto e explique o roteamento de trabalho.
```

## 10. Checklist de validacao

O procedimento esta pronto quando:

- O repositorio GitHub existe e esta sincronizado.
- `README.md` explica o escopo do projeto.
- `AI_COLLABORATION.md` define postura, fontes de verdade e limites criativos.
- `CLAUDE.md` aponta os arquivos obrigatorios de leitura.
- `.claude/skills/` contem as skills do projeto.
- `docs/ai/CLAUDE_SKILLS_INDEX.md` espelha as skills.
- `docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md` diz quais arquivos estao no repo e quais dependem de fontes externas.
- Claude consegue listar as skills e explicar quando usar cada uma.
- Codex e Claude passam a usar a mesma arquitetura de trabalho.

## 11. Riscos especificos de Veracrucia

- Publicar sem querer texto literario inedito em repositorio publico.
- Misturar rascunho canonico com sugestao editorial.
- Fazer Claude ou Codex "normalizar" demais a prosa.
- Perder ambiguidade, subtexto ou brutalidade formal por excesso de explicacao.
- Usar autores de referencia como imitacao, em vez de decupagem tecnica.
- Adicionar material de terceiros ao Git comum.
- Criar skills demais antes de testar as quatro essenciais.

## 12. Proximo passo recomendado

Quando Mario indicar a pasta raiz de Veracrucia, repetir o processo em modo economico:

1. Criar Git local e `.gitignore`.
2. Criar README, AI_COLLABORATION e CLAUDE.md.
3. Converter quatro skills essenciais.
4. Criar espelho em `docs/ai/`.
5. Fazer commit inicial.
6. Criar repo GitHub privado.
7. Conectar ao Claude e testar.

Depois do teste, expandir apenas se houver necessidade real.
