# MUTAGEN:ZERO — Bestiário

> **O que este documento é.** O catálogo de adversários de MUTAGEN:ZERO e as regras que só se
> aplicam a criaturas. Ele é, antes de tudo, **o alvo que faltava**: até a Aprovação 025, todo número
> de balanceamento deste projeto — os DPR das ~76 armas, as rodadas por luta, os pontos de Horda e de
> Infecção, as curvas das oito classes — foi medido contra um *"zumbi comum hipotético"* que nunca
> tinha sido aprovado. Este documento o torna real.

> **Regras relacionadas:** tipos de dano e a escala de resistência em `docs/gdd/GDD_Combate.md` §6.3 ·
> categorias de **tamanho** em `docs/gdd/GDD_Combate.md` §14 · a Atração e o uivo em `docs/gdd/GDD_Ruido.md`
> §2 e §6 · a leva em `docs/gdd/GDD_Horda.md` §3 · o acúmulo da Trilha em `docs/gdd/GDD_Infeccao.md` §1.

> **Aprovação 025.** Todo o conteúdo deste documento é canônico salvo onde o campo diz
> `[A CALIBRAR]`. Implementadores **não inventam valor padrão no motor**.

---

## 1. A régua — e por que ela não mudou

**Zumbi comum: Defesa 14, HP 12.** Os dois valores estavam marcados `[A CALIBRAR]` em
`docs/gdd/GDD_Armas.md` §1.2 desde a primeira aprovação de armamento, com a observação *"zumbi comum
hipotético"*.

**A Aprovação 025 os ratifica como canon**, e a razão é de engenharia, não de gosto: toda a tabela de
armas, as simulações de 200.000 tiradas, o ritmo do Medidor de Horda e as curvas de progressão das
oito classes estão calibrados contra eles. Mudá-los não corrigiria um defeito — não há defeito
apontado —, apenas invalidaria tudo o que já foi medido.

**A consequência é que a régua inverte a lógica do Bestiário.** O Zumbi comum não é "mais uma
criatura": ele é a **unidade de medida**, e toda outra criatura se define por comparação com ele.
Quando este documento diz que o Zumbi Resistente tem Defesa 16, o que isso significa é *"dois pontos
mais difícil de acertar que a régua"*.

---

## 2. ND — Nível de Desafio

Cada criatura carrega um **ND de 0 a 5**.

> ### Por que não "CD"
>
> A proposta original usava `CD`. **`CD` já significa Classe de Dificuldade** em 27 lugares do canon,
> incluindo uma fórmula viva: *"CD de Infecção = 10 + pontos ganhos naquele combate"*
> (`docs/gdd/GDD_Infeccao.md` §2). Na mesa, *"um Zumbi de Sangue CD 3"* e *"teste de AGI CD 13"* na mesma
> frase é confusão garantida.
>
> **`ND` foi adotado na Aprovação 025** — é o termo padrão em português para o *Challenge Rating*, e
> não colidia com nada. Esta é a **sétima colisão do projeto que foi evitada antes de acontecer**, em
> vez de documentada depois; ver `docs/gdd/GDD_Glossario.md` §2.

| ND | Leitura de mesa |
|---|---|
| **0** | Carne. Sozinho não é ameaça; **em número, é a ameaça** |
| **1** | Um problema por jogador |
| **2** | Exige foco do grupo |
| **3** | Muda a tática da cena |
| **4** | Encontro inteiro sozinho |
| **5** | Cena de clímax |

### 2.1 A que nível de grupo cada ND pertence (Aprovação 030)

Até a Aprovação 030 o ND não tinha âncora no nível dos personagens. A matriz de dificuldade do §4.6
deu uma, medida:

| ND | Conteúdo de | Leitura |
|---|---|---|
| **0 a 2** | **Patamar 1** — níveis 1 a 4 | Moderado a difícil para quem começa; fácil a partir do patamar 2 |
| **3 a 4** | **Patamar 2** — níveis 5 a 8 | Difícil no patamar 1, moderado no patamar 2 |
| **5** | **Patamar 3** — níveis 9 a 12 | Mortal nos patamares 1 e 2, difícil no 3, moderado nos 4 e 5 |
| **6 em diante** | **Patamares 4 e 5** — níveis 13 a 20 | **Ainda não existe.** Bloco 5 |

> **O Bestiário atual termina no patamar 3.** Para grupos de nível 13 a 20, **nenhuma das 18 criaturas é
> mortal sozinha** — só empilhando Gigantes. A escala de ND continua acima de 5, e as criaturas que a
> ocupam são o próximo trabalho do Bestiário.

---

## 3. A regra de desenho — medida, não escolhida

> ### Criatura de ND alto ameaça a Trilha de Infecção por EFEITO, nunca por mais ataques.

Esta regra **não foi uma preferência de design**: ela saiu de uma simulação que contrariou a
expectativa. O mesmo orçamento de **80 HP**, distribuído de três formas, grupo de 4 personagens,
8.000 iterações por linha:

| Forma | Dano por personagem | **Infecção gerada** |
|---|---|---|
| **7 Zumbis** de 12 HP (ND 0) | 10,5 | **12,00** |
| 3 Mutantes de 28 HP (ND 2) | 10,1 | 6,38 |
| **1 Gigante** de 80 HP, 1 ação | 11,9 | **3,74** |

**O bando de ND 0 gera 3,2× mais Infecção que o chefe**, com HP e dano equivalentes. O limiar de
Infecção base é **15**: o bando chega perto de matar por mutação, o chefe não chega a um quarto do
caminho.

A causa é uma regra já aprovada: **a Trilha conta acertos, não dano** (`docs/gdd/GDD_Infeccao.md` §1).
Ameaça à Trilha é função do **número de ataques**, e um corpo só ataca uma vez.

A saída óbvia — dar mais ações ao chefe — foi testada e **não funciona**:

| Gigante de 80 HP | Dano por personagem | Infecção |
|---|---|---|
| 1 ação | 11,9 | 3,74 |
| 2 ações | 23,5 | 7,38 |
| **3 ações** | **31,5** | 9,89 |

Para igualar a Infecção de um bando, o chefe precisa de três ações — e então causa **três vezes o
dano**. Mata por HP muito antes de ameaçar por Trilha. **Os dois botões estão acoplados através do
número de ataques e não podem ser separados por ali.**

**Por isso as criaturas de ND 4 e 5 usam aura e cisão**: aura aplica Infecção **sem rolagem de
ataque**, e cisão converte o chefe em bando. São os dois únicos mecanismos que desacoplam ameaça à
Trilha de ameaça a HP.

> **Nota de coerência.** Esta regra é a mesma frase que governa as armas desde a primeira aprovação de
> armamento — *"o poder de tier alto vem de EFEITO, nunca de dado maior"* (`docs/gdd/GDD_Armas.md` §1.1).
> O sistema já pedia isso das criaturas; a simulação só tornou visível.

---

### 3.1 Armadura protege contra ataque, não contra efeito (Aprovação 030)

A escala de Defesa (`docs/gdd/GDD_Combate.md` §5.3) deixou o tanque real. Mas duas criaturas quase não se
importam com ele, e isso é medido, no patamar 1:

| Encontro | Sem armadura (Def 13) | Pesada + escudo (Def 20) |
|---|---|---|
| **8× Zumbi** | 55% do HP · 4,7 de Infecção | **25% · 2,1** |
| **2× Zumbi de Sangue** | 33% · 2,8 | **28% · 2,4** |

Contra o bando, o tanque corta a perda à metade. Contra o Zumbi de Sangue, quase nada muda: **a
explosão é teste de resistência, não rolagem de ataque**, e a Defesa não entra nela. O **miasma** do
Gigante também não rola.

> **O tanque tem inimigos naturais, e isso é desenho.** É o mesmo padrão do d20 clássico, em que uma
> CA alta não protege contra efeito que pede teste de resistência. Criatura de **efeito** é a
> resposta do Bestiário ao personagem de Defesa alta — e é por isso que o **Bloco 5** deve incluir
> criaturas de efeito em todos os patamares altos.

### 3.2 No fim do jogo, quem mata é a Trilha (Aprovação 030)

No patamar 5, dois Gigantes custam ao grupo só **21% do HP** — mas **6,5 pontos de Infecção por
personagem**, o que é mutação em cerca de três lutas. O motivo é estrutural:

| | Nível 1 | Nível 20 | Crescimento |
|---|---|---|---|
| **HP** (dado d8, CON +2) | 30 | 136 | **4,5×** |
| **Limiar de Infecção** | 18 | 22 | **1,2×** |

**Decisão do Diretor: fica assim.** É o canon desde a primeira aprovação de Infecção — *a letalidade
do MUTAGEN não está no HP, está na Trilha* — e é o gênero. O HP do personagem de nível alto o protege
da morte; nada o protege de virar o que ele combate. As criaturas de fim de jogo do Bloco 5 devem
**pressionar a Trilha de propósito**, como o Gigante já faz.

---

## 4. Orçamento de encontro — por patamar (Aprovações 027 e 030)

> **Histórico.** A Aprovação 027 mediu um orçamento contra um grupo de nível baixo **sem armadura**,
> com os ataques antigos. A escala de Defesa (Aprovação 029) mudou os dois lados, e a Aprovação 030
> remediu tudo: pontos, multiplicador e — o que é novo — **limiares por patamar**, no mesmo
> formato das tabelas de XP do d20 clássico. **O custo da criatura é fixo; o que cresce com o nível é
> quanto o grupo aguenta.**

### 4.1 O modelo

```
custo do encontro  =  Σ(pontos das criaturas)  ×  M(n)

M(1) = 1     M(2) = 1,5     M(n ≥ 3) = n − 1
```

O ponto base é *ameaça por rodada × rodadas que a criatura sobrevive ao foco do grupo* — **é aí que o
HP entra**. O multiplicador existe porque o grupo mata um alvo por vez: o total de ataques inimigos
numa luta de `n` corpos é `n + (n−1) + … + 1`, e **o risco escala com o triângulo de `n`, não com
`n`**.

> **Por que `n − 1` e não mais `3n/4`.** Com os ataques da curva nova o bando ficou mais íngreme, e o
> `3n/4` da Aprovação 027 passou a errar −14% com 10 criaturas. O ajuste aos dados é
> `0,72n + 0,015n²`, que na mesa vira simplesmente **`n − 1`** — erro de **±5% entre 2 e 10
> criaturas**. Acima disso ele superestima, mas acima disso o grupo já morreu (§4.5).

### 4.2 Tabela de pontos

Medidos contra o grupo de **patamar 1 equipado** (Defesa 15). As criaturas de **ND 3 em diante** foram
medidas contra o **patamar 2** — contra o patamar 1 elas **exterminam o grupo**, e quando o grupo morre o
custo para de crescer (o Gigante aparecia com 61 pontos por saturação) — e convertidas pela **ponte do
Mutante**, que não satura em nenhum dos dois.

| Criatura | ND | **Pontos** | Antes (027) |
|---|---|---|---|
| Zumbi · Cachorro Zumbi | 0 | **1** | 1 |
| Maratonista · Arrastador | 1 | **1** | 1 |
| Zumbi Cibernético | 1 | **1,5** | 1 |
| Zumbi Resistente | 1 | **2** | 1,5 |
| Saqueador Humano | 1 | **0,5** | 0,5 |
| Vigia | 1 | **0 sozinho · 2 acompanhado** | 0 |
| Cachorro Explosivo | 2 | **0,5** | 0,5 |
| Uivante | 2 | **3** | 1,5 |
| Touro Mecânico | 2 | **3,5** | 3,5 |
| **Mutante** | 2 | **6,5** | 4 |
| **Casulo** | 2 | **8** | 4 |
| Cuspidor | 4 | **3,5** | 2 |
| **Doutora Zumbi** | 3 | **5** | 1 |
| **Zumbi de Sangue** | 3 | **18** | 10 |
| **Zumbi Venenoso** | 4 | **30** | 27 |
| **Gigante Mutagênico** | 5 | **132** | 91 |

**Novas entradas — Bloco 5, Patamares 1–3 (Aprovação 035).** Sem coluna "Antes": não existiam antes
desta aprovação. Fichas completas em §20.

| Criatura | ND | Pontos |
|---|---|---|
| Rastejante | 0 | **1** |
| Enxame de Ratos Mutantes | 1 | **0,5** |
| Zumbi Guia | 1 | **1** *(acompanhado, §4.3)* |
| Zumbi Inchado | 1 | **2** |
| Fungo Ambulante | 2 | **7** |
| Zumbi Viscoso | 2 | **2,5** |
| Posto Automatizado | 3 | **4** |
| Parasita de Controle | 3 | **4** |
| Zumbi Corrosivo | 3 | **5** |
| Carcaça de Aço | 3 | **7** |
| Mutante Encouraçado | 4 | **9** |

**Novas entradas — Bloco 5, Patamares 4–5 (Aprovação 035).** ⚠ **Medidas em duas convenções
diferentes**, tratado como limitação aceita (§4.5) — não tratar os pontos abaixo como diretamente
comparáveis entre si, mesma família de imprecisão que o Touro/Mutante entre Patamares 1 e 2.

| Criatura | ND | Pontos |
|---|---|---|
| Devorador de Aço | 6 | **70** |
| Enxame de Morcegos Mutantes | 6 | **100** |
| Colmeia Ambulante | 6 | **120** |
| Sentinela Corporativa | 6–7 | **230** |
| Matriarca Mutagênica | 8 | **255** |
| Enxame-Rainha | 8 | **260** |
| Colosso de Sucata | 9 | **350** |
| Fonte Zero | 10 | **470** *(piso de faixa 470–600)* |
| Núcleo Mutagênico | 10 | **720** |

### 4.3 ND e pontos NÃO precisam concordar — e isto é canon

O Cuspidor é **ND 4** e custa **3,5**; o Zumbi de Sangue é **ND 3** e custa **18**. As duas escalas
continuam vivas e independentes:

- **ND é leitura de mesa** e âncora de nível (§2.1) — *que tipo de ameaça é isto, e para quem.*
- **Pontos são orçamento** — *quanto isto custa ao grupo em HP e Trilha.*

> ### Regra de suporte — agora só para o Vigia
>
> A Aprovação 027 dobrava o custo de criaturas de suporte acompanhadas, porque elas eram medidas
> sozinhas e valiam quase nada. A Aprovação 030 **mediu a Doutora Zumbi e o Uivante acompanhados de
> dois Zumbis** — os pontos da tabela já incluem as curas e o efeito, e **não se dobram mais**.
>
> A regra fica só para o **Vigia**: **0 pontos sozinho, 2 acompanhado.** O dano dele é ao Medidor de
> Horda, que o motor de simulação não mede.

### 4.4 Limiares por patamar

Grupo de **4 personagens, equipado para o patamar** (Defesa 15 · 17 · 19 · 20 · 21):

| Patamar do grupo | Fácil | **Moderado** a partir de | **Difícil** a partir de | **Mortal** a partir de | Acerto |
|---|---|---|---|---|---|
| **P1** — níveis 1 a 4 | até 16 | **17** | **21** | **39** | 87% |
| **P2** — níveis 5 a 8 | até 20 | **21** | **66** | **116** | 84% |
| **P3** — níveis 9 a 12 | até 53 | **54** | **108** | **180** | 83% |
| **P4** — níveis 13 a 16 | até 89 | **90** | **130** | **300** | — |
| **P5** — níveis 17 a 20 | até 89 | **90** | **180** | **300** · **Catastrófico a partir de 450** | — |

**Grupo maior ou menor:** escale os limiares na proporção (um quarto por personagem).

> **Catastrófico (Patamar 5, Aprovação 035) não é "mais mortal".** É uma categoria de leitura
> diferente: Colosso de Sucata (350), Fonte Zero (470+) e Núcleo Mutagênico (720) superam "mortal"
> sozinhos, e "mortal a partir de 300" não diferencia mais "luta dura" de "quase impossível sem
> retirada". **Uma criatura catastrófica não é desenhada para ser vencida em combate direto** — é
> set-piece de fuga, objetivo ambiental, ou relógio narrativo (a própria Fonte Zero mede "quanto
> tempo o grupo aguenta ficar perto", não "o grupo consegue vencer"). O Mestre que planeja um encontro
> catastrófico deveria sempre ter uma saída de cena construída — retirada, objetivo alternativo,
> interrupção do ritual — como parte do desenho do encontro, não como falha do grupo em "fazer dano o
> suficiente".

**Exemplo.** Grupo de patamar 2: **1 Mutante + 4 Zumbis** custa `(6,5 + 4) × M(5) = 10,5 × 4 = 42` →
**moderado**. Trocar o Mutante por um **Zumbi de Sangue** dá `(18 + 4) × 4 = 88` → **difícil**.

> **Os patamares 4 e 5 eram provisórios por faltar criatura na faixa — o Bloco 5 (§20.4–§20.5)
> preenche isso**, com ressalvas: para o Patamar 4, moderado e difícil se confirmaram e mortal parece
> ser teto de combinação, não de criatura solo (§20.4.5); para o Patamar 5, moderado e difícil também
> se confirmam, mas mortal (~300) deixa de funcionar como teto a partir de ND 9 — três das cinco
> criaturas o superam sozinhas (§20.5.6). Os dois lotes usaram convenções de medição diferentes (ver
> §18), então tratar os números como definitivos ainda depende de uma validação cruzada.

> **O patamar 1 é oscilante.** A faixa difícil vai só de 21 a 39: um encontro um pouco acima do previsto
> passa direto de difícil para mortal. É o nível 1 do d20 clássico, e o Mestre precisa saber.

#### 4.4.1 Banda de desgaste de equipamento (Aprovação 035)

HP perdido e Infecção não capturam criaturas cuja ameaça principal é degradar o **equipamento**
(`docs/gdd/GDD_Equipamentos.md` §3) em vez do personagem — o Bloco 5 trouxe três casos (Zumbi Corrosivo,
Devorador de Aço, Colosso de Sucata) que ficariam mal rotulados ("fácil"/"moderado") se só os dois
eixos de §4.4 fossem lidos. Eixo novo, mesma régua de §3.1: **estados de desgaste esperados por
combate**, na peça mais exposta.

| Faixa | Estados de desgaste / combate |
|---|---|
| **Leve** | < 0,3 |
| **Moderado** | 0,3 – 1,0 |
| **Severo** | 1,0 – 2,0 |
| **Catastrófico** | > 2,0 |

| Criatura | Faixa | Medido |
|---|---|---|
| Touro Mecânico (§8.4) | Leve | Rasgar 1×/combate, só se acertar |
| Devorador de Aço (§20.4.2) | Moderado | ~0,66/combate com equipamento real de Patamar 4 |
| Zumbi Corrosivo (§20.2.3) | Severo | ~1,1/combate em Patamar 1 |
| Colosso de Sucata (§20.5.3) | Catastrófico | até 3 Rasgar garantidos por combate |

### 4.5 Onde o modelo é fraco — declarado

| Caso | Situação |
|---|---|
| **Pontos não são exatos entre patamares** | O valor **relativo** das criaturas muda com o nível do grupo: Touro ÷ Mutante vale **0,53 no patamar 1 e 0,72 no patamar 2**. Nenhuma tabela fixa acerta todos os patamares — é a mesma limitação do XP do d20. Os limiares acertam **83 a 88%** dos rótulos reais |
| **Criatura sozinha** | Continua o pior caso: grupos de nível alto a matam antes que ela aja |
| **Mais de 10 criaturas** | `n − 1` superestima (12 Zumbis: +14%; 16: +95%) — mas nessa faixa o grupo já está morto, e o custo real para de crescer |
| **Casulo e Zumbi de Sangue** | Pontos **medidos**, não calculados. Criatura com explosão de morte ou geração contínua deve ser medida |
| **O que não é modelado** | Movimento, cobertura, terreno, modificações, Especializações e uso tático. O orçamento mede **atrito**, não **dificuldade tática** |
| **Patamares 4 e 5 (Bloco 5) usam convenções de medição diferentes** | O lote de ND 6–7 mediu contra uma party de orçamento fixo (validada contra o Gigante); o de ND 8–10 mediu contra a party real do Patamar 5 (§5). Mesma família de imprecisão que o Touro/Mutante (0,53× vs 0,72× entre patamares, acima) — **decisão do Diretor: tratar como limitação já aceita**, não investir em reconciliar |
| **`M(n)` subestima pilhas de criatura "dano puro, sem Infecção"** | Confirmado em três casos — 2× Posto Automatizado, 2× Touro Mecânico e **4× Saqueador Humano** (20.000 iterações: a fórmula prevê custo 6, "fácil"; medido, 20,9% de HP perdido, perto de "moderado"). O padrão é geral, não um acaso de uma criatura: toda criatura com "Gera Infecção: Não", empilhada, tende a superar o rótulo que a fórmula prevê. **Mitigação prática, sem reescrever `M(n)`:** ao montar um encontro só com criaturas que não geram Infecção, suba o rótulo em um degrau em relação ao que a fórmula indica |

A leva do Medidor de Horda custa **1 ponto por errante** e chega **por cima** do orçamento — e o Medidor é
**recurso do Mestre, não obrigação**: ele pode ser desligado numa cena em que não serve à história.

### 4.6 Os panoramas medidos (Aprovação 030)

**Por patamar — cada grupo com a armadura esperada para ele.** Perda de HP do grupo · Infecção por
personagem por luta. 2.000 iterações por célula.

| Encontro | **P1** | **P2** | **P3** | **P4** | **P5** |
|---|---|---|---|---|---|
| 4× Zumbi | 🟢 11% · 1,0 | 🟢 3% · 0,5 | 🟢 | 🟢 | 🟢 |
| **8× Zumbi** (bando) | 🔴 46% · 4,0 | 🟠 15% · 2,2 | 🟡 6% · 1,3 | 🟢 | 🟢 |
| 2 Resistentes + 2 Maratonistas | 🟡 17% · 1,5 | 🟢 | 🟢 | 🟢 | 🟢 |
| 2× Mutante | 🟡 25% · 1,2 | 🟢 | 🟢 | 🟢 | 🟢 |
| 2× Zumbi de Sangue | 🟠 31% · 2,7 | 🟠 14% · 2,1 | 🟡 8% · 1,8 | 🟡 5% · 1,5 | 🟡 3% · 1,3 |
| Venenoso + 2 Zumbis | 🟠 40% · 2,4 | 🟡 12% · 1,3 | 🟢 | 🟢 | 🟢 |
| **Gigante** | 🔴 98% · 5,9 | 🔴 38% · 3,8 | 🟠 16% · 2,6 | 🟡 9% · 2,0 | 🟡 6% · 1,7 |
| **2× Gigante** | 🔴 100% | 🔴 100% | 🔴 58% · 10,0 | 🔴 32% · 7,5 | 🔴 21% · 6,5 |

🟢 fácil · 🟡 moderado · 🟠 difícil · 🔴 mortal

**Efeito da armadura — patamar 1.**

| Encontro | Sem armadura (13) | Leve (15) | Média + escudo (17) | Pesada + escudo (20) |
|---|---|---|---|---|
| 4× Zumbi | 🟡 13% · 1,1 | 🟢 11% · 0,9 | 🟢 9% · 0,8 | 🟢 6% · 0,5 |
| **8× Zumbi** | 🔴 55% · 4,7 | 🔴 45% · 3,9 | 🟠 38% · 3,2 | 🟠 25% · 2,1 |
| 2× Mutante | 🟡 29% · 1,4 | 🟡 25% · 1,2 | 🟡 21% · 1,0 | 🟡 17% · 0,8 |
| 2× Zumbi de Sangue | 🟠 33% · 2,8 | 🟠 31% · 2,7 | 🟠 30% · 2,6 | 🟠 28% · 2,4 |
| Venenoso + 2 Zumbis | 🟠 44% · 2,7 | 🟠 39% · 2,4 | 🟠 36% · 2,1 | 🟡 31% · 1,7 |
| Gigante | 🔴 99% | 🔴 98% | 🔴 93% | 🔴 81% |

**Critério dos rótulos** (vale o pior dos dois):

| | Fácil | Moderado | Difícil | Mortal |
|---|---|---|---|---|
| **Perda de HP do grupo** | < 15% | 15–35% | 35–60% | ≥ 60%, ou wipe ≥ 5% |
| **Infecção por personagem por luta** | < 1 | 1–2 | 2–3,5 | ≥ 3,5 *(mutação em ~5 lutas)* |

Se **alguém cai em 25% ou mais** das lutas, o encontro é no mínimo difícil.

> **A validação da Aprovação 027 continua de pé, com uma nuance.** Quatro Zumbis são **moderado para
> um grupo sem armadura e fácil para um grupo equipado**. A premissa antiga — *"luta típica de quatro
> errantes"* (`docs/gdd/GDD_Horda.md` §5) — assumia grupo sem armadura. Agora a armadura faz diferença,
> que era o objetivo da Aprovação 029.

## 5. Ficha padrão de criatura

Cada verbete traz os mesmos campos, e **três deles são exclusivos do MUTAGEN** — não existem em
bestiário de d20 nenhum:

| Campo | O que é |
|---|---|
| ND · HP · Defesa · Ataque · Dano · Movimento · Tamanho | O convencional |
| **Gera Infecção?** | Se o dano dela é **Necrótico**, cada acerto dela em você vale **1 ponto de Trilha** (2 no crítico). **Criatura que não causa Necrótico não toca na sua Trilha** |
| **Uiva?** | Se ela produz **Atração** por conta própria (`docs/gdd/GDD_Ruido.md` §6) |
| **Resistências** | Na **escada de dados**: Vulnerável sobe um degrau, Resistente desce um, Muito Resistente desce dois, Imune zera (`docs/gdd/GDD_Combate.md` §6.3) |

**Parâmetros de simulação (Aprovação 030) — cinco patamares**, derivados do canon de progressão
(proficiência +2 a +6 nos níveis 1/5/9/13/17; HP `8 + CON` no nível 1 e `+5 + CON` por nível; atributo
principal 16 → 18 → 20):

| Patamar | Níveis | Ataque | Dano | HP | Defesa equipada |
|---|---|---|---|---|---|
| P1 | 1–4 | +5 | 1d8+3 | 30 | 15 |
| P2 | 5–8 | +7 | 1d10+4 | 52 | 17 |
| P3 | 9–12 | +9 | 1d10+5 | 80 | 19 |
| P4 | 13–16 | +10 | 1d12+5 | 108 | 20 |
| P5 | 17–20 | +11 | 1d12+5 | 136 | 21 |

O patamar 1 é o personagem de `docs/gdd/GDD_Armas.md` §1.2, agora com armadura.

---

## 6. Catálogo — ND 0

### 6.1 Zumbi

| | |
|---|---|
| **ND / Custo** | 0 · **1 ponto** |
| **HP / Defesa** | **12 / 14** — *a régua* |
| **Ataque / Dano** | +4 · **1d6 Necrótico** |
| **Movimento / Tamanho** | **4 hex** · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | — |

**Ele anda 4 hex contra os 6 do personagem.** Essa diferença de dois hexágonos é a única razão pela
qual recuar é sempre uma opção, e é a tradução mecânica do gênero inteiro: o morto-vivo básico não te
alcança, ele te **cansa**. Toda a economia de Infecção depende disso — quem entra no corpo a corpo com
um Zumbi comum **escolheu** entrar.

Resiste a Perfurante e Balístico porque **não tem órgão vital para furar** (`docs/gdd/GDD_Combate.md`
§6.3). É Vulnerável a Fogo, e é isso que dá função ao maçarico, à Ponta Incendiária e à "Boca de
Forno".

### 6.2 Cachorro Zumbi

| | |
|---|---|
| **ND / Custo** | 0 · **1 ponto** |
| **HP / Defesa** | 8 / 15 |
| **Ataque / Dano** | +5 · **1d4 Necrótico** |
| **Movimento / Tamanho** | **8 hex** · **Miúdo** |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Matilha:** tem **Vantagem** no ataque se um aliado seu está adjacente ao mesmo alvo |

**Ele resolve o problema que o Zumbi comum cria.** Se todo inimigo básico anda 4 hex, recuar é sempre
certo e o jogo trava. O Cachorro anda **8** — mais que o personagem — e chega. O dado é minúsculo
(1d4), mas **cada acerto vale 1 ponto de Trilha igual ao de qualquer outro**, e a Matilha faz cada um
acertar muito mais.

É a demonstração mais limpa da regra de acerto: **oito cachorros são mais perigosos para a sua Trilha
do que um Gigante.**

---

## 7. Catálogo — ND 1

### 7.1 Zumbi Resistente

| | |
|---|---|
| **ND / Custo** | 1 · **2 pontos** |
| **HP / Defesa** | **14 / 16** |
| **Ataque / Dano** | +4 · **1d6 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | **Concussão** |
| **MUITO Resistente** | **Perfurante, Balístico** |
| **Habilidade** | As placas metálicas são blindagem, não carne |

> **Esta criatura dá sujeito ao grau *Muito Resistente***, cuja coluna estava **inteiramente vazia**
> desde a Aprovação 020 — a divergência 30 do glossário está fechada por ela.

**Repare no que ele NÃO tem: HP.** 14 contra os 12 da régua, quase nada. As placas viraram **Defesa e
resistência**, não carne, porque blindagem não é vida — é dificuldade de penetrar. Um sistema que
traduzisse armadura em HP teria criado um zumbi "gordo"; este é um zumbi **duro**, que é outra coisa.

**E a vulnerabilidade a Concussão é o coração dele.** Placa para bala; não para pancada — chapa de
metal *transmite* impacto. A resposta certa ao Zumbi Resistente é a marreta.

> **A consequência é cruel de propósito.** A marreta é **Ruído Alto** (6 pontos de Medidor por
> rodada). O rifle, que é a resposta errada, é o que você tem na mão. **O zumbi blindado cobra o seu
> silêncio** — e essa é a mesma inversão que rege o jogo inteiro desde a Aprovação 009.

### 7.2 Zumbi Cibernético

| | |
|---|---|
| **ND / Custo** | 1 · **1,5 ponto** |
| **HP / Defesa** | 14 / 15 |
| **Ataque / Dano** | +5 · **1d6 Necrótico** |
| **Movimento / Tamanho** | 5 hex · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | **Elétrico/EMP** |
| **Resistente** | Perfurante, Necrótico, Químico |
| **Habilidade** | **Usa cobertura:** quando alvo de ataque à distância, age como se tivesse tomado a ação **Esquivar** (atacante rola com **Desvantagem**) |

O perfil de resistência dele **já era canon** — é a linha *"Alvo com cibernética"* de
`docs/gdd/GDD_Combate.md` §6.3. Este documento só lhe deu corpo.

**Ele é o primeiro inimigo que ataca a sua escolha de sistema, e não o seu HP.** Atirar nele é
ineficiente; a resposta é fechar a distância — e fechar a distância é entrar na Trilha de Infecção.
Ele **empurra o grupo do orçamento de Horda para o orçamento de Infecção**, sem nunca dizer isso.

O EMP finalmente tem um alvo que justifica carregá-lo.

### 7.3 Maratonista

| | |
|---|---|
| **ND / Custo** | 1 · **1 ponto** |
| **HP / Defesa** | 10 / 15 |
| **Ataque / Dano** | +5 · **1d6 Necrótico** |
| **Movimento / Tamanho** | **10 hex** · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Investida:** fecha do alcance de rifle até o corpo a corpo **em um único turno** |

**Ele anula o alcance.** Dez hexágonos contra os seis do personagem: não existe cenário em que você
atire duas vezes antes de ele chegar. Quem contava com a distância como plano descobre que a distância
era um **empréstimo**.

HP 10 e sem resistência: ele é de vidro. O problema nunca é matá-lo — é matá-lo **antes**.

### 7.4 Arrastador

| | |
|---|---|
| **ND / Custo** | 1 · **1 ponto** |
| **HP / Defesa** | 10 / 13 |
| **Ataque / Dano** | +5 · **1d6 Necrótico** |
| **Movimento / Tamanho** | **3 hex** · **Miúdo** |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | **Emboscada:** começa a cena **Escondido** sob entulho. **Percepção CD 14** para localizá-lo antes do ataque; o primeiro ataque dele tem **Vantagem** · **Tornozelo:** ao acertar, o alvo testa **AGI CD 13** ou fica **Agarrado** (movimento 0) |

**Ele dá função de combate à perícia Percepção**, que até aqui só servia para detectar emboscada de
forma abstrata. Agora há um número: 14, e um preço por falhar.

O Tornozelo é o que o torna perigoso apesar do ND 1 — um personagem Agarrado **não recua**, e não
recuar de um bando de Zumbis comuns é como a Trilha de Infecção realmente enche.

### 7.5 Vigia

| | |
|---|---|
| **ND / Custo** | 1 · **0 pontos sozinho, 2 acompanhado** — *ver §4.3: ele fere o Medidor, não o grupo* |
| **HP / Defesa** | 12 / 15 |
| **Ataque / Dano** | **não ataca** |
| **Movimento / Tamanho** | 8 hex · Médio |
| **Gera Infecção?** | **Não** |
| **Uiva?** | Não — *ele corre, não grita* |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Alarme:** no turno dele, move-se **para longe**, em direção à borda do mapa. Se **sair do mapa**, o **Medidor de Horda sobe +10 imediatamente** |

**O primeiro inimigo que ataca o seu recurso, e não o seu personagem.** Ele não pode te ferir. Ele
pode fazer a próxima meia hora de jogo ser muito pior.

O dilema é exato: derrubá-lo rápido exige a arma de alcance — que é **barulhenta** e alimenta o mesmo
Medidor que você está tentando proteger. Deixá-lo ir custa metade de um limiar de uma vez.

> **Ele é a prova de que o Medidor de Horda é um alvo legítimo de design.** Até aqui, o Medidor só
> subia por culpa do jogador. Agora o mundo também empurra.

### 7.6 Saqueador Humano

| | |
|---|---|
| **ND / Custo** | 1 · **0,5 ponto** |
| **HP / Defesa** | 16 / 14 *(o que a armadura dele der)* |
| **Ataque / Dano** | +5 · **arma do catálogo** — padrão: Pistola leve, **1d6 Balístico** |
| **Movimento / Tamanho** | 6 hex · Médio |
| **Gera Infecção?** | **NÃO** |
| **Uiva?** | Não |
| **Vulnerável** | — |
| **Resistente** | — *(só o que o material da armadura der)* |
| **Habilidade** | **Usa cobertura** e o catálogo de armas inteiro · **Pode ser negociado:** **Persuasão** ou **Intimidação CD 15** encerra o combate sem rolagem de ataque |

> **Variante Arqueiro/Besteiro (Aprovação 035).** O Mestre pode equipar o Saqueador com qualquer arma
> **Perfurante** do catálogo — Besta de Caça, Besta Pesada, Arco Artesanal, Lança Artesanal, Forcado —
> em vez da pistola padrão. Dano e Ruído mudam conforme a arma (`docs/gdd/GDD_Armas.md`). Isto é
> documentação, não uma criatura nova: Perfurante já não é decorativo, porque o **Colete Balístico
> Civil** que o próprio Saqueador pode vestir é **Resistente a Perfurante** (`docs/gdd/GDD_Equipamentos.md`
> §10) — times que só atacam com besta ou lança encontram resistência real nele.

> **Ele já era canon e ninguém tinha reparado.** A linha *"Humano (saqueador)"* está na tabela de
> perfis de resistência de `docs/gdd/GDD_Combate.md` §6.3 desde a Aprovação 020. **O MUTAGEN já havia
> decidido que nem todo inimigo é morto-vivo.**

Três coisas o tornam diferente de tudo o mais neste documento:

1. **Ele usa o seu catálogo.** Toda arma, toda modificação, todo tier — e portanto todo Ruído. Um
   saqueador com rifle enche o **seu** Medidor de Horda.
2. **Ele não gera Infecção.** Matar humanos é limpo. É a assimetria moral mais dura do sistema: a
   forma mais segura de sobreviver é lutar contra gente.
3. **Ele finalmente dá função de combate a CAR.** Persuasão e Intimidação tinham utilidade social e
   nenhuma resposta numa iniciativa. Agora têm.

---

## 8. Catálogo — ND 2

### 8.1 Mutante

| | |
|---|---|
| **ND / Custo** | 2 · **6,5 pontos** |
| **HP / Defesa** | 28 / 15 |
| **Ataque / Dano** | +7 · **1d8+2 Necrótico** |
| **Movimento / Tamanho** | 5 hex · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | **Fogo** |
| **Resistente** | Perfurante, Necrótico |
| **Habilidade** | **Regeneração:** cura **5 HP** no início de cada turno seu — **anulada se sofreu dano de Fogo desde o fim do turno anterior** |

Perfil de resistência **já canônico** (`docs/gdd/GDD_Combate.md` §6.3).

**A Regeneração é o que dá à vulnerabilidade a Fogo uma segunda razão de existir.** Contra o Mutante,
Fogo não é só "mais dano": é o **desligador** de uma habilidade. Uma tocha barata, mantida acesa,
vale mais que um dado maior — e isso é exatamente o princípio de tier alto aplicado ao avesso.

### 8.2 Uivante

| | |
|---|---|
| **ND / Custo** | 2 · **3 pontos** |
| **HP / Defesa** | 20 / 14 |
| **Ataque / Dano** | +5 · **1d6 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | **SIM** |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Uivo:** gasta a **Ação**. Produz **Nível de Ruído Alto (3)** e gera **Atração** em raio amplo — todo mutante fora de combate no raio move-se para a fonte no próximo turno dele |

> **Ele preenche o `[A CALIBRAR]` mais antigo de `docs/gdd/GDD_Ruido.md` §6**, que estabelecia o
> mecanismo do uivo e dizia explicitamente que *quais* criaturas uivam pertencia ao Bestiário.

**O Uivante é a tese do jogo inteiro comprimida numa criatura.** `docs/gdd/GDD_Ruido.md` §6 já previa que
ele viraria alvo prioritário — *"silenciá-lo passa a valer mais do que o inimigo mais forte ou mais
próximo"*. O que o Bestiário acrescenta é que **não existe resposta grátis**:

- matá-lo rápido exige **arma de fogo** → enche o **Medidor de Horda**;
- atravessar a sala até ele exige **corpo a corpo** → enche a **Trilha de Infecção**;
- ignorá-lo deixa ele **encher o Medidor sozinho**.

Três saídas, três preços, nenhum zero. É o dilema central do MUTAGEN forçado num único inimigo.

### 8.3 Cachorro Explosivo

| | |
|---|---|
| **ND / Custo** | 2 · **0,5 ponto** |
| **HP / Defesa** | 8 / 15 |
| **Ataque / Dano** | **não ataca** |
| **Movimento / Tamanho** | **10 hex** · **Miúdo** |
| **Gera Infecção?** | **NÃO** |
| **Uiva?** | Não — mas a aproximação dele é **Ruído Alto** (o guincho) |
| **Vulnerável** | **Fogo** — *e isso é um presente* |
| **Resistente** | — |
| **Habilidade** | **Detonação:** ao chegar adjacente a um personagem, **detona**. Raio **2 hex**, **3d6 Fogo e Concussão**, **AGI CD 14** para metade. Ele morre no processo |

**Ele não toca na sua Trilha.** Pode te matar, e não te infecta — e essa separação é o que dá ao
Bestiário um vocabulário tático que nenhum bestiário de d20 tem.

**A vulnerabilidade a Fogo é presente, não punição.** Acertar fogo nele à distância faz o cão detonar
**onde está** em vez de onde você está. É a única criatura do catálogo em que o jogador *quer* que a
vulnerabilidade exista — e o custo é que a arma de fogo é barulhenta.

### 8.4 Touro Mecânico

| | |
|---|---|
| **ND / Custo** | 2 · **3,5 pontos** |
| **HP / Defesa** | 35 / 15 |
| **Ataque / Dano** | +7 · **2d8 Concussão** |
| **Movimento / Tamanho** | 6 hex · **GRANDE** |
| **Gera Infecção?** | **NÃO** |
| **Uiva?** | Não |
| **Vulnerável** | **Elétrico/EMP** |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | **Investida:** se move **6 hex ou mais em linha reta** e então ataca, o alvo testa **FOR CD 15** ou é **empurrado 3 hex** e fica **Caído** · **Rasgar** *(quebra-armadura, Aprov. 034)*: 1× por combate, ao acertar, a peça atingida desce **um estado de desgaste** mesmo sem crítico (`docs/gdd/GDD_Equipamentos.md` §3.2) |

> **Ele é a primeira criatura Grande do canon**, e com isso **destrava o "Extrator" arpão de resgate**
> (`docs/gdd/GDD_Armas.md` §7.4), congelado desde a aprovação de tier alto por depender de categorias de
> tamanho.

Metade zumbi, metade cibernético: **Concussão, não Necrótico**. Como o Cachorro Explosivo, ele é uma
criatura que você pode enfrentar de perto sem pagar Trilha.

---

## 9. Catálogo — ND 2, continuação

### 9.1 Casulo

| | |
|---|---|
| **ND / Custo** | 2 · **8 pontos** — *vale pelo que gera* |
| **HP / Defesa** | 25 / **10** — *imóvel, não esquiva* |
| **Ataque / Dano** | **não ataca** |
| **Movimento / Tamanho** | **0** · Grande |
| **Gera Infecção?** | **Não** |
| **Uiva?** | Não |
| **Vulnerável** | **Fogo** |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | **Gestação:** ao fim de cada rodada, gera **1 Zumbi (ND 0)** adjacente a si |

**É um cronômetro com HP.** Ele não pode te ferir, não pode te alcançar e não pode fugir — e cada
rodada que você gasta em outra coisa custa um corpo a mais no mapa.

Defesa 10 é de propósito: acertá-lo é trivial, **atravessar os 25 HP enquanto o bando cresce é que
não é**. E o bando que ele gera é o de ND 0, ou seja, **o que mais enche a Trilha** — o Casulo ataca a
sua Infecção sem nunca te tocar.

---

## 10. Catálogo — ND 3

### 10.1 Zumbi de Sangue

| | |
|---|---|
| **ND / Custo** | 3 · **18 pontos** |
| **HP / Defesa** | 30 / 14 |
| **Ataque / Dano** | +6 · **1d6 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | **Sim — duas vezes** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Explosão de sangue:** ao chegar a **0 HP**, explode em raio de **2 hex**. Toda criatura no raio testa **AGI CD 14**; quem falha sofre **2d6 Necrótico e +2 pontos de Infecção**. **Zumbis e mutantes no raio, em vez disso, curam 2d6** |

**Ele é anti-corpo-a-corpo por construção, e a construção é honesta:** quem o matou de perto está,
por definição, dentro do raio. O golpe que resolve o problema é o mesmo que cobra o preço.

E a cura aos aliados pune matá-lo **no meio do bando** — o momento em que você mais quer matá-lo.

> **Ele te obriga a atirar.** Matar o Zumbi de Sangue à distância é gratuito em Trilha e caro em
> Horda; matá-lo de perto é o contrário. É a primeira criatura que **escolhe por você qual moeda de
> atrito você vai gastar** — e cobra as duas se você hesitar.

### 10.2 Doutora Zumbi

| | |
|---|---|
| **ND / Custo** | 3 · **5 pontos** — *medido acompanhada, já inclui as curas* |
| **HP / Defesa** | 24 / 14 |
| **Ataque / Dano** | +6 · **1d6 Necrótico** *(seringa)* |
| **Movimento / Tamanho** | 5 hex · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante |
| **Habilidade** | **Tratamento:** gasta a **Ação** para curar **2d6 HP** em um zumbi ou mutante adjacente |

**Alvo prioritário nº 2, depois do Uivante** — e a diferença entre os dois é instrutiva. O Uivante
piora a cena; a Doutora Zumbi **desfaz o seu trabalho**. Contra ela, dano concentrado vale mais que dano
espalhado, e a decisão de foco passa a existir de verdade.

Ela é o que impede o Bestiário de ser só uma escala de números: **duas criaturas de ND 3 podem pedir
táticas opostas.**

---

## 11. Catálogo — ND 4

### 11.1 Zumbi Venenoso

| | |
|---|---|
| **ND / Custo** | 4 · **30 pontos** |
| **HP / Defesa** | 45 / 15 |
| **Ataque / Dano** | +10 · **1d8+2 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | **Sim — por ataque E por aura** |
| **Uiva?** | Não |
| **Vulnerável** | **Fogo** |
| **Resistente** | Perfurante, Balístico |
| **IMUNE** | **Químico** |
| **Habilidade** | **Aura venenosa (2 hex):** toda criatura que **começa o turno** dentro do raio sofre **1d6 Químico** e testa **CON CD 14** ou ganha **1 ponto de Infecção** |

> **É a única criatura do MVP imune a um tipo de dano**, e ela passa na trava do §13: uma criatura
> **feita de veneno** não morre de veneno.

**A aura é o mecanismo que a simulação do §3 provou ser necessário.** Ela aplica Infecção **sem
rolagem de ataque** — é o único jeito de uma criatura grande ameaçar a Trilha sem virar uma
picadora de HP. O Zumbi Venenoso não precisa te acertar para te infectar; **basta você estar perto no
começo do seu turno**.

Tática que ele impõe: ou se atira de longe (Horda), ou se aceita um ponto de Trilha por rodada de
contato. Não há terceira.

### 11.2 Cuspidor

| | |
|---|---|
| **ND / Custo** | 4 · **3,5 pontos** |
| **HP / Defesa** | 35 / 14 |
| **Ataque / Dano** | +10 **à distância, 8 hex** · **2d6 Químico** |
| **Movimento / Tamanho** | **3 hex** · Médio |
| **Gera Infecção?** | **NÃO** — *o cuspe é Químico, não Necrótico* |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | **Químico** — *não imune; ver §13* |
| **Habilidade** | **Cuspe corrosivo:** ignora **meia cobertura** (o +2 de Defesa não se aplica) |

**É o primeiro zumbi que atira.** Até aqui, ficar longe era seguro e custava só Horda. O Cuspidor
cobra por ficar longe — e ignorar meia cobertura significa que a resposta tática usual (se abrigar)
não resolve.

Move-se 3 hex: ele é lento, e é isso que o mantém justo. A resposta é **flanquear**, não recuar.

> **Ele é o caso de teste da trava de imunidade, e ela funcionou.** O Cuspidor **produz** ácido; ele
> não **é feito** de ácido. Por isso é **Resistente** a Químico e não Imune, ao contrário do Zumbi
> Venenoso. A regra do §13 foi escrita para decidir exatamente este tipo de caso, e decidiu sozinha.

---

## 12. Catálogo — ND 5

### 12.1 Gigante Mutagênico

| | |
|---|---|
| **ND / Custo** | 5 · **132 pontos** |
| **HP / Defesa** | **80 / 16** |
| **Ataque / Dano** | +11 · **2d8+4 Necrótico** |
| **Movimento / Tamanho** | 5 hex · **ENORME** |
| **Gera Infecção?** | **Sim — por ataque, por miasma e pela Cisão** |
| **Uiva?** | Não |
| **Vulnerável** | **Fogo** |
| **Resistente** | Perfurante, Balístico, Concussão |
| **IMUNE** | **Agarrado** e **Enganchar** *(imunidade de condição por tamanho, não de dano)* |
| **Habilidades** | **Duas ações** por rodada · **Miasma (1 hex):** criatura que começa o turno adjacente ganha **1 ponto de Infecção**, sem teste · **CISÃO:** ao chegar a **0 HP**, não morre — **transforma-se em 4 Zumbis (ND 0)** no espaço que ocupava |

Um conglomerado de zumbis fundidos num corpo só.

**A Cisão não é sabor: é a correção mecânica do problema medido no §3.** Um chefe, por construção, é
fraco contra uma Trilha que conta acertos. Ao chegar a zero, o Gigante **vira o bando** — que é a
única coisa que de fato ameaça a Trilha. A luta tem **dois atos**, e o segundo é o perigoso.

Ele é Imune a **Agarrado** e **Enganchar** por ser **Enorme**, seguindo a regra canônica de que
Enganchar não afeta alvos duas categorias maiores. Isso **não é imunidade a dano** e não passa pela
trava do §13 — é geometria.

---

## 13. Imunidades — a trava antes da lista

Imunidade é a **única regra do sistema que zera dano**. Um erro aqui pode travar um grupo inteiro numa
luta que não tem como vencer. Por isso ela tem regra própria:

> ### Imunidade a tipo de dano exige que a criatura SEJA feita daquilo.
>
> Produzir, usar ou resistir não basta. **Ser.**

**No MVP isso qualifica exatamente uma criatura:** o **Zumbi Venenoso**, imune a **Químico**.

A trava já foi testada uma vez e decidiu sozinha: o **Cuspidor** produz ácido como arma, mas não é
feito dele — ficou **Resistente**, não Imune (§11.2).

**Duas observações para implementadores:**

1. **Imunidade de condição é outra categoria** e não passa por esta trava. O Gigante é imune a
   Agarrado e Enganchar por **tamanho**, o que já era canon. O talento *Nervos de Aço* dá imunidade a
   **Amedrontado**. Nenhuma das duas é imunidade a tipo de dano.
2. **O grau *Imune* da escala deve existir no motor mesmo com um só sujeito.** A escada precisa dos
   cinco degraus para funcionar; que apenas um esteja povoado hoje é fato do Bestiário, não da regra.

---

## 14. Infecção por criatura — a tabela que decide o corpo a corpo

**Criatura que não causa dano Necrótico não toca na sua Trilha.** É a consequência mais prática deste
documento, e ela cria um vocabulário tático novo:

| Gera Infecção | Não gera Infecção |
|---|---|
| Zumbi · Cachorro Zumbi · Zumbi Resistente · Zumbi Cibernético · Maratonista · Arrastador · Mutante · Uivante · Zumbi de Sangue · Doutora Zumbi · Zumbi Venenoso · Gigante Mutagênico | **Cachorro Explosivo** · **Touro Mecânico** · **Saqueador Humano** · **Vigia** · **Casulo** · **Cuspidor** |

**Seis das dezoito criaturas são seguras para o corpo a corpo.** Isso significa que a decisão
"encostar ou atirar" deixa de ser um reflexo e vira **leitura de mesa**: contra o Touro, encoste;
contra o bando de Zumbis, pense duas vezes.

> A assimetria mais dura da lista: **o Saqueador Humano é a criatura mais segura de se matar de
> perto.** Lutar contra gente não infecta ninguém. O sistema não comenta isso — apenas cobra.

---

## 15. Ruído de criatura

`docs/gdd/GDD_Ruido.md` §6 estabeleceu o mecanismo e deixou os sujeitos para cá. O resultado é curto de
propósito:

| Criatura | Ruído próprio | Efeito |
|---|---|---|
| **Uivante** | **Alto (3)**, gastando a Ação | **Atração** em raio amplo |
| **Cachorro Explosivo** | **Alto (3)** na aproximação | O guincho denuncia a posição dele — e a sua |
| **Todas as demais** | **Silencioso (0)** | — |

**Os zumbis básicos não emitem ruído**, conforme o canon de `docs/gdd/GDD_Ruido.md` §6.

> **Criatura não alimenta o Medidor de Horda.** O Medidor conta **o ruído que o grupo produziu**
> (`docs/gdd/GDD_Horda.md` §1); o ruído de criatura gera **Atração**, que é outro sistema. A única exceção
> é o **Vigia**, e ela é explícita: se ele escapa, o Medidor sobe **+10** — não por barulho, mas
> porque ele foi buscar gente.

---

## 16. A leva, em criaturas

`docs/gdd/GDD_Horda.md` §3 define o piso: **2 errantes na primeira leva, `+1` a cada leva subsequente na
mesma cena**. Este documento diz o que é um errante:

**Errante = Zumbi (ND 0).** Uma leva de piso custa **2 pontos** de orçamento e chega **por cima** do
encontro planejado, porque é consequência, não desenho.

> **O piso continua sendo piso.** `docs/gdd/GDD_Horda.md` §3 declara a leva um **recurso do Mestre**, que
> pode escalar tamanho e composição acima do piso quando a cena pedir. Substituir um Zumbi da leva por
> um Maratonista ou um Uivante é uso legítimo do sistema — e é a forma mais barata de fazer uma cena
> barulhenta doer mais.

---

## 17. Tamanho

As categorias **Miúdo · Médio · Grande · Enorme** **não moram aqui** — são regra de combate, porque
governam ocupação de hexágono, cobertura, Enganchar e o arpão "Extrator". Estão em
**`docs/gdd/GDD_Combate.md` §14** (Aprovação 025). Este documento apenas **usa** a escala.

---

## 18. O que continua `[A CALIBRAR]`

| Campo | Estado |
|---|---|
| **Orçamento de encontro** | ✅ **CANON por patamar** (Aprovação 030) — limiares P1–P3 medidos (83–88% de acerto); **P4 e P5 provisórios** até existirem criaturas de ND 6+ (Bloco 5) |
| **Dano de Sangrando** | Ainda aberto — nenhuma criatura deste catálogo o aplica, e a serra "Denteira" continua dependendo dele |
| **XP / recompensa por criatura** | Não desenhado. O MVP não tem economia de experiência |
| **Iniciativa de criatura** | Usa-se `d20 + mod. AGI`; o modificador de AGI por criatura não está fichado |
| **Atributos completos das criaturas** | Só os derivados (Defesa, ataque, dano) estão fixados. FOR/AGI/CON/INT/PER/CAR por criatura: aberto |
| **Comportamento do Zumbi Cibernético com INT alta** | A ficha dá "usa cobertura"; o quanto mais ele faz com INT é decisão do Mestre |

> Quatro achados do Bloco 5 que chegaram aqui como pendência **já foram resolvidos** nesta aprovação:
> a banda de desgaste de equipamento (§4.4.1), a banda Catastrófico do Patamar 5 (§4.4), e as duas
> imprecisões de medição (convenção P4/P5 e o ponto cego do `M(n)` em pilhas sem Infecção), ambas
> documentadas como limitação aceita em §4.5.

---

## 19. Notas de balanceamento

**Todas as fichas foram simuladas** contra um grupo de 4 personagens com os parâmetros canônicos
(ataque +5, dano +3, Defesa 13, arma 1d8), 8.000 iterações por perfil. Três achados que sobreviveram
à medição:

1. **Quantidade vence tamanho contra a Trilha de Infecção**, por um fator de **3,2×** no mesmo
   orçamento de HP. É o que produziu a regra do §3.
2. **O bando de 8 Zumbis comuns gerou 16,89 pontos de Infecção** numa única luta — acima do limiar
   base de 15. Um encontro de ND 0 puro e numeroso é, hoje, o mais letal do catálogo pela via da
   Trilha. **Isso é intencional e é o gênero**, mas o Mestre precisa saber.
3. **Nenhum perfil individual produziu mais de 1% de wipe** do grupo. A letalidade do MUTAGEN não está
   no HP: está na Trilha, que cobra depois.

> **O que estas simulações não provam.** Elas medem um grupo homogêneo de nível baixo com arma média,
> sem modificações, sem Especializações e sem uso tático de cobertura ou terreno. **Servem para
> comparar criaturas entre si**, não para prever a dificuldade real de uma mesa.

---

## 20. Catálogo — Bloco 5 (Aprovação 035)

> **O que o Bloco 5 resolve.** O Bestiário parava em ND 5 (Gigante Mutagênico, Patamar 3) — os
> Patamares 4 e 5 (níveis 13 a 20) não tinham nenhuma criatura, e os limiares de §4.4 eram
> **provisórios** por isso (§2.1). O Bloco 5 estende a escala até **ND 10** (`docs/gdd/GDD_Combate.md`
> §5.3.1) e adiciona ~20 criaturas novas, espalhadas por todos os patamares — não só os altos —,
> incluindo as duas pendências que vieram do Bloco 4b de Equipamentos: uma fonte de dano **Perfurante**
> fora do controle do Mestre, e mais criaturas **quebra-armadura** além do Touro Mecânico.
>
> **Regra nova desta rodada:** nenhum efeito de criatura que não seja o ataque corpo a corpo/à
> distância normal dispara automaticamente. Aura, explosão, desgaste de equipamento e controle sempre
> exigem um teste de resistência da vítima. É uma exigência explícita do Diretor para todo o Bloco 5,
> e vale mesmo onde a ficha não diz isso em voz alta.

### 20.1 Patamar 1 — ND 0–1

#### 20.1.1 Rastejante

| | |
|---|---|
| **ND / Custo** | 0 · **1 ponto** |
| **HP / Defesa** | 10 / 12 |
| **Ataque / Dano** | +4 · **1d6 Necrótico** |
| **Movimento / Tamanho** | **2 hex** · Miúdo |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | **Emboscada Rasteira:** começa a cena **Escondido** sob um carro, entulho ou cobertura baixa equivalente. **Percepção CD 14** para localizá-lo antes do ataque; o primeiro ataque dele tem **Vantagem** |

Ele é deliberadamente parecido com o **Arrastador** (§7.4) — mesmo esconderijo, mesma pose — e isso
precisa ser dito em voz alta, não escondido: o Rastejante é a versão **ND 0** do mesmo arquétipo. Sem
Tornozelo, sem agarrar — só a emboscada, e dois hexágonos de movimento em vez de três, porque sem as
pernas ele literalmente não persegue ninguém. É a peça de variedade que faltava ao ND 0 ao lado do
Zumbi e do Cachorro Zumbi: o primeiro inimigo da lista que ataca **antes** de você decidir se vale a
pena brigar, mas que — revelado — é o mais fraco e mais lento zumbi do catálogo.

**Resiste a Perfurante e Balístico** pela mesma razão do Zumbi comum (não tem órgão vital para furar)
e é Vulnerável a Fogo por ser, como todo zumbi, carne morta.

> **Medido em 8.000 iterações.** Sozinho, ele é "carne" de livro: 0,2% de HP do grupo e 0,02 de
> Infecção por personagem. Em bando de 4, com a emboscada garantida a cada um, o grupo perde **13,5%
> do HP** e acumula **1,16 de Infecção por personagem** — praticamente idêntico ao bando de 4 Zumbis
> comuns (13,3%/1,15), 4 Maratonistas (14,2%/1,22) e 4 Arrastadores com emboscada (15,1%/1,29), todos
> criaturas de **1 ponto**. HP e Defesa mais baixos que a régua são compensados pelo primeiro golpe
> garantido em Vantagem — por isso fecha no mesmo 1 ponto dos seus pares de ND 0.

#### 20.1.2 Zumbi Inchado

| | |
|---|---|
| **ND / Custo** | 1 · **2 pontos** |
| **HP / Defesa** | 14 / 14 |
| **Ataque / Dano** | +5 · **1d6 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | **Sim — pela mordida.** A explosão NÃO gera Infecção (é Química, não Necrótica) |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Nuvem de Gás:** ao chegar a **0 HP**, libera uma explosão de gás Químico em raio de **1 hex**. Toda criatura no raio testa **CON CD 13**; quem falha sofre **2d4 Químico**, quem passa sofre a metade (arredondado para baixo) |

A explosão usa **CON**, não AGI como a Explosão de Sangue do Zumbi de Sangue (§10.1) — a diferença é
proposital: a do Zumbi de Sangue é um estouro físico, que se esquiva; isto é uma nuvem tóxica, que se
resiste no corpo, igual ao que `docs/gdd/GDD_Combate.md` §3 já manda (CON resiste a Veneno). Nunca é
automática: exige o teste.

O gás ser Químico e não Necrótico é a decisão que mais importa aqui: é **puro dano de HP**, sem tocar
a Trilha — a forma de ameaça que `docs/gdd/GDD_Bestiario.md` §3 diz faltar, uma que não vem de "mais um
ataque". É também o segundo caso do catálogo (depois do Zumbi de Sangue) em que matar de perto cobra
um preço que matar de longe não cobra, mas aqui o preço é em HP, não em Infecção.

> **Medido em 8.000 iterações.** Isolado num bando de 4 (1 Inchado + 3 Zumbis comuns): **20,3% HP /
> 1,18 Infecção**, contra 13,3%/1,15 do bando de controle de 4 Zumbis — um ganho de ~7 pontos
> percentuais de HP, equivalente a mais um Zumbi inteiro. Isso o coloca ao lado do Zumbi Resistente
> (2 pontos, 17,3%/1,48), não do Zumbi comum (1 ponto).

#### 20.1.3 Enxame de Ratos Mutantes

| | |
|---|---|
| **ND / Custo** | 1 · **0,5 ponto** |
| **HP / Defesa** | 10 / 12 |
| **Ataque / Dano** | +5 (sempre com **Vantagem**) · **1d6 Perfurante** |
| **Movimento / Tamanho** | 6 hex · Miúdo |
| **Gera Infecção?** | **NÃO** — a mordida é Perfurante, nunca Necrótica |
| **Uiva?** | Não |
| **Vulnerável** | **Concussão** |
| **Resistente** | — |
| **Habilidade** | **Enxame:** ataca sempre com **Vantagem** — é uma massa de corpos pequenos, não um único animal. A mordida é **Perfurante** por natureza, não por escolha do Mestre |

Esta é a criatura que resolve a pendência de `docs/gdd/GDD_Equipamentos.md` §11: *"Criatura ou habilidade
dedicada de dano Perfurante."* Hoje Perfurante só existe em combate se o Mestre decidir armar um
Saqueador Humano com besta, arco ou lança (§7.6) — uma escolha dele, não uma garantia do sistema. O
Enxame causa Perfurante **sempre**, por ficha: é a primeira fonte de Perfurante que o jogador pode
prever antes da mesa, e finalmente testa o **Colete Balístico Civil** (Resistente a Perfurante,
kevlar) contra um inimigo que não é uma variante opcional de outro.

**Deliberadamente não resiste a Perfurante nem a Balístico.** O rato é vivo, não morto-vivo — tem
órgão vital para furar — e essa ausência de resistência é metade do que o diferencia. A vulnerabilidade
a **Concussão**, e não a Fogo, também é escolha: não é um corpo seco que pega fogo fácil, é uma massa
que se esmaga com impacto — a marreta, já resposta ao Zumbi Resistente, ganha um segundo uso tático.

> **Medido em 8.000 iterações.** Em bando de 4, o Enxame perde **17,6% do HP** do grupo e gera **0,00
> de Infecção**. É quase idêntico ao bando de referência de 4 Saqueadores Humanos no mesmo simulador
> (17,3% / 0,00, que custam 0,5 ponto por não gerar Infecção) — o mesmo perfil de ameaça, mesmo preço,
> mesmo sem a saída social do Saqueador.

#### 20.1.4 Zumbi Guia

| | |
|---|---|
| **ND / Custo** | 1 · **1 ponto** — *medido acompanhado; não se dobra (§4.3)* |
| **HP / Defesa** | 12 / 15 |
| **Ataque / Dano** | **não ataca** |
| **Movimento / Tamanho** | 8 hex · Médio |
| **Gera Infecção?** | **Não** |
| **Uiva?** | **Não** — guia por gesto, não por grito; é o par silencioso do Uivante |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Direção (raio 4 hex):** no turno dele, movimenta-se e aponta uma direção. Todo Zumbi comum no raio que ainda for agir nesta rodada ganha **Vantagem** no ataque que fizer. Nunca ataca, nunca gera Infecção, nunca produz Ruído nem Atração |

**Ele é o Vigia ao contrário.** O Vigia (§7.6) ameaça o Medidor de Horda sem tocar seu personagem; o
Zumbi Guia ameaça a Trilha de Infecção sem tocar seu personagem — não morde ninguém, mas faz os
zumbis à volta dele morderem com mais certeza. É o par silencioso do Uivante (§8.2): o Uivante chama
reforço gritando (Ruído Alto, Atração); o Guia coordena a briga já em andamento, por gesto, sem
alimentar o Medidor. O Uivante cobra em Horda, o Guia cobra em Infecção.

**Não recebe a exceção "0 pontos sozinho" do Vigia** — essa regra (§4.3) é só dele. O Zumbi Guia segue
a regra do Uivante/Doutora: custa 1 ponto acompanhado, cheio, sem fator de dobra.

> **Medido em 8.000 iterações**, acompanhado de dois Zumbis comuns (precedente do §4.3). O trio sem o
> Guia perde 2,7% HP / 0,23 Infecção; com ele dando Vantagem a ambos todo turno, sobe para **7,5% HP /
> 0,64 Infecção** — um ganho atribuível a ele de +4,8 pontos/+0,41, quase idêntico ao ganho de
> adicionar um **terceiro Zumbi de verdade** ao grupo (+5,3/+0,46 na mesma faixa). Por isso custa o
> mesmo de um Zumbi comum: 1 ponto, mesmo nunca atacando.

### 20.2 Patamar 2 — ND 2–3

#### 20.2.1 Fungo Ambulante

| | |
|---|---|
| **ND / Custo** | 2 · **7 pontos** |
| **HP / Defesa** | 22 / 13 |
| **Ataque / Dano** | +5 · **1d6+1 Químico** |
| **Movimento / Tamanho** | 3 hex · Médio |
| **Gera Infecção?** | **Sim — só pela aura** (o ataque é Químico, não toca a Trilha) |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Químico |
| **Habilidade** | **Nuvem de Esporos (1 hex):** toda criatura que começa o turno adjacente ao Fungo testa **CON CD 12**. Falha: **1d4 Químico e 1 ponto de Infecção**. Sucesso: nada |

O conceito original — "aplica Infecção sem rolagem de ataque" — era uma aura pura, igual ao Miasma do
Gigante. O Diretor cortou isso de propósito: o Miasma é ND 5 e a Aura Venenosa do Zumbi Venenoso (CON
CD 14) é ND 4 — dar o mesmo mecanismo automático a uma criatura de ND 2 romperia a curva do §3.1 antes
da hora. O teste é o preço de trazer o mecanismo para baixo na escala: CD 12 fica abaixo da CD 14 do
Venenoso (mais fácil de resistir, porque o Fungo é dois ND mais fraco), e o raio de 1 hex (contra os 2
do Venenoso) é o segundo freio — só quem já está no corpo a corpo paga.

Resistente a Químico, não Imune: a trava do §13 reserva Imune para quem é feito *só* daquilo, e o
Fungo também tem corpo orgânico que queima.

> **Medido em 8.000 iterações.** Acompanhado de 2 Zumbis (mesmo formato do Venenoso): **P1 12,6% ·
> 1,08 Infecção**; **P2 4,3% · 0,69**. A Infecção por combate já supera a de 2× Mutante sem
> Regeneração medido pelo mesmo método (0,81 somado). Os 7 pontos ficam entre Mutante (6,5, Infecção
> condicionada ao ataque) e Casulo (8, "vale pelo que gera"): mais caro que o Mutante porque a aura não
> depende de acertar; mais barato que o Casulo porque não escala com o tempo.

#### 20.2.2 Zumbi Viscoso

| | |
|---|---|
| **ND / Custo** | 2 · **2,5 pontos** |
| **HP / Defesa** | 26 / 13 |
| **Ataque / Dano** | +5 · **1d4+1 Necrótico** |
| **Movimento / Tamanho** | 3 hex · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | **Lodo Pegajoso:** ao acertar, o alvo testa **AGI CD 13** ou tem o deslocamento reduzido à metade (arredondado para baixo) até o fim do seu próximo turno |

Dano baixo de propósito — a ameaça dele não é HP, é posição. A diferença para o Tornozelo do
Arrastador é deliberada: o Arrastador **para** o alvo (Agarrado, precisa de teste oposto para
escapar); o Zumbi Viscoso só reduz à metade, sem travar ninguém, e o efeito **expira sozinho**, sem
custar uma Ação para se livrar. A CD 13 reaproveita o número do Arrastador de propósito — o efeito é
mais fraco, então a mesma CD num ND mais alto ainda é justa. É "lama que atrasa", não "garra que
prende": uma leva de Viscosos não impede recuar, torna recuar **caro**.

> **Medido em 8.000 iterações.** Acompanhado de 2 Zumbis: **P1 10,0% · 0,86**; **P2 3,2% · 0,48** —
> abaixo do limiar "moderado" nos dois critérios do §4.4, consistente com uma criatura de controle, não
> de atrito. 2,5 pontos ficam entre o Zumbi Resistente (2, sem efeito) e o Touro/Uivante (3–3,5).

#### 20.2.3 Zumbi Corrosivo

| | |
|---|---|
| **ND / Custo** | 3 · **5 pontos** |
| **HP / Defesa** | 30 / 13 |
| **Ataque / Dano** | +6 · **1d6+2 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | **Sim — pelo ataque.** A aura ataca o **equipamento**, não a Trilha |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Químico |
| **Habilidade** | **Aura Corrosiva (1 hex):** toda criatura que começa o turno adjacente testa **CON CD 13**. Falha: rola 1d6 na tabela de local (`docs/gdd/GDD_Equipamentos.md` §3) e a peça atingida desce **um estado de desgaste** (sem peça correspondente: nada acontece). Sucesso: nada |

Primeira criatura do Bestiário que ataca o **equipamento** diretamente, não como efeito colateral de
crítico — Rasgar (Touro Mecânico) e Crítico 19–20 (`docs/gdd/GDD_Equipamentos.md` §3.2) exigem um ataque
acertar primeiro; o Corrosivo inverte isso com uma aura recorrente, sem rolagem de ataque, e é
exatamente por isso que o teste de resistência aqui é obrigatório — sem CD, dado o custo de reparo de
Equipamentos §4 (até 1 Liga Pré-Queda para peça Épica, o gargalo do jogo), qualquer peça boa seria
insustentável contra um só inimigo. Reaproveita o 1d6 de localização do próprio Equipamentos §3 — não
precisa de tabela própria.

Esta criatura fecha a pendência de `docs/gdd/GDD_Equipamentos.md` §11: *"Criaturas quebra-armadura além do
Touro — Bloco 5."*

> **Medido em 8.000 iterações.** Acompanhado de 2 Zumbis: **P1 12,3% HP · 0,96 Infecção · 1,13
> eventos de desgaste**; **P2 3,9% · 0,55 · 0,74**. O ritmo de ~1,1 degradação por combate em P1 é
> comparável ao Rasgar do Touro (garantido, mas só 1×/combate), apesar de ser probabilístico. Os 5
> pontos replicam de propósito o custo da Doutora Zumbi (ND 3, 5 pontos) — as duas são "especialistas
> de recurso secundário": a Doutora ataca o tempo de combate do grupo, o Corrosivo ataca o orçamento de
> manutenção. **Nota em aberto para o Diretor:** os critérios de rótulo do §4.4 (HP e Infecção) não têm
> banda para "desgaste de equipamento" — esta é a primeira criatura cuja ameaça principal não é medida
> por nenhum dos dois eixos existentes.

#### 20.2.4 Posto Automatizado

| | |
|---|---|
| **ND / Custo** | 3 · **4 pontos** |
| **HP / Defesa** | 32 / 15 |
| **Ataque / Dano** | +9 · **2d6 Balístico** |
| **Movimento / Tamanho** | **0 hex** · Médio |
| **Gera Infecção?** | **Não** |
| **Uiva?** | Não |
| **Vulnerável** | Elétrico/EMP |
| **Resistente** | Perfurante |
| **Habilidade** | **Sensor de Movimento:** ataques contra quem se moveu neste turno têm **Vantagem** · **Hackear** (Ação, a até 1 hex): teste de **Mecânica ou Eletrônica CD 15** — Vantagem com um **Kit de Eletrônica** (`docs/gdd/GDD_Equipamentos.md` §10.8). Sucesso: o Posto fica **Inerte**; quem o hackeou pode, em qualquer turno futuro, gastar a própria Ação para **Operá-lo** — ele ataca com a ficha acima contra o alvo escolhido. Falha: nada muda, mas o próximo ataque do Posto contra quem tentou tem Vantagem |

Torreta de segurança pré-Queda, Movimento 0: a ameaça é **precisão**, não mobilidade. O Sensor de
Movimento pune quem se move, em vez de ignorar cobertura como o Cuspidor — uma tensão nova, entre
Desengajar e ficar parado.

**Sobre poder ser operada pelo jogador:** fica **Inerte** por padrão, com Operar como extensão presa
à própria Ação de quem a hackeou, nunca como "ela luta pelo grupo" automaticamente — transformá-la em
aliado ativo exigiria lhe dar turno próprio na iniciativa, e nenhuma das criaturas existentes faz isso
no meio do combate. A CD 15 reaproveita o número do Saqueador Humano (Persuasão/Intimidação CD 15,
§7.6); o Kit de Eletrônica (Equipamentos §10.8) ganha, com isso, um uso de combate.

Perfil Elétrico/EMP vulnerável e Perfurante resistente repete o padrão de máquina já canônico (Touro
Mecânico, Zumbi Cibernético) — é metal, não carne.

> **Medido em 8.000 iterações.** Sozinho: 6,7% de HP do grupo contra Defesa 15, 1,9% contra Defesa 17.
> 2× Posto deu 25,0% de HP em P1 — acima do que a fórmula `(4+4)×M(2)=12` prevê. O mesmo desvio
> apareceu com 2× Touro Mecânico (30,9%) e, num teste de confirmação à parte, com 4× Saqueador Humano
> (20,9%, contra 6 pontos previstos — "fácil" pela fórmula). O padrão é geral — `M(n)` subestima
> pilhas de criatura sem Infecção — e está documentado como limitação aceita em §4.5, com mitigação
> prática (suba o rótulo em um degrau nesses encontros).

### 20.3 Patamar 3 — ND 3–4

#### 20.3.1 Carcaça de Aço

| | |
|---|---|
| **ND / Custo** | 3 · **7 pontos** |
| **HP / Defesa** | 32 / **18** |
| **Ataque / Dano** | +8 · **1d6+1 Necrótico** |
| **Movimento / Tamanho** | **2 hex** · Médio |
| **Gera Infecção?** | **Sim** |
| **Uiva?** | Não |
| **Vulnerável** | Concussão |
| **Resistente** | Perfurante, Balístico |
| **Habilidade** | — |

Testa uma pergunta que a escala de Defesa (`docs/gdd/GDD_Combate.md` §5.3) deixou aberta: existe criatura
cujo design inteiro é Defesa, sem efeito nenhum por trás? Defesa 18 é mais alta que qualquer criatura
do catálogo atual — até mais que o Gigante Mutagênico (16, ND 5). Chega lá do jeito mais simples
possível: chapas de sucata soldadas no corpo, sem HP extra, sem segunda habilidade. O preço é
Movimento: 2 hex, a metade do Zumbi comum — nunca alcança quem recua.

A diferença para o Touro Mecânico é que o Touro paga Defesa comum (15) com dano alto e Investida; a
Carcaça paga tudo em Defesa e cobra em rodadas. E continua sendo zumbi por dentro: o ataque é
Necrótico, então cada rodada extra tentando furar essa Defesa é uma rodada inteira de risco de
Infecção que ninguém escolheu correr.

> **Medido em 20.000 iterações**, grupo de Patamar 2 contra a Carcaça sozinha: 3,0% de perda de HP,
> 0,35 de Infecção por personagem, 3,2 rodadas médias até morrer — contra 2,2%/0,18/2,2 rodadas do
> Mutante (ND 2, 6,5 pts). Supera o Mutante nos dois eixos apesar do ataque mais fraco, porque a
> Defesa alta estende a luta, e luta mais longa aqui significa mais Necrótico recebido. Por isso 7
> pontos: acima do Mutante, longe do Zumbi de Sangue (18, que tem explosão medida aparte).

#### 20.3.2 Parasita de Controle

| | |
|---|---|
| **ND / Custo** | 3 · **4 pontos** |
| **HP / Defesa** | 20 / 14 |
| **Ataque / Dano** | +8 à distância, **10 hex** · **1d4 Perfurante** |
| **Movimento / Tamanho** | 7 hex · Miúdo |
| **Gera Infecção?** | Não |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | — |
| **Habilidade** | **Controle parasitário:** se o alvo atingido já está **debilitado** (HP atual ≤ metade do máximo), ele testa **CON CD 14**; se falhar, fica **Controlado** até o início do seu próprio próximo turno — o Mestre assume a ação dele, que se move e ataca o aliado mais próximo com a arma que já tem em mãos, usando ataque e dano normais |

Não é feito para ferir — é feito para fazer **você** ferir o próprio grupo, e só funciona quando o
grupo já pagou um preço antes dele aparecer. O gatilho é "HP ≤ metade do máximo", não Sangrando:
Sangrando ainda está `[A CALIBRAR]` (§18), e amarrar uma criatura nova a uma regra sem número seria o
motor inventando valor padrão, que a Aprovação 025 proíbe. O atributo de resistência é CON — o mesmo
que já resiste a Infecção, Radiação e Veneno (`docs/gdd/GDD_Combate.md` §3).

> **Medido em 20.000 iterações.** Contra um grupo saudável, o Controle disparou **zero vezes**. Com o
> grupo a 60% do HP máximo, disparou em **16–27%** das lutas, causando em média **0,55–0,99 ponto**
> de dano entre aliados por luta; a 45% do HP máximo, a frequência sobe para **62–65%** e o dano de
> fogo amigo chega a **2,2–2,4 por luta**. Como o Vigia, o número da tabela não é o número que importa
> na mesa: numa campanha sem descanso entre cenas — o gênero que MUTAGEN:ZERO simula —, é a criatura
> que faz o personagem mais ferido virar, por uma rodada, o problema do grupo.

#### 20.3.3 Mutante Encouraçado

| | |
|---|---|
| **ND / Custo** | 4 · **9 pontos** |
| **HP / Defesa** | 50 / 15 |
| **Ataque / Dano** | +10 · **1d10+3 Perfurante** |
| **Movimento / Tamanho** | 4 hex · Médio |
| **Gera Infecção?** | Não |
| **Uiva?** | Não |
| **Vulnerável** | Concussão |
| **Resistente** | Perfurante |
| **Habilidade** | **Espinhos Rasgantes** *(Rasgar, variante)*: dano Perfurante dos espinhos ósseos. Toda vez que acerta — sem limite por combate —, o alvo testa **AGI CD 14**; se falhar, a peça de armadura atingida desce **um estado de desgaste**, mesmo sem crítico (`docs/gdd/GDD_Equipamentos.md` §3.2) |

Resolve duas pendências de `docs/gdd/GDD_Equipamentos.md` §11 com a mesma decisão: o dano é **Perfurante**,
não Necrótico — a primeira criatura **fora do controle do Mestre** a causar Perfurante como fonte
primária — e por isso, pela regra do §5, **não gera Infecção**: espinho ósseo não é mordida. Entra na
família do Touro Mecânico (§8.4) — efeito sem Trilha — com Rasgar deliberadamente diferente: o Touro
arranca a armadura uma vez, garantido (1×/combate, sem teste); o Mutante Encouraçado tenta em todo
acerto, mas o alvo pode resistir (AGI CD 14). É a variante "mais generosa com a vítima" pedida pelo
Diretor — cada aplicação é incerta, mas sem teto de uso, o que lhe dá, numa luta mais longa, frequência
de erosão comparável à do Touro por um caminho probabilístico em vez de garantido.

> **Medido em 20.000 iterações**, grupo de Patamar 2 contra o Mutante Encouraçado sozinho: 7,5% de
> perda de HP em 3,5 rodadas médias — mais que o dobro do Touro Mecânico (4,2%) e do Cuspidor (3,6%),
> as âncoras sem Infecção. 0,00 de Infecção, idêntico às duas âncoras. O teste de Rasgar variante
> disparou em média 0,96 vez por luta, próximo do garantido do Touro. A ausência total de Infecção é o
> que mantém o custo (9) bem abaixo do Zumbi Venenoso (30) ou do Gigante (132).

### 20.4 Patamar 4 — ND 6–7 *(primeira faixa inteiramente nova)*

> **Nota de metodologia.** Estas quatro fichas foram calibradas pela metodologia de **orçamento**
> (grupo de 4, ataque+5/dano 1d8+3 fixos — o par que §3 e §19 já usam para medir pontos), não pela
> metodologia dos "panoramas medidos" de §4.6 (que escala os dois lados). A âncora de validação foi o
> próprio **Gigante Mutagênico**: medido com os mesmos parâmetros fixos contra Defesa 20, deu **19,6%
> de HP / 3,25 de Infecção** — "difícil" por §4.6, e **132 pontos bate quase exato** com o limiar
> "difícil" de Patamar 4 (~130). Isso validou o método usado abaixo.

#### 20.4.1 Colmeia Ambulante

| | |
|---|---|
| **ND / Custo** | 6 · **120 pontos** |
| **HP / Defesa** | 95 / 15 |
| **Ataque / Dano** | +13 · **2d6+3 Necrótico** |
| **Movimento / Tamanho** | 4 hex · Grande |
| **Gera Infecção?** | **Sim — por ataque E por aura** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico |
| **Habilidade(s)** | **Zumbido Constante (2 hex):** toda criatura que começa o turno no raio testa **CON CD 15**; falha = 1 ponto de Infecção. **Cisão:** ao chegar a 0 HP, libera **3 Insetos Mutantes** (ND 0: HP 4 · Defesa 15 · Ataque +5 · 1d4 Necrótico · Movimento 6 hex · Miúdo · Gera Infecção: Sim · Vulnerável: Fogo) nos hexágonos adjacentes |

Um amontoado ambulante de insetos fundidos pela mutação — não um inseto gigante, um **enxame com
forma**. É a prova de que o padrão do Gigante (aura + cisão, §12) não é um truque de uma criatura só:
é um mecanismo **reutilizável**. A diferença deliberada é que o **Zumbido testa e o Miasma não** — o
Gigante foi a primeira criatura a provar, sem ambiguidade, que aura e cisão desacoplam Trilha de HP, e
seu automatismo é a exceção que se ganhou; toda aura nova a partir daqui é testável, por exigência
desta rodada de aprovação. O preço de ser testável é pago em área, não em certeza: raio de **2 hex**
contra o 1 do Gigante — ameaça quem se aglomera, de um jeito que o Gigante não ameaça.

> **Medido em 20.000 iterações**, grupo de orçamento contra Defesa 20. Com o grupo inteiro dentro do
> raio todas as rodadas (pior caso): **8,8% de HP / 4,08 de Infecção** — a Colmeia **supera o Gigante**
> (3,25) nesse cenário, apesar do teste. Com só 1 personagem engajado por rodada (cenário realista):
> Infecção cai para **1,79** (moderado). A lição de mesa: contra a Colmeia, aglomerar é o erro — nunca
> verdade contra o Gigante, cujo raio de 1 hex só pune quem já está em corpo a corpo.

#### 20.4.2 Devorador de Aço

| | |
|---|---|
| **ND / Custo** | 6 · **70 pontos** — *pela via HP/Trilha; o custo real está em equipamento, ver nota* |
| **HP / Defesa** | 110 / 16 |
| **Ataque / Dano** | **+9** *(reduzido de propósito — a linha cheia do ND 6 é +13)* · **2d8+3 Concussão** |
| **Movimento / Tamanho** | 5 hex · Grande |
| **Gera Infecção?** | **NÃO** — Concussão, não Necrótico (mesmo perfil do Touro Mecânico) |
| **Uiva?** | Não |
| **Vulnerável** | Elétrico/EMP |
| **Resistente** | Perfurante, Balístico |
| **Habilidade(s)** | **Mandíbulas Trituradoras:** a cada acerto (não só crítico), a peça de equipamento atingida — sorteio de 1d6 de local, como de costume (`docs/gdd/GDD_Equipamentos.md` §3) — desce **um estado de desgaste**. Sem limite por combate, ao contrário do Rasgar do Touro (1×) |

Metade zumbi, metade sucata: mastiga placa como se fosse osso. É o Touro Mecânico levado ao limite —
mesmo dano sem Infecção, mesma vulnerabilidade de máquina, mesma resistência de corpo blindado — mas
o Rasgar 1×/combate do Touro virou **sem limite**. O ataque precisou ser reduzido de propósito: um
"sem limite" na linha cheia de ND 6 (+13) destruiria uma peça por combate, o que não é mais traço de
criatura, é punição. Reduzido a +9 (~43% de acerto contra Defesa 20, era ~70%), o Diretor pediu
exatamente essa baixa chance de acerto.

> **Medido — efeito real na durabilidade**, comparado ao ritmo de `docs/gdd/GDD_Equipamentos.md` §3.1–3.2.
> No combate de orçamento (luta de ~7,5 rodadas), o Devorador acerta o Corpo com frequência suficiente
> para destruir a peça em **1,83 combates de aparição constante**; com o personagem real de Patamar 4
> (arma melhor, luta mais curta), sobe para **4,53 combates**. Ajustando para a mesma taxa de
> aparição do Touro (1/4 dos encontros, §3.2), o cenário com equipamento real dá **≈ 6 combates por
> ponto de Defesa perdido** — quase igual ao Touro; o cenário de orçamento dá **≈ 2,4**, 2 a 3× mais
> rápido. **Aviso de mesa:** um grupo sub-equipado sofre a erosão bem mais rápido que a referência do
> Touro prevê. Pelos eixos que o orçamento mede (HP, Infecção) ele sai **fácil** (9,7%/0) — como o
> Vigia (§4.3), isso **subestima** o custo real, que é ao inventário, não ao personagem. Por isso o
> preço (70) fica abaixo do piso "moderado" (90): é a tradução justa do que o modelo mede, com o
> desgaste de equipamento cobrando separadamente (ver §18, "terceira banda").

#### 20.4.3 Enxame de Morcegos Mutantes

| | |
|---|---|
| **ND / Custo** | 6 · **100 pontos** |
| **HP / Defesa** | 80 / 17 |
| **Ataque / Dano** | +13 · **2d6+2 Perfurante** |
| **Movimento / Tamanho** | 8 hex (voador) · Médio |
| **Gera Infecção?** | **NÃO** — Perfurante, não Necrótico |
| **Uiva?** | Não |
| **Vulnerável** | Concussão |
| **Resistente** | — |
| **Habilidade(s)** | **Voo Errático:** ataques corpo a corpo comuns (alcance 1 hex) contra o Enxame têm **Desvantagem** — nunca está exatamente onde a mão chega. Armas de alcance estendido, ataques à distância e efeitos de área não são afetados |

Preenche a pendência de `docs/gdd/GDD_Equipamentos.md` §11 — mordida/garra Perfurante real, fora da
escolha do Mestre. **Médio, não Grande:** tamanho no MUTAGEN é sobre massa e ocupação de hex
(`docs/gdd/GDD_Combate.md` §14), e o Enxame é sobre velocidade, não massa. **Vulnerável a Concussão, não
Fogo** — primeira variação do trope: espingarda, granada e coronhada dispersam um enxame de um jeito
que lâmina ou rifle não. O **Voo Errático inverte o dilema usual**: em toda outra criatura que gera
Infecção, corpo a corpo é arriscado e a distância é segura (mas custa Horda); aqui a Trilha nunca entra
— mas o corpo a corpo vira taticamente pior, então o jogador é empurrado à arma de fogo pela eficácia,
não pelo medo da Infecção, e paga o mesmo preço de sempre: o Medidor de Horda.

> **Medido.** Grupo priorizando distância: **8,0% de HP**, 0 Infecção → fácil. Forçado ao corpo a
> corpo: **20,1%** → moderado. O rótulo depende de quem decide — a leitura de mesa é o ponto.

#### 20.4.4 Sentinela Corporativa

| | |
|---|---|
| **ND / Custo** | 6–7 · **230 pontos** |
| **HP / Defesa** | 100 / **20** |
| **Ataque / Dano** | +14 · **2d8+4 Balístico** |
| **Movimento / Tamanho** | 5 hex · Médio |
| **Gera Infecção?** | **NÃO** — construto pré-Queda, nem morto-vivo nem mutante (mesmo motivo do Saqueador, Cachorro Explosivo, Touro e Casulo) |
| **Uiva?** | Não |
| **Vulnerável** | Elétrico/EMP |
| **Resistente** | Perfurante, Balístico |
| **Habilidade(s)** | **Duas ações** por rodada (padrão de ND alto, como o Gigante) · **Sistema de Combate Corporativo:** nunca recarrega, nunca trava · **Crítico com 19 ou 20 natural** (`docs/gdd/GDD_Equipamentos.md` §3.2), em vez de Rasgar |

A primeira criatura canônica que **não é** morto-vivo nem fruto direto da mutação: um robô de
segurança corporativo hibernando desde a Queda, ainda executando o protocolo original. **A Defesa 20
é a resposta certa ao personagem Furtivo, não ao tanque** — quem é blindado sofre uma luta difícil e
aguenta; quem construiu Defesa alta via AGI e HP baixo para nunca ser acertado descobre que **Crítico
19–20** o encontra duas vezes mais vezes, e um crítico contra HP baixo é letal de um jeito que o
acerto comum nunca seria. A Defesa alta dela não é sobre ser difícil de ferir — é sobre fazer o
jogador duvidar que vale a pena tentar.

> **Medido.** Metodologia de orçamento: **49,3% de HP perdido**, 0 Infecção, 2,03 críticos por
> combate, wipe 1,47% → **difícil**. Com o personagem real de Patamar 4: **16,6%**, 0,67 críticos →
> cai para moderado-alto — o comportamento correto de um miniboss, morder bem mais um grupo
> mal-equipado que um bem-equipado.

#### 20.4.5 Nota sobre os limiares provisórios do Patamar 4 (§4.4)

**Moderado (~90) e difícil (~130) se sustentam.** A ordem medida — Devorador (70, de propósito,
abaixo do piso) < Morcegos (100) < Colmeia (120) < Gigante (132) < Sentinela (230) — é monotônica e
os dois limiares baixos não pedem ajuste. **Mortal (~300) parece calibrado para pares ou pequenos
grupos de ND 6–7, não para uma criatura solo:** a Sentinela, o kit mais agressivo deste lote, ficou em
230 pontos e 49,3% de HP (difícil, não mortal, wipe de só 1,47%). É consistente com o que §4.5 já
avisa ("criatura sozinha: continua o pior caso, o grupo mata antes que ela aja") — um "mortal sozinho"
de Patamar 4 pode genuinamente não existir até ND 8+, e 300 continuar correto como teto para
**combinações**. Confirmado abaixo com os dados do Patamar 5.

### 20.5 Patamar 5 — ND 8–10 *(teto da escala, clímax de campanha)*

> **Nota de metodologia — divergência entre lotes, não resolvida, declarada.** Este lote foi medido
> contra a party **totalmente escalada** de Patamar 5 (`docs/gdd/GDD_Bestiario.md` §5: Ataque +11, Dano
> 1d12+5, HP 136, Defesa 21) — a mesma convenção dos "panoramas medidos" de §4.6. O lote do Patamar 4
> (§20.4) usou a convenção de **orçamento** (party com ataque+5/dano 1d8+3 fixos, só a Defesa
> variando), validada contra o Gigante. Tentei reconciliar os dois convertendo as cinco fichas abaixo
> para a convenção de orçamento antes de publicar — e a simulação de verificação não reproduziu o
> número-âncora do Patamar 4 (Gigante a Defesa 20 = 19,6%/3,25) com confiança suficiente para confiar
> no resultado convertido. **Por isso os pontos abaixo ficam como o agente do Patamar 5 mediu — na
> convenção escalada —, sem conversão forçada.** Isto significa que comparar diretamente um ponto do
> §20.4 com um ponto do §20.5 pode não refletir ameaça relativa real; os dois lotes precisam de uma
> segunda passada de validação cruzada antes que a tabela de pontos ND 6–10 seja tratada como
> definitiva. Registrado para o Diretor decidir a prioridade disso.

#### 20.5.1 Enxame-Rainha

| | |
|---|---|
| **ND / Custo** | 8 · **260 pontos** |
| **HP / Defesa** | 125 / 18 |
| **Ataque / Dano** | +16 · **2d6+3 Necrótico** |
| **Movimento / Tamanho** | 6 hex · Grande |
| **Gera Infecção?** | **Sim — por ataque e pela aura** |
| **Uiva?** | Não — mas eleva o Medidor de Horda sozinha, sem gritar |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante |
| **Habilidade(s)** | **Secreção da Prole (2 hex):** criatura que começa o turno no raio sofre **1d6 Necrótico** e testa **CON CD 16** ou ganha 1 ponto de Infecção · **Grito de Comando (6 hex):** zumbis e mutantes no raio curam **5 HP** no início do turno dela e têm Vantagem no próximo ataque · **Chamado Constante:** enquanto viva, o Medidor de Horda sobe **+5** no fim de cada rodada, independentemente de ruído |

É o Vigia reescrito em escala de clímax: o Vigia ataca o Medidor num gesto (+10, sair do mapa); a
Enxame-Rainha ataca o mesmo recurso **continuamente**, todo turno em que respira. A Secreção da Prole
segue o molde do Miasma/Aura Venenosa, com teste (CD 16, mais dura que a do Venenoso porque ND 8 cobra
mais). **O Grito de Comando é quase inútil medido solo** — só funciona com zumbis de verdade ao redor
dela — então o número medido abaixo é **piso, não teto**: ela é desenhada para ser enfrentada dentro
de uma horda, não isolada, do mesmo jeito que medir o Uivante sem nenhum mutante por perto já
subestimaria ele.

> **Medido em 8.000 iterações** (convenção escalada, §5): **13,5% de HP perdido · 2,83 de Infecção
> por personagem · ~4,3 rodadas até cair · 0% de wipe.** Morre rápido quando focada (HP baixo de
> propósito — é suporte, não tanque), mas em 4 rodadas já entrega quase o dobro da Infecção de um
> Gigante sozinho numa luta inteira (1,7). Acompanhada do próprio bando que ela potencializa, o custo
> efetivo de mesa é maior que os 260 pontos medidos aqui.

#### 20.5.2 Matriarca Mutagênica

| | |
|---|---|
| **ND / Custo** | 8 · **255 pontos** |
| **HP / Defesa** | 130 / 18 |
| **Ataque / Dano** | +16 · **2d8+4 Necrótico** |
| **Movimento / Tamanho** | 5 hex · Grande |
| **Gera Infecção?** | **Sim — por ataque e pelos Zumbis que gera** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Necrótico |
| **Habilidade(s)** | **Oviposição:** processo contínuo que não consome a Ação — a cada rodada em que houver menos de **4 Zumbis (ND 0)** vivos gerados por ela, nasce um adjacente a si; ela ataca normalmente no mesmo turno · **Regeneração:** cura **3 HP** no início de cada turno seu, anulada se sofreu dano de Fogo desde o fim do turno anterior |

**Decisão de design testada e revertida por medição.** A primeira versão a fazia gerar um **Casulo**
(§9.1) que gerava os Zumbis, reaproveitando a peça existente — mas a luta esticou para ~22 rodadas: o
Casulo (25 HP) nunca é o alvo de menor HP enquanto houver Zumbis (12 HP) por perto, então sobrevive o
bastante para repor indefinidamente, e o grupo fica preso numa esteira sem fim — ritmo errado para uma
cena de clímax. A segunda versão (Oviposição concorrendo pela Ação) ficou mais fraca que o próprio
Gigante solo. A versão final — gera Zumbis direto, em paralelo, sem gastar a Ação — foi a que sobrou de
pé, e faz sentido temático: ela **se move e gesta ao mesmo tempo**; o Casulo não se move e por isso
precisa gestar sozinho.

> **Medido em 8.000 iterações** (convenção escalada): **15,6% de HP perdido · 2,04 de Infecção por
> personagem · ~9,4 rodadas · 0% de wipe.** Supera o Gigante sozinho nos dois eixos (6%/1,7), com
> ritmo de mesa comparável ao Colosso e ao Núcleo.

#### 20.5.3 Colosso de Sucata

| | |
|---|---|
| **ND / Custo** | 9 · **350 pontos** |
| **HP / Defesa** | 170 / 18 |
| **Ataque / Dano** | +17 · **2d10+5 Concussão** |
| **Movimento / Tamanho** | 6 hex · **ENORME** |
| **Gera Infecção?** | **NÃO** |
| **Uiva?** | Não — move-se com Ruído Alto, mas sem gerar Atração |
| **Vulnerável** | Elétrico/EMP |
| **Resistente** | Perfurante, Balístico |
| **Habilidade(s)** | **Duas ações** por rodada · **Rasgar (3× por combate):** ao acertar, a peça atingida desce um estado de desgaste mesmo sem crítico — o triplo do Touro Mecânico (§8.4, 1×) · **Investida:** como o Touro — FOR CD 17 ou Empurrado 3 hex e Caído · **Nuvem de Estilhaços (1 hex, fim do turno):** criatura adjacente sofre 1d8 Concussão · **Colapso em Sucata (cisão):** ao chegar a 0 HP, desmorona em **2 Drones de Sucata** (ND 2: HP 20/Defesa 14, +7, 1d8 Concussão) que continuam a luta |

O quebra-armadura definitivo: Concussão, não Necrótico, mantendo-o entre as criaturas "seguras para o
corpo a corpo" (§14) mesmo no teto da escala. Três Rasgar por combate (em vez de um) é o ponto em que
o Mestre precisa decidir se vale gastar reparo de emergência no meio da luta — a peça pode descer dois
estados antes do fim do combate. A Cisão em Drones (não em Zumbis) mantém sua identidade "limpa" (sem
Trilha) do início ao fim.

> **Nota para §4.5.** O par %HP/Infecção rotularia o Colosso como "moderado" (28,9% HP, 0 Infecção) —
> claramente errado para o quebra-armadura definitivo do jogo. O custo de 350 pontos não vem dessa
> leitura: inclui o valor do desgaste de equipamento que a simulação de HP/Infecção não mede, na mesma
> lógica que Casulo e Zumbi de Sangue já são "medidos, não calculados" (§4.5). Reforça o mesmo achado
> do Devorador de Aço e do Zumbi Corrosivo (§18, "terceira banda").
>
> **Medido em 8.000 iterações** (convenção escalada): **28,9% de HP perdido · 0,00 Infecção · ~8,4
> rodadas · 0% de wipe.**

#### 20.5.4 Núcleo Mutagênico

| | |
|---|---|
| **ND / Custo** | 10 · **720 pontos** |
| **HP / Defesa** | 160 / 19 |
| **Ataque / Dano** | +19 · **2d10+6 Necrótico** |
| **Movimento / Tamanho** | 5 hex · **ENORME** |
| **Gera Infecção?** | **Sim — por ataque, por Miasma, pelo Pulso de Mutagênese e pela Cisão** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico, Concussão |
| **Imune** | Agarrado e Enganchar *(tamanho, não dano — como o Gigante)* |
| **Habilidade(s)** | **Duas ações** por rodada · **Miasma (2 hex):** criatura que começa o turno no raio ganha 1 ponto de Infecção, sem teste — o dobro do raio do Gigante · **Pulso de Mutagênese (4 hex, a cada 2 rodadas):** criatura no raio que já tenha ao menos 1 ponto de Infecção ganha **+1 ponto adicional, sem teste** · **Cisão:** ao chegar a 0 HP, transforma-se em **6 Zumbis (ND 0)** — metade mais que o Gigante |

O chefe que `docs/gdd/GDD_Bestiario.md` §3.2 encomendou: *"as criaturas de fim de jogo devem pressionar a
Trilha de propósito, como o Gigante já faz."* É o molde do Gigante com cada parafuso que empurra
Infecção apertado, e nenhum dos que empurram dano: Miasma em raio dobrado, Cisão em produção dobrada e
meia, e o Pulso de Mutagênese como peça nova — não ameaça quem está limpo, só agrava quem já está
contaminado, fechando o cerco sobre quem o grupo já deixou vulnerável. HP e Defesa ficam
deliberadamente comparáveis ao Colosso: se o Núcleo matasse por HP como mata por Trilha, Cisão e
Miasma seriam decoração.

> **Medido em 8.000 iterações** (convenção escalada): **30,8% de HP perdido · 9,93 de Infecção por
> personagem · ~9,6 rodadas · 0% de wipe.** Para contexto: 2× Gigante mede 21%/6,5 (mortal) em §4.6 —
> o Núcleo sozinho supera os dois eixos do combo de dois Gigantes, com quase 6× a Infecção de um
> Gigante solo. Pelo ritmo que §3.2 descreve (6,5 pontos ≈ mutação em três lutas), uma única luta
> contra o Núcleo já aproxima o grupo de duas lutas inteiras de acúmulo — o chefe mais perigoso para a
> Trilha que o Bestiário já teve.

#### 20.5.5 Fonte Zero

| | |
|---|---|
| **ND / Custo** | 10 · **470 pontos** *(piso de uma faixa 470–600 — ver nota)* |
| **HP / Defesa** | 260 / 16 |
| **Ataque / Dano** | **não ataca** |
| **Movimento / Tamanho** | **0 hex** · **ENORME** |
| **Gera Infecção?** | **Sim — apenas pela aura** |
| **Uiva?** | Não |
| **Vulnerável** | Fogo |
| **Resistente** | Perfurante, Balístico, Concussão |
| **Habilidade** | **Aura Crescente:** no início de cada rodada em que sobrevive, o raio e o dado de dano da aura **sobem um degrau** (o teto de 1d12 não limita criatura, `docs/gdd/GDD_Combate.md` §5.3.1). Criatura que termina o turno no raio testa **CON CD (12 + número da rodada)**: falha = dano cheio e 1 ponto de Infecção sem redução; sucesso = metade do dano, sem Infecção |

Não ataca — como o Casulo, mas invertido: o Casulo é um cronômetro de HP baixo e Defesa 10 (acertá-lo
é trivial); a Fonte Zero é o mesmo cronômetro em escala de clímax, com HP alto o bastante para não
morrer de supetão e Defesa baixa o bastante (16) para não depender de acerto — a decisão do grupo nunca
é "conseguimos acertá-la", é "quanto tempo aguentamos ficar perto". Pressão de tempo, não de dado.

| Rodada | Dado | CD de CON | P(falha) | Dano esperado |
|---|---|---|---|---|
| 1 | 1d6 | 13 | 50% | 2,6 |
| 3 | 1d10 | 15 | 60% | 4,4 |
| 5 | 2d8 | 17 | 70% | 7,7 |
| 7 | 2d12 | 19 | 80% | 11,7 |
| 9 | 3d12 | 21 | 90% | 18,5 |
| 10 | 4d12 | 22 | 95% | 25,4 |

Até a rodada 4 ela é administrável, comparável ao Gigante. Depois da rodada 7 fica insustentável mesmo
para quem resiste bem: o CD já supera a Defesa esperada de Patamar 5 (21), e o dano esperado por rodada
já rivaliza com a perda de HP de uma luta inteira contra outra criatura deste lote — é a mecânica, não
uma descrição, que obriga a decisão de queimar tudo ou recuar.

> **Medido em 8.000 iterações, cenário de foco total** (o grupo queima o máximo de dano desde a
> rodada 1, sem distração): **27,7% de HP perdido · 4,07 de Infecção por personagem · ~7,4 rodadas ·
> 0% de wipe.** Isto mede o **melhor caso** — não mede o cenário para o qual ela foi desenhada (grupo
> dividido, atenção fragmentada, luta esticada além da rodada 8–9), porque isso depende de decisão de
> mesa, não de um loop de combate fechado. Por isso o custo deve ser lido como **piso de uma faixa
> (470–600)**, não um número fixo.

#### 20.5.6 Nota sobre os limiares do Patamar 5 (§4.4) — resolvido com a banda Catastrófico

**Moderado (~90) e difícil (~180) se confirmam** — Enxame-Rainha (260) e Matriarca (255) caem dentro
de "difícil", perto do teto. **Mortal (~300) não aguentava o teto a partir de ND 9** — Colosso (350),
Fonte Zero (470+) e Núcleo (720) o superam sozinhos, o Núcleo em 2,4×. O Diretor aprovou a banda
**Catastrófico, a partir de 450** (§4.4), com a orientação explícita de que criatura catastrófica não
é desenhada para ser vencida em combate direto — é fuga, objetivo alternativo ou relógio narrativo.

---

*Este arquivo é canônico (Aprovações 025 e 035). Qualquer alteração exige nova aprovação do Diretor de
Criação. Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*
