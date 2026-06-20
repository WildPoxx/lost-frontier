# Diretrizes de Atualizacao de Relogios — Rust under the Stars

## 1. Proposito

Este documento define o protocolo operacional para atualizar, apos cada sessao ou evento relevante, a pagina **8. Atualizacao Pos-Sessao** da Journal Entry:

`Rust under the Stars: 02. Elenco, Faccões e Relogios`

O objetivo e evitar edicao manual em HTML dentro do Foundry VTT.  
O usuario informa os acontecimentos em linguagem natural ou em formato estruturado, e a IA deve devolver o bloco HTML atualizado pronto para colar na pagina correspondente.

---

## 2. Principio Central

A pagina **8. Atualizacao Pos-Sessao** nao deve ser tratada como texto estatico.

Ela e um **painel de estado vivo** do Modulo 1.

Sempre que o usuario solicitar:

> “Gere as atualizacoes correspondentes ao seguinte conteudo com base no protocolo de atualizacao de relogios”

A IA deve:

1. identificar os eventos relevantes;
2. atualizar relogios de pressao;
3. atualizar niveis de informacao;
4. atualizar controle dos objetos centrais;
5. registrar mudancas de NPCs e faccoes;
6. gerar um novo bloco HTML completo da pagina **8. Atualizacao Pos-Sessao**;
7. preservar a estrutura visual compativel com Journal Text Page do Foundry VTT.

---

## 3. Escopo da Atualizacao

O protocolo afeta prioritariamente:

- **Journal Entry:** `02. Elenco, Faccões e Relogios`
- **Page:** `8. Atualizacao Pos-Sessao`

Pode afetar secundariamente, se o usuario pedir:

- `6. Relogios de Pressao`
- `7. Niveis de Informacao`
- paginas dos atos especificos;
- paginas de cenas;
- handouts;
- notas de preparacao do mestre.

Por padrao, entretanto, a IA deve atualizar **somente a pagina 8**, salvo ordem expressa em contrario.

---

## 4. Relogios Oficiais do Modulo 1

Os relogios de pressao ativos sao:

| Relogio | Escala | Mede | Consequencia em 6 |
|---|---:|---|---|
| Corrida pelo SWIX | 0-6 | Quanto a descoberta virou disputa aberta. | Faccoes externas tratam o SWIX como ativo estrategico. |
| Shizuka | 0-6 | Quanto Shizuka sabe e quao perto esta de agir diretamente. | Ela tenta capturar a expedicao, Floyd/Dentinho ou dados tecnicos. |
| Raast vs Synthas | 0-6 | Tensao entre soberania civil e controle tecnico da Companhia. | Crise institucional sobre a expedicao. |
| Floyd | 0-6 | Exposicao de Floyd e Dentinho como pecas centrais do rastro. | Floyd e sequestrado, isolado ou colocado sob custodia. |
| Abutres de Aco | 0-6 | Envolvimento criminal local no SWIX, Chave e dados. | Abutres tentam vender, roubar ou capturar informacao em campo. |

---

## 5. Niveis de Informacao Oficiais

A pagina 8 deve registrar tres eixos:

| Eixo | Escala | Funcao |
|---|---:|---|
| PCs — SWIX | 1-10 | O que os personagens sabem sobre o SWIX, Starwalker-IX e os fragmentos principais. |
| PCs — Floyd/Dentinho | 1-8 | O que os personagens sabem sobre Floyd, Dentinho, Arreio de Rastro e Segunda Trilha. |
| Shizuka | 0-6 | O que Shizuka sabe e como isso altera sua postura. |

---

## 6. Objetos Centrais a Monitorar

A pagina 8 deve sempre rastrear:

| Objeto | Estados possiveis |
|---|---|
| SWIX | intacto, danificado, travado, analisado, perdido, sob custodia, transportado |
| Chave de Rastro | inexistente, criada, intacta, danificada, perdida, copiada, recuperada |
| Arreio de Rastro | disponivel, lacrado, danificado, roubado, sob custodia, liberado com condicoes |
| Dentinho | livre, com Floyd, com Companhia, em disputa, capturado, ferido, exausto |
| Dados tecnicos | seguros, vazados, parciais, corrompidos, copiados, destruidos, criptografados |
| Floyd | livre, exposto, protegido, ameacado, sob custodia, sequestrado, ferido |

---

## 7. Formato de Entrada do Usuario

O usuario pode fornecer informacoes em linguagem natural ou no formulario abaixo.

### Formato recomendado

```markdown
# Atualizacao de Sessao — Rust under the Stars

## Identificacao
- Sessao no:
- Ato atual:
- Cena final da sessao:

## Eventos principais
-

## Decisoes relevantes dos PCs
-

## Informacoes descobertas pelos PCs
-

## Informacoes que vazaram
-

## Acoes de NPCs ou faccoes
-

## Estado dos objetos
- SWIX:
- Chave de Rastro:
- Arreio de Rastro:
- Dentinho:
- Floyd:
- Dados tecnicos:

## Resultado mecanico relevante
- Dramatic Tasks:
- Chases:
- Social Conflicts:
- Combates:
- Falhas criticas:
- Raises importantes:

## Pedido especifico
- Atualizar apenas a pagina 8.
- Atualizar pagina 8 e sugerir ajustes nos relogios.
- Atualizar pagina 8 e gerar consequencias para proxima sessao.
```

---

## 8. Regras de Interpretacao

Ao receber o relato do usuario, a IA deve aplicar os seguintes criterios.

### 8.1. Avanco de Relogios

Um relogio deve avancar quando houver:

- exposicao publica;
- vazamento de informacao;
- falha critica;
- acao de faccao;
- perda de objeto central;
- demora relevante;
- captura, ameaca ou isolamento de NPC;
- escalada politica;
- escalada criminal;
- interferencia tecnica com Aethera ou SWIX.

### 8.2. Nao avancar relogio automaticamente

A IA nao deve avancar relogio apenas porque uma cena foi dramatica.

Avanco exige causa concreta.

### 8.3. Avanco multiplo

Um mesmo evento pode avancar mais de um relogio.

Exemplo:

- Nikko rouba a Chave e foge para territorio dos Abutres:
  - Corrida pelo SWIX +1
  - Shizuka +1 ou +2
  - Abutres de Aco +1
  - Floyd +1 se Dentinho/Floyd foram identificados como parte do metodo

### 8.4. Limite de avanco

Por padrao:

- evento menor: +1 em um relogio;
- evento importante: +1 em dois ou tres relogios;
- falha critica ou virada de ato: +2 em um relogio principal;
- consequencia extrema: relogio pode ir direto para 6, mas apenas se isso for claramente justificado.

---

## 9. Tabela de Gatilhos Rapidos

| Evento | Relogios provaveis |
|---|---|
| Rumor publico sobre Aethera | Corrida pelo SWIX +1; Shizuka +1 |
| SWIX falha ou pulsa em publico | Corrida pelo SWIX +1 |
| PCs revelam que ha fragmentos | Corrida pelo SWIX +1; Shizuka +1 se ela puder saber |
| Chave de Rastro e criada | Corrida pelo SWIX +1 |
| Chave e roubada | Corrida pelo SWIX +1; Abutres +1; Shizuka +1 |
| Nikko escapa com dados | Shizuka +1 ou +2; Abutres +1 |
| Nikko e capturado vivo | Abutres +1; Shizuka pode estagnar ou acelerar |
| Floyd e citado publicamente como essencial | Floyd +1 |
| Dentinho reage ao SWIX diante de terceiros | Floyd +1; Shizuka +1 se observavel |
| Synthas lacra recursos | Raast vs Synthas +1 |
| Raast exige autorizacao formal | Raast vs Synthas +1 |
| PCs contornam Companhia clandestinamente | Raast vs Synthas +1; Corrida pelo SWIX +1 se descoberto |
| Lorna e envenenada | Corrida pelo SWIX +1; Shizuka +1; Raast vs Synthas +1 |
| Shizuka e confrontada e foge | Shizuka +1; Corrida pelo SWIX +1 |
| Haikyo morre | Shizuka +1 ou +2; proxima reacao deve ser pessoal e estrategica |
| Abutres sequestram Floyd | Floyd chega a 6; Abutres +1; Shizuka +1 se envolvida |
| Expedicao parte sem legitimidade | Raast vs Synthas +1 ou +2 |
| Expedicao parte com coalizao formal | Raast vs Synthas pode reduzir ou estabilizar |

---

## 10. Saida Obrigatoria da IA

A resposta da IA deve conter:

1. **Diagnostico curto**
   - O que mudou.
   - Quais relogios avancaram.
   - Quais niveis de informacao mudaram.
   - Quais objetos mudaram de estado.

2. **Justificativa**
   - Explicar cada avanco em 1 frase curta.

3. **Bloco HTML completo**
   - Pronto para substituir todo o conteudo da pagina **8. Atualizacao Pos-Sessao**.

4. **Proxima pressao natural**
   - Uma ou mais aberturas possiveis para a proxima sessao.

---

## 11. Modelo de Resposta Esperado da IA

```markdown
# [Task] : ATUALIZACAO : relogios : pos-sessao : Rust under the Stars

## Diagnostico

- Corrida pelo SWIX: 2 -> 3
- Shizuka: 1 -> 3
- Abutres de Aco: 1 -> 2
- PCs — SWIX: 5 -> 6
- Chave de Rastro: criada, roubada, recuperada danificada

## Justificativa

A Chave foi criada e exposta; Nikko escapou tempo suficiente para transmitir dados parciais; os PCs descobriram a existencia provavel do Energy Core.

## HTML para substituir a pagina 8

```html
[HTML completo aqui]
```

## Proxima pressao natural

Abrir a proxima sessao com Synthas lacrando o Arreio de Rastro e Raast exigindo que a expedicao seja formalmente autorizada.
```

---

## 12. Padrao HTML da Pagina 8

A IA deve preservar a estrutura abaixo, ajustando o conteudo conforme o estado atualizado.

```html
<p>Use esta pagina ao final de cada sessao. Nao confie na memoria. Este modulo depende de consequencia acumulada.</p>

<hr>

<h2>Registro Rapido</h2>

<table>
  <thead>
    <tr>
      <th>Pergunta</th>
      <th>Resposta</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Sessao no</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>Ato atual</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>Cena final da sessao</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>Ultima decisao relevante dos PCs</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>Informacao nova descoberta pelos PCs</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>Informacao que vazou</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>NPC que mudou de atitude</td>
      <td>[preencher]</td>
    </tr>
    <tr>
      <td>Faccao que ganhou vantagem</td>
      <td>[preencher]</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Relogios ao Final da Sessao</h2>

<table>
  <thead>
    <tr>
      <th>Relogio</th>
      <th>Antes</th>
      <th>Depois</th>
      <th>Motivo do Avanco</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Corrida pelo SWIX</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[motivo]</td>
    </tr>
    <tr>
      <td>Shizuka</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[motivo]</td>
    </tr>
    <tr>
      <td>Raast vs Synthas</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[motivo]</td>
    </tr>
    <tr>
      <td>Floyd</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[motivo]</td>
    </tr>
    <tr>
      <td>Abutres de Aco</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[motivo]</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Niveis de Informacao</h2>

<table>
  <thead>
    <tr>
      <th>Eixo</th>
      <th>Nivel Antes</th>
      <th>Nivel Depois</th>
      <th>Como Foi Obtido</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>PCs — SWIX</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[como]</td>
    </tr>
    <tr>
      <td>PCs — Floyd/Dentinho</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[como]</td>
    </tr>
    <tr>
      <td>Shizuka</td>
      <td>[antes]</td>
      <td>[depois]</td>
      <td>[como]</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Estado dos Objetos</h2>

<table>
  <thead>
    <tr>
      <th>Objeto</th>
      <th>Estado Atual</th>
      <th>Quem Controla?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>SWIX</td>
      <td>[estado]</td>
      <td>[controle]</td>
    </tr>
    <tr>
      <td>Chave de Rastro</td>
      <td>[estado]</td>
      <td>[controle]</td>
    </tr>
    <tr>
      <td>Arreio de Rastro</td>
      <td>[estado]</td>
      <td>[controle]</td>
    </tr>
    <tr>
      <td>Dentinho</td>
      <td>[estado]</td>
      <td>[controle]</td>
    </tr>
    <tr>
      <td>Floyd</td>
      <td>[estado]</td>
      <td>[controle]</td>
    </tr>
    <tr>
      <td>Dados tecnicos</td>
      <td>[estado]</td>
      <td>[controle]</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Proxima Pressao Natural</h2>

<ul>
  <li>[pressao 1]</li>
  <li>[pressao 2]</li>
  <li>[pressao 3]</li>
</ul>
```

---

## 13. Comando Curto para o Usuario

O usuario pode acionar este protocolo com o seguinte comando:

```markdown
[Task] : ATUALIZACAO : relogios : pos-sessao : Rust under the Stars

Use o documento “Diretrizes de Atualizacao de Relogios — Rust under the Stars”.

Atualize a pagina 8 de `02. Elenco, Faccões e Relogios` com base nos eventos abaixo:

[relato da sessao ou evento]
```

---

## 14. Regra Final

A IA deve sempre devolver HTML pronto para colar no Foundry, sem exigir que o usuario edite manualmente tabelas, tags ou estrutura.

O usuario informa ficcao, consequencia e estado de mesa.

A IA converte isso em painel operacional.
