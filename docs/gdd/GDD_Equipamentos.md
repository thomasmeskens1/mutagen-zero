# MUTAGEN:ZERO — Equipamentos

> **O que este documento é.** As regras de tudo que o personagem **veste e carrega** — armadura,
> capacete, luvas, botas, óculos, escudo, mochila: os espaços do corpo, como a Defesa de cada peça
> soma, como elas se desgastam, como se consertam, como se modificam e como variam. O **catálogo** de
> peças (Bloco 4b, Aprovação 035) está na Seção 10.

> **Regras relacionadas:** a fórmula de Defesa, as categorias e a curva de ataque por ND em
> `docs/gdd/GDD_Combate.md` §5.2–§5.3.1 · a resistência por material em `docs/gdd/GDD_Combate.md` §6.3 · o
> sistema de Modificações em `docs/gdd/GDD_Modificacoes.md` · a raridade e o saque em `docs/gdd/GDD_Saque.md`.

> **Aprovações 034–035.** Canônico salvo onde o campo diz `[A CALIBRAR]`.

---

## 1. Os espaços de equipamento

| Espaço | Dá Defesa? | Slots de modificação |
|---|---|---|
| **Cabeça** | Sim (Média e Pesada) | 1 |
| **Olhos** | Não — espaço de **informação** | 0 |
| **Corpo** | **Sim — a maior parte** | **2** |
| **Mãos** | Não — espaço de **função** | 1 |
| **Pernas** | Sim | 1 |
| **Pés** | Não — espaço de **função** | 1 |
| **Escudo** | Sim (componente próprio da fórmula) | **2** |
| **Costas** | Não — espaço de **carga** (Mochila, §10.9) | 0 |

**O escudo exige mão livre** e é incompatível com a propriedade **Duas mãos**
(`docs/gdd/GDD_Combate.md` §5.2).

> ### Peças de dois espaços
>
> **Uma peça cujo benefício é forte demais para um espaço só pode ocupar dois.** É o preço dela. O
> caso que criou a regra é o **Capuz de Moletom**, que ocupa **Corpo e Cabeça**: Furtividade é
> passiva demais, e relevante demais, para custar um espaço só.

---

## 2. Como a Defesa do conjunto soma

```
armadura = Defesa do Corpo + Defesa da Cabeça + Defesa das Pernas
Defesa   = 10 + mod. AGI (limitado) + armadura + escudo + cobertura
```

Cada espaço tem um teto por categoria. Os tetos foram montados para que **o conjunto reproduza
exatamente as faixas da Aprovação 029** (Leve +1 a +3, Média +3 a +5, Pesada +5 a +7):

| Espaço | Leve | Média | Pesada |
|---|---|---|---|
| **Corpo** | +1 a +2 | +2 a +3 | +4 a +5 |
| **Cabeça** | +0 | +1 | +1 |
| **Pernas** | +1 | +1 | +1 |
| **Conjunto completo** | **até +3** | **até +5** | **até +7** |

> ### A categoria do conjunto é a da peça mais pesada
>
> É a peça mais pesada que impõe o **limite de AGI** e a **FOR mínima** do conjunto (12 para Média,
> 14 para Pesada). Ninguém de FOR 8 veste um capacete pesado "só na cabeça", e ninguém leva a AGI
> inteira para a Defesa usando perneiras de placa.

**Mãos, Pés e Olhos não dão Defesa.** São espaços de função: Vantagem, deslocamento, informação.

---

## 3. Desgaste — só por crítico

**Estados de desgaste:** **Intacta → Marcada → Rachada → Destruída.**

| Estado | Efeito |
|---|---|
| **Intacta** | — |
| **Marcada** | **−1 de Defesa** da peça (mínimo 0) |
| **Rachada** | **−2 de Defesa**, e **o benefício da peça para**: resistência, Vantagem, efeito |
| **Destruída** | A peça some |

**Cada acerto crítico sofrido faz uma peça descer um estado.** Qual peça é decidido por `1d6`:

| 1d6 | Peça atingida |
|---|---|
| 1–3 | **Corpo** |
| 4 | Cabeça — ou **Olhos**, se não houver nada na cabeça |
| 5 | Pernas |
| 6 | **Escudo** — sem escudo, **Mãos ou Pés**, à escolha do Mestre |

> **Não é "degrau".** A palavra *degrau* já tem cinco sentidos queimados (`docs/gdd/GDD_Glossario.md` §4);
> o desgaste fala em **estado**, como a conservação das armas.

### 3.1 Ritmo medido

Encontros moderados de cada Patamar, 3.000 iterações cada:

| Patamar | Críticos sofridos por personagem por combate | Combates até o conjunto perder 1 de Defesa | Combates até destruir o Corpo **sem reparo** |
|---|---|---|---|
| P1 | 0,13 | 8 | 46 |
| P2 | 0,08 | 12 | 71 |
| P4 | 0,11 | 9 | 53 |
| P5 | 0,10 | 10 | 59 |

**Só com o 20 natural, o conjunto perde cerca de 1 ponto de Defesa por Patamar.** É desgaste real,
mas destruir uma peça leva a campanha inteira. *(O P3 fica fora da tabela: o encontro moderado dele,
dois Zumbis de Sangue, quase não rola ataque, e o número sai distorcido.)*

### 3.2 Quebra-armadura — dois traços de criatura

| Traço | Efeito |
|---|---|
| **Rasgar** | **1× por combate**, ao acertar, a peça atingida desce **um estado** mesmo sem crítico |
| **Crítico 19–20** | A criatura obtém crítico com **19 ou 20** natural |

**Medido:** com uma criatura quebra-armadura em **um quarto dos encontros**, a erosão sobe para **1
ponto de Defesa a cada 5–7 combates**, e a peça de Corpo dura **cerca de três Patamares** sem reparo.
É o ritmo que transforma o reparo na economia do equipamento.

**O Touro Mecânico tem Rasgar** desde esta aprovação (`docs/gdd/GDD_Bestiario.md` §8.4). Os demais
quebra-armadura nascem com as criaturas de ND 6 em diante.

---

## 4. Reparo

Feito com **Mecânica**, na **bancada do Refúgio** ou pela **Oficina de Campo** do Cientista. Cada
reparo devolve **um estado**. O custo segue a **raridade da peça**:

| Raridade da peça | Custo por estado |
|---|---|
| Abundante · Comum | 1 Sucata |
| Incomum | 1 Peças Mecânicas |
| Raro | 1 Componente Incomum |
| **Épico** | **1 Liga Pré-Queda** |

> **Manter uma peça Épica custa o gargalo do jogo.** É coerente com o saque: quem acha um Épico vai
> precisar de Liga para mantê-lo, e Liga é o que menos aparece.

### 4.1 Remendo de campo

Na via **Gambiarra**, em qualquer lugar: Mecânica **CD 13** e **2 Sucata** devolvem um estado — mas a
peça **nunca volta acima de Marcada**. Só a bancada devolve uma peça ao estado **Intacto**.

### 4.2 Peça destruída

**Não se repara.** Uma modificação de **Oficina** instalada nela pode ser salva com Mecânica
**CD 15**; uma de **Gambiarra** se perde junto.

---

## 5. Modificação de equipamento

Equipamento usa o **mesmo sistema de Modificações** das armas (`docs/gdd/GDD_Modificacoes.md`): via
Gambiarra ou Oficina, os oito componentes, porte **Simples** (1 slot) ou **Estrutural** (2 slots).
Os slots de cada espaço estão no §1.

> ### Regra de ouro: modificação de equipamento nunca dá Defesa — dá efeito.
>
> É a mesma frase que governa as armas: *"o poder de tier alto vem de efeito, nunca de dado maior"*
> (`docs/gdd/GDD_Armas.md` §1.1). Se modificação desse Defesa, o teto de +7 por conjunto viraria ficção e
> a curva de ataque da Aprovação 029 deixaria de proteger a Trilha de Infecção.

**As 13 modificações de equipamento** (Bloco 4b, Aprovação 035). Nenhuma dá Defesa — é a regra de
ouro acima, em números:

| Modificação | Onde | Porte | Efeito | Gambiarra | Oficina | CD |
|---|---|---|---|---|---|---|
| **Placa de Liga Pré-Queda** | Corpo · Escudo | Estrutural | **Resistente a Balístico** *(já era canon, `docs/gdd/GDD_Combate.md` §6.3)* | — *(só Oficina)* | Liga ×1, Peças ×1 | 15 |
| Enchimento de Impacto | Corpo · Cabeça · Pernas | Simples | **Resistente a Concussão** — contra o Touro | Sucata ×2 | Peças ×2 | 12 |
| Forro Isolante | Corpo · Mãos · Pés | Simples | **Resistente a Elétrico** | Fiação ×1, Sucata ×1 | Química ×1 | 12 |
| Forro Térmico | Corpo · Pernas · Mãos | Simples | **Resistente a Fogo** | Química ×1, Sucata ×1 | Química ×1, Peças ×1 | 13 |
| Selagem Química | Corpo · Cabeça | Simples | **Resistente a Químico** | Química ×2 | Química ×1, Peças ×1 | 14 |
| Bolsos e Alças | Corpo · Pernas | Simples | **+2 slots** de inventário | Sucata ×1 | Peças ×1 | 8 |
| Abafador | Corpo · Pés · Escudo | Simples | **−1 degrau de Ruído** ao se mover | Sucata ×2 | Peças ×1, Química ×1 | 10 |
| Camuflagem | Corpo · Cabeça · Pernas | Simples | Vantagem em Furtividade **parado** | Sucata ×1 | Química ×1 | 10 |
| Fivelas de Soltura | Corpo · Pernas | Simples | Vantagem para escapar de **Agarrado** | Sucata ×1, Peças ×1 | Peças ×1 | 10 |
| Porta-carregador | Corpo | Simples | **Recarregar 1×/combate** como interação livre | Sucata ×1, Peças ×1 | Peças ×2 | 12 |
| Lanterna Montada | Cabeça · Escudo | Simples | Luz de 6 hex sem mão · Carga (6) | Fiação ×1, Célula ×1 | Eletrônicos ×1, Célula ×1 | 12 |
| Visor | Cabeça | Simples | Imune a **Cego** por estilhaço | Sucata ×1 | Óptica ×1 | 10 |
| Espinhos | Escudo | Simples | O empurrão do escudo causa **1d4 Perfurante** | Sucata ×2 | Peças ×1 | 10 |

> **Enchimento de Impacto é o mais útil da lista agora:** o Touro Mecânico causa Concussão e é o único
> quebra-armadura que existe (`docs/gdd/GDD_Bestiario.md` §8.4).

---

## 6. Resistência por material

A Aprovação 034 **emenda** `docs/gdd/GDD_Combate.md` §6.3:

> **Armadura comum continua sem resistência nenhuma.** Mas uma peça **cujo material é específico** —
> kevlar, borracha, malha metálica — concede **uma** resistência, e isso é o que a distingue de uma
> peça comum da mesma categoria. O caso que motivou a emenda: o **Colete Balístico Civil** é kevlar,
> e por isso é **Resistente a Perfurante**.

Três travas:

1. **Graus de resistência não se somam.** Duas fontes de Resistente a Balístico não viram Muito
   Resistente; vale a maior.
2. **Resistência a Necrótico nunca vem de equipamento.** Seria a armadura que neutraliza o zumbi — e o
   zumbi é o jogo.
3. **Rachada desliga a resistência.** O material rompido não protege.

---

## 7. Variações

> **Uma variação é o item-base com uma modificação já instalada, ou — só para equipamento — o
> item-base em outro material.**

O **Taco c/ Pregos** é uma variação do Taco de Baseball. Um **Capacete de Obra de alumínio** é uma
variação do de aço: mais leve, uma categoria abaixo.

### 7.1 Por que esta definição — as três opções avaliadas

| Opção | O que é | Custo de balanço |
|---|---|---|
| **A — base + modificação** *(adotada)* | A variação é calculada pelas regras de modificação e de material que já existem | **Zero.** O balanço é automático |
| B — item próprio | Cada variação tem ficha própria, como no d20 clássico | ~74 armas × 2–3 variações = **mais de 200 itens** para medir e manter |
| C — só material | Variação muda o material e nada mais | Barata, mas pobre — perde o Taco c/ Pregos, que é o caso mais natural |

A opção A foi escolhida porque **a parte mais medida do projeto é a tabela de DPR das armas**, e
qualquer outra opção abriria uma segunda tabela de armas para manter em paralelo.

### 7.2 As regras

1. **Armas variam só por modificação, nunca por material.** Variação de material numa arma mexeria
   no dado ou nas propriedades, e a tabela de DPR deixaria de ser a fonte da verdade.
2. **A variação ocupa o slot da modificação instalada.** Um Taco c/ Pregos tem o slot do Pregos
   ocupado; o outro continua livre.
3. **A variação herda o tier e a raridade do item-base** — e fica **uma raridade acima** se a
   modificação instalada for de **Oficina**. Variação com **Gambiarra** carrega a penalidade de
   Gambiarra (**+1 na faixa de quebra**): o que se acha pronto no mundo costuma ser remendado.
4. **No saque, a variação aparece como item.** Na bancada, desmonta como qualquer modificação.

> **O efeito econômico, declarado:** achar uma variação poupa o grupo de fabricar a modificação. A
> raridade acima para as de Oficina é o que compensa — elas aparecem menos. As de Gambiarra não sobem
> de raridade porque já pagam em quebra.

O catálogo da Seção 10 lista, para cada item-base, **duas ou três variações nomeadas**.

---

## 8. Vantagem dada por equipamento

> **A Vantagem de equipamento é estreita e permanente.** Ela vale para **um uso** de uma perícia —
> escalar, mas não todo o Atletismo; abrir fechadura mecânica, mas não todo o Arrombamento.

**Exceção:** quando a peça cobre a perícia **inteira**, a Vantagem é **1× por descanso longo**. O caso
que define a exceção é a **Luva do Piloto**, que cobre toda a Pilotagem.

**Por quê.** Vantagem vale, em média, cerca de **+3 a +5** numa rolagem de d20 — mais que a
proficiência que uma Especialização Menor compra no início do jogo. Uma peça Comum que desse Vantagem
permanente numa perícia inteira tornaria a Especialização dispensável. Estreita, ela **complementa**
a Especialização, como o Diretor definiu: quem foca tudo em uma perícia fica forte nela, e
involuntariamente perde potencial nas outras.

---

## 9. Equipamento habilita; nunca replica

> **Um equipamento pode tornar uma ação possível para quem não tem a perícia — nunca pode copiar a
> assinatura de uma classe.**

Um **Kit de Primeiros Socorros** deixa qualquer personagem estancar Sangrando ou estabilizar um
aliado em Estado Crítico — com **Desvantagem** se não tiver Medicina. **Nenhum** equipamento entrega
o *Estabilizar* do Médico, que mexe na Trilha de Infecção.

É a regra que dá **flexibilidade de build**: um Piloto pode virar um bom socorrista combinando a
Especialização *Medicina* com um bom kit. O Médico continua sendo o único que trata a Infecção.

---

## 10. Catálogo de Peças — Bloco 4b (Aprovação 035)

### 10.0 Capacidade de inventário — fixada

**Base, sem mochila: 6 slots.** Número apertado de propósito: o resto do sistema já vive de escassez
medida (nove perícias, não dez; faixa de quebra; Gambiarra que cobra em degradação). Um inventário
generoso por padrão tornaria a Mochila (§10.9) decorativa — com 6, carregar arma, munição e 1–2 Cargas
já aperta, e a escolha de mochila passa a ser a primeira decisão real de build de carga.

### 10.1 CORPO — 16 peças · 2 slots

| Peça | Cat. · Def | FOR | Raridade | Benefício | Variações |
|---|---|---|---|---|---|
| Roupa de Rua | — · 0 | — | Abundante | — | — |
| Jaqueta de Couro Grosso | Leve · +1 | — | Comum | — | c/ Bolsos · c/ Enchimento |
| Macacão de Mecânico | Leve · +1 | — | Comum | Vantagem em Mecânica ao reparar equipamento | c/ Forro Isolante · c/ Bolsos |
| Colete Refletivo de Obra | Leve · +1 | — | Comum | +2 slots de inventário · Desvantagem em Furtividade | c/ Camuflagem |
| Jaleco de Laboratório | — · 0 | — | Comum | Vantagem em Medicina para diagnosticar condição ou veneno | c/ Selagem Química |
| **Capuz de Moletom** — *Corpo + Cabeça* | Leve · +1 | — | Comum | Vantagem em Furtividade, permanente — o 2º espaço é o preço | c/ Camuflagem · c/ Abafador |
| Capa de Chuva Industrial | Leve · +1 | — | Incomum | Resistente a Químico (borracha) | c/ Bolsos |
| **Colete Balístico Civil** | Média · +2 | 12 | Incomum | **Resistente a Perfurante** (kevlar) | c/ Porta-carregador · c/ Bolsos |
| Colete Antimotim | Média · +3 | 12 | Incomum | Imune a Caído por empurrão | c/ Enchimento · c/ Fivelas |
| Jaqueta de Bombeiro | Média · +2 | 12 | Incomum | Resistente a Fogo | c/ Bolsos |
| Colete Tático Militar | Média · +3 | 12 | Raro | Recarregar 1× por combate como interação livre | c/ Placa de Liga · c/ Camuflagem |
| Armadura de Placas Soldadas | Pesada · +4 | 14 | Comum | Ruído +1 degrau ao se mover | c/ Abafador · c/ Enchimento |
| **Placas Balísticas Militares** | Pesada · +5 | 14 | Raro | **Resistente a Balístico** (cerâmica) | c/ Fivelas · c/ Porta-carregador |
| **Colete de Couro Encouraçado** | Média · +2 | 12 | Incomum | **Resistente a Balístico** (couro com placas de sucata cosidas) | c/ Fivelas · c/ Bolsos |
| **Traje de Contenção** | Média · +2 | 12 | Épico | Vantagem no teste de Infecção ao fim do combate | c/ Selagem Química |
| **Exoesqueleto de Carga** | Pesada · +5 | **10** | Épico | O exo carrega o peso: FOR mínima 10 · Carga (6): +2 FOR num teste | c/ Placa de Liga · c/ Fivelas |

> **Resistência a Perfurante não é decorativa.** O Saqueador Humano pode vir armado com besta, arco ou
> lança (`docs/gdd/GDD_Bestiario.md` §7.6) — quem só ataca assim encontra, no Colete Balístico Civil, uma
> resistência real. A troca de material em relação à primeira proposta (Balístico → Perfurante neste
> item, Balístico passando para o Couro Encouraçado e as Placas Militares) preserva o nerf já medido do
> Explorador e o conserto da Lança Artesanal (`docs/gdd/GDD_Combate.md` §6.3).

### 10.2 CABEÇA — 11 peças · 1 slot

| Peça | Cat. · Def | FOR | Raridade | Benefício | Variações |
|---|---|---|---|---|---|
| Boné ou Gorro | — · 0 | — | Abundante | — | — |
| Bandana Molhada | Leve · 0 | — | Abundante | Vantagem contra Químico inalado por 1 combate · descartável | — |
| Capacete de Mineiro | Leve · 0 | — | Comum | Luz de 6 hex sem ocupar a mão · Carga (6) | c/ Visor |
| Capacete de Soldador | Leve · 0 | — | Comum | Imune a Cego por luz · Desvantagem em Percepção visual | c/ Lanterna |
| Máscara de Gás | Leve · 0 | — | Incomum | Imune a aura e gás Químico · Carga (3) filtros, repostos com Química | c/ Visor |
| Capacete de Obra | Média · +1 | 12 | Comum | — | de alumínio *(Leve, 0)* · c/ Lanterna |
| Capacete de Motociclista | Média · +1 | 12 | Comum | Imune a Cego por estilhaço · Desvantagem em Percepção auditiva | c/ Enchimento |
| Capacete Antimotim c/ Viseira | Média · +1 | 12 | Incomum | Imune a Cego por estilhaço e spray | c/ Selagem Química |
| Capacete Balístico Militar | Média · +1 | 12 | Raro | Vantagem contra Atordoado | c/ Lanterna |
| Elmo de Sucata | Pesada · +1 | 14 | Comum | Ruído +1 degrau | c/ Enchimento · c/ Visor |
| **Capacete Corporativo c/ HUD** | Média · +1 | 12 | Épico | Vantagem em Percepção para detectar emboscada · Carga (3) | c/ Lanterna |

> A peça mais pesada limita a AGI do conjunto: o Capacete de Obra (+1, Média) limita a AGI a +2 — é
> para quem tem AGI baixa, não para um personagem ágil.

### 10.3 OLHOS — 10 peças · 0 slots

| Peça | Raridade | Benefício |
|---|---|---|
| Óculos Escuros | Abundante | Vantagem contra Cego por luz |
| Óculos Rachados | Abundante | Vantagem contra Cego · Desvantagem em Percepção |
| Óculos de Proteção | Comum | Imune a Cego por estilhaço |
| Visor de Solda | Comum | Imune a Cego por luz · Desvantagem em Percepção |
| Máscara de Mergulho | Comum | Vantagem contra Químico |
| Binóculo | Incomum | Dobra o alcance de Percepção visual |
| Luneta Destacável | Incomum | Vantagem em Percepção além de 8 hex |
| Óculos de Visão Noturna | Raro | Enxerga no escuro · Carga (4) |
| Monóculo de Diagnóstico | Raro | Ajustado: com Medicina CD 13, vê a banda de Infecção de um alvo |
| Lente Corporativa | Épico | Vantagem em Saber Pré-Queda |

### 10.4 MÃOS — 12 peças · 1 slot

| Peça | Raridade | Benefício | Variações |
|---|---|---|---|
| Luvas de Couro | Abundante | Pegar objeto em chamas ou eletrificado sem dano | c/ Forro Isolante |
| Luvas de Trabalho | Comum | Construção e reparo no Refúgio levam metade do tempo | c/ Forro Térmico |
| Luvas de Atletismo | Comum | Vantagem em Atletismo para escalar | — |
| Luvas Cirúrgicas | Comum | Vantagem em Medicina para estabilizar aliado em Estado Crítico | — |
| Luvas Anti-corte | Comum | Vantagem em testes que envolvem Sangrando | c/ Forro Térmico |
| Luvas de Corrente | Comum | Vantagem em Arrombamento para forçar grade, corrente ou cadeado | — |
| Manopla de Sucata | Comum | Soco 1d4+2 Concussão — Pugilista 1d6+2 | c/ Pregos · c/ Eletrodos |
| Luva do Piloto | Incomum | Vantagem em Pilotagem — cobre a perícia inteira → 1× por descanso longo | — |
| Luvas de Eletricista | Incomum | Imune ao retorno da Vólt-9 em hexágono molhado e a fio vivo | — |
| Luvas Térmicas | Incomum | Pegar e arremessar objeto em chamas | — |
| Luvas Táteis | Incomum | Vantagem em Prestidigitação | — |
| Manopla Hidráulica Corporativa | Épico | Soco 1d6+2 — Pugilista 1d8+2 · Carga (4): +2 FOR num teste | c/ Eletrodos |

### 10.5 PERNAS — 11 peças · 1 slot

| Peça | Cat. · Def | FOR | Raridade | Benefício | Variações |
|---|---|---|---|---|---|
| Calça Jeans | — · 0 | — | Abundante | — | — |
| Calça Cargo | Leve · 0 | — | Comum | +2 slots de inventário | c/ Camuflagem |
| Joelheiras | Leve · 0 | — | Comum | Vantagem em Acrobacia para cair e rolar | — |
| Calça Térmica | Leve · 0 | — | Comum | Vantagem em Vigor contra frio | — |
| Calça de Motociclista | Leve · +1 | — | Comum | — | c/ Bolsos · c/ Enchimento |
| Perneiras de Couro | Leve · +1 | — | Comum | Vantagem para escapar de Agarrado — o Arrastador agarra o tornozelo | c/ Fivelas |
| Calça Tática Militar | Leve · +1 | — | Incomum | 2 slots de modificação em vez de 1 | c/ Bolsos · c/ Camuflagem |
| Calça de Bombeiro | Média · +1 | 12 | Incomum | Atravessa hexágono em chamas sem dano | c/ Bolsos |
| Saia de Correntes | Pesada · +1 | 14 | Comum | Ruído +1 degrau | c/ Abafador |
| Perneiras de Placa | Pesada · +1 | 14 | Incomum | — | c/ Enchimento |
| Perneiras Anti-mordida | Média · +1 | 12 | Raro | 1× por descanso longo, um acerto Necrótico não gera Infecção | c/ Fivelas |

> A diferenciação é por função, não por Defesa — Pernas dão no máximo +1 em qualquer categoria.

### 10.6 PÉS — 10 peças · 1 slot

| Peça | Raridade | Benefício | Variações |
|---|---|---|---|
| Chinelos | Abundante | −1 hex de deslocamento | — |
| Tênis | Abundante | — | — |
| Botas de Trabalho | Comum | Deslocamento normal em terreno difícil | c/ Abafador · c/ Forro Isolante |
| Botas de Borracha | Comum | Imune a Elétrico vindo do chão | — |
| Botas de Bico de Aço | Comum | Chute 1d4+2 — Pugilista 1d6+2 | — |
| Tênis de Corrida | Comum | +1 hex — não ajuda em terreno difícil | — |
| Botas de Combate | Incomum | Como as de Trabalho, +1 hex em terreno difícil | c/ Abafador |
| Botas de Solado de Feltro | Incomum | −1 degrau de Ruído ao se mover | — |
| Botas Magnéticas | Raro | Vantagem contra empurrão e Caído | — |
| Botas Corporativas Amortecidas | Épico | Ignora as 3 primeiras hex de queda · Carga (4): salto de 2 hex | — |

> **Ordem de operações no terreno difícil:** soma-se o deslocamento total primeiro e **depois**
> aplica-se a metade, arredondando para baixo. Com Tênis de Corrida, 7 hex viram 3.

### 10.7 ESCUDOS — 11 peças · 2 slots

| Escudo | Cat. · Def | FOR | Raridade | Benefício | Variações |
|---|---|---|---|---|---|
| Bandeja de Cantina | leve · +1 | — | Abundante | Frágil: o primeiro crítico a destrói | — |
| Placa de Trânsito | leve · +1 | — | Abundante | — | c/ Espinhos |
| Broquel de Sucata | leve · +1 | — | Comum | — | c/ Espinhos · c/ Lanterna |
| Grade de Ventilação | leve · +1 | — | Comum | Não bloqueia a visão | — |
| Escudo Leve Policial | leve · +2 | — | Incomum | — | c/ Lanterna |
| Tampa de Bueiro | pesado · +3 | 14 | Abundante | Também é arma (1d6) | c/ Espinhos |
| Porta de Carro | pesado · +3 | 14 | Comum | Fincar (Ação): vira meia cobertura para quem está atrás | — |
| Escudo de Placas Soldadas | pesado · +3 | 14 | Comum | Ruído +1 degrau | c/ Abafador · c/ Espinhos |
| Escudo Antimotim | pesado · +3 | 12 | Incomum | Empurra 1 hex | c/ Lanterna · c/ Espinhos |
| Escudo Antimotim Eletrificado | pesado · +3 | 13 | Incomum | Também é arma (1d6) · Carga (4) | c/ Lanterna |
| Escudo Balístico Corporativo | pesado · +3 | 12 | Épico | Resistente a Balístico · não bloqueia a visão | c/ Lanterna |

### 10.8 KITS — categoria nova · carregados, sem espaço de inventário

**Kits habilitam** ações para quem não tem a perícia, sempre com Desvantagem, e nunca copiam uma
assinatura de classe (§9).

| Kit | Raridade | O que habilita |
|---|---|---|
| Kit de Primeiros Socorros | Comum | Qualquer um estanca Sangrando ou estabiliza aliado *(sem Medicina: Desvantagem)* · Carga (5) |
| Caixa de Ferramentas | Comum | Qualquer um faz reparo e remendo de campo *(sem Mecânica: Desvantagem)* |
| Bússola e Mapa de Zona | Comum | Vantagem em Sobrevivência para se orientar |
| Kit de Sobrevivência | Incomum | Vantagem no teste do saque — +10% de itens |
| Kit de Arrombamento | Incomum | Qualquer um abre fechadura mecânica *(sem perícia: Desvantagem)* |
| Kit de Eletrônica | Incomum | Qualquer um extrai Eletrônicos de aparelhos *(sem perícia: Desvantagem)* |
| Rede de Camuflagem | Incomum | Vantagem em Furtividade para esconder o acampamento |
| Rádio de Ondas Curtas | Incomum | Contato com facções neutras — número no Bloco 6 |
| Kit de Mecânico Automotivo | Incomum | Reparo de veículo — número no módulo de Veículos |
| Kit Cirúrgico de Campo | Raro | Com Medicina: Vantagem para estabilizar e estancar · Carga (5) |
| Seringa de Adrenalina | Raro | Consumível: aliado em Estado Crítico volta com 1 HP |

### 10.9 MOCHILAS — espaço Costas, categoria nova

Mochila ocupa o espaço **Costas** (§1), separado de Corpo. Capacidade somada à base de 6 slots (§10.0):

| Mochila | Raridade | Capacidade | Total com a mochila | Contrapartida |
|---|---|---|---|---|
| Mochila Escolar | Abundante | +4 slots | 10 | — |
| Mochila de Trilha | Comum | +6 slots | 12 | Ruído +1 degrau ao se mover |
| Mochila Discreta | Incomum | +3 slots | 9 | Vantagem em Furtividade |
| Mochila Tática Militar | Raro | +8 slots | 14 | FOR mínima 12 |

---

## 11. O que continua `[A CALIBRAR]`

| Campo | Estado |
|---|---|
| **Criaturas quebra-armadura além do Touro** | ✅ Resolvido (Bloco 5, Aprovação 035): Zumbi Corrosivo, Mutante Encouraçado, Devorador de Aço e Colosso de Sucata (`docs/gdd/GDD_Bestiario.md` §20) |
| **Mochila de topo (Épico)** | Fora do Bloco 4b por decisão do Diretor — sem necessidade identificada neste momento |
| **Criatura ou habilidade dedicada de dano Perfurante** | ✅ Resolvido (Bloco 5, Aprovação 035): Enxame de Ratos Mutantes, Mutante Encouraçado e Enxame de Morcegos Mutantes causam Perfurante por ficha, fora do controle do Mestre (`docs/gdd/GDD_Bestiario.md` §20) |

---

*Este arquivo é canônico (Aprovações 034–035). Qualquer alteração exige nova aprovação do Diretor de
Criação.*
