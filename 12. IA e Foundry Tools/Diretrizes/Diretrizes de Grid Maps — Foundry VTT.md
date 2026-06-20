# Diretrizes de Grid Maps — Foundry VTT
## Projeto: Outsiders — Lost Frontier

## 1. Função

Este documento define o padrão visual, técnico e funcional para geração de mapas de cena destinados ao Foundry VTT.

Os mapas devem servir como espaços jogáveis para exploração, combate, investigação, horror, perseguição e interação ambiental.

## 2. Especificação técnica obrigatória

- Resolução: 2000 × 1500 px.
- Proporção: 4:3.
- Orientação: horizontal.
- Perspectiva: top-down.
- Grid: não desenhar grid.
- Estilo: comic book art simplificado.
- Realismo: baixo a médio.
- Legibilidade tática: alta.

## 3. Estilo visual

Os mapas devem usar traço claro, cores estilizadas e sombreamento simples.

Referências aceitáveis:

- battlemap top-down;
- comic book art;
- lineart com pintura simples;
- deserto rochoso estilizado;
- ruínas tecnológicas;
- sucata sci-fi;
- cavernas orgânicas;
- instalações modulares.

Evitar:

- fotorrealismo;
- render 3D;
- mapas com grid embutido;
- excesso de textura;
- perspectiva isométrica;
- enquadramento cinematográfico;
- ilustração sem função tática.

## 4. Coerência com o cenário

Todo mapa deve se conectar visualmente ao mundo de Tanelohr.

Elementos recorrentes:

- Teleritha;
- sucata tecnológica;
- sinais de escassez;
- estruturas reaproveitadas;
- fendas dimensionais;
- areia vitrificada;
- ruínas arkannonas;
- fungos energéticos;
- fragmentos de casco;
- instabilidade ambiental.

## 5. Função jogável

Cada mapa deve indicar claramente:

- áreas transitáveis;
- obstáculos;
- cobertura;
- entradas;
- saídas;
- pontos de interesse;
- perigos ambientais;
- zonas de investigação;
- possíveis rotas alternativas.

## 6. Composição tática mínima

Cada mapa deve conter, sempre que possível:

- 2 ou mais rotas de circulação;
- 1 gargalo tático;
- 2 ou mais coberturas;
- 1 área aberta perigosa;
- 1 elemento interativo central;
- 1 elemento ambiental que possa mudar a cena.

## 7. Padrões por região

### Rust Hollow

- ravinas;
- oficinas;
- currais;
- sucata;
- ferrugem;
- passarelas;
- fragmentos de satélite;
- trilhas de Bondaks.

### Campo das Estrelas Cadentes

- crateras;
- destroços;
- areia metálica;
- quedas recentes;
- fendas;
- áreas de instabilidade;
- peças tecnológicas desconhecidas.

### Mar de Areia

- dunas compactas;
- areia fluida;
- ossadas vitrificadas;
- carcaças de criaturas;
- plataformas;
- barcas;
- sumidouros.

### Nexo Umbra

- laboratórios;
- passadiços;
- zonas de contenção;
- geometrias instáveis;
- microfendas;
- sombras anômalas;
- módulos isoláveis.

### Veyridia

- plataformas de montanha;
- cabos;
- trilhos;
- cristais;
- estruturas vibracionais;
- arquitetura industrial vertical.

### Krom’Vathra

- cavernas;
- micélio;
- câmaras orgânicas;
- biotecnologia;
- osso;
- quitina;
- umidade;
- estruturas vivas.

## 8. Prompt-base recomendado

Gerar um mapa de cena para Foundry VTT, resolução 2000x1500, proporção 4:3, visão top-down, sem grid desenhado, estilo comic book art simples, traço limpo, cores estilizadas, sombreamento simples, alta legibilidade tática. O mapa deve mostrar [LOCAL/CENA], com áreas transitáveis claras, obstáculos, cobertura, entradas e saídas, pontos de interesse interativos e coerência visual com o cenário sci-fi de fronteira de Tanelohr. Não usar fotorrealismo, não usar perspectiva isométrica, não desenhar grid.

## 9. Prompt negativo padrão

grid lines, visible grid, square grid, hex grid, isometric view, perspective view, cinematic angle, photorealistic, realistic render, 3D render, excessive texture, cluttered details, unreadable terrain, blurry, low contrast, text labels, UI elements, tokens, characters, miniatures.