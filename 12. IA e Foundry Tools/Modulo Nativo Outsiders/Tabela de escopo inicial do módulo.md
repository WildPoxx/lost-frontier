

# 1. Tabela de escopo inicial do módulo

Esta é a primeira versão da **constituição operacional** do módulo. Ela define o que entra, quando entra e em qual forma dentro do Foundry.

## 1.1. Núcleo técnico

| Bloco                       | Entra no módulo? | Entra agora? | Tipo no Foundry     | Prioridade | Observações                                                    |
| --------------------------- | ---------------: | -----------: | ------------------- | ---------: | -------------------------------------------------------------- |
| `module.json`               |              Sim |          Sim | Manifesto do módulo |       Alta | Arquivo obrigatório para o Foundry reconhecer o módulo.        |
| Nome do módulo              |              Sim |          Sim | Metadado            |       Alta | Sugestão: `Outsiders — Lost Frontier`.                         |
| ID técnico do módulo        |              Sim |          Sim | Metadado            |       Alta | Sugestão: `outsiders-lost-frontier`. Sem acentos, sem espaços. |
| Compatibilidade Foundry v13 |              Sim |          Sim | Manifesto           |       Alta | Deve mirar Foundry v13, não v14.                               |
| Dependência do SWADE        |              Sim |          Sim | Manifesto           |       Alta | O módulo deve depender do sistema `swade`.                     |
| Scripts próprios            |              Sim |          Não | JavaScript          |      Média | Só entram quando houver macros consolidadas.                   |
| CSS próprio                 |              Sim |          Não | Style               |      Baixa | Pode esperar. Não é necessário no início.                      |
| Tradução própria            |              Sim |       Depois | `lang/pt-BR.json`   |      Média | Útil, mas não bloqueia o primeiro protótipo.                   |

---

# 2. Conteúdo de personagem

## 2.1. Ancestralidades

|Bloco|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Humanos|Sim|Sim|Ancestry|Alta|Base adaptativa. Precisa ser jogável desde o início.|
|Krohminitas|Sim|Sim|Ancestry|Alta|Espécie central, com ciclo biológico e linhagens.|
|Orunai|Sim|Sim|Ancestry|Alta|Essenciais para Teleritha e Sincrisólise.|
|Kitanos|Sim|Sim|Ancestry|Alta|Importantes para Rust Hollow e Programa Segunda Trilha.|
|Kadiff|Sim|Depois|Ancestry|Média|Importantes no cenário, mas podem entrar após o núcleo inicial.|
|Tarekhs|Sim|Depois|Ancestry|Média|Relevantes ao Conclave e antagonismos regionais.|
|Migma|Sim|Depois|Ancestry ou NPC/Creature|Baixa|Melhor decidir depois se são jogáveis ou apenas criaturas semi-sencientes.|
|Dicianos/Arkannones|Não agora|Não|NPC/Lore|Baixa|Devem permanecer como camada oculta/mítica, não opção inicial.|

### Decisão

O primeiro pacote jogável deve conter:

```text
Humanos
Krohminitas
Orunai
Kitanos
```

---

## 2.2. Linhagens e subtipos

|Bloco|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Linhagens Krohminitas Guerreiras|Sim|Sim|Edge ou Ability|Alta|Não devem reforçar clichê de “raça guerreira”; são adaptação funcional.|
|Linhagens Krohminitas Mantenedoras|Sim|Sim|Edge ou Ability|Alta|Ligadas à sobrevivência e estabilidade biológica.|
|Linhagens Krohminitas Sacerdotais|Sim|Sim|Edge ou Ability|Alta|Potencial acesso a Psionics, com controle do GM.|
|Linhagens Mistas|Sim|Depois|Edge ou Ability|Média|Melhor depois que as três bases estiverem testadas.|
|Estruturas Vibracionais Orunai — Fluxa|Sim|Sim|Ability ou Edge|Alta|Condução energética.|
|Estruturas Vibracionais Orunai — Gravis|Sim|Sim|Ability ou Edge|Alta|Estabilização.|
|Estruturas Vibracionais Orunai — Veyra|Sim|Sim|Ability ou Edge|Alta|Expansão/propagação.|
|Estruturas Vibracionais Orunai — Pyra|Sim|Sim|Ability ou Edge|Alta|Liberação de energia com risco.|
|Estruturas Vibracionais Orunai — Aethera|Sim|Sim, mas restrita|Ability ou Edge|Alta|Deve exigir controle do GM. Muito forte para uso aberto.|

### Decisão

Linhagens e estruturas entram como **subescolhas mecânicas**, mas não devem virar sistema separado ainda.

---

# 3. Hindrances

|Hindrance|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Dependência — Teleritha|Sim|Sim|Hindrance|Alta|Essencial para Orunai.|
|Vulnerabilidade — Vibração|Sim|Sim|Hindrance|Alta|Essencial para Orunai.|
|Cognição Alienígena|Sim|Sim|Hindrance|Alta|Penalidade social e interpretação de padrões.|
|Rigidez de Padrão|Sim|Sim|Hindrance|Alta|Limita improvisação Orunai.|
|Ciclo Biológico Krohminita|Sim|Sim|Hindrance|Alta|Essencial para Krohminitas.|
|Fraqueza Ambiental — Atmosfera Rarefeita|Sim|Sim|Hindrance|Alta|Krohminitas e ambientes extremos.|
|Vulnerabilidade ao Frio|Sim|Sim|Hindrance|Alta|Krohminitas.|
|Exposição ao Véu|Sim|Depois|Hindrance|Média|Melhor após regras de Véu Rasgado.|
|Ressonância Instável|Sim|Sim|Hindrance|Alta|Conecta Sincrisólise e risco de Teleritha.|
|Dívida de Companhia|Sim|Depois|Hindrance|Média|Boa para Rust Hollow, mas pode ser Edge/Hindrance social posterior.|
|Marcado por Facção|Sim|Depois|Hindrance|Média|Pode ser genérico demais agora.|
|Contaminação por Pulvis|Sim|Depois|Hindrance|Média|Precisa de regra de exposição antes.|

### Decisão

Primeiro pacote de Hindrances:

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

---

# 4. Edges

|Edge|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Sintonia com Teleritha|Sim|Sim|Edge|Alta|Edge-base para interagir com cepas.|
|Iniciado em Sincrisólise|Sim|Sim|Edge|Alta|Porta de entrada para a regra própria.|
|Ressonador Orunai|Sim|Sim|Edge|Alta|Especialização Orunai.|
|Condutor de Bondak|Sim|Sim|Edge|Alta|Importante em Rust Hollow.|
|Condutor de Tal’Bondak|Sim|Sim|Edge|Alta|Central para SWIX e prospecção avançada.|
|Interface Neural de Rastro|Sim|Sim|Edge|Alta|Deve exigir Condutor de Tal’Bondak ou acesso à Companhia.|
|Prospector de Rust Hollow|Sim|Sim|Edge|Alta|Identidade inicial de campanha.|
|Cartógrafo do Véu|Sim|Depois|Edge|Média|Melhor após módulo do Véu Rasgado.|
|Cepador Aprendiz|Sim|Depois|Edge|Média|Depende de regras de refino.|
|Veterano do Campo das Estrelas Cadentes|Sim|Depois|Edge|Média|Pode entrar no arco de prospecção.|
|Operador de Aethera|Sim|Não agora|Edge|Alta futura|Deve ser restrito. Não abrir no pacote inicial sem custo claro.|
|Agente de Facção|Sim|Depois|Edge|Média|Criar quando facções tiverem mecânica própria.|

### Decisão

Primeiro pacote de Edges:

```text
Sintonia com Teleritha
Iniciado em Sincrisólise
Ressonador Orunai
Condutor de Bondak
Condutor de Tal’Bondak
Interface Neural de Rastro
Prospector de Rust Hollow
```

---

# 5. Teleritha

## 5.1. Cepas

|Cepa|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Pyra|Sim|Sim|Journal + Trapping|Alta|Energia explosiva, risco de instabilidade.|
|Gravis|Sim|Sim|Journal + Trapping|Alta|Estabilidade, ancoragem, resistência.|
|Fluxa|Sim|Sim|Journal + Trapping|Alta|Condução, consciência, interface.|
|Veyra|Sim|Sim|Journal + Trapping|Alta|Vibração, expansão, propagação.|
|Aethera|Sim|Sim, restrita|Journal + Trapping|Alta|Espaço-tempo; deve ter aviso de uso controlado.|
|Pulvis|Sim|Sim|Journal|Alta|Base industrial degradada.|
|Osmério|Sim|Sim|Journal|Alta|Importante para Tal’Bondaks e LMT.|
|Occanium|Sim|Depois|Journal|Média|Ligada a Victor Walker; melhor preservar mistério.|
|Fio de Walker|Sim|Não agora|Journal/Artifact|Alta futura|Deve ser revelação avançada, não material inicial.|
|Prismas Primordiais|Sim|Depois|Journal/Item|Média|Relevantes, mas não para o primeiro módulo jogável.|

### Decisão

Primeiro pacote de Teleritha:

```text
Pyra
Gravis
Fluxa
Veyra
Aethera
Pulvis
Osmério
```

Occanium e Fio de Walker ficam guardados para não estragar revelações.

---

# 6. Powers e trappings

|Bloco|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Lista completa de Powers SWADE duplicada|Não|Não|Power|Baixa|Não duplicar o livro básico.|
|Trappings por cepa|Sim|Sim|Journal/Power notes|Alta|Forma mais limpa de adaptar Teleritha.|
|Powers específicos de Aethera|Sim|Depois|Power|Alta futura|Muito fortes; precisam de custo.|
|Powers Orunai inatos|Sim|Sim, poucos|Ability/Power|Alta|Apenas os centrais.|
|Powers Krohminitas sacerdotais|Sim|Depois|Power/Edge|Média|Melhor com controle do GM.|
|Sincrisólise como Power|Não agora|Não|Power|Média|Melhor começar como Edge + regra + macro.|

### Decisão

Não vamos criar uma lista gigante de Powers agora.

Vamos criar:

```text
Journal: Trappings de Teleritha
Journal: Uso de Powers com Cepas
Edge: Iniciado em Sincrisólise
Macro futura: Teste de Sincrisólise
```

---

# 7. Sincrisólise

|Bloco|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Regra textual de Sincrisólise|Sim|Sim|Journal|Alta|Deve ser clara para jogadores e mestre.|
|Edge: Iniciado em Sincrisólise|Sim|Sim|Edge|Alta|Acesso inicial.|
|Hindrance: Ressonância Instável|Sim|Sim|Hindrance|Alta|Risco recorrente.|
|Tabela de Sobrecarga|Sim|Sim|RollTable|Alta|Útil em mesa desde o início.|
|Macro de Teste de Sincrisólise|Sim|Depois|Macro/Script|Alta|Depois de fechar a regra textual.|
|Automação completa|Sim|Não agora|Script/hooks|Baixa inicial|Só após testes.|

### Decisão

Sincrisólise entra agora como **regra jogável**, mas não como automação pesada.

---

# 8. Rust Hollow e primeiro arco

|Bloco|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Rust Hollow|Sim|Sim|Journal|Alta|Base da campanha inicial.|
|Companhia Bask-Callico|Sim|Sim|Journal/Faction|Alta|Agente central da cidade.|
|Programa Segunda Trilha|Sim|Sim|Journal|Alta|Conecta Floyd, Kitanos e Tal’Bondaks.|
|Bondaks|Sim|Sim|Journal/Creature|Alta|Recurso central de rastreio.|
|Tal’Bondaks|Sim|Sim|Journal/Creature/Item|Alta|Central no arco SWIX.|
|Floyd Merian|Sim|Sim|NPC/Journal|Alta|Gatilho humano da aventura.|
|Dentinho|Sim|Sim|NPC/Creature|Alta|Tal’Bondak chave.|
|Fragmento SWIX|Sim|Sim|Item/Journal|Alta|McGuffin inicial.|
|Starwalker-IX|Sim|Não agora|Journal oculto|Alta futura|Revelação posterior.|
|Outpost-87|Sim|Não agora|Journal oculto|Alta futura|Horizonte de campanha, não abertura.|
|Victor Walker|Sim|Não agora|Journal oculto|Alta futura|Deve ser tratado como mistério progressivo.|

### Decisão

Entram agora os elementos visíveis do primeiro arco. Os elementos de revelação avançada entram depois, ou como documentos secretos do GM.

---

# 9. Facções

|Facção|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Companhia Bask-Callico|Sim|Sim|Journal/Faction|Alta|Núcleo de Rust Hollow.|
|Stargazers|Sim|Sim|Journal/Faction|Alta|Ligados a Lorna Kamen.|
|Expedicionários|Sim|Sim|Journal/Faction|Alta|Fundamentais para Walker, Véu e SWIX.|
|Guilda de Ferro|Sim|Sim|Journal/Faction|Alta|Pressão externa sobre Rust Hollow.|
|Cyberdome|Sim|Sim|Journal/Faction|Alta|Interesse por tecnologia e Aethera.|
|LMT|Sim|Sim|Journal/Faction|Alta|Refino, Osmério, Teleritha.|
|Abutres de Aço|Sim|Sim|Journal/Faction|Média|Ameaça local útil.|
|Chifres da Areia Baixa|Sim|Depois|Journal/Faction|Média|Podem esperar até maior foco no Alário.|
|Culto dos Deuses Mortos|Sim|Depois|Journal/Faction|Média|Importante, mas talvez não no primeiro pacote.|
|Cruz de Sangue|Sim|Não agora|Journal/Faction|Baixa inicial|Tema pesado e localizado no Alário.|
|Dark Spawn|Sim|Não agora|Journal/Faction|Média futura|Melhor quando Sunirae/Krohminitas entrarem mais forte.|
|Technoyakuza|Sim|Depois|Journal/Faction|Alta futura|Inicialmente aparece por Cyberdome.|

### Decisão

Primeiro pacote de facções:

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

# 10. NPCs e criaturas

|Bloco|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Floyd Merian|Sim|Sim|Actor/NPC|Alta|Gatilho da aventura.|
|Dentinho|Sim|Sim|Actor/Creature|Alta|Tal’Bondak especial.|
|Synthas Abi|Sim|Sim|Actor/NPC|Alta|Presidente da Companhia.|
|Lorna Kamen|Sim|Sim|Actor/NPC|Alta|Stargazers e legado de Lionel.|
|Lionel Kamen|Sim|Journal|Journal/NPC morto|Média|Importante como passado recente.|
|Agente da Guilda|Sim|Sim|Actor/NPC genérico|Média|Pressão externa.|
|Técnico Cyberdome|Sim|Sim|Actor/NPC genérico|Média|Pressão técnica/corporativa.|
|Cepador LMT|Sim|Sim|Actor/NPC genérico|Média|Refino e certificação.|
|Bondak comum|Sim|Sim|Actor/Creature|Alta|Criatura utilitária.|
|Tal’Bondak comum|Sim|Sim|Actor/Creature|Alta|Criatura utilitária especial.|
|Bestiário amplo|Sim|Não agora|Actors|Baixa inicial|Depois.|

### Decisão

Primeiro pacote de NPCs/criaturas:

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

# 11. Tabelas

|Tabela|Entra no módulo?|Entra agora?|Tipo no Foundry|Prioridade|Observações|
|---|--:|--:|---|--:|---|
|Sobrecarga de Teleritha|Sim|Sim|RollTable|Alta|Essencial para Sincrisólise.|
|Reação de Tal’Bondak|Sim|Sim|RollTable|Alta|Útil em prospecção e SWIX.|
|Complicações de Prospecção|Sim|Sim|RollTable|Alta|Mesa inicial.|
|Fenômenos do Campo das Estrelas Cadentes|Sim|Sim|RollTable|Alta|Ambiente ativo.|
|Interferência do Véu Rasgado|Sim|Depois|RollTable|Média|Quando Outpost-87 se aproximar.|
|Interesse de Facção|Sim|Sim|RollTable|Média|Reação ao SWIX.|
|Mutação/Contaminação|Sim|Depois|RollTable|Média|Depende de regra específica.|

### Decisão

Primeiro pacote de tabelas:

```text
Sobrecarga de Teleritha
Reação de Tal’Bondak
Complicações de Prospecção
Fenômenos do Campo das Estrelas Cadentes
Interesse de Facção
```

---

# 12. Macros

|Macro|Entra no módulo?|Entra agora?|Prioridade|Observações|
|---|--:|--:|--:|---|
|Teste de Sincrisólise|Sim|Depois|Alta|Primeiro precisamos fechar a regra.|
|Sobrecarga de Teleritha|Sim|Depois|Alta|Pode puxar RollTable.|
|Reação de Tal’Bondak|Sim|Depois|Alta|Pode rolar tabela e postar no chat.|
|Complicação de Prospecção|Sim|Depois|Alta|Útil para o GM.|
|Fenômeno do Véu Rasgado|Sim|Depois|Média|Melhor quando a campanha chegar perto do Véu.|
|Criar item automaticamente|Não agora|Não|Baixa|Automação demais para início.|
|Aplicar efeitos automaticamente|Sim|Depois|Média|Só após testar as regras.|

### Decisão

Macros não entram antes da regra textual estar consolidada.

---

# 13. O que fica fora do módulo inicial

|Bloco|Motivo para ficar fora agora|
|---|---|
|Fork do sistema SWADE|Risco alto e desnecessário neste momento.|
|Automação completa de Sincrisólise|A regra ainda precisa ser testada em mesa.|
|Todos os mapas|Melhor tratar mapas como pacote separado.|
|Músicas e ambientação sonora|Não são prioridade funcional.|
|Bestiário completo|Pode inflar o módulo cedo demais.|
|Todas as colônias completas|O foco inicial é Rust Hollow.|
|Sistema econômico detalhado|Alto custo de preparação, baixo retorno inicial.|
|Crafting completo de Teleritha|Precisa de fase própria.|
|Regras completas de veículos/chases|Entram quando houver cenas específicas.|
|Outpost-87 completo|Deve ser preparado como segundo grande bloco da campanha.|
|Segredos macro do cenário|Devem entrar como journals secretos apenas quando necessários.|

---

# 14. Versão resumida do escopo inicial

## Entra agora

```text
Manifesto do módulo
Ancestralidades iniciais
Hindrances centrais
Edges centrais
Teleritha básica
Regra textual de Sincrisólise
Rust Hollow
Companhia Bask-Callico
Programa Segunda Trilha
Bondaks e Tal’Bondaks
Floyd, Dentinho, Synthas e Lorna
Facções do arco inicial
Tabelas de risco e prospecção
```

## Entra depois

```text
Macros
Active Effects refinados
Kadiff, Tarekhs e Migma jogáveis
Outpost-87
Starwalker-IX
Victor Walker
Véu Rasgado
Bestiário expandido
Colônias completas
Crafting e economia
```

## Não entra por enquanto

```text
Alteração do sistema SWADE
Automação pesada
Fork
Interface própria
Pacote completo de mapas e música
```

---

# 15. Próximo passo

O próximo passo é transformar esse escopo em um **Plano de Construção do Módulo v0.1**.

Esse plano deve definir:

```markdown
1. Nome oficial do módulo
2. ID técnico
3. descrição curta
4. lista de compêndios iniciais
5. lista de documentos que criaremos primeiro
6. ordem de trabalho
7. critério de pronto
```

Minha recomendação é que a versão v0.1 tenha este objetivo:

> Fazer o módulo aparecer no Foundry v13 e conter o primeiro pacote jogável de Outsiders — Lost Frontier, ainda sem automação pesada.

Isso nos mantém no chão. Primeiro a carcaça. Depois o sangue.