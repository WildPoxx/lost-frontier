# Diretrizes para Infográficos de Recapitulação - Outsiders: Lost Frontier

```yaml
Título: Diretrizes para Infográficos de Recapitulação
Projeto: Outsiders - Lost Frontier
Uso: Handouts visuais de recapitulação pós-sessão
Formato preferencial: Markdown / Obsidian
Status: Procedimento consolidado
Versão: 1.0
```

---

## 1. Função do Documento

Este documento define o procedimento-padrão para criação de **Infográficos de Recapitulação** em _Outsiders: Lost Frontier_.

O infográfico de recapitulação é um handout visual destinado a resumir uma sessão, bloco de sessão ou etapa jogada da campanha, com foco em:

- registrar o que aconteceu em mesa;
    
- reforçar memória dos jogadores;
    
- organizar personagens, lugares, facções e objetos relevantes;
    
- criar material visual reaproveitável;
    
- preservar o mistério sem antecipar revelações futuras.
    

O infográfico **não é um resumo de bastidor do módulo**.  
Ele **não deve saber mais do que os jogadores sabem**.

---

## 2. Princípio Central

Todo Infográfico de Recapitulação deve ser baseado, antes de qualquer outra fonte, no **relatório de sessão fornecido pelo operador no momento da solicitação**.

```text
Fonte primária obrigatória:
Relatório de sessão informado pelo operador.
```

As demais fontes — atos da aventura, bíblia canônica, arquivos de facção, documentos de colônia, lore geral e notas de preparação — devem ser usadas apenas como:

1. controle de coerência;
    
2. filtro de spoilers;
    
3. referência visual;
    
4. checagem de nomes e termos;
    
5. apoio para evitar contradições.
    

Elas **não substituem** o relatório de sessão.

---

## 3. Regra de Ouro

```text
O infográfico registra a superfície dramática conhecida pelos jogadores.
Ele não revela a verdade oculta da aventura.
```

A imagem deve funcionar como se tivesse sido montada a partir daquilo que os personagens viram, ouviram, inferiram ou poderiam saber publicamente naquele momento da campanha.

Se uma informação aparece apenas em ato futuro, nota de mestre, plano secreto de facção ou consequência ainda não jogada, ela **não entra** no infográfico.

---

## 4. Camadas de Informação

Toda informação candidata ao infográfico deve ser classificada em uma das cinco camadas abaixo.

|Camada|Pode entrar?|Critério|
|---|--:|---|
|Informação jogada|Sim|Aconteceu explicitamente na sessão.|
|Informação dita|Sim|Foi dita por NPC, documento, rumor ou personagem.|
|Informação pública|Sim|É lore comum do cenário ou local.|
|Informação inferível|Sim, com cautela|Pode ser deduzida pelos jogadores sem revelar bastidor.|
|Informação oculta/futura|Não|Pertence a ato futuro, segredo de facção ou verdade não revelada.|

---

## 5. Fonte Primária: Relatório de Sessão

Ao solicitar um infográfico, o operador deve fornecer, preferencialmente, um relatório de sessão ou resumo estruturado.

O relatório pode ser narrativo ou esquemático. A IA deve extrair dele:

- acontecimentos principais;
    
- personagens presentes;
    
- NPCs relevantes;
    
- locais visitados;
    
- decisões dos personagens;
    
- informações descobertas;
    
- rumores ou boatos em circulação;
    
- objetos encontrados;
    
- facções percebidas;
    
- consequências visíveis;
    
- ganchos para a próxima sessão.
    

O relatório define o limite do que o infográfico pode afirmar.

---

## 6. Formato Recomendado de Entrada

```markdown
# Solicitação de Infográfico de Recapitulação

## Identificação
- Campanha:
- Módulo:
- Ato:
- Sessão:
- Título da sessão:
- Data da sessão:

## Relatório de Sessão
[Inserir relatório narrativo ou resumo dos acontecimentos.]

## Personagens dos Jogadores
-

## NPCs que apareceram em cena
-

## Locais visitados
-

## Objetos ou achados relevantes
-

## Informações descobertas pelos jogadores
-

## Rumores ou informações incertas
-

## Facções percebidas ou mencionadas
-

## Consequências visíveis
-

## Informações que NÃO devem aparecer
-

## Pedido visual específico
-
```

---

## 7. Procedimento Obrigatório

A criação do infográfico deve seguir a ordem abaixo.

---

### 7.1. Etapa 1 — Leitura do Relatório de Sessão

A IA deve ler o relatório fornecido pelo operador e identificar:

```text
O que foi vivido?
O que foi descoberto?
O que foi apenas sugerido?
O que foi entendido errado?
O que ainda permanece oculto?
```

A IA não deve completar lacunas com informações de atos futuros.

---

### 7.2. Etapa 2 — Mapa de Informação

Antes de propor o infográfico, a IA deve organizar uma matriz simples:

|Informação|Fonte|Status|Pode entrar?|
|---|---|---|---|
|Exemplo: Floyd encontrou o SWIX|Relatório de sessão|jogado|Sim|
|Exemplo: SWIX é satélite|Ato II / estrutura futura|oculto/futuro|Não|
|Exemplo: há rumores de energia incomum|Relatório / NPC|rumor|Sim, como rumor|
|Exemplo: Core de Aethera|Ato III / bastidor|oculto/futuro|Não|

Essa etapa pode ser resumida, mas deve guiar todo o processo.

---

### 7.3. Etapa 3 — Auditoria de Spoilers

A IA deve comparar o relatório de sessão com os arquivos da aventura e separar:

- informação já revelada;
    
- informação preparada mas ainda não revelada;
    
- informação que só o mestre sabe;
    
- informação que pode ser insinuada;
    
- informação que deve ser removida.
    

A função dos arquivos da aventura, nesta etapa, é principalmente **impedir vazamento**, não enriquecer livremente o infográfico.

---

### 7.4. Etapa 4 — Briefing Visual

Antes de gerar imagem final, a IA deve entregar um briefing visual em Markdown.

Esse briefing deve conter:

- formato;
    
- proporção;
    
- paleta;
    
- estilo;
    
- estrutura de blocos;
    
- personagens ou elementos visuais centrais;
    
- ícones ou símbolos necessários;
    
- grau de textura;
    
- restrições visuais;
    
- observações sobre legibilidade.
    

---

### 7.5. Etapa 5 — Mini-Roteiro Textual

Antes da imagem final, a IA deve entregar também o mini-roteiro textual do infográfico.

Esse mini-roteiro deve listar:

- título;
    
- subtítulo;
    
- blocos principais;
    
- texto de cada bloco;
    
- legendas;
    
- nomes corretos;
    
- facções;
    
- chamadas curtas;
    
- palavras proibidas.
    

O operador deve revisar esse texto antes da geração final.

---

### 7.6. Etapa 6 — Aprovação do Operador

A imagem final só deve ser gerada depois que o operador aprovar:

1. briefing visual;
    
2. mini-roteiro textual;
    
3. nível de revelação;
    
4. lista de elementos proibidos.
    

Exceção: o operador pode pedir explicitamente geração direta, mas isso deve ser tratado como exceção operacional.

---

### 7.7. Etapa 7 — Geração da Imagem

Após aprovação, gerar a imagem seguindo o padrão visual definido.

Se houver texto extenso ou necessidade de precisão tipográfica, a IA deve favorecer uma das duas soluções:

1. gerar imagem com texto curto e revisável;
    
2. gerar imagem-base e fornecer textos separados para aplicação manual em Photoshop.
    

Quando a legibilidade for crítica, o texto final deve ser aplicado ou corrigido manualmente.

---

### 7.8. Etapa 8 — Correções por Camadas

Após a primeira imagem, as correções devem ser feitas preferencialmente por elementos isolados:

- símbolo de facção;
    
- retrato de NPC;
    
- bloco de texto;
    
- ícone;
    
- moldura;
    
- objeto central;
    
- faixa inferior;
    
- cabeçalho.
    

Isso facilita edição em Photoshop e evita refazer a imagem inteira por erro pontual.

---

### 7.9. Etapa 9 — Consolidação Final

A versão final deve ser validada contra o checklist:

- a proporção está correta?
    
- os textos estão legíveis?
    
- todos os nomes estão corretos?
    
- os símbolos seguem o mesmo estilo?
    
- não há spoilers?
    
- não há informação de ato futuro?
    
- o infográfico corresponde ao relatório da sessão?
    
- o tom visual está coerente com _Outsiders: Lost Frontier_?
    
- o arquivo funciona como handout para jogadores?
    

---

## 8. Proporção e Formato

### 8.1. Proporção Padrão

```text
4:3 horizontal
```

Essa é a proporção preferencial para Infográficos de Recapitulação.

Ela favorece:

- leitura em tela;
    
- organização em blocos;
    
- uso em VTT;
    
- exportação como handout;
    
- adaptação para Obsidian, Foundry e apresentações.
    

### 8.2. Uso de 1:1

A proporção 1:1 pode ser usada para:

- testes visuais;
    
- versões de prévia;
    
- cortes para redes sociais;
    
- ícones isolados;
    
- retratos;
    
- elementos complementares.
    

Não deve ser o padrão final do infográfico principal.

---

## 9. Estilo Visual Padrão

O Infográfico de Recapitulação deve seguir a identidade visual geral de _Outsiders: Lost Frontier_:

```text
western sci-fi de fronteira
horror cósmico materialista
dossiê diegético
sucata industrial
papel gasto
ferrugem
ocre
preto carvão
branco sujo
textura de impressão degradada
```

### 9.1. Paleta Recomendada

- preto carvão;
    
- marrom queimado;
    
- ferrugem;
    
- ocre;
    
- dourado envelhecido;
    
- branco sujo;
    
- púrpura discreto para elementos anômalos;
    
- laranja queimado para títulos secundários.
    

### 9.2. Estilo Gráfico

- pôster de fronteira;
    
- painel jornalístico diegético;
    
- dossiê visual;
    
- textura de papel gasto;
    
- ícones planos;
    
- molduras rústicas;
    
- tipografia industrial;
    
- ilustração semi-realista suja;
    
- composição de handout de RPG.
    

### 9.3. Evitar

- estética limpa de sci-fi branca;
    
- UI futurista neon;
    
- excesso de hologramas;
    
- render 3D polido;
    
- visual corporativo moderno demais;
    
- excesso de partículas;
    
- textos longos demais;
    
- símbolos hiper-renderizados;
    
- facções com marcas em estilos divergentes.
    

---

## 10. Padrão dos Ícones e Símbolos

Ícones de facção devem seguir o mesmo padrão visual.

### 10.1. Regras

- uma cor principal;
    
- textura plana desgastada;
    
- silhueta clara;
    
- sem volume 3D;
    
- sem brilho metálico realista;
    
- sem renderização pictórica;
    
- boa leitura em tamanho pequeno;
    
- estilo de stencil, marca impressa ou símbolo de facção.
    

### 10.2. Exemplo de Aplicação

Símbolos como **Guilda de Ferro**, **Axyon Core**, **LMT**, **Abutres de Aço** e **Chifres da Areia Baixa** devem parecer parte da mesma família gráfica, mesmo que tenham identidades conceituais diferentes.

A distinção deve vir da silhueta, não de mudanças bruscas de estilo.

---

## 11. Estrutura Recomendada do Infográfico

Um Infográfico de Recapitulação pode seguir a estrutura abaixo.

```text
Cabeçalho
├── Título do local / evento
├── Subtítulo
└── Texto curto de ambientação

Bloco de Visão Geral
├── 4 a 6 pontos rápidos
└── ícones simples

Bloco Central
├── local, evento ou achado principal
└── imagem focal

Bloco de Contexto
├── instituição local
├── histórico seguro
└── função social

Bloco de Personagens Importantes
├── 2 a 4 NPCs
├── retrato pequeno
└── descrição curta

Bloco de Mecânica Diegética / Cultura Local
├── animais, tecnologia, prática social ou economia
└── explicação jogador-safe

Bloco de Interesses e Ameaças
├── facções percebidas
├── símbolos
└── intenções superficiais ou públicas
```

---

## 12. Padrão de Texto

### 12.1. Extensão

Textos devem ser curtos.

Recomendação:

```text
Título: 1 linha
Subtítulo: 1 linha
Bloco curto: 20 a 45 palavras
Descrição de NPC: 25 a 50 palavras
Facção no rodapé: 10 a 20 palavras
```

### 12.2. Linguagem

Usar linguagem:

- direta;
    
- diegética;
    
- evocativa;
    
- sem explicação de mestre;
    
- sem termos mecânicos;
    
- sem “os jogadores descobriram”;
    
- sem “no próximo ato”;
    
- sem “isso será importante depois”.
    

### 12.3. Verbos Recomendados

- encontra;
    
- observa;
    
- protege;
    
- pressiona;
    
- deseja;
    
- busca;
    
- teme;
    
- disputa;
    
- guarda;
    
- fareja;
    
- atrai;
    
- resiste;
    
- transforma;
    
- ameaça.
    

### 12.4. Fórmulas Seguras

Usar:

```text
parece
rumores indicam
foi visto
atraiu atenção
peça marcada por
achado tecnológico
sinal incomum
energia instável
interesse externo
pressão crescente
```

Evitar, salvo se já revelado em sessão:

```text
é
revela
confirma
contém
prova que
satélite
Core
Aethera confirmada
Starwalker-IX
Outpost-87
três fragmentos
Chave de Rastro
```

---

## 13. Regra de Spoiler

Uma informação só pode aparecer como fato se estiver em pelo menos uma das categorias abaixo:

1. foi descoberta pelos personagens;
    
2. foi dita a eles;
    
3. foi vista diretamente;
    
4. é conhecimento público do cenário;
    
5. foi explicitamente autorizado pelo operador.
    

Caso contrário, deve ser:

- removida;
    
- transformada em rumor;
    
- substituída por formulação neutra;
    
- ou reservada para infográfico futuro.
    

---

## 14. Regra de Progressão de Revelação

Spoiler não é categoria permanente.

Uma informação proibida no Infográfico de Recapitulação da Sessão 01 pode se tornar permitida na Sessão 03, desde que o relatório de sessão confirme que os jogadores a descobriram.

```text
A informação passa de oculta para pública apenas quando entra no relatório de sessão.
```

Exemplo:

|Informação|Sessão 01|Sessão posterior|
|---|--:|--:|
|SWIX é apenas código em uma peça|Permitido|Permitido|
|SWIX é parte de satélite|Proibido até descoberta|Permitido após revelação|
|Existem três fragmentos|Proibido até descoberta|Permitido após revelação|
|Core de Aethera|Proibido até descoberta|Permitido após revelação|
|Chave de Rastro|Proibido antes de existir|Permitido após criação em jogo|

---

## 15. Uso dos Arquivos da Aventura

Os arquivos da aventura devem ser usados como **fontes de controle**, não como fonte primária do conteúdo do infográfico.

### 15.1. Usos Corretos

- verificar se um termo está correto;
    
- checar o nome de NPCs, facções e locais;
    
- identificar o que ainda é spoiler;
    
- evitar contradições com o módulo;
    
- confirmar a função de uma facção;
    
- manter coerência visual e temática.
    

### 15.2. Usos Incorretos

- revelar cena futura;
    
- antecipar facção ainda não vista;
    
- expor intenção secreta de NPC;
    
- transformar metaplot em conhecimento público;
    
- completar o relatório de sessão com informação que não foi jogada;
    
- revelar objeto, função ou consequência antes da hora.
    

---

## 16. Facções em Infográficos

Facções devem aparecer conforme o nível de informação disponível aos jogadores.

### 16.1. Facção percebida publicamente

Pode aparecer com descrição direta.

Exemplo:

```text
Abutres de Aço
Prospectores fora da lei que roubam salvage e atacam equipes isoladas.
```

### 16.2. Facção interessada, mas não revelada plenamente

Deve aparecer com formulação genérica.

Exemplo:

```text
Axyon Core
Interessa-se por dados, rastreio e tecnologia energética de fronteira.
```

### 16.3. Facção com plano secreto

Não revelar o plano.

Errado:

```text
Axyon Core quer capturar a expedição e monopolizar o Core.
```

Correto:

```text
Axyon Core observa tecnologias que podem alterar o equilíbrio energético local.
```

---

## 17. Exemplo de Filtro — SWIX

### 17.1. Informação segura para Sessão 01

```text
Floyd Merian e Dentinho encontraram uma peça marcada pelo código SWIX.
O achado parece tecnológico, incomum e valioso demais para ser sucata comum.
```

### 17.2. Informação insegura para Sessão 01

```text
O SWIX é um fragmento de satélite.
O SWIX pertence ao Starwalker-IX.
Há três fragmentos.
Um fragmento contém um Core de Aethera.
O SWIX está ligado a Victor Walker e ao Outpost-87.
```

### 17.3. Formulação recomendada

```text
O ACHADO: SWIX
Floyd Merian e seu Tal’Bondak Dentinho encontraram uma peça tecnológica identificada apenas pelo código SWIX.
Ela ainda pulsa, resiste à análise e atrai atenção demais para ser apenas sucata.
```

---

## 18. Exemplo de Filtro — LMT

### 18.1. Formulação cedo demais

```text
LMT
Vê no SWIX a chance de reativar a ferrovia e pôr Rust Hollow no centro da rota.
```

Essa formulação pode ser correta para uma etapa futura, mas é forte demais antes da cena de Declan Kestrel ou antes da LMT entrar formalmente em jogo.

### 18.2. Formulação jogador-safe

```text
LMT
Observa achados capazes de mudar rotas, trilhos e poder logístico.
```

### 18.3. Formulação após revelação em sessão

Depois que Declan Kestrel apresentar seu plano, pode-se usar:

```text
LMT
Vê no SWIX a chance de reativar a ferrovia e pôr Rust Hollow no centro da rota.
```

---

## 19. Lista de Palavras Sensíveis

Antes de gerar o infográfico, a IA deve verificar se alguma palavra abaixo aparece indevidamente.

```text
satélite
Starwalker-IX
Victor Walker
Outpost-87
Lost Frontier
três fragmentos
Core
Core de Aethera
Aethera confirmada
Chave de Rastro
Arreio de Rastro
bússola viva
Shizuka como agente da Axyon
Declan Kestrel
ferrovia como plano já revelado
Lorna envenenada
Haikyo como futuro obstáculo
Nikko como ferramenta de Shizuka
```

A presença dessas palavras não é proibida para sempre.  
Ela depende do relatório de sessão.

---

## 20. Briefing Visual — Modelo

```markdown
# Briefing Visual — Infográfico de Recapitulação

## Identificação
- Campanha:
- Módulo:
- Sessão:
- Título:

## Proporção
4:3 horizontal.

## Função Visual
Handout de recapitulação jogador-safe, com aparência de pôster/dossiê de fronteira.

## Estilo
Western sci-fi de sucata, papel gasto, textura industrial, ocre, ferrugem, preto carvão, branco sujo.

## Composição
- Cabeçalho no topo esquerdo.
- Arte principal do local ou evento no topo/centro.
- Bloco de visão geral à esquerda.
- Bloco de instituição ou contexto no centro.
- Bloco de personagens à direita.
- Bloco de cultura/tecnologia local na região inferior.
- Rodapé com facções, interesses e ameaças.

## Restrições
- Não revelar informações futuras.
- Não usar texto em inglês.
- Não inserir facções que não apareceram ou não foram autorizadas.
- Não usar símbolos fora do padrão gráfico.
- Não mencionar [lista de spoilers].
```

---

## 21. Mini-Roteiro Textual — Modelo

```markdown
# Mini-Roteiro Textual — Infográfico de Recapitulação

## Cabeçalho
Título:
Subtítulo:
Texto curto:

## Visão Geral
1.
2.
3.
4.
5.

## Bloco Central
Título:
Texto:

## Bloco de Contexto
Título:
Texto:

## Personagens Importantes
### NPC 1
Texto:

### NPC 2
Texto:

### NPC 3
Texto:

## Cultura / Tecnologia Local
Título:
Pontos:

## Interesses e Ameaças
### Facção 1
Texto:

### Facção 2
Texto:

### Facção 3
Texto:

## Palavras Proibidas Nesta Versão
-
```

---

## 22. Checklist Antes da Geração

Antes de gerar a imagem, confirmar:

```markdown
- [ ] O relatório de sessão foi fornecido pelo operador.
- [ ] O infográfico está baseado no relatório, não em ato futuro.
- [ ] Os arquivos da aventura foram usados apenas como controle de coerência e spoiler.
- [ ] O mini-roteiro textual foi aprovado.
- [ ] O briefing visual foi aprovado.
- [ ] A proporção será 4:3 horizontal.
- [ ] Todos os nomes próprios estão corretos.
- [ ] Nenhum texto está em inglês.
- [ ] Nenhuma facção indevida aparece.
- [ ] Os símbolos seguem o mesmo padrão visual.
- [ ] Os textos cabem visualmente.
- [ ] Informações incertas foram tratadas como rumor.
- [ ] Informações futuras foram removidas.
```

---

## 23. Checklist Pós-Geração

Após gerar a imagem, revisar:

```markdown
- [ ] O texto está legível.
- [ ] Não houve invenção de nomes.
- [ ] Não houve tradução indevida.
- [ ] Não houve distorção de facções.
- [ ] Não apareceu símbolo errado.
- [ ] Não apareceu spoiler visual.
- [ ] A composição está equilibrada.
- [ ] A proporção está correta.
- [ ] O tom visual corresponde a Outsiders: Lost Frontier.
- [ ] A imagem pode ser mostrada aos jogadores sem correção de conteúdo.
```

---

## 24. Procedimento de Correção

Se a imagem estiver boa, mas houver erro pontual, não refazer tudo automaticamente.

Priorizar geração de elementos isolados:

```text
símbolo corrigido
caixa de texto corrigida
bloco de facção
retrato substituto
ícone avulso
moldura
cabeçalho
objeto central
```

Isso permite correção manual em Photoshop sem perder a composição geral.

---

## 25. Padrão de Nomeação

Sugestão de nomes de arquivo:

```text
OLF_Recap_SessaoXX_Titulo_v01.png
OLF_Recap_SessaoXX_Titulo_v02_corrigida.png
OLF_Recap_SessaoXX_Titulo_FINAL.png
```

Para elementos avulsos:

```text
OLF_Icone_Faccao_LMT_v01.png
OLF_BlocoTexto_AxyonCore_v01.png
OLF_Retrato_FloydMerian_v01.png
```

---

## 26. Regra Final

```text
O infográfico de recapitulação deve parecer memória organizada da mesa, não revelação do mestre.
```

Ele deve ajudar os jogadores a lembrar o que viveram, não ensinar o que ainda vão descobrir.

A lâmina deve ser bonita, clara e útil — mas deve saber menos do que o módulo.