# Diretrizes de Desenvolvimento de Aventura de RPG

## I. Função do Documento

Use este documento como referência obrigatória para desenvolver, revisar ou expandir aventuras de RPG.

A IA deve tratar estas diretrizes como um **modelo operacional**, não como teoria narrativa abstrata.

Sempre que o usuário solicitar o desenvolvimento de atos, módulos, cenas, eventos, NPCs, facções, desafios ou estruturas de aventura, a IA deve aplicar este documento antes de escrever conteúdo definitivo.

---

# II. Regra-Mãe

A aventura de RPG não deve ser tratada como roteiro fechado.

A IA deve desenvolvê-la como:

> uma rede modular de agentes, eventos, cenas, lugares, objetivos, pressões e consequências.

O objetivo não é prever tudo que acontecerá em mesa, mas preparar uma estrutura robusta para que o mestre consiga reagir às escolhas dos jogadores sem perder coerência narrativa, mecânica ou temática.

---

# III. Ordem Obrigatória de Trabalho

A IA deve seguir esta ordem:

1. Definir ou revisar os **5W + HOW**.
    
2. Identificar os **agentes ativos**.
    
3. Definir o **conflito central**.
    
4. Definir os **objetos de desejo**.
    
5. Mapear os **Focal Points**.
    
6. Organizar a aventura em **Atos**.
    
7. Dividir os Atos em **Módulos**.
    
8. Desenvolver os Módulos em **Cenas**.
    
9. Inserir **Eventos Espontâneos possíveis**.
    
10. Definir **gatilhos, entradas, saídas e consequências**.
    
11. Integrar o sistema de regras.
    
12. Revisar coerência, liberdade dos jogadores e ritmo.
    

A IA não deve escrever cenas completas antes de mapear a estrutura mínima acima, salvo se o usuário solicitar explicitamente uma cena isolada.

---

# IV. 5W + HOW para Aventuras de RPG

## 1. WHO — Quem age?

A IA deve identificar os agentes relevantes da aventura.

Na **Fase 1**, quando os PCs ainda não estão definidos, a IA deve trabalhar com:

- NPCs;
    
- facções;
    
- instituições;
    
- antagonistas;
    
- aliados potenciais;
    
- criaturas inteligentes;
    
- forças ambientais organizadas;
    
- agentes indiretos.
    

Para cada agente, definir:

```markdown
### Nome do Agente

- Tipo:
- Objetivo:
- Motivação:
- Recursos:
- Método de ação:
- Limites:
- Relações:
- O que faz se os PCs não interferirem:
```

A IA não deve presumir motivações pessoais dos PCs antes de eles serem apresentados.

---

## 2. WHAT — O que está em jogo?

A IA deve definir:

- conflito central;
    
- incidente incitante;
    
- ameaça principal;
    
- objetivos práticos;
    
- McGuffins;
    
- recompensas;
    
- perdas possíveis;
    
- riscos;
    
- verbos de interação.
    

Modelo:

```markdown
## WHAT — Conflito e Objetivos

- Incidente incitante:
- Conflito central:
- Objeto(s) de desejo:
- Ameaça principal:
- Riscos imediatos:
- Riscos de longo prazo:
- Verbos de jogo incentivados:
- Recompensas possíveis:
- Perdas possíveis:
```

Verbos de jogo recomendados:

- investigar;
    
- rastrear;
    
- negociar;
    
- sobreviver;
    
- recuperar;
    
- proteger;
    
- fugir;
    
- escoltar;
    
- sabotar;
    
- infiltrar;
    
- decifrar;
    
- explorar;
    
- resistir;
    
- combater.
    

---

## 3. WHERE — Onde acontece?

A IA deve tratar lugares como **espaços reativos**, não como cenários estáticos.

Para cada local relevante:

```markdown
### Nome do Local

- Função narrativa:
- Função mecânica:
- Agentes presentes:
- Recursos disponíveis:
- Perigos:
- Segredos:
- Estado inicial:
- Como muda se os PCs intervêm:
- Como muda se os PCs ignoram:
- Conexões com outros locais:
```

O WHERE também deve indicar em que ponto modular da aventura uma cena pode ocorrer.

---

## 4. WHEN — Quando muda a pressão?

A IA deve tratar o WHEN como **linha meta-narrativa**, não apenas cronologia histórica.

Definir:

- sequência provável;
    
- gatilhos;
    
- timers;
    
- escalada;
    
- cronograma dos antagonistas;
    
- consequências da inação;
    
- posição dos Focal Points.
    

Modelo:

```markdown
## WHEN — Linha Meta-Narrativa

- Estado inicial:
- Primeiro gatilho:
- Primeira escalada:
- Ponto de pressão intermediário:
- Evento de virada:
- Ponto de não retorno:
- Clímax provável:
- O que acontece se os PCs não fizerem nada:
```

---

## 5. WHY — Por que importa?

A IA deve definir a motivação e a função dramática.

Modelo:

```markdown
## WHY — Motivação e Tema

- Tema central:
- Por que o conflito importa:
- Por que os agentes se importam:
- Por que os PCs podem se envolver:
- Que dilema a aventura coloca:
- Que mudança deve ocorrer até o final:
```

O WHY deve orientar improvisação, consequência e ritmo.

---

## 6. HOW — Como funciona em jogo?

A IA deve traduzir narrativa em mecânica.

Modelo:

```markdown
## HOW — Resolução em Sistema

- Sistema:
- Regras centrais aplicáveis:
- Tipos de teste prováveis:
- Desafios mecânicos principais:
- Uso de combate:
- Uso de exploração:
- Uso de interação social:
- Uso de horror:
- Uso de perigos ambientais:
- Consequências mecânicas recorrentes:
```

Para SWADE, considerar especialmente:

- Tests;
    
- Support;
    
- Dramatic Tasks;
    
- Quick Encounters;
    
- Chases;
    
- Fear Checks;
    
- Hazards;
    
- Fatigue;
    
- Wounds;
    
- Social Conflicts;
    
- Interludes.
    

---

# V. Categorias Estruturais Obrigatórias

## 1. Ato

Unidade macro da aventura.

Modelo:

```markdown
# Ato [Número] — [Título]

## Sinopse narrativa

[Texto em prosa, com 1 a 3 parágrafos desenvolvidos.]

## Função narrativa do ato

- Função principal:
- Estado inicial:
- Estado esperado ao final:
- Pressão dominante:
- Agentes centrais:
- Conflito principal:
- Revelações esperadas:
- Decisões esperadas dos PCs:

## Possível desenrolar da ação

- Caminho provável:
- Eventos condicionais:
- Reações de facções:
- Consequências da inação:

## Cenas-chave

- Cena 1:
- Cena 2:
- Cena 3:

## Alternativas possíveis

- Encerramento alternativo:
- Focal Point contornado:
- Facção vence parcialmente:
- PCs falham com consequência:
```

Ao final de cada ato, deve estar claro **o que mudou**.

---

## 2. Módulo

Unidade intermediária, agrupando cenas relacionadas.

Modelo:

```markdown
## Módulo [Nome]

- Ato correspondente:
- Função:
- Local principal:
- Objetivo do módulo:
- Agentes envolvidos:
- Entrada padrão:
- Entradas alternativas:
- Saída padrão:
- Saídas alternativas:
- Focal Points associados:
- Consequências herdadas:
- Consequências geradas:
```

Quanto mais avançado o módulo, mais entradas e saídas alternativas ele deve possuir.

---

## 3. Cena

Unidade prática de jogo.

Modelo obrigatório:

```markdown
## Cena — [Título]

### Tipo de Cena

[Investigação / combate / exploração / negociação / sobrevivência / horror / perseguição / revelação / clímax / outro.]

### Local

### Gatilho de Entrada

### Agentes Presentes

### Objetivo Dramático

### Objetivo Prático

### Conflito

### Informações Reveláveis

- Revelação mínima:
- Revelação provável:
- Revelação profunda:
- Revelação opcional:

### Desafio Mecânico

- Regra sugerida:
- Perícias prováveis:
- Dificuldade:
- Complicações:

### Consequências

- Sucesso:
- Sucesso parcial:
- Falha:
- Falha crítica:
- Custo voluntário:

### Saídas Possíveis

- Saída padrão:
- Saída alternativa 1:
- Saída alternativa 2:

### Notas Condicionais

- Se os PCs fizeram X:
- Se os PCs falharam em Y:
- Se a facção Z foi alertada:
- Se determinado NPC morreu:
- Se os PCs possuem determinado objeto:
```

---

## 4. Evento

Evento é aquilo que acontece no mundo ficcional.

Modelo:

```markdown
### Evento — [Nome]

- Tipo:
- Causa:
- Gatilho:
- Agentes envolvidos:
- Cena associada:
- Consequência imediata:
- Consequência futura:
```

---

## 5. Focal Point

Focal Point é evento estrutural importante para a progressão da aventura.

Modelo:

```markdown
### Focal Point — [Nome]

- Função narrativa:
- Informação revelada:
- Forma esperada:
- Formas alternativas:
- Momento provável:
- O que muda se ocorrer:
- O que muda se for evitado:
- Como reinserir sem forçar railroading:
```

A IA deve preservar a **função** do Focal Point, não necessariamente sua forma exata.

---

## 6. Evento Espontâneo

Evento espontâneo nasce de decisões dos jogadores, improvisação do mestre, tabelas aleatórias ou resultados mecânicos.

Modelo:

```markdown
### Evento Espontâneo Possível — [Nome]

- Origem provável:
- Condição de ocorrência:
- Efeito imediato:
- Como o mestre pode usar:
- Como pode escalar:
- Como pode ser encerrado:
```

---

# VI. Regras Específicas para IA

A IA deve cumprir as seguintes regras:

1. Não começar por cenas completas sem antes definir a estrutura mínima.
    
2. Não tratar a aventura como roteiro fechado.
    
3. Separar sempre:
    
    - Ato;
        
    - Módulo;
        
    - Cena;
        
    - Evento;
        
    - Focal Point;
        
    - Evento Espontâneo.
        
4. Indicar claramente o que é:
    
    - fixo;
        
    - provável;
        
    - condicional;
        
    - emergente.
        
5. Não presumir motivações dos PCs antes de eles serem definidos.
    
6. Usar NPCs e facções como agentes principais na Fase 1.
    
7. Toda facção relevante deve ter:
    
    - objetivo;
        
    - recurso;
        
    - método;
        
    - padrão de ação;
        
    - reação provável.
        
8. Todo Focal Point deve ter função narrativa explícita.
    
9. Toda cena avançada deve conter entradas e saídas alternativas.
    
10. Toda revelação importante deve ter:
    

- momento;
    
- forma;
    
- consequência.
    

11. Toda ameaça deve gerar decisão, não apenas obstáculo.
    
12. Todo elemento de cenário deve ter função jogável.
    
13. Toda mecânica sugerida deve servir ao ritmo da aventura.
    
14. Horror deve alterar percepção, risco e decisão, não apenas inserir monstros.
    
15. Sandbox exige pressão temporal, ambiental ou reativa.
    
16. McGuffins devem mudar o estado da aventura a cada parte recuperada.
    
17. Facções rivais devem agir fora da tela.
    
18. Ao final de cada ato, indicar:
    

- o que foi revelado;
    
- o que mudou;
    
- quem ganhou;
    
- quem perdeu;
    
- qual nova pressão surgiu.
    

---

# VII. Fases de Trabalho

## Fase 1 — Desenvolvimento sem PCs definidos

Usar quando os personagens jogadores ainda não foram apresentados.

A IA deve:

- trabalhar com NPCs e facções;
    
- mapear conflito;
    
- definir locais;
    
- estruturar atos;
    
- criar Focal Points;
    
- propor ganchos genéricos;
    
- evitar presumir desejos pessoais dos PCs.
    

Saída esperada:

```markdown
- 5W + HOW;
- agentes ativos;
- estrutura de atos;
- Focal Points;
- módulos prováveis;
- riscos e pressões.
```

---

## Fase 2 — Reprocessamento com PCs definidos

Usar quando os PCs forem apresentados.

A IA deve revisar:

- ganchos pessoais;
    
- conexões com NPCs;
    
- dilemas individuais;
    
- recompensas significativas;
    
- riscos emocionais;
    
- prováveis escolhas;
    
- cenas de introdução.
    

Saída esperada:

```markdown
- leitura preditiva da aventura;
- adaptação de ganchos;
- cenas personalizadas;
- riscos específicos;
- antagonismos direcionados.
```

---

## Fase 3 — Desenvolvimento de Atos

A IA deve criar cada ato conforme o modelo:

```markdown
1. Sinopse narrativa;
2. Função narrativa;
3. Possível desenrolar;
4. Cenas-chave;
5. Alternativas possíveis.
```

---

## Fase 4 — Desenvolvimento de Módulos

A IA deve transformar atos em módulos jogáveis.

Cada módulo deve indicar:

- objetivo;
    
- entrada;
    
- saída;
    
- cenas internas;
    
- agentes;
    
- Focal Points;
    
- consequências.
    

---

## Fase 5 — Desenvolvimento de Cenas

A IA deve transformar módulos em cenas completas.

Cada cena deve seguir o modelo obrigatório de cena.

---

## Fase 6 — Conversão Mecânica

A IA deve revisar as cenas e definir como serão jogadas.

Para SWADE, deve indicar:

- perícias;
    
- dificuldades;
    
- testes;
    
- Dramatic Tasks;
    
- Quick Encounters;
    
- Chases;
    
- Fear Checks;
    
- Hazards;
    
- inimigos;
    
- consequências mecânicas.
    

---

## Fase 7 — Revisão de Consistência

Antes de consolidar a aventura, a IA deve revisar:

- coerência dos agentes;
    
- coerência das facções;
    
- progressão de mistério;
    
- uso dos Focal Points;
    
- liberdade real dos jogadores;
    
- consequências;
    
- ritmo;
    
- integração com sistema;
    
- função jogável dos elementos de cenário.
    

---

# VIII. Padrão de Resposta Esperado da IA

Ao desenvolver qualquer parte da aventura, a IA deve usar Markdown claro.

A IA deve preferir:

- títulos objetivos;
    
- seções bem delimitadas;
    
- parágrafos desenvolvidos quando estiver escrevendo sinopse;
    
- listas quando estiver organizando estrutura operacional;
    
- tabelas apenas quando ajudarem na comparação;
    
- separação entre narrativa, análise e mecânica.
    

A IA deve evitar:

- frases de efeito vazias;
    
- one-liners;
    
- excesso de lore sem função;
    
- cenas sem consequência;
    
- ameaças sem decisão;
    
- revelações sem impacto;
    
- mecânicas decorativas;
    
- railroading disfarçado.
    

---

# IX. Aplicação em Outsiders — Lost Frontier

Em aventuras deste cenário, a IA deve cumprir diretrizes adicionais:

1. Todo elemento importante deve se conectar à Teleritha, ao Véu Rasgado, à crise energética, às facções ou à sobrevivência colonial.
    
2. Toda tecnologia avançada deve seguir o princípio de Clarke: aparência de maravilha, base material.
    
3. Nenhuma descoberta deve ser apenas informativa. Ela deve gerar conflito, custo ou decisão.
    
4. Facções devem agir por interesses materiais, políticos, econômicos, ontológicos ou estratégicos.
    
5. O ambiente deve funcionar como agente ativo.
    
6. Horror cósmico deve emergir de instabilidade dimensional, Aethera, tecnologia incompreendida ou contato com realidades incompatíveis.
    
7. McGuffins devem revelar camadas progressivas do cenário.
    
8. A escassez energética deve permanecer como pressão estrutural.
    
9. Povos e espécies não devem ser reduzidos a clichês simples.
    
10. A aventura deve priorizar jogabilidade sobre exposição de cenário.
    

---

# X. Comando de Uso Recomendado

Quando o usuário disser:

> Desenvolva o ato da aventura a partir das “Diretrizes de Desenvolvimento de Aventura de RPG.md”.

A IA deve responder usando esta ordem:

```markdown
# Ato [Número] — [Título]

## 1. Sinopse narrativa

## 2. Função narrativa do ato

## 3. Possível desenrolar da ação

## 4. Cenas-chave

## 5. Alternativas possíveis

## 6. Estado final esperado do ato
```

Quando o usuário disser:

> Desenvolva uma cena a partir das “Diretrizes de Desenvolvimento de Aventura de RPG.md”.

A IA deve responder usando esta ordem:

```markdown
## Cena — [Título]

### Tipo de Cena
### Local
### Gatilho de Entrada
### Agentes Presentes
### Objetivo Dramático
### Objetivo Prático
### Conflito
### Informações Reveláveis
### Desafio Mecânico
### Consequências
### Saídas Possíveis
### Notas Condicionais
```

---

# XI. Regra Final

Antes de consolidar qualquer conteúdo de aventura, a IA deve verificar:

> Quem age?  
> O que está em disputa?  
> Onde isso ocorre?  
> Quando a pressão muda?  
> Por que importa?  
> Como isso será jogado?

Se qualquer resposta estiver fraca, a aventura ainda precisa ser desenvolvida.