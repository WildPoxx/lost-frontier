
# [Task] : ESPECIFICAÇÃO : ancestralidade modular : Foundry/SWADE : Danahimm

## Objetivo

Criar a implementação modular da ancestralidade Danahimm para o módulo nativo de **Outsiders — Lost Frontier**, compatível com:

- Foundry VTT v13
    
- SWADE 5.2.6
    
- estrutura modular baseada em compêndios
    
- integração futura com Sincrisálise e Teleritha
    

A implementação deve priorizar:

- modularidade;
    
- clareza;
    
- compatibilidade com SWADE;
    
- expansão futura;
    
- baixa automação inicial;
    
- fácil manutenção.
    

Base conceitual e estrutural definida em:  
  
  
  

---

# 1. Estrutura Foundry Recomendada

A ancestralidade Danahimm NÃO deve ser um único bloco monolítico.

Ela deve ser dividida em:

|Elemento|Tipo Foundry|Função|
|---|---|---|
|Danahimm|Ancestry / Item|Estrutura racial principal|
|Passo Limiar|Ability ou Power custom|Teleporte racial|
|Afinidade com Aethera|Ability|Interação energética|
|Palavra Vinculante|Ability/Hindrance híbrida|Fraqueza racial|
|Longevidade Danahimm|Ability passiva|Lore + efeitos narrativos|
|Outsider|Hindrance padrão|Aplicação automática/manual|
|Sensibilidade ao Calor|Ability negativa|Penalidade ambiental|

---

# 2. Filosofia de Implementação

## NÃO transformar em “raça mágica genérica”

Os Danahimm:

- não são elfos;
    
- não usam magia arbitrária;
    
- não possuem spellcasting clássico.
    

Toda habilidade deve ser tratada como:

```text
Fenômeno biotecnológico liminar
+
Sincronização vibracional residual
+
Afinidade com Aethera
```

---

# 3. Modelo Mecânico Central

## Núcleo da ancestralidade

### Benefícios

|Benefício|Tipo|
|---|---|
|+1 Smarts|Trait bonus|
|+1 Spirit|Trait bonus|
|Visão Crepuscular|Ability passiva|
|Passo Limiar|Power racial|
|Afinidade com Aethera|Ability passiva|

---

## Fraquezas

|Fraqueza|Tipo|
|---|---|
|Outsider (Minor)|Hindrance|
|Sensibilidade ao Calor|Ability negativa|
|Palavra Vinculante|Ability narrativa/mecânica|

---

# 4. Implementação de Passo Limiar

## Tipo recomendado

```text
Power customizado
```

OU:

```text
Ability que concede versão limitada de Teleport
```

O segundo modelo é mais compatível com SWADE.

---

# 5. Estrutura Mecânica de Passo Limiar

## Base

Inspirado em:

- Teleport (SWADE)
    
- Blink/Misty Step
    
- curta translocação tática
    

---

## Regras

|Elemento|Valor|
|---|---|
|Tipo de ação|Action|
|Custo|2 PP|
|Distância|6”|
|Linha de visão|Obrigatória|
|Transporte de aliados|Não|
|Ignora ataques de oportunidade|Sim|
|Atravessa paredes?|Não normalmente|
|Shorting|Permitido|
|Falha crítica|Risco liminar|

---

# 6. Implementação Técnica Recomendada

## Item separado

Criar:

```text
Ability/Power:
Passo Limiar
```

E a ancestralidade:

- concede;
    
- referencia;
    
- ou instrui adicionar.
    

NÃO embutir tudo na Ancestry.

---

# 7. Power Points Raciais

## Modelo aprovado

Danahimm possuem:

```text
5 PP raciais
```

Esses PP:

- NÃO são Arcane Background;
    
- NÃO exigem Edge arcana;
    
- NÃO representam magia tradicional.
    

Eles são:

```text
Reserva vibracional biológica residual
```

---

# 8. Regras de Recuperação

## Recuperação padrão

- descanso normal SWADE
    

## Recuperação acelerada

Aethera refinada:

- restaura PP;
    
- pode sobrecarregar;
    
- pode gerar eventos liminares.
    

Isso deve ficar preparado para futura integração com:

```text
Sistema de Teleritha
```

---

# 9. Afinidade com Aethera

## Tipo

```text
Ability passiva
```

---

## Funções

### Deve permitir:

- recarga de PP via Aethera;
    
- interação com tecnologia Danahimm;
    
- identificação de fenômenos Aethera.
    

### NÃO deve conceder:

- detecção universal;
    
- leitura mental;
    
- awareness constante;
    
- supersensores mágicos.
    

---

# 10. Palavra Vinculante

Essa é uma das partes mais importantes da ancestralidade.

## Tipo recomendado

```text
Special Ability narrativa
```

e NÃO Hindrance padrão.

Porque:

- ela depende de interpretação;
    
- possui escala variável;
    
- funciona como regra social;
    
- e tem forte peso narrativo.
    

---

# 11. Mecânica Recomendada

Quebrar juramentos formais pode causar:

|Consequência|
|---|
|Fatigue|
|Wounds|
|degradação vibracional|
|doença|
|instabilidade liminar|

Implementação:

- inicialmente textual;
    
- automação futura opcional.
    

---

# 12. Sensibilidade ao Calor

## Tipo

Ability negativa.

---

## Efeito

```text
-2 para resistir Fatigue causada por calor extremo
```

Implementação simples.

---

# 13. Longevidade Danahimm

## NÃO criar regra pesada

SWADE praticamente não recompensa mecanizar idade extrema.

Então:

## recomendado

```text
Ability passiva narrativa
```

Exemplo:

```text
Danahimm envelhecem extremamente devagar, podendo viver séculos ou milênios.
```

Sem efeito mecânico direto por enquanto.

---

# 14. Estrutura Recomendada no Foundry

## Compêndio

```text
OLF — Ancestralidades
```

---

## Itens separados

|Item|Tipo|
|---|---|
|Danahimm|Ancestry|
|Passo Limiar|Ability/Power|
|Afinidade com Aethera|Ability|
|Palavra Vinculante|Ability|
|Sensibilidade ao Calor|Ability negativa|
|Longevidade Danahimm|Ability|

---

# 15. NÃO Automatizar Agora

Evitar:

- hooks;
    
- teleporte automático;
    
- controle automático de juramentos;
    
- recuperação automática de PP;
    
- rastreamento de Aethera.
    

Primeiro:

- consolidar mecânica;
    
- testar em mesa;
    
- validar equilíbrio.
    

---

# 16. Objetivo Imediato

O outro chat deve produzir:

## Fase 1

- estrutura Ancestry;
    
- items individuais;
    
- grants simples;
    
- compatibilidade SWADE.
    

## Fase 2

- testes em Foundry;
    
- arrastar ancestralidade para ficha;
    
- verificar grants;
    
- verificar PP raciais.
    

## Fase 3

- integração com sistema Teleritha.
    

---

# 17. Objetivo Final

Quando concluído:

- Yellora poderá ser criada corretamente;
    
- Danahimm virarão ancestrais jogáveis reais;
    
- Passo Limiar será funcional;
    
- Aethera poderá alimentar PP;
    
- Sincrisálise terá infraestrutura modular;
    
- e Lost Frontier começará a deixar de ser apenas cenário para virar sistema jogável integrado.
    

E honestamente?

Esse é o ponto em que o projeto começa a ganhar ossos.