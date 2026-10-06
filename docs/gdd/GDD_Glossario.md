# MUTAGEN:ZERO — Glossário de Termos Reservados

> **O que este documento é.** Um índice de **palavras já ocupadas**. Ele não cria regra nenhuma: cada
> verbete aponta para o documento onde a regra mora. Onde o canon não fechou um número, o verbete diz
> `[A CALIBRAR]` e nada mais — **implementadores não inventam padrão no motor**.

---

## 1. Como usar este glossário

Ele serve a **dois públicos** e as duas leituras são legítimas:

**Quem projeta o sistema.** Antes de batizar qualquer conceito novo — uma propriedade, uma família,
um contador, uma habilidade, um recurso — **procure a palavra aqui primeiro**. Se ela aparece, está
ocupada. Escolha outra. O §4 (Palavras QUEIMADAS) é a versão curta dessa checagem.

**Mestres iniciantes.** Cada verbete responde três perguntas na ordem em que elas aparecem na mesa:
o que o termo **significa**, **onde a regra mora** (para você não arbitrar de memória) e com o que
ele **não deve ser confundido** — porque quase toda dúvida de mesa em MUTAGEN:ZERO é uma palavra
sendo lida no sentido errado.

> ### REGRA DE OURO
> **Antes de nomear qualquer conceito novo, consulte este glossário.** Seis colisões já aconteceram
> neste projeto. Nenhuma delas foi descoberta no desenho — todas foram descobertas depois, em
> implementação ou em revisão, e **todas exigiram retrabalho**: renomear, reescrever documento,
> reemitir aprovação.
>
> **E a regra vale nos dois sentidos: termo novo se registra aqui no mesmo ato que o cria.** Este
> documento acabou de ser posto em dia depois de **sete aprovações** que o atravessaram sem tocá-lo —
> as 18 perícias, o sistema inteiro de Especializações e a escala de resistência a dano estavam em
> canon e **fora daqui**. `docs/gdd/GDD_Pericias.md` §8.1 (item 3) chegou a registrar a falta por escrito, e
> ela sobreviveu assim mesmo. **A checagem falha em silêncio quando o índice está velho**, e foi
> exatamente esse silêncio que produziu as seis colisões. As novas candidatas estão em **§2.1**.

**Campo Status**, em todos os verbetes: `canon` = fechado por aprovação do Diretor · `[A CALIBRAR]` =
o conceito existe, o número não · `pós-MVP` = aprovado como desenho, fora do escopo do motor atual.

---

## 2. As seis colisões que já aconteceram

Esta seção é a justificativa do documento, e é franca de propósito: **nenhuma destas colisões foi
erro de implementação. Todas foram erro de nomenclatura**, cometido por alguém que escolheu a
primeira palavra que descrevia bem o conceito sem verificar se a palavra estava livre.

| # | Termo em colisão | O que ele significa HOJE | O que foi renomeado para resolver |
|---|---|---|---|
| 1 | **Pesada** | **Propriedade de arma**: exige FOR mínima (12 a 16); abaixo dela, desvantagem no ataque (`docs/gdd/GDD_Armas.md` §3) | Os **portes de modificação ofensiva** passaram de "Leve / Pesada" para **Simples / Estrutural** (Aprovação 012, `docs/gdd/GDD_Modificacoes.md` §6). A propriedade ficou com a palavra; o porte cedeu |
| 2 | **Utilitária** | **Propriedade de arma**: a arma serve como ferramenta — Vantagem em testes de FOR para arrombar (`docs/gdd/GDD_Armas.md` §3) | A **família de modificação** de mesmo nome passou a chamar-se **Suporte** (Aprovação 013, `docs/gdd/GDD_Modificacoes.md` §5). Motivo declarado: a palavra repetida "confundia busca e implementação" |
| 3 | **quebra × travamento** | **Dois contadores distintos.** Travamento = a arma emperra (só arma de fogo, `1` natural, modulado pela conservação, resolvido com 1 Ação Bônus). Quebra = a arma se parte (propriedade **Frágil** + `+1` por modificação Gambiarra) | Nada foi renomeado: foi emitida a **regra de não-soma** (Aprovação 013). Os dois eram usados como sinônimos em texto corrido. Hoje: **uma rolagem, duas checagens independentes**, e os números **nunca se somam** (`docs/gdd/GDD_Modificacoes.md` §7.1, `docs/gdd/GDD_Combate.md` §7.3) |
| 4 | **Projéteis** | **Pool de munição**: flechas, virotes, dardos — o único pool **recuperável** do jogo (`docs/gdd/GDD_Combate.md` §13.1) | A **família de arma** passou a chamar-se **Projéteis Mecânicos** (CANON 017 §2). Texto canônico: *"O nome curto colidia com o pool de munição chamado Projéteis. Famílias e pools são coisas diferentes."* |
| 5 | **Estabilizar** | **Três mecânicas sem relação entre si**, e o canon nunca renomeou nenhuma: (a) **Estabiliza** = acumular 3 sucessos em testes de morte e parar de rolar; (b) **estabilizar um aliado** = um uso da Ação **Usar Objeto**, aberto a qualquer personagem; (c) **Estabilizar** = a assinatura do **Médico**, que remove pontos da Trilha de Infecção | **Esta é a única das seis que continua aberta.** A colisão foi *documentada*, não resolvida: `docs/classes/Classe_Medico.md` §5.4 declara as três e instrui **"três identificadores distintos no motor"**. A assinatura **não** interage com testes de morte, **não** concede sucessos e **não** tira ninguém do Estado Crítico |
| 6 | **Oficina** | **RESOLVIDA (Aprovação 023) — desceu de 3 para 2 sentidos.** Eram: a **via de fabricação** limpa e cara das Modificações (`docs/gdd/GDD_Modificacoes.md` §2), a **Oficina de Campo** do Cientista, e a *"Oficina médica"* do Refúgio | **A instalação médica foi renomeada para Enfermaria** e a palavra *Oficina médica* **saiu do canon**. Restam dois sentidos, ambos de fabricação de equipamento, e o qualificador continua obrigatório entre eles: *via Oficina* × *Oficina de Campo*. **Esta é a primeira colisão deste glossário resolvida por renomeação, e não por convivência** — ver §2.2 |

**O padrão comum às seis.** Em cinco dos seis casos a palavra descrevia *corretamente* os dois
conceitos — "pesada" descreve mesmo uma modificação que come 2 slots, "utilitária" descreve mesmo
uma família de suporte. **Descrever bem não é estar livre.**

### 2.0 A colisão que NÃO aconteceu — `CD` (Aprovação 025)

A proposta original do Bestiário classificava criaturas por **`CD 0` a `CD 5`**. `CD` já significa
**Classe de Dificuldade** em **27 lugares do canon**, incluindo uma fórmula viva — *"CD de Infecção =
10 + pontos ganhos naquele combate"* (`docs/gdd/GDD_Infeccao.md` §2). Na mesa, *"um Zumbi de Sangue CD 3"* e
*"teste de AGI CD 13"* na mesma frase seria confusão garantida.

**Adotou-se `ND` — Nível de Desafio**, que não colidia com nada.

> **É a primeira colisão deste projeto barrada ANTES de entrar no canon**, em vez de documentada
> depois. As seis primeiras foram achadas em auditoria, com os documentos já escritos e a regra já em
> uso. Esta foi achada na proposta — que é o momento em que corrigir custa uma tecla.

---

### 2.1. Candidatas — colisões que ainda não foram declaradas por nenhuma aprovação

Esta subseção existe porque as seis acima **só entraram no documento depois de custar retrabalho**.
Estas não custaram nada ainda. Nenhuma delas está resolvida, nenhuma foi renomeada, e **nenhuma é
regra** — são **avisos de nomenclatura** registrados no ciclo em que foram notados.

| Candidata | Os sentidos vivos | Por que está aqui |
|---|---|---|
| **Vigor** | (1) **perícia de CON** — esforço prolongado por escolha própria · (2) o **teste de resistência de CON** contra Infecção, que **não é** a perícia | **A mais perigosa das quatro**, e a única que o canon já antecipou. `docs/gdd/GDD_Pericias.md` §1.1 dedica uma seção inteira a separar as duas, com justificativa de balanceamento: o modificador de CON é **dial fraco de propósito**, e somar proficiência de Vigor ali faria a Trilha de Infecção deixar de morder. Hoje **não é colisão** — mas basta alguém escrever *"teste de vigor"* em minúscula para que vire. **Esse erro exato já aconteceu neste projeto**: `docs/gdd/GDD_Combate.md` §4 descreve a ação **Esconder** como *"teste de **furtividade** oposto à PER"*, em minúscula, porque não havia substantivo próprio. A minúscula foi o sintoma; a perícia **Furtividade** foi a cura, e chegou depois |
| **Estabilizar** | Ganhou um **quarto** contexto | A colisão 5 é declarada e **diz "três"**. Com a perícia **Medicina** (`docs/gdd/GDD_Pericias.md` §2.11 e §3.3) a palavra passa a aparecer em **quatro** lugares da ficha. Medicina **não cria mecânica nova** — ela **opera o sentido (b)**, estabilizar um aliado via **Usar Objeto** — mas `docs/classes/Classe_Medico.md` §5.4 manda o motor ter **três identificadores distintos**, e `docs/gdd/GDD_Pericias.md` §3.3 acrescenta que **Medicina não deve compartilhar identificador com nenhum dos três**. São **quatro identificadores**, não três, e o verbete da colisão 5 estava desatualizado até este ciclo |
| **Porte** | (1) **porte de modificação ofensiva** (Simples / Estrutural) · (2) **porte de Especialização** (Menor / Média / Maior / Assinatura) | Notada **neste ciclo**, ao registrar o sistema de Especializações. É o padrão das seis em estado puro: a palavra descreve bem os dois — *porte* é mesmo o tamanho de uma coisa —, mas um mede **slots de arma** e o outro mede **nível de personagem**, e eles **não se tocam**. Mitigação hoje: **qualificador obrigatório** (§5, convenção 5) |
| **Assinatura** | (1) **habilidade-assinatura** de classe · (2) o **porte** de Especialização que a compra | Consequência direta da anterior. A Aprovação 022 agravou o caso ao levar o porte Assinatura de **8 para 15 entradas**, das quais **7 não são assinaturas** — são Recursos "II" que **escalam** uma. Dizer *"ele tem três Assinaturas"* hoje é ambíguo entre "três habilidades" e "três escolhas daquele porte" |

**As duas latentes já registradas em §6 (item 22) continuam valendo:** **Sucata** (tier · componente ·
estado de conservação) e **Carga** (propriedade · Munições Especiais · **Energia da Célula** ·
**mecanismo Explosivo**).

> **O que fazer com esta lista.** Nada, por enquanto — **declarar colisão é ato de aprovação, não de
> glossário**. O que o documento pode fazer, e faz, é garantir que nenhuma das seis se repita pelo
> mesmo motivo: ninguém as viu a tempo.

---

### 2.2 Por que a colisão 6 foi resolvida por renomeação, e as outras cinco não

As outras cinco colisões deste glossário convivem por **qualificador obrigatório** — escreve-se
*faixa de quebra* ou *faixa de travamento*, *limiar pessoal* ou *limiar do Medidor*, e segue-se o
jogo. A colisão 6 foi a única **desfeita**, e a diferença é instrutiva.

**Convive-se quando os dois sentidos têm dono.** *Quebra* é da arma e *travamento* é da arma: os dois
nomes estão presos a regras vivas, e renomear qualquer um quebraria documentos aprovados.

**Renomeia-se quando um dos sentidos é acidente de redação.** *"Oficina médica"* nunca foi decisão de
design — foi a palavra que apareceu numa frase de `docs/gdd/GDD_Infeccao.md` e nunca mais foi revisada. Os
**dez** outros documentos que citam a mesma instalação já a chamavam de **enfermaria**. Não havia
empate: havia um documento contra dez, e o único voto minoritário usava justamente a palavra que
este glossário registra como a mais sobrecarregada do sistema.

**O critério, para as próximas:** antes de propor qualificador obrigatório, pergunte se um dos
sentidos é **jovem, isolado e substituível**. Se for, renomeie — o qualificador é imposto ao Mestre
para sempre, e só vale a pena quando os dois lados têm raiz.

---

### 2.3 Duas colisões criadas e resolvidas no mesmo ciclo (Aprovações 025 e 026)

O catálogo de criaturas introduziu **duas** palavras que encostavam em canon já existente. Ambas
foram **renomeadas na Aprovação 026**, antes de qualquer regra passar a depender delas.

| Nome original | Colidia com | Nome canônico |
|---|---|---|
| ~~Enfermeira~~ | **Enfermaria**, a instalação do Refúgio canonizada **duas aprovações antes** (023). *"Leva ele para a Enfermeira"* e *"para a Enfermaria"* diferiam em **uma letra** e significavam coisas opostas | **Doutora Zumbi** |
| ~~Corredor~~ | **corredor** no sentido de passagem do mapa, que o grid hexagonal de `docs/gdd/GDD_Combate.md` §11 usa. *"Tem um Corredor no corredor"* era uma frase que o sistema permitia | **Maratonista** |

> **O critério do §2.2 decidiu os dois casos sem discussão.** Renomeia-se quando um dos sentidos é
> **jovem, isolado e substituível**: nos dois, o sentido jovem era o da criatura — ambas tinham
> nascido no ciclo anterior e nenhuma regra dependia do nome delas.
>
> **Somando com o `CD` do §2.0, este foi o ciclo em que o glossário passou a funcionar como projetado:**
> três colisões apanhadas **na proposta ou no mesmo ciclo**, nenhuma delas chegando a virar dívida. As
> seis primeiras colisões do projeto foram achadas em auditoria, meses de canon depois.

---

## 3. Termos reservados

Em ordem alfabética. Cada verbete traz **Significa** · **Onde mora** · **Não confundir com** ·
**Status**.

> **93 verbetes**, dos quais **44 entraram neste ciclo de atualização**: as **18 perícias** e os dois
> termos que as organizam (Perícia, Teste de resistência) · os **10 termos do sistema de
> Especializações** (Menor, Média, Maior, Assinatura, Cota, Trajetória, Fonte diegética, Talento
> Geral, Recurso de classe, Ápice) · os **4 graus da escala de resistência a dano** (Resistente, Muito
> Resistente, Vulnerável, Imune) · os **7 termos que a Aprovação 018 deixou sem verbete** (Improviso,
> Arruinada, Lâminas Curtas, Lâminas Longas, Munições Especiais, Energia da Célula, Mecanismo
> Explosivo) · e **3 termos soltos** que estavam citados em regra e em lugar nenhum (Soro de Campo,
> Enfermaria, Degrau). Dois verbetes antigos foram **corrigidos**, não só ampliados: **Especialização**
> (que dava por aberto o que está fechado desde a Aprovação 021) e **Estabilizar** (que contava três
> sentidos quando há quatro contextos). **Porte** passou a declarar os dois sentidos que tem.

- **Ação** — *Significa:* o recurso principal do turno; **exatamente uma por turno**, escolhida de uma lista fechada de dez (Atacar, Correr, Desengajar, Esquivar, Ajudar, Esconder, Usar Objeto, Mirar, Recarregar). *Onde mora:* `docs/gdd/GDD_Combate.md` §4 e §2.4. *Não confundir com:* **Ação Bônus**, **Reação**, **interação livre** — são quatro recursos separados, repostos separadamente. *Status:* canon.
- **Ação Bônus** — *Significa:* um slot por turno com **escopo fechado**: no MVP tem **um único uso aprovado, Destravar uma arma de fogo** (Aprovação 003). *Onde mora:* `docs/gdd/GDD_Combate.md` §2.4 e §7.3. *Não confundir com:* a **Ação**. Nenhum talento, item, arma, classe ou modificação concede outro uso sem aprovação explícita do Diretor; implementadores criam o slot e expõem só Destravar. *Status:* canon (escopo fechado).
- **Acrobacia** — *Significa:* **perícia de AGI** — equilíbrio em superfície estreita ou instável, queda controlada, rolamento, passar por vão apertado, recuperar-se de um tropeço, e o lado de **AGI** do teste oposto para escapar de **Agarrado**. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.3 e §4.4. *Não confundir com:* **Atletismo** — *Atletismo é força aplicada ao corpo, Acrobacia é controle do corpo*; e com a Ação **Esquivar**, que é **ação**, não perícia (`docs/gdd/GDD_Combate.md` §4). *Status:* canon quanto à existência, ao atributo e às listas de classe (CANON 021 §1); **todas as faixas de CD são `[A CALIBRAR]`**, e a redução de dano de queda por sucesso também — o canon não tem tabela de queda.
- **Ágil** — *Significa:* **propriedade de arma** — permite usar AGI no lugar de FOR no ataque **e** no dano. *Onde mora:* `docs/gdd/GDD_Armas.md` §3 (Aprov. 006); interação com atributo em `docs/gdd/GDD_Combate.md` §5.1. *Não confundir com:* a **família** de proficiência (Ágeis não é família na taxonomia nova) nem com a propriedade **Leve**. *Status:* canon.
- **Ápice** — *Significa:* o **Recurso de nível 20** de cada classe — um por classe, oito no total (Um Tiro, Ceifa, Protótipo, O Refúgio é Meu, Ninguém Me Vê, Reverter, Aríete Rodante, Nunca Desarmado). *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §9.2; a linha de nível 20 de cada `Classe_*.md` §6. *Não confundir com:* **Recurso de classe** comum e **Assinatura** — o Ápice é o único ganho que a classe entrega depois de toda a carreira. *Status:* canon quanto à lista; **nunca adquirível por Especialização, por fonte diegética ou por acordo de mesa** (Regra 3 de contenção). Abrir um é **mudança de canon**, não uso do sistema.
- **Arrombamento** — *Significa:* **perícia de FOR** — abrir o que foi feito para não abrir: portas, grades, cadeados, correntes, tampas de bueiro, grelhas, caixas lacradas, veículos trancados, com ferramenta, alavanca ou técnica. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.2 e §3.6. *Não confundir com:* **Eletrônica** (fechadura eletrônica e painel corporativo), **Mecânica** (mecanismo que se quer preservar intacto) e a **interação livre com objeto** — porta destrancada **não se rola**. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. É a perícia que finalmente dá destino à propriedade **Utilitária**, que concedia **Vantagem** numa coisa que não existia em ficha nenhuma.
- **Arruinada** — *Significa:* o **pior dos quatro estados de conservação** da arma: faixa de travamento **15,0%** (`1`, `2` ou `3` naturais). *Onde mora:* `docs/gdd/GDD_Combate.md` §7.3; a escada `Calibrada → Boa → Desgastada → Arruinada` em `docs/gdd/GDD_Modificacoes.md` §7.4. *Não confundir com:* o **tier Improviso** e o **componente Sucata** — arma arruinada é arma **gasta**, não arma **ruim de origem**; uma Corporativa pode estar Arruinada e continua Corporativa. Também não confundir com **quebra**: arma Arruinada ainda dispara. *Status:* canon (valores fechados desde a Aprovação 006).
- **Assinatura** — *Significa:* **duas coisas**. (a) A **habilidade-assinatura** de uma classe — uma por classe, oito no total (Tiro Calculado, Corte Contínuo, Oficina de Campo, Mão Calejada, Esquiva Reflexa, Estabilizar, Modificação Veicular, Combate Desarmado). (b) O **porte mais alto de Especialização**, disponível **só no nível 17**, que compra a assinatura alheia. *Onde mora:* (a) `CANON_CLASSES.md` e cada `Classe_*.md` §3; (b) `docs/gdd/GDD_Especializacoes.md` §2 e §8. *Não confundir com:* entre si, nem com **porta suave** — assinatura é habilidade de classe e **não abre pilar**. *Status:* ambos canon. A Aprovação 022 levou o porte Assinatura de **8 para 15 entradas**, somando os sete Recursos "II" que escalam uma assinatura. Ver §2.1: a palavra ganhou um segundo sentido e é candidata a colisão.
- **Atletismo** — *Significa:* **perícia de FOR** — escalar, saltar, nadar, correr contra o tempo, empurrar e arrastar peso, arrombar **pela força bruta do corpo**, e o lado de **FOR** do teste oposto para escapar de **Agarrado**. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.1 e §4.4. *Não confundir com:* **Acrobacia** (equilíbrio e queda), **Arrombamento** (ferramenta na tranca) e **Vigor** — *Atletismo é pico, Vigor é duração*. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`.
- **Atração** — *Significa:* efeito **imediato** do Ruído — todo mutante dentro do raio que **não** esteja já engajado move-se na direção da fonte no próximo turno dele. Automática, sem rolagem. *Onde mora:* `docs/gdd/GDD_Ruido.md` §2. *Não confundir com:* o **Medidor de Horda**, que é acúmulo de cena; Atração é instantânea e não gera leva. *Status:* canon; a definição de "engajado" e o efeito de obstáculos são `[A CALIBRAR]`.
- **Banda (de Infecção)** — *Significa:* uma das quatro faixas da Trilha de Infecção — Saudável (até 1/3 do limiar), Infectado (1/3 a 2/3), Infectado grave (2/3 até o limiar), mutação ou morte (no limiar). São **frações do limiar pessoal**, não valores fixos. *Onde mora:* `docs/gdd/GDD_Infeccao.md` §3. *Não confundir com:* **faixa de quebra** e **faixa de travamento**, que são intervalos de d20. *Status:* canon; a formalização do arredondamento é `[A CALIBRAR]` (usa-se piso).
- **Cobertura** — *Significa:* bônus de Defesa por posicionamento: meia **+2**, três quartos **+5**, total **não pode ser alvo**. Só o grau mais favorável se aplica e **não somam entre si**. *Onde mora:* `docs/gdd/GDD_Combate.md` §5.4 e §11.3. *Não confundir com:* a "cobertura parcial" concedida por itens como Tampa de Bueiro e Escudo Antimotim, que é texto de arma. *Status:* canon; o percentual de bloqueio que define cada grau é `[A CALIBRAR]`.
- **Conservação (estado de)** — *Significa:* os quatro estados da arma que modulam a **faixa de travamento**: Calibrada (~0,5%), Boa (5%), Desgastada (10%), Arruinada (15%). *Onde mora:* `docs/gdd/GDD_Combate.md` §7.3 (Aprovação 006). *Não confundir com:* faixa de **quebra**, que vem de outro lugar; e com o **tier Improviso** e o **componente Sucata**, que não têm relação com o estado Arruinada. *Status:* canon (valores fechados).
- **Corte Contínuo** — *Significa:* assinatura do **Ceifador** — ao reduzir um alvo a 0 HP com arma **Cortante**, mover 1 hexágono e atacar outro alvo. **Uma vez por turno.** *Onde mora:* CANON 017 §1. *Não confundir com:* "ataque extra", que **não existe no MVP**; o gatilho é a morte do alvo, não a economia do turno. *Status:* canon (CANON 017); progressão `[A CALIBRAR]`.
- **Cota** — *Significa:* o **teto de 2 Especializações por classe de origem** (Regra 1 de contenção). O teto lê **classe**, não porte: uma Média + uma Maior do Ceifador **esgotam o Ceifador para sempre**, e nenhuma Assinatura de Ceifador será possível no nível 17. Menores **não contam** — perícias, famílias de arma, testes de resistência e Talentos Gerais não pertencem a classe nenhuma. *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §3 (Regra 1) e §8.0. *Não confundir com:* **slot** (três sentidos, nenhum deles este), o **teto de dado 1d12** e o **teto de DPR**. *Status:* canon. Consequência canônica declarada: na melhor das hipóteses um personagem toca **quatro** classes alheias rasamente, ou **duas** com profundidade — **nunca uma inteira**.
- **Defesa** — *Significa:* `10 + mod. AGI + bônus de armadura + bônus de cobertura`; acerta-se com rolagem **≥** Defesa. *Onde mora:* `docs/gdd/GDD_Combate.md` §5.2. *Não confundir com:* HP, nem com o **+1 de Defesa** do Guarda-mão (que é modificação, não regra de Defesa). *Status:* canon, **escala fechada na Aprovação 029**: `10 + mod. AGI (limitado) + armadura + escudo + cobertura`, faixa prática **10 a 22**. Categorias: Leve **+1 a +3** (sem limite de AGI) · Média **+3 a +5** (AGI máx. +2, **FOR 12**) · Pesada **+5 a +7** (AGI máx. +0, **FOR 14**) · Escudo **+1 a +3**, exige mão livre. **Não há teto de Defesa**: o ataque das criaturas escala por ND (+4 a +11) e é a **diferença líquida** que conta — medido, escalar os dois lados deixa a Infecção idêntica até a segunda decimal (`docs/gdd/GDD_Combate.md` §5.3.1).
- **Degrau** — *Significa:* **um passo em qualquer escada do sistema** — e são **cinco escadas diferentes** que usam a palavra: (a) **escada de dados** `d4→d6→d8→d10→d12`, teto **1d12 absoluto**; (b) **Nível de Ruído** 0–3, que o silenciador desce um degrau e a munição Subsônica outro, com **piso Baixo** para arma de fogo; (c) **estado de conservação** `Calibrada→Boa→Desgastada→Arruinada`, que a falha crítica de fabricação desce um degrau; (d) o **porte de modificação ofensiva**, em que Simples vale `+1` degrau de dado e Estrutural `+2`; (e) **resistência e vulnerabilidade a tipo de dano**, que movem o dado um ou dois degraus (`docs/gdd/GDD_Combate.md` §6.3). *Onde mora:* (a) `docs/gdd/GDD_Armas.md` §1.1; (b) `docs/gdd/GDD_Ruido.md` §1 e §3; (c) `docs/gdd/GDD_Modificacoes.md` §7.4; (d) `docs/gdd/GDD_Modificacoes.md` §6; (e) `docs/gdd/GDD_Combate.md` §6.3. *Não confundir com:* entre si — **degraus de escadas diferentes nunca se convertem um no outro**. *Status:* as cinco escadas são canon; a palavra **não** é. Sempre qualifique: *degrau de dado*, *degrau de Ruído*, *degrau de conservação*.
- **Desvantagem** — *Significa:* rolar `2d20` e usar o **menor**. *Onde mora:* `docs/gdd/GDD_Combate.md` §1.1. *Não confundir com:* penalidade numérica. **Vantagem e Desvantagem não acumulam:** uma fonte de cada lado zera as duas e rola-se `1d20` normal, por mais fontes que existam. *Status:* canon.
- **Eletrônica** — *Significa:* **perícia de INT** — placa, sensor, chip, fiação viva, baterias e **Célula de Energia**, painéis, câmeras, terminais e **interfaces corporativas**; e a desmontagem que extrai o componente **Eletrônicos**, que *não se fabrica, só se desmonta de algo que já existia*. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.10, §3.2 e §4.2. *Não confundir com:* **Mecânica** — *Mecânica é o que tem peça, Eletrônica é o que tem corrente*; e com **Arrombamento**, que é o alvo puramente mecânico. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs de interface corporativa `[A CALIBRAR]`. Em **receita mista** (encaixar e ligar, ex.: Designador Laser) o canon **não diz** qual das duas o Mestre pede: `[A CALIBRAR]`.
- **Energia da Célula** — ⚠ **TERMO APOSENTADO (Aprovação 028).** Era a carga armazenada no componente **Célula de Energia**, consumida pelas modificações elétricas. **Hoje é apenas `Carga (N)`**, como a de qualquer outro item: `docs/gdd/GDD_Consumiveis.md` §2 unificou os três recursos que faziam a mesma coisa — `Carga (N)`, *combustível* e *Energia da Célula*. **Não escreva mais "Energia da Célula"**; escreva **Carga**, e o componente que a repõe é a **Célula de Energia**. Definição histórica: *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §5.1 e §8.1; o componente em §4. *Não confundir com:* a propriedade **Carga (N)**, que é recurso do item e **não usa pool de calibre**; as **Munições Especiais**; e o **mecanismo Explosivo** — quatro usos vivos da palavra *carga* (§4). Também não confundir a **Energia da Célula** (a carga) com a **Célula de Energia** (o componente Incomum). *Status:* canon quanto à existência; **consumo, recarga e a disputa com o gerador do Refúgio são `[A CALIBRAR]`** (`docs/gdd/GDD_Modificacoes.md` §9.2, item 4).
- **Enfermaria** — *Significa:* a instalação de Refúgio que remove pontos da Trilha de Infecção **sem passar por personagem nenhum**: *"descanso longo em Refúgio com Enfermaria remove pontos"*. É a saída do grupo que não tem Médico, e existe para que essa saída não dependa de ninguém estar na mesa. *Onde mora:* `docs/gdd/GDD_Infeccao.md`, "Remoção" (tabela das quatro vias) · os oito `Classe_*.md` §6 · `docs/gdd/GDD_Especializacoes.md` §8.6 e §13.9. *Não confundir com:* a **Oficina** de Modificações e a **Oficina de Campo** do Cientista — são instalações **diferentes do mesmo Refúgio** e **não se destravam uma à outra**; e com os **dois soros**, que são itens e não instalação. *Status:* **nome canônico desde a Aprovação 023**, que aposentou *"Oficina médica"*. A **quantidade removida por descanso e o tempo são `[A CALIBRAR]`**.
- **Escada de dados** — *Significa:* `d4 → d6 → d8 → d10 → d12`, com **teto 1d12 ABSOLUTO**. Dado secundário (armas de dois tipos de dano) tem teto **1d6**. *Onde mora:* `docs/gdd/GDD_Armas.md` §1.1; `docs/gdd/GDD_Modificacoes.md` §6; **resistência, vulnerabilidade e imunidade** em `docs/gdd/GDD_Combate.md` §6.3. *Não confundir com:* a escada de **Ruído** (0–3), a escada de **conservação** (4 estados) e o "degrau" de modificação — **cinco** escadas diferentes usam a palavra *degrau* (ver **Degrau**). *Status:* canon. Duas consequências canônicas: **poder de tier alto vem de efeito, nunca de dado maior**; e **a escada de dados é também a moeda da resistência** — Resistente desce um degrau, Muito Resistente dois, Vulnerável sobe um, em vez da metade do d20 clássico.
- **Especialização** — *Significa:* aquisição cruzada entre classes, **8 na carreira inteira**, nos níveis **3, 5, 7, 9, 11, 13, 15 e 17**, sempre com **fonte diegética** (mentor NPC, manual saqueado, prática em campo validada pelo Mestre). Existe em **quatro portes** — Menor (nv 3), Média (nv 7), Maior (nv 13), Assinatura (nv **17**, uma única oportunidade na carreira) — e sob **três regras de contenção**: cota de 2 por classe, pré-requisito lê proficiência de família de arma, e Recursos de nível 18 e Ápices não são adquiríveis. **O dado de vida nunca muda.** *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §1 a §9 (catálogo completo); `CANON_021` §2; todos os `Classe_*.md` §6. *Não confundir com:* "arma especializada", que é a arma de **3 slots** (rifle de precisão, besta, metralhadora); e com **Recurso de classe**, que é o que a classe dá de graça no próprio nível. *Status:* **canon — os quatro portes, os oito níveis e as três regras estão FIXOS** (CANON 021 §2, catalogados na Aprovação 021); a Aprovação 022 reclassificou **sete Recursos "II"** de Média para porte **Assinatura** e fixou a contagem em Menor 41 · Média 10 · Maior 16 · Assinatura 15 = **82 adquiríveis** + 16 inadquiríveis. Continuam `[A CALIBRAR]`: os parâmetros de **ritmo das fontes diegéticas** e os valores citados em `docs/gdd/GDD_Especializacoes.md` §13.9. **Nota de correção:** até este ciclo este verbete afirmava que *"todas as listas e pré-requisitos de nível são `[A CALIBRAR]`"* — era defasagem do glossário, registrada em `docs/gdd/GDD_Pericias.md` §8.1 (item 5), e está corrigida aqui. Os oito `Classe_*.md` §7 continuam repetindo a frase antiga (§6, divergência 23).
- **Estabilizar** — *Significa:* **três mecânicas distintas e um quarto contexto** — ver §2, colisão 5, e §2.1. As três mecânicas: (a) **Estabiliza** = acumular 3 sucessos em testes de morte e parar de rolar; (b) **estabilizar um aliado** = um uso da Ação **Usar Objeto**, aberto a qualquer personagem; (c) **Estabilizar** = a assinatura do **Médico**, que remove pontos da Trilha de Infecção. O **quarto contexto** é a perícia **Medicina**, que passou a ser a perícia que **opera o sentido (b)** — ela não cria mecânica nova, mas põe a palavra num quarto lugar da ficha. *Onde mora:* `docs/gdd/GDD_Combate.md` §8.3 · §4 e §8.5 · `docs/classes/Classe_Medico.md` §3 · `docs/gdd/GDD_Pericias.md` §2.11 e §3.3. *Não confundir com:* entre si. **Medicina destrava apenas (b)**: não concede sucessos em teste de morte, não tira ninguém do Estado Crítico por si só, e não substitui nem alimenta a assinatura. A assinatura do Médico **não** dá sucessos em teste de morte. *Status:* colisão **aberta e agravada**; as três existem, nenhuma foi renomeada, e o glossário declarava **três** sentidos quando já há **quatro contextos vivos**. `docs/classes/Classe_Medico.md` §5.4 instrui **três identificadores distintos no motor**; `docs/gdd/GDD_Pericias.md` §3.3 acrescenta que Medicina **não deve compartilhar identificador com nenhum dos três**. Os números da assinatura (quantidade removida, custo em ação, frequência) são `[A CALIBRAR]`.
- **Estado Crítico** — *Significa:* a condição de quem chega a **0 HP**: Inconsciente e Caído, sem ação, movimento ou Reação, com **teste de morte no fim de cada turno próprio** (`d20` vs. CD 10; 3 sucessos estabiliza, 3 falhas mata). *Onde mora:* `docs/gdd/GDD_Combate.md` §8.2 a §8.5. *Não confundir com:* **acerto crítico** (§6.2) nem com **falha crítica** de fabricação (`docs/gdd/GDD_Modificacoes.md` §7.4) — três "críticos" sem relação. *Status:* canon; efeito de `20`/`1` natural no próprio teste de morte é `[A CALIBRAR]`.
- **Família de arma** — *Significa:* a **taxonomia de proficiência**, com **uma só dimensão**, em que **cada arma pertence a exatamente uma** família: Desarmado, Lâminas Curtas, Lâminas Longas, Contundentes, Hastes, Projéteis Mecânicos, Pistolas, Longas, Espingardas, Dispositivos. *Onde mora:* CANON 017 §2. *Não confundir com:* **propriedade de arma** (Ágil, Leve, Pesada, Arremessável…), **tipo de dano** e **tier** — as proficiências antigas misturavam os três. *Status:* canon (CANON 017), e **substitui** as proficiências antigas.
- **Família de modificação** — *Significa:* os cinco agrupamentos das 17 modificações: Ofensiva (6), Precisão (3), Furtiva (2), Confiabilidade (3), **Suporte** (3). *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §5. *Não confundir com:* **família de arma** (acima). São duas taxonomias independentes que usam a mesma palavra. *Status:* canon; teto de modificações por família numa mesma arma é `[A CALIBRAR]`.
- **Fonte diegética** — *Significa:* o **custo de toda Especialização, pago em ficção e não em matemática**. Não há pontos, moeda nem árvore de talentos: há **três tipos de fonte** — **mentor NPC** (alguém vivo que sabe e aceita ensinar), **manual saqueado** (documento pré-Queda, decifrado com **Saber Pré-Queda**) e **prática em campo** (o personagem fez, repetidamente, sob risco real, e o Mestre valida pelo histórico da mesa). A fonte precisa ser **plausível para o porte pedido**. *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §10; repetido em cada `Classe_*.md` §6. *Não confundir com:* **pré-requisito** (Regra 2) — a fonte **não contorna** nível mínimo, cota de 2 por classe nem pré-requisito de proficiência. Um mentor perfeito não ensina *Tiro Calculado* a quem não tem arma de fogo. *Status:* canon quanto aos três tipos e à regra de plausibilidade; **todos os parâmetros de ritmo são `[A CALIBRAR]`** — fontes por arco, tempo de treinamento, custo em componentes ou favores, número de tentativas, e se uma fonte serve a mais de um personagem. Consequência declarada: **o ritmo do sistema está na mão do Mestre, não na ficha.**
- **Frágil** — *Significa:* **propriedade de arma** — em um `1` natural, a arma **quebra**. *Onde mora:* `docs/gdd/GDD_Armas.md` §3. *Não confundir com:* **travamento**; e com a fragilidade adquirida por Gambiarra, que é `+1` na mesma faixa mas vem de outra fonte. Uma arma Frágil **com** gambiarra acumula duas fontes na faixa de quebra. *Status:* canon.
- **Furtividade** — *Significa:* **perícia de AGI** — mover-se sem ser visto nem ouvido, permanecer parado e despercebido, acompanhar um alvo sem ser notado; é o teste que sustenta a Ação **Esconder**, **oposto à Percepção** dos observadores. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.4, §3.4 e §6.2; a Ação em `docs/gdd/GDD_Combate.md` §4. *Não confundir com:* **Prestidigitação** — *Furtividade esconde a pessoa, Prestidigitação esconde a coisa*; e com silenciar uma arma, que é **modificação e munição, nunca perícia**. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. **Ela não anula o raio de Ruído:** o Nível de Ruído alcança quem alcança, sem rolagem, e a **Atração** é automática dentro do raio. A **forma exata da interação** entre Furtividade e Nível de Ruído — Desvantagem, penalidade numérica ou falha automática — é `[A CALIBRAR]`. A direção, essa, é canon: **o Ruído age sobre a Furtividade, e a Furtividade nunca age sobre o Ruído.**
- **Gambiarra** — *Significa:* a via de fabricação **de campo** das Modificações: mais unidades de escassez menor, **nunca** exige Liga Pré-Queda, e **soma `+1` à faixa de quebra da arma** por modificação. *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §2 e §7. *Não confundir com:* **Oficina** (a outra via); e com "arma improvisada" — a propriedade **Improvisada** é do catálogo, não da via. *Status:* canon (a regra central de custo).
- **Imune** — *Significa:* o grau extremo da escala de resistência: dano **0**. *Onde mora:* `docs/gdd/GDD_Combate.md` §6.3. *Não confundir com:* **Muito Resistente** (dois degraus abaixo, mas ainda causa dano) e com imunidades de **condição** — o talento **Nervos de Aço** dá imunidade a **Amedrontado**, e **Enganchar** não afeta alvos duas categorias maiores; nenhuma dessas é imunidade a **tipo de dano**. *Status:* canon quanto ao efeito; **nenhuma criatura da tabela canônica de perfis é Imune a nada** — a coluna existe para o Bestiário, que **ainda não foi desenhado**.
- **Improvisada** — *Significa:* **propriedade de arma** — **não soma** o bônus de proficiência ao ataque. *Onde mora:* `docs/gdd/GDD_Armas.md` §3; anulada pela assinatura **Mão Calejada** (`docs/classes/Classe_Construtor.md` §3). *Não confundir com:* **Silencioso** (`docs/gdd/GDD_Ruido.md` §4 é explícito: *"improvisada não implica silenciosa"*), com o **tier Improviso** e com a via **Gambiarra**. *Status:* canon. Nota canônica: *gambiarra não apaga a origem da arma* — modificar não remove Improvisada.
- **Improviso** — *Significa:* o **primeiro dos seis tiers** de procedência de arma: *"lixo improvisado, quase sempre com **Improvisada** e/ou **Frágil**"*. *Onde mora:* `docs/gdd/GDD_Armas.md` §2 e §4.1. *Não confundir com:* a **propriedade Improvisada** (nem toda arma de tier Improviso a tem, e a assinatura **Mão Calejada** *"promove o tier Improviso a tier Civil sem tocar em nenhum dado"*); o estado de conservação **Arruinada**; a via **Gambiarra**; e o Recurso **Improviso Rápido** do Construtor. *Status:* canon (é um dos seis valores fechados da lista de tiers).
- **Infecção** — *Significa:* a trilha de pontos gerada por dano **Necrótico** de mutantes e zumbis (golpe que acerta = **1**; crítico = **2**), resolvida ao fim do combate com `d20 + CON` vs. **CD 10 + pontos ganhos naquele combate**; sucesso remove **metade** dos pontos ganhos. *Onde mora:* `docs/gdd/GDD_Infeccao.md`; condição **Infectado** em `docs/gdd/GDD_Combate.md` §10. *Não confundir com:* a condição **Irradiado** (outra trilha, também resistida com CON) nem com dano. A conversão é **por ataque acertado, não proporcional ao dano**. *Status:* canon; penalidades por faixa, critério entre mutação e morte e efeitos de mutação são `[A CALIBRAR]`.
- **Interação livre com objeto** — *Significa:* **uma por turno**, sem custo de Ação: sacar ou guardar arma, abrir porta destrancada, soltar ou pegar um item adjacente, apertar um botão ao alcance. *Onde mora:* `docs/gdd/GDD_Combate.md` §4.2 e §2.4. *Não confundir com:* a Ação **Usar Objeto**, que é o que se exige quando a interação livre **não** basta. *Status:* canon.
- **Intimidação** — *Significa:* **perícia de CAR** — ameaçar, impor presença, extrair informação pelo medo, dispersar um grupo sem violência, sustentar um blefe armado. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.18 e §4.7. *Não confundir com:* **Persuasão** — *Persuasão deixa a porta aberta, Intimidação a fecha atrás de você*; e com a condição **Amedrontado**, que é condição de combate com fonte própria. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. **Se Intimidação pode aplicar Amedrontado:** `[A CALIBRAR]` — hoje **a perícia não a aplica sozinha**. O "rastro" que ela deixa é **consequência narrativa**, não penalidade mecânica; transformá-lo em regra exigiria aprovação do Diretor.
- **Investigação** — *Significa:* **perícia de PER** — deduzir o que **esteve** lá: vasculhar cena, ler indício, reconstruir sequência de eventos, achar compartimento falso, cruzar documentos, identificar inconsistência num relato. É o pilar de **investigação** do jogo na ficha. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.14, §4.1 e §4.8. *Não confundir com:* **Percepção** — *Percepção é o instante, Investigação é o minuto*; e **Saber Pré-Queda** — *Saber Pré-Queda é o que a coisa era, Investigação é o que aconteceu com ela*. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. **Não tem nenhum uso canônico dentro do turno** — é perícia de cena; abrir um é `[A CALIBRAR]`.
- **Katana** — *Significa:* arma de **tier Militar**: 1d8 Cortante, Ruído **Silencioso**, propriedades **Ágil** e **Flexível** (2 mãos: 1d10); família **Lâminas Longas**. *Onde mora:* `docs/gdd/GDD_Armas.md` §4.4 (tier Militar) · `docs/classes/Classe_Ceifador.md` §5.3 (simulação de DPR) · aba *Corpo a Corpo* da planilha. *Não confundir com:* tier Civil — a justificativa canônica é explícita: *"uma espada de verdade num mundo de sucata não se acha numa garagem"*; e com a **Foice de Ceifar**, que tem o mesmo 1d8 Cortante Silencioso mas é *Lenta* e de *Duas mãos* — a Katana domina a Foice em dado, e só **Enganchar** salva a Foice. *Status:* canon, **integrada ao catálogo na Aprovação 024**, que também a **migrou de Lâminas Curtas para Lâminas Longas** (a taxonomia da Aprovação 018 é por tamanho de lâmina). A divergência 5 está fechada.
- **Lâminas Curtas** — *Significa:* uma das **dez famílias de arma** (taxonomia de proficiência): faca, facão, machadinha, garrafa quebrada, antena de carro, seringa de pressão. **A katana saiu desta família na Aprovação 024** e hoje é **Lâminas Longas**. **Não é arma de fogo.** *Onde mora:* CANON 017 §2; exemplos em `docs/gdd/GDD_Especializacoes.md` §5.2. *Não confundir com:* a propriedade **Leve** (quatro sentidos vivos, e este é um deles), o **calibre Leve** e o **tipo de dano Cortante** — família, propriedade, calibre e tipo de dano são quatro dimensões distintas. *Status:* canon (CANON 017 §2). Nota de leitura: **Cortante é tipo de dano, não família** — o mapeamento *Cortante → Lâminas Curtas / Lâminas Longas* usado em `docs/gdd/GDD_Especializacoes.md` está **inferido, não canônico** (§13.2 daquele documento).
- **Lâminas Longas** — *Significa:* uma das **dez famílias de arma**: **katana** (desde a Aprovação 024), machado de bombeiro, foice de ceifar, pá de sapador, machado corta-anteparo. **Não é arma de fogo.** *Onde mora:* CANON 017 §2; exemplos em `docs/gdd/GDD_Especializacoes.md` §5.2. *Não confundir com:* a propriedade **Pesada** (quatro sentidos vivos) e o tipo de dano **Cortante**. **Rebarbadora e Serra "Denteira" NÃO são Lâminas Longas** (Aprovação 018, registrada em `docs/classes/Classe_Ceifador.md` §5): são **ferramentas motorizadas**, e é a cláusula de motor que decide o Ruído delas, não a família. *Status:* canon (CANON 017 §2; recorte confirmado pela Aprovação 018).
- **Leve** — *Significa:* **propriedade de arma** — ocupa **meio slot de inventário**. *Onde mora:* `docs/gdd/GDD_Armas.md` §3. *Não confundir com:* o **porte Simples** de modificação (que antes se chamava Leve — colisão 1), o **calibre Leve** de munição, e a família **Lâminas Curtas**. Quatro usos da palavra, todos vivos. *Status:* canon.
- **Liga Pré-Queda** — *Significa:* o componente **RARO** (aço e titânio militares) e o **gargalo proposital** do sistema: **não é fabricável por nenhum meio, em nenhum tier, em nenhuma circunstância** — só se encontra saqueando. *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §4 e §4.1. *Não confundir com:* os outros sete componentes, e com "peça nova" (a modificação **Peças Novas**). Implementadores: marcar como recurso **não-fabricável** no motor. *Status:* canon; taxa de aparição em saque por tipo de local é `[A CALIBRAR]`.
- **Limiar** — *Significa:* **dois limiares independentes**. (a) **Limiar de Infecção**: pessoal, base **15**, faixa de classe ≈ `±3`, e atingi-lo causa **mutação ou morte**. (b) **Limiar do Medidor de Horda**: **20, em escada** — cruzou, subtrai 20 e continua contando. *Onde mora:* (a) `docs/gdd/GDD_Infeccao.md` §3; (b) `docs/gdd/GDD_Horda.md` §2. *Não confundir com:* entre si, nem com **banda**. Sempre qualifique: *limiar de Infecção* ou *limiar do Medidor*. *Status:* ambos canon; a progressão do limiar de Infecção em níveis 2+ é `[A CALIBRAR]`.
- **Maior** — *Significa:* o **terceiro porte de Especialização**, disponível a partir do **nível 13**. Compra **um Recurso de nível 10 ou 14 de outra classe**, e **conta contra a cota de 2 por classe**. São **16** entradas no catálogo. *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §2 e §7. *Não confundir com:* **Média** (Recurso de nível 2 ou 6) e com o adjetivo comum. *Status:* canon. Consequência canônica: como só há **três** níveis em que uma Maior cabe (13, 15 e 17) e o 17 costuma ir para a Assinatura, **a maioria dos personagens leva uma ou duas Maiores na carreira inteira** — são as escolhas mais caras em custo de oportunidade do sistema.
- **Mecânica** — *Significa:* **perícia de INT** — tudo que tem **peça**: fabricar, consertar, adaptar, desmontar. **É a perícia do teste de INT das Modificações**, das escoras e estruturas do Refúgio, dos mecanismos de porta, das armadilhas mecânicas e da manutenção de veículo. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.9, §3.1 e §4.2. *Não confundir com:* **Eletrônica** (*peça × corrente*), **Saber Pré-Queda** (*para que servia*), **Pilotagem** (*conduzir o que consertou*); nem com o componente **Peças Mecânicas** ou a família **Projéteis Mecânicos**, que só confundem busca. *Status:* canon quanto à existência e ao atributo (CANON 021 §1). **As 17 CDs de fabricação já são canônicas, de 8 a 16** (`docs/gdd/GDD_Modificacoes.md` §5.1) e **não** foram recalibradas. A falha crítica em `1` natural continua canônica. **Utilitária NÃO dá Vantagem em Mecânica** — a propriedade é *"Vantagem em testes de FOR para arrombar"* e nada mais; ver §6, divergência 24.
- **Mecanismo Explosivo** — *Significa:* o **mecanismo de arma** que a cláusula de motor classifica em Ruído **Alto** — pistola de pinos, granada — **sobrepondo a precedência**, inclusive quando a arma é de alcance 2 hex ou arremessável. *Onde mora:* `docs/gdd/GDD_Ruido.md` §1 (cláusula de motor, Aprovação 012); repetida em `docs/gdd/GDD_Armas.md` §8.1 e `docs/classes/Classe_Piloto.md` §5. *Não confundir com:* o tipo de dano **Fogo**, a propriedade **Carga (N)** e as **Munições Especiais** — *carga explosiva* é o quarto sentido vivo da palavra *carga* (§4). *Status:* canon (Aprovação 012, dentro da cláusula que sobrepõe a **Precedência de Ruído**).
- **Média** — *Significa:* o **segundo porte de Especialização**, disponível a partir do **nível 7**. Compra **um Recurso de nível 2 ou 6 de outra classe**, e **conta contra a cota de 2 por classe**. *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §2 e §6. *Não confundir com:* **Maior** e com "média" aritmética. *Status:* canon. **A Aprovação 022 reduziu este porte de 17 para 10 entradas** — 9 Recursos de classe + **Cicatrizado**, o único Talento Geral de porte Média — ao reclassificar sete Recursos "II" para porte **Assinatura**. Os verbetes dos sete continuam fisicamente no §6 de `docs/gdd/GDD_Especializacoes.md`, marcados com ⚠ e com o porte correto; **não devem ser contados como Médias**.
- **Medicina** — *Significa:* **perícia de INT** — ferimento, hemorragia, **estabilizar um aliado em Estado Crítico**, estancar **Sangrando**, tratamento da **Trilha de Infecção**, aplicação do **Soro de Campo**, farmácia improvisada, diagnóstico. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.11 e §3.3. *Não confundir com:* a **assinatura Estabilizar** do Médico, que é habilidade de classe e **não depende desta perícia**; o **teste de resistência de CON** contra Infecção, que é CON puro; e a **Enfermaria** do Refúgio, que é instalação, não perícia (o nome *"Oficina médica"* foi aposentado pela Aprovação 023). *Status:* canon quanto à existência e ao atributo (CANON 021 §1); as três CDs que ela ganhou são **herdadas e `[A CALIBRAR]`** — estabilizar aliado (`docs/gdd/GDD_Combate.md` §8.5), estancar Sangrando (§10), tratar Infecção (`docs/gdd/GDD_Infeccao.md`, "Remoção"). **Ela é o quarto contexto da palavra Estabilizar** e **não deve compartilhar identificador** com nenhum dos três já existentes (§2.1).
- **Medidor de Horda** — *Significa:* contador **de cena**, mantido pelo Mestre, que soma **apenas o ruído mais alto que o grupo produziu por rodada** (0/1/3/6) e traz uma leva a cada 20 pontos. **Zera no fim da cena**, não no fim do combate. *Onde mora:* `docs/gdd/GDD_Horda.md`. *Não confundir com:* a **Atração** (imediata) e o **contador de Rastreio** da telemetria corporativa. *Status:* canon. **Regra de visibilidade, não sugestão: é recurso EXCLUSIVO DO MESTRE** — nunca exposto ao jogador, nem como número, nem como barra, nem como alerta.
- **Menor** — *Significa:* o **primeiro porte de Especialização**, disponível a partir do **nível 3**. Compra **uma** de quatro coisas: **uma perícia · uma família de arma · um teste de resistência · um Talento Geral**. **Não conta contra a cota de 2 por classe**, porque nenhuma dessas quatro pertence a classe nenhuma. São **41** entradas no catálogo (18 perícias + 10 famílias + 6 resistências + 7 Talentos Gerais de porte Menor). *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §2 e §5. *Não confundir com:* **Média** — e note que **Cicatrizado**, apesar de ser Talento Geral, é de porte **Média**, não Menor. *Status:* canon. Duas consequências canônicas: **as duas primeiras escolhas de qualquer personagem (níveis 3 e 5) são obrigatoriamente Menores**, e é por isso que elas são o lugar natural de pagar os pré-requisitos da Regra 2; e a Menor é **irreversível** — a família comprada fica na ficha para sempre. **Teto de perícias adquiridas por Menor, se houver:** `[A CALIBRAR]`.
- **Mirar** — *Significa:* uma **Ação** inteira que concede **Vantagem** no próximo ataque à distância **e +2 de dano**, se você não se moveu. **Não** combina com **Rajada** nem com **Automático** (Aprovação 002). *Onde mora:* `docs/gdd/GDD_Combate.md` §4. *Não confundir com:* a **Marcação** do Fuzil "Testemunha" (que *usa* Mirar) e com **Tiro Calculado** (assinatura do Atirador de Elite, que só altera a faixa de crítico sob Mirar). *Status:* canon; nenhuma classe barateia o custo de Mirar.
- **Modificação** — *Significa:* uma das **17** alterações permanentes de arma, existentes em duas vias (**Gambiarra** e **Oficina**) com **efeito mecânico idêntico** e custos diferentes. *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §5. *Não confundir com:* **Modificação Veicular** (assinatura do Piloto, **bloqueada** — o módulo de Veículos não existe) e com **Munições Especiais** de munição, que não são modificação. *Status:* canon; tempo de fabricação, remoção e teto por família são `[A CALIBRAR]`.
- **Muito Resistente** — *Significa:* o grau de resistência que faz o dado de dano **descer dois degraus** na escada. *Onde mora:* `docs/gdd/GDD_Combate.md` §6.3. *Não confundir com:* **Resistente** (um degrau) e **Imune** (dano 0). *Status:* canon quanto ao efeito; **nenhuma criatura da tabela canônica de perfis usa a coluna hoje** — ela existe para o Bestiário, que ainda não foi desenhado. O **piso** vale igual: arma já em `1d4` perde **1 de dano** em vez de descer degrau, mínimo 1.
- **Munição Padrão** — *Significa:* a munição que **se saqueia**, sem efeito especial, dentro de um dos seis pools. *Onde mora:* `docs/gdd/GDD_Combate.md` §13.1. *Não confundir com:* as **dez Munições Especiais**, que **não se acham — fabricam-se**, com os mesmos oito componentes das Modificações; e com a propriedade **Carga (N)**, que é recurso do item e **não usa pool de calibre**. *Status:* canon no princípio; o módulo de *tipos* e *melhorias* de munição está pendente por pedido do Diretor.
- **Munições Especiais** — *Significa:* as **dez** munições que **não se acham — fabricam-se**, com os **mesmos oito componentes** das Modificações. *Onde mora:* `docs/gdd/GDD_Combate.md` §13.1; a aba `Munições Especiais` da planilha. *Não confundir com:* **Munição Padrão** (a que se saqueia), **Modificação** (munição **não é** modificação — `docs/classes/Classe_Cientista.md` §5.3 é explícito), a propriedade **Carga (N)** e a propriedade **Munição Exótica**. *Status:* canon no princípio; **o módulo de *tipos* e *melhorias* de munição está pendente por pedido do Diretor**. Regra canônica já fechada: **munição de Gambiarra soma `+1` à faixa de travamento** enquanto estiver carregada, e a de Oficina não tem penalidade. **Nenhuma das dez é anti-Infecção** (`docs/classes/Classe_Cientista.md` §5.3).
- **Nível de Ruído** — *Significa:* a escala **0 a 3** com raio fixo: Silencioso (0, sem raio) · Baixo (1, **4 hex / 6 m**) · Médio (2, **20 hex / 30 m**) · Alto (3, **50 hex / 75 m**), valendo 0 / 1 / 3 / 6 pontos no Medidor. *Onde mora:* `docs/gdd/GDD_Ruido.md` §1. *Não confundir com:* nível de personagem. **Piso canônico: arma de fogo nunca chega a Silencioso**, por mais que se empilhe silenciador e munição Subsônica — a combinação **para em Baixo**. *Status:* canon.
- **Oficina** — *Significa:* a **via de fabricação** limpa das Modificações — menos unidades de escassez maior, quase sempre exige **Liga Pré-Queda**, **nenhuma penalidade** de quebra —, que requer **bancada em Refúgio**. *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §2. *Não confundir com:* **Oficina de Campo**, a assinatura do **Cientista**, que executa **uma** modificação de qualidade Oficina **sem bancada**, 1× por descanso longo, **sem dispensar componentes nem Liga**; e com **Gambiarra**, a outra via. *Status:* canon. **A Aprovação 023 retirou o terceiro sentido:** a instalação médica do Refúgio chama-se **Enfermaria**, e *"Oficina médica"* não é mais nome canônico. A palavra continua na tabela de queimadas de §4 com **dois** sentidos, e o qualificador entre eles continua obrigatório.
- **Percepção** — *Significa:* **perícia de PER** — notar o que **está lá agora**: emboscada, alvo escondido, som fora de lugar, fio de armadilha, movimento na periferia. É o lado **defensivo** dos testes opostos de **Esconder** e de **Prestidigitação**. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.13, §3.5, §4.1 e §6. *Não confundir com:* **Investigação** (*o instante × o minuto*), **Rastrear** (seguir até a origem), **Sobrevivência** (ler o terreno para decidir rota) — nem com o **atributo PER**, que é a sigla e não a perícia. *Status:* canon quanto à existência e ao atributo (CANON 021 §1). Ela é a dona da **CD do teste de PER para detectar emboscada**, aberta desde `docs/gdd/GDD_Combate.md` §2.2 — **e o número continua `[A CALIBRAR]`**: dar dono não é calibrar. Aparece em **6 das 8** listas de classe. Uso defensivo é **livre**; se notar alvo escondido durante o turno é livre, parte do Movimento ou custa a Ação: `[A CALIBRAR]`.
- **Perícia** — *Significa:* um **campo de competência treinada** que se soma a um atributo: `d20 + mod. de atributo + proficiência (SE treinado) vs. CD`. São **18**, distribuídas por seis atributos (FOR 2 · AGI 4 · CON 2 · INT 4 · PER 4 · CAR 2). **Cada classe escolhe 3 de uma lista de 6.** *Onde mora:* `docs/gdd/GDD_Pericias.md` §1, §2 e §5. *Não confundir com:* **teste de resistência** — *se o Mestre pediu o teste, é resistência; se o jogador pediu, é perícia*. *Status:* canon quanto à estrutura (CANON 021 §1); **todas as faixas de CD são `[A CALIBRAR]`**, exceto as 17 CDs de fabricação (8 a 16), que já eram canônicas. Quatro regras de mesa fechadas: **não ter a perícia não impede o teste** (rola-se `d20 + atributo`); **nenhuma perícia é obrigatória** — *um Médico sem Medicina é um personagem, não um erro*; **nenhuma perícia adiciona proficiência a teste de resistência**; e **implementadores não podem bloquear a ação no motor por falta de perícia** — ela apenas deixa de somar proficiência. Efeito de `20` e `1` natural em teste de perícia e regra de empate em teste oposto: `[A CALIBRAR]`.
- **Persuasão** — *Significa:* **perícia de CAR** — negociar, convencer, acalmar, mentir de forma plausível, conseguir passagem ou informação **sem arma na mão**, mediar entre facções, comprar tempo. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.17 e §4.7. *Não confundir com:* **Intimidação**, que nunca aparece na mesma lista de classe — *nenhuma lista tem mais de uma perícia de CAR*, o que impede um "personagem social" construído só por perícia. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. **Se a banda Infectado impõe Desvantagem em Persuasão:** `[A CALIBRAR]` — hoje `docs/gdd/GDD_Infeccao.md` §3 declara o custo da banda como **social, não mecânico**.
- **Pesada** — *Significa:* **propriedade de arma** — exige **FOR mínima** (faixa autorizada 12 a 16, por arma); abaixo dela, **desvantagem no ataque**. *Onde mora:* `docs/gdd/GDD_Armas.md` §3 (Aprov. 009). *Não confundir com:* o antigo porte de modificação de mesmo nome, hoje **Estrutural** (colisão 1); com o **calibre Pesado**; e com a família **Lâminas Longas**. Na **precedência de Ruído**, Pesada é o topo: **se é Pesada, o Ruído é Baixo**, qualquer que seja o tipo de dano. *Status:* canon; a FOR mínima por arma é editável pelo Diretor dentro de 12–16.
- **Pilotagem** — *Significa:* **perícia de AGI** — conduzir veículo terrestre sob pressão, manobra evasiva, trafegar em entulho, atravessar barricada, controlar derrapagem. É **a ficha da porta suave do Piloto**. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.6 e §3.7. *Não confundir com:* **Mecânica** (consertar o veículo), **Sobrevivência** (ler o terreno para escolher a rota) e a assinatura **Modificação Veicular**, que continua **bloqueada**. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); **é a única perícia que aparece em uma só lista de classe**. É plenamente rolável em condução narrada, mas **velocidade, colisão, dano de veículo, capacidade, combustível e perseguição em grid pertencem ao módulo de Veículos, que ainda não foi desenhado**: `[A CALIBRAR]`. Registrá-la agora evita que aquele módulo invente uma segunda.
- **Porta suave** — *Significa:* o desenho canônico de pilar — **qualquer personagem acessa em tier ruim; a classe especialista é indispensável para o tier bom, não para o acesso**. São **três**: Modificações (**Cientista**), Refúgio (**Construtor**), Veículos (**Piloto**). *Onde mora:* `CANON_CLASSES.md` §2, replicado em todos os `Classe_*.md` §4. *Não confundir com:* **assinatura**, que é habilidade de classe e não abre pilar. Médico, Pugilista, Explorador e Atirador de Elite **não têm** porta suave, e isso é declarado, não lacuna. *Status:* canon; uma quarta porta é **por padrão inexistente** e exigiria proposta nova.
- **Porte** — *Significa:* **duas coisas, em dois sistemas que não se tocam**. (a) **Porte de modificação ofensiva:** **Simples** (1 slot, `+1` degrau de dado) ou **Estrutural** (2 slots, `+2` degraus). Só a família Ofensiva declara porte. (b) **Porte de Especialização:** **Menor** (nv 3), **Média** (nv 7), **Maior** (nv 13), **Assinatura** (nv **17**) — o que a Especialização pode comprar e a partir de que nível. *Onde mora:* (a) `docs/gdd/GDD_Modificacoes.md` §3 e §6 (Aprovações 012 e 013); (b) `docs/gdd/GDD_Especializacoes.md` §2 (fixado pelo CANON 021 §2, recontado pela Aprovação 022). *Não confundir com:* as propriedades **Leve** e **Pesada**, que foram os nomes antigos dos dois portes de modificação (colisão 1) e **não interagem** com eles; e os dois sentidos **entre si** — um mede **slots de arma**, o outro mede **nível de personagem**. *Status:* ambos canon. **Qualificador obrigatório:** escreva sempre *porte de modificação* ou *porte de Especialização*, nunca a palavra nua. Ver §2.1 — a palavra é candidata a colisão.
- **Precedência de Ruído** — *Significa:* a ordem fixa para armas que caem em mais de uma categoria: **PESADA vence CONCUSSÃO, que vence CORTANTE / PERFURANTE / LEVE**. A **cláusula de motor** (Aprovação 012) **sobrepõe** a precedência: tensão mecânica = Silencioso · pneumático ou motor leve = Baixo a Médio · **motor pesado = Alto** · **mecanismo Explosivo = Alto**. *Onde mora:* `docs/gdd/GDD_Ruido.md` §1; repetida em `docs/gdd/GDD_Armas.md` §8.1. *Não confundir com:* ordem de resolução de um ataque (`docs/gdd/GDD_Combate.md` §5.5). *Status:* canon; corpo a corpo motorizado acima de Baixo existe no catálogo como exceção **não formalizada** (ver §6, divergência 9).
- **Prestidigitação** — *Significa:* **perícia de AGI** — mãos rápidas e finas: furtar de um bolso ou mochila, plantar um item, ocultar objeto no corpo, trocar um item por outro, manipular mecanismo delicado **sob observação**, truque de mão para distrair. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.5 e §4.6. *Não confundir com:* **Furtividade** (*esconde a pessoa* × *esconde a coisa*), **Mecânica** (montar ou consertar, mesmo com dedo fino) e **Arrombamento**. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. Ela **existe para o risco de ser pego** — sem observador não há teste —, e por isso costuma ser **teste oposto contra a Percepção** de quem observa.
- **Projéteis** — *Significa:* um dos **seis pools de munição** — flechas, virotes, dardos — e o **único recuperável** do jogo. *Onde mora:* `docs/gdd/GDD_Combate.md` §13.1. *Não confundir com:* a família **Projéteis Mecânicos** (colisão 4). Nota canônica: **flecha recuperada perde a melhoria** — recupera-se o projétil, não a carga. *Status:* canon; a regra de recuperação (quantas voltam, teste, chance de quebra) é `[A CALIBRAR]`.
- **Projéteis Mecânicos** — *Significa:* a **família de arma** de tensão mecânica: arco artesanal, besta de caça, besta pesada, fisga de rolamentos, arpão pneumático, lançador de cabo. *Onde mora:* CANON 017 §2. *Não confundir com:* o pool **Projéteis** — o nome longo existe **exatamente** para não colidir com ele. *Status:* canon (CANON 017).
- **Propriedade de arma** — *Significa:* uma das **24 propriedades canônicas** que uma arma carrega (Ágil, Leve, Pesada, Duas mãos, Lenta, Improvisada, Utilitária, Arremessável, Alcance 2 hex, Frágil, Flexível, Enganchar, Recarga, Cone, Acoplada, Dupla Face, Transfixante, Estacar, Enxertada, Carga, Trilha de Calor, Munição Exótica, Espalhamento, Linha). *Onde mora:* `docs/gdd/GDD_Armas.md` §3. *Não confundir com:* **família de arma** e **tipo de dano**. Regra de nomenclatura: **proficiência lê a propriedade, nunca o nome da arma**. *Status:* canon. **"Confiável" (nunca trava) foi REJEITADA** na Aprovação 009 e não deve reaparecer.
- **Quebra** — *Significa:* a arma **se parte**. A **faixa de quebra** é o intervalo de resultados naturais do d20 de ataque que a partem: 0 gambiarras = 0% · 1 = 5% · 2 = 10% · 3 = 15%. Vem da propriedade **Frágil** e do `+1` que cada modificação **Gambiarra** acrescenta, **inclusive em corpo a corpo**. *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §7 e §7.1. *Não confundir com:* **travamento** (colisão 3) — **nunca se somam**; as duas podem disparar no mesmo `1` natural sem que os números interajam. *Status:* canon (Aprovação 013).
- **Rajada** — *Significa:* modo de disparo: **−2** no ataque, **+1 dado de dano**, **3** de munição, **uma** rolagem de ataque. **Restrita ao calibre Rifle.** No crítico soma **UM dado adicional** em vez de dobrar. *Onde mora:* `docs/gdd/GDD_Combate.md` §7.2; exceção de crítico em `docs/gdd/GDD_Armas.md` §1.2 (Aprovação 009). *Não confundir com:* **Automático** (10 de munição, cone, sem rolagem de ataque, sem crítico e sem travamento). Não combina com **Mirar**. *Status:* canon; é a **única exceção deliberada** ao teto de DPR (7,28), contida pela escassez do calibre.
- **Raridade** — *Significa:* **quão difícil é achar** um item ou componente. Escala única de seis degraus: **Abundante · Comum · Incomum · Raro · Épico · Mítico**. *Onde mora:* `docs/gdd/GDD_Saque.md` §2; a raridade de cada arma em `docs/gdd/GDD_Armas.md` §2.1. *Não confundir com:* **Tier**, que é **procedência** (de onde veio, quão bem foi feita) — as duas se correlacionam mas não são hierarquia; uma katana é Militar e Rara, uma Carabina M-24 é Militar e Incomum. *Status:* canon (Aprovação 032). **Unificou a antiga "escassez" dos componentes**, que usava as mesmas palavras para o mesmo conceito.
- **Mítico** — *Significa:* o topo da escala de raridade. **Nunca cai de tabela**: é decisão exclusiva do Diretor. *Onde mora:* `docs/gdd/GDD_Saque.md` §2. *Não confundir com:* **Protótipo**, que é tier (procedência) — a maioria dos Protótipos é **Épica**, e só dois são Míticos. *Status:* canon (Aprovação 032); substitui o termo *raridade extrema*.
- **Raridade extrema** — ⚠ **TERMO APOSENTADO (Aprovação 032).** Virou **Mítico**, o topo da escala de raridade (`docs/gdd/GDD_Saque.md` §2), com a mesma regra: as quatro armas que mexem na Trilha — *Miséria, Segunda Boca, Boca de Forno, Ferro de Marca* — e o Soro Anti-Infecção **não caem de tabela nenhuma**; a distribuição é decisão exclusiva do Diretor.
- **Rastrear** — *Significa:* **perícia de PER** — seguir pegada, sangue, arrasto e trilha de horda; estimar **número, direção e há quanto tempo**; distinguir rastro humano de mutante; perceber que estão **seguindo o grupo**. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.16 e §4.3. *Não confundir com:* **Sobrevivência** — *Sobrevivência busca uma categoria e responde "onde"; Rastrear segue um indivíduo e responde "quem, quantos e quando"*; e **Percepção**, quando o rastro é notado **no instante**, sem ser procurado. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. Em terreno que **não guarda marca** o Mestre deve declarar a impossibilidade antes, **não transformá-la em CD impossível**.
- **Reação** — *Significa:* **uma por turno**, reposta no **início do próprio turno**. Cobre o **ataque de oportunidade** e as reações concedidas por propriedades (**Estacar**) ou assinaturas (**Esquiva Reflexa**). *Onde mora:* `docs/gdd/GDD_Combate.md` §4.1 e §2.4. *Não confundir com:* **Ação Bônus**. Nota de mesa: quem gasta a Reação logo após o próprio turno fica sem ela por quase uma rodada inteira, e **ataque de oportunidade e defesa reativa disputam o mesmo recurso**. *Status:* canon; reações de talento, cibernética e equipamento são `[A CALIBRAR]`.
- **Recurso de classe** — *Significa:* o que uma classe entrega **de graça, no próprio nível**, sem gastar Especialização: **cinco** por classe, nos níveis **2, 6, 10, 14 e 18**, mais o **Ápice** no 20. São **48** catalogados. *Onde mora:* a tabela de progressão de cada `Classe_*.md` §6; catálogo transcrito em `docs/gdd/GDD_Especializacoes.md` §6 a §9. *Não confundir com:* **Especialização** (o que se compra de outra classe), **Assinatura** (que vem no nível 1) e **Ápice** (nível 20). *Status:* canon quanto à lista. A ponte entre os dois sistemas é fixa: um Recurso de **nível 2 ou 6** é exportável como **Média**; um de **nível 10 ou 14**, como **Maior**; e os de **nível 18 nunca são exportáveis** (Regra 3). **Ritmo idêntico nas oito classes** (Aprovação 019): ao fim da carreira, **8 Especializações · 5 Aumentos de atributo · 5 Recursos de classe · 1 Ápice**.
- **Resistente** — *Significa:* o grau de resistência que faz o dado de dano **descer um degrau** na escada. **Resistência não corta o dano pela metade — ela move a arma na escada de dados**, e é essa a moeda: medido em 200.000 tiradas, a metade clássica custaria 52–54% de DPR, contra 12–19% de um degrau. *Onde mora:* `docs/gdd/GDD_Combate.md` §6.3. *Não confundir com:* **teste de resistência** (instrumento de ficha, sem relação nenhuma com isto), **Defesa** e **Cobertura**. *Status:* canon. Cinco regras fechadas: **piso** — arma já em `1d4` perde **1 de dano** em vez de descer degrau, mínimo 1; **aplica-se POR DADO, não ao total** — a Soqueira "Vólt-9" (1d6 Concussão + 1d6 Elétrico) contra alvo Resistente a Concussão vira `1d4 + 1d6`; é por isso que o **dado secundário foi travado em 1d6** (Aprovação 009); **armadura comum não concede resistência nenhuma** — ela já reduz a frequência de acerto pela Defesa, e resistência vem de **material**, não de peça (placa de **Liga Pré-Queda** = Resistente a Balístico); e os perfis canônicos são **zumbi comum** (Vulnerável a Fogo; Resistente a Perfurante e Balístico), **mutante** (Vulnerável a Fogo; Resistente a Perfurante e Necrótico) e **alvo com cibernética** (Vulnerável a Elétrico/EMP; Resistente a Perfurante, Necrótico e Químico).
- **Resistir Toxinas** — *Significa:* **perícia de CON** — identificar, diluir, neutralizar e tolerar veneno, gás, solvente e reagente **de forma ativa e voluntária**: julgar se a água serve, reconhecer uma fumaça, dosar um estimulante conhecido, trabalhar perto de **Química** sem se intoxicar. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.8 e §4.5. *Não confundir com:* o **teste de resistência de CON** que a condição **Envenenado** e o dano **Químico** exigem, nem o de **Radiação** — a perícia serve para **não chegar lá**; depois que a toxina entrou, o problema é do teste de resistência e de **Medicina**. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`.
- **Sangrando** — *Significa:* condição com **trilha de camadas**: o alvo sofre **1 ponto de dano por camada** no **início de cada um dos seus turnos**, com **teto de 5 camadas**. Cessa com **qualquer cura** ou com a **Ação** de estancamento (Usar Objeto, **Medicina CD 12**), que remove **todas** as camadas de uma vez. *Onde mora:* `docs/gdd/GDD_Combate.md` §10 e §10.2 (Aprovação 028). *Não confundir com:* a **Trilha de Infecção**, que persiste além do combate e não é dano; e com **Envenenado**, cujo dano contínuo continua `[A CALIBRAR]`. *Status:* canon. **Propriedade medida, não desenhada: Sangrando é anti-chefe.** Como dispara no início do turno do alvo, ele rende **+8%** contra um Zumbi comum de 12 HP e **+40%** contra o Gigante de 80 — **a única mecânica do sistema cuja inclinação favorece alvo único em vez de bando**, e por isso o corretivo exato do problema medido em `docs/gdd/GDD_Bestiario.md` §3. Quem o aplica: a serra **"Denteira"**, 1 camada por acerto e 2 no crítico.
- **Saber Pré-Queda** — *Significa:* **perícia de INT** — o mundo que acabou: siglas, logotipos, protocolos, hierarquias corporativas, para que servia um prédio, como se lia um formulário, o que significava um símbolo de risco, onde ficava o almoxarifado numa fábrica. É também a perícia que **decifra um manual saqueado** como fonte diegética. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.12 e §4.8; uso em fonte diegética em `docs/gdd/GDD_Especializacoes.md` §10. *Não confundir com:* **Investigação** — *Saber Pré-Queda é o que a coisa era, Investigação é o que aconteceu com ela*; e com **Mecânica** / **Eletrônica**, que operam o que foi reconhecido. *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. Era um dos **dois termos novos sem verbete** apontados em `docs/gdd/GDD_Pericias.md` §8.1 (item 3) — este ciclo fecha a pendência.
- **Slot** — *Significa:* **slot de modificação** — arma comum **2**, arma especializada **3** (rifle de precisão, besta, metralhadora). Ofensiva Simples = 1, Estrutural = 2, qualquer não ofensiva = 1 salvo indicação contrária. **Slot gasto não volta: modificação é permanente.** *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §3. *Não confundir com:* **slot de inventário** (a propriedade **Leve** ocupa meio) e o **slot da Ação Bônus**. Três slots diferentes, mesma palavra. *Status:* canon (Aprovação 013).
- **Sobrevivência** — *Significa:* **perícia de PER** — ler terreno, achar água potável e abrigo, forragear, orientar-se, prever o tempo, montar acampamento, evitar zona quente — **e encontrar os oito componentes de fabricação no saque**, que é o que a liga direto na economia. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.15, §3.8 e §4.3. *Não confundir com:* **Rastrear** (seguir um alvo específico), **Resistir Toxinas** (julgar se a água achada é tóxica) e **Mecânica**/**Eletrônica** (fabricar com o que achou). *Status:* canon quanto à existência e ao atributo (CANON 021 §1). **Desde a Aprovação 033 ela decide o tamanho do saque do grupo** (CD 13: sucesso = `3d6` mantendo os 2 maiores; falha = os 2 menores — `docs/gdd/GDD_Saque.md` §4.1). Componente específico não se procura mais por teste: ele sai da tabela única. Continua `[A CALIBRAR]`: assim como saber se a busca consome tempo de cena, de descanso ou de downtime. Dois limites duros que a perícia **não move**: **Liga Pré-Queda continua não-fabricável** — uma Sobrevivência excelente **encontra** Liga, nenhuma a **produz** —, e a taxa de aparição de Liga por tipo de local continua `[A CALIBRAR]`. O talento **Faro para Sucata** dá **Vantagem em Sobrevivência para encontrar componentes**, e fica **inerte** sem esta perícia.
- **Soro Anti-Infecção** — *Significa:* o item de **raridade extrema** que **zera a Trilha de Infecção inteira**, de qualquer banda. É **trava de distribuição**: nenhuma habilidade, classe ou Especialização o produz, e só entra em jogo por **decisão do Diretor**. *Onde mora:* `docs/gdd/GDD_Infeccao.md`, "Remoção" (tabela das quatro vias); a trava em `docs/gdd/GDD_Armas.md` §7.4. *Não confundir com:* o **Soro de Campo**, que é outro item — **são dois desde a Aprovação 023 e não devem compartilhar identificador no motor**. *Status:* canon; quantidade de doses e critério de distribuição `[A CALIBRAR]`.
- **Soro de Campo** — *Significa:* o soro que o **Médico fabrica a partir do nível 14**, um por **descanso longo**, consumindo **Química**. Remove **`N` pontos** da Trilha e **nunca a zera**. *Onde mora:* `docs/classes/Classe_Medico.md` §6 (nível 14) e `docs/gdd/GDD_Especializacoes.md` §7.12, que o exporta como **Maior**. Aplicá-lo é **Medicina** (`docs/gdd/GDD_Pericias.md` §2.11); a exigência de componente vem da regra geral de produção (`docs/gdd/GDD_Modificacoes.md` §4). *Não confundir com:* o **Soro Anti-Infecção** de raridade extrema, que **zera**; a assinatura **Estabilizar**, que remove pontos **sem soro nenhum**; e as **Munições Especiais**, das quais **nenhuma é anti-Infecção**. *Status:* canon quanto a ser item próprio, parcial e pago em componente (Aprovação 023). `[A CALIBRAR]`: **quanto remove (`N`)** e **quanta Química custa**. A tensão registrada em §6, divergência 26, está **resolvida** — eram dois itens, não uma contradição.
- **Suporte** — *Significa:* a **família de modificação** de defesa, iluminação e economia de turno — Guarda-mão, Lanterna Acoplada, Alça Tática. *Onde mora:* `docs/gdd/GDD_Modificacoes.md` §5. *Não confundir com:* a **propriedade Utilitária**, cujo nome esta família usava antes (colisão 2). *Status:* canon (Aprovação 013).
- **Talento Geral** — *Significa:* uma aquisição que **não pertence a classe nenhuma** e, por isso, **não conta contra a cota de 2 por classe**. São **oito**: **Nervos de Aço** (imune a Amedrontado), **Pé Firme** (não fica Caído por empurrão ou Enganchar), **Carregador** (`+2` slots de inventário), **Faro para Sucata** (Vantagem em Sobrevivência para componentes), **Mão Firme** (Recarregar deixa de custar a Ação, 1× por combate), **Ouvido Treinado** (direção da última fonte de ruído fora do campo de visão), **Sangue Frio** (1× por combate, refaz um teste de resistência de morte) — todos de porte **Menor** — e **Cicatrizado** (**Limiar de Infecção +2**), o único de porte **Média**. *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §5.4. *Não confundir com:* **Recurso de classe** e **assinatura**. *Status:* canon quanto à lista e aos efeitos. **Nenhum Talento Geral concede uso novo de Ação Bônus** — o escopo dela segue fechado em Destravar. **Talento inerte:** *Mão Firme* sem arma de fogo e *Faro para Sucata* sem a perícia Sobrevivência não fazem nada; se isso os torna **indisponíveis** (leitura da Regra 2) ou apenas **inertes** é pendência registrada em `docs/gdd/GDD_Especializacoes.md` §13.10.
- **Teste de resistência** — *Significa:* o instrumento oposto à perícia — **o mundo rola contra você**. São **6** (FOR, AGI, CON, INT, PER, CAR) e cada classe tem **2 fixos**. *Onde mora:* `docs/gdd/GDD_Pericias.md` §1.1; lista e coberturas em `docs/gdd/GDD_Especializacoes.md` §5.3; listas por classe em `docs/gdd/GDD_Pericias.md` §5. *Não confundir com:* **perícia** — *se o Mestre pediu o teste, é resistência; se o jogador pediu, é perícia*; nem com **Resistente**, que é resistência a **tipo de dano** e não tem relação alguma com isto. *Status:* canon quanto à estrutura (CANON 021 §1). **Regra absoluta: nenhuma perícia soma proficiência a teste de resistência.** O caso canônico é **o teste de CON contra Infecção, que NÃO é a perícia Vigor** — o modificador de CON é um **dial fraco de propósito**, e se Vigor somasse ali, a Trilha de Infecção deixaria de morder. Um teste de resistência é comprável por Especialização **Menor**, e a resistência de **CON** é descrita como *"a Menor de maior impacto silencioso do jogo"*.
- **Tier** — *Significa:* um dos **seis** níveis de procedência de arma (o segundo se chamava *Comum* até a Aprovação 032 e virou **Civil**, para liberar a palavra para a **Raridade**): Improviso, Civil, **Modificada**, Militar, Corporativa, Protótipo. Só **Modificada** se fabrica; de Militar para cima, só se encontra. *Onde mora:* `docs/gdd/GDD_Armas.md` §2. *Não confundir com:* **estado de conservação**, **raridade extrema** e o "tier bom / tier ruim" das portas suaves, que fala de qualidade de acesso a pilar, não de arma. *Status:* canon.
- **Trajetória** — *Significa:* a **sequência completa das oito Especializações de um personagem, do nível 3 ao 17**, lida como um todo. Não é mecânica: é a unidade de análise com que o canon avalia se um conjunto de escolhas se soma ou se anula. `docs/gdd/GDD_Especializacoes.md` §12 traja **seis** delas por extenso, **uma das quais é declaradamente uma armadilha**. *Onde mora:* `docs/gdd/GDD_Especializacoes.md` §12. *Não confundir com:* **Trilha** (contador de pontos que persiste além do combate) — as duas palavras se parecem e não têm relação; nem com **porta suave**. *Status:* as trajetórias catalogadas são **exemplos canônicos de leitura**, não listas aprovadas de build. A lição declarada: *"antes de gastar a primeira Especialização numa classe, decida qual das quatro você quer daquela classe — só duas caberão, e a Assinatura só existe no 17"*. O sistema **não avisa** quando a cota fecha uma porta, e **não deve avisar**.
- **Travamento** — *Significa:* a arma de fogo **emperra**. Gatilho: qualquer `1` natural em rolagem de ataque com arma de fogo (a faixa cresce com o estado de conservação). A arma **não dispara em nenhum modo** até ser destravada, e **destravar custa 1 Ação Bônus**, não a Ação — o custo total de um travamento é de **1 turno, não 2**. *Onde mora:* `docs/gdd/GDD_Combate.md` §7.3. *Não confundir com:* **quebra** (colisão 3). **Armas de corpo a corpo nunca travam** — mas modificadas em Gambiarra, podem quebrar. *Status:* canon; o teste exigido para destravar, se houver, é `[A CALIBRAR]`.
- **Patamar** — *Significa:* as cinco faixas de nível usadas pelo orçamento de encontro e pelas simulações: **P1** níveis 1–4 · **P2** 5–8 · **P3** 9–12 · **P4** 13–16 · **P5** 17–20. Os cortes seguem a proficiência (+2 a +6 nos níveis 1/5/9/13/17). *Onde mora:* `docs/gdd/GDD_Bestiario.md` §5 (parâmetros) e §4.4 (limiares). *Não confundir com:* **Tier**, que é a **procedência de arma** (Improviso a Protótipo). *Status:* canon (Aprovação 030, **renomeado na 031**). Nasceu como *"tier de grupo"* e colidiu com o Tier de arma no mesmo ciclo; pelo critério do §2.2 — o sentido novo era recente, isolado e substituível — foi renomeado antes de virar dívida.
- **Trilha** — *Significa:* um contador de pontos que persiste **além do combate**. Existem várias e elas não se misturam: **Trilha de Infecção** (`docs/gdd/GDD_Infeccao.md`), a trilha de **Radiação** da condição Irradiado, a trilha de camadas de **Sangrando**, e a propriedade **Trilha de Calor (N)** do "Vigília". *Onde mora:* `docs/gdd/GDD_Combate.md` §10 lista as condições com trilha; `docs/gdd/GDD_Armas.md` §3 a propriedade. *Não confundir com:* entre si — **condições não acumulam com elas mesmas, salvo as que têm trilha de pontos**. *Status:* Infecção, Trilha de Calor e **Sangrando** são canon — o dano por camada foi fechado na **Aprovação 028** em **1 ponto, teto de 5 camadas**. Penalidades por faixa de **Radiação** continuam `[A CALIBRAR]`.
- **Utilitária** — *Significa:* **propriedade de arma** — a arma serve como ferramenta: **Vantagem em testes de FOR para arrombar**. *Onde mora:* `docs/gdd/GDD_Armas.md` §3. *Não confundir com:* a família de modificação hoje chamada **Suporte** (colisão 2). *Status:* canon.
- **ND (Nível de Desafio)** — *Significa:* a classificação de ameaça de uma criatura, de **0 a 5**, usada como **leitura de mesa** e, desde a Aprovação 030, como **âncora de nível**: ND 0–2 é conteúdo de **patamar 1** (níveis 1–4), ND 3–4 de **patamar 2** (5–8), ND 5 de **patamar 3** (9–12). **ND 6 em diante ainda não existe** — o Bestiário atual termina no patamar 3. *Onde mora:* `docs/gdd/GDD_Bestiario.md` §2 e §2.1. *Não confundir com:* **CD** (Classe de Dificuldade), que é o alvo de um teste de d20 — foi exatamente para evitar essa confusão que `ND` foi adotado (§2.0); e com **patamar** de arma e **porte** de Especialização, que são outras duas escalas. *Status:* canon (Aprovação 025). **ND NÃO é o orçamento** — as duas escalas foram declaradas independentes na Aprovação 027 e **não precisam concordar**: o Cuspidor é ND 4 e custa 2 pontos, o Zumbi de Sangue é ND 3 e custa 10. A razão é que **criatura de suporte vale quase nada sozinha**. Ver o verbete **Pontos de encontro**.
- **Aura** — *Significa:* efeito de criatura que se aplica a quem **começa o turno** dentro de um raio, **sem rolagem de ataque**. Duas no catálogo: a **aura venenosa** do Zumbi Venenoso (2 hex, 1d6 Químico + teste de CON ou 1 ponto de Infecção) e o **miasma** do Gigante Mutagênico (1 hex, 1 ponto de Infecção sem teste). *Onde mora:* `docs/gdd/GDD_Bestiario.md` §11.1 e §12.1. *Não confundir com:* **Atração** (efeito de Ruído sobre criaturas) e com ataque de área, que exige rolagem. *Status:* canon. **É o mecanismo que resolve o problema medido em `docs/gdd/GDD_Bestiario.md` §3:** aura ameaça a Trilha sem aumentar o número de ataques, e é o único jeito de uma criatura grande ser perigosa à Infecção sem virar uma picadora de HP.
- **Carga (N)** — *Significa:* **propriedade de arma** — o item tem `N` cargas, gastas por usos especiais dele. **NÃO é munição:** não usa pool de calibre, não se conta em pente e **não aparece na tabela de saque**. *Onde mora:* `docs/gdd/GDD_Armas.md` §3; a economia de reposição em `docs/gdd/GDD_Consumiveis.md` §3. *Não confundir com:* **Munições Especiais**, o **mecanismo Explosivo** — três sentidos vivos da palavra *carga*, não mais quatro — e o **pool de munição**. *Status:* canon (Aprov. 009), **com reposição fechada na Aprovação 028**: repor 1 Carga custa **1 unidade do componente** que a alimenta (Célula de Energia para elétricas, Química para incendiárias, Peças Mecânicas para o chamariz), **só em Refúgio com bancada** ou pela Oficina de Campo do Cientista. Ela **absorveu** *combustível* e *Energia da Célula* — o Maçarico de Solda passou de *"combustível 6 rodadas"* para **`Carga (6)`**.
- **Ponto de saque** — ⚠ **TERMO APOSENTADO (Aprovação 033).** Era a oportunidade de saque **por personagem**, 2 por cena, que rolava só munição. Foi substituído pelo **Saque** do grupo (`docs/gdd/GDD_Saque.md` §4). Não use mais o termo.
- **Tabela de saque** — *Significa:* a **tabela única** `1d100`, com uma coluna por **Patamar**, que diz o que cada item de um saque é: nada, sucata, componente, munição, arma ou equipamento. *Onde mora:* `docs/gdd/GDD_Saque.md` §4.2. *Não confundir com:* a antiga tabela de munição `1d20` da Aprovação 028, **substituída**; e com a fabricação de **Munições Especiais**, que não se acham. *Status:* canon (Aprovação 033), **calibrada**: arma de fogo com munição em **20–27%** dos combates, ~1 item Raro por personagem ao fim do P2, 1 a 2 Épicos ao fim do P5. **O ponto dela continua sendo o desequilíbrio** — o grupo pode ter muita munição e nenhuma arma.
- **Saque** — *Significa:* a oportunidade que o **Mestre concede ao grupo** de revirar um lugar: **uma rolagem por grupo**, `3d6` itens mantendo os 2 maiores (se o teste de **Sobrevivência CD 13** passa) ou os 2 menores (se falha) — média **7,1**, de 2 a 12. *Onde mora:* `docs/gdd/GDD_Saque.md` §4. *Não confundir com:* recompensa de combate — **matar uma criatura não gera tesouro**. *Status:* canon (Aprovação 033). Ritmo de referência: **~6 por Patamar**, onde o Mestre decidir.
- **Categoria de armadura** — *Significa:* **Nenhuma · Leve · Média · Pesada**, mais **Escudo leve** e **Escudo pesado**. Cada uma fixa uma faixa de bônus, um **limite de mod. de AGI** e uma **FOR mínima**. *Onde mora:* `docs/gdd/GDD_Combate.md` §5.3 (Aprovação 029). *Não confundir com:* **raridade** (Comum a Mítico, em construção no Bloco 3) — categoria é *quanto pesa*, raridade é *quão boa é a peça*; e com **tamanho** de criatura. *Status:* canon. **A FOR mínima é gate, não preço:** sem ela a peça não se veste. **Armadura pesada não é "melhor" — é a armadura de quem tem AGI baixa**: um personagem de AGI 16 ganha só 1 ponto de Defesa trocando Leve +3 por Pesada +7, e paga com Desvantagem em Furtividade.
- **Cisão** — *Significa:* a habilidade do **Gigante Mutagênico** de, ao chegar a 0 HP, **não morrer** e transformar-se em **4 Zumbis (ND 0)** no espaço que ocupava. *Onde mora:* `docs/gdd/GDD_Bestiario.md` §12.1. *Não confundir com:* a **leva** do Medidor de Horda, que vem da borda do mapa por ruído acumulado. *Status:* canon. Como a **aura**, existe por razão medida: um chefe de corpo único é estruturalmente fraco contra uma Trilha que conta acertos, e virar bando é a correção.
- **Errante** — *Significa:* a criatura que chega numa **leva** do Medidor de Horda. **Errante = Zumbi (ND 0)**, e uma leva de piso custa **2 pontos** de orçamento. *Onde mora:* `docs/gdd/GDD_Horda.md` §3 (o piso) e `docs/gdd/GDD_Bestiario.md` §16 (o que é). *Não confundir com:* o Bestiário inteiro — errante é **um** tipo, não um sinônimo de inimigo. *Status:* canon. O piso continua **piso**: o Mestre pode trocar um Zumbi da leva por um Maratonista ou um Uivante, e isso é uso legítimo do sistema.
- **Gera Infecção** — *Significa:* o campo de ficha de criatura que diz se o dano dela é **Necrótico** e portanto se cada acerto dela em você vale **1 ponto de Trilha** (2 no crítico). *Onde mora:* `docs/gdd/GDD_Bestiario.md` §14 (a tabela completa). *Não confundir com:* a **CD de Infecção**, que é o teste ao fim do combate. *Status:* canon. **Seis das dezoito criaturas NÃO geram** — Cachorro Explosivo, Touro Mecânico, Saqueador Humano, Vigia, Casulo e Cuspidor —, e isso cria vocabulário tático: são as criaturas seguras para o corpo a corpo.
- **Tamanho (categoria de)** — *Significa:* **Miúdo · Médio · Grande · Enorme**, que governam ocupação de hexágono, linha de visão, cobertura, o limite de **Enganchar** e **Agarrado** (não afetam alvo duas categorias maiores), empurrão e movimento através do espaço alheio. *Onde mora:* **`docs/gdd/GDD_Combate.md` §14** — é regra de combate, não de criatura; o Bestiário apenas usa a escala. *Não confundir com:* **ND**, que é ameaça e não volume — um Cachorro Explosivo é **Miúdo** e **ND 2**, um Casulo é **Grande** e também ND 2. *Status:* canon (Aprovação 025). **Tamanho não altera dado, HP nem Defesa** — acoplar as duas coisas criaria uma segunda escada competindo com o ND. `[A CALIBRAR]`: Minúsculo e Colossal, sem sujeito no MVP.
- **Pontos de encontro** — *Significa:* a moeda de **orçamento** do Bestiário, separada do ND. `custo = Σ(pontos) × M(n)`, com **M(1) = 1, M(2) = 1,5, M(n ≥ 3) = n − 1**. O ponto base é *ameaça por rodada × rodadas que a criatura sobrevive ao foco do grupo* — é aí que o HP entra. *Onde mora:* `docs/gdd/GDD_Bestiario.md` §4 (Aprovações 027 e 030). *Não confundir com:* **ND**, que é leitura de mesa e âncora de nível; com **pontos de Infecção**, **pontos do Medidor** e **pontos de saque**. *Status:* canon **por patamar**, no formato das tabelas de XP do d20: o custo da criatura é fixo, e cada **patamar** tem seus limiares de moderado, difícil e mortal (P1: 17 · 21 · 39; P2: 21 · 66 · 116; P3: 54 · 108 · 180; **P4 e P5 provisórios** até o Bloco 5). Acerta **83–88%** dos rótulos reais. **Limitação declarada:** o valor *relativo* das criaturas muda com o nível do grupo, então nenhuma tabela fixa é exata em todos os patamares. O multiplicador era `3n/4` na Aprovação 027; com os ataques da curva nova o bando ficou mais íngreme, e `n − 1` erra ±5% entre 2 e 10 criaturas.
- **Regra de suporte** — *Significa:* o **Vigia** custa **0 pontos sozinho e 2 acompanhado**, porque o dano dele é ao Medidor de Horda, que o orçamento não mede. *Onde mora:* `docs/gdd/GDD_Bestiario.md` §4.3. *Não confundir com:* a ação **Ajudar**. *Status:* canon, **reduzida na Aprovação 030**: até ali ela dobrava também a Doutora Zumbi, o Uivante e o Casulo, que eram medidos sozinhos. Hoje a Doutora Zumbi e o Uivante são **medidos acompanhados** e seus pontos já incluem o efeito — **não se dobram mais**.
- **Régua (o Zumbi comum como)** — *Significa:* a ratificação, pela Aprovação 025, de **Defesa 14 e HP 12** como valores **canônicos** do Zumbi comum — deixaram de ser *"zumbi comum hipotético `[A CALIBRAR]`"*. *Onde mora:* `docs/gdd/GDD_Bestiario.md` §1; os parâmetros em `docs/gdd/GDD_Armas.md` §1.2. *Não confundir com:* os **parâmetros do personagem** (ataque +5, dano +3, Defesa 13), que são o outro lado da mesma simulação. *Status:* canon. **Toda a tabela de armas, as simulações de 200.000 tiradas, o ritmo da Horda e as curvas das oito classes estão calibrados contra estes dois números** — por isso foram ratificados em vez de redesenhados.
- **Espaço de equipamento** — *Significa:* os sete lugares do corpo onde se veste algo: **Cabeça · Olhos · Corpo · Mãos · Pernas · Pés · Escudo**. Só Corpo, Cabeça, Pernas e Escudo dão Defesa; Olhos, Mãos e Pés são espaços de **função**. *Onde mora:* `docs/gdd/GDD_Equipamentos.md` §1. *Não confundir com:* **slot** de modificação e **slot** de inventário — a palavra *slot* já tem três sentidos, e por isso o lugar do corpo se chama **espaço**. *Status:* canon (Aprovação 034). Uma peça forte demais para um espaço pode ocupar dois — o Capuz de Moletom ocupa Corpo e Cabeça.
- **Estado de desgaste** — *Significa:* **Intacta → Marcada (−1 Defesa) → Rachada (−2 Defesa, benefício desligado) → Destruída**. Uma peça desce **um estado** a cada **acerto crítico sofrido** (local por `1d6`) ou pelo traço **Rasgar**. *Onde mora:* `docs/gdd/GDD_Equipamentos.md` §3. *Não confundir com:* o **estado de conservação** das armas (Calibrada a Arruinada), que mexe em travamento, não em Defesa; e com **degrau** — evitado de propósito, porque já tem cinco sentidos. *Status:* canon (Aprovação 034). Medido: só com o 20 natural, o conjunto perde ~1 de Defesa por Patamar.
- **Rasgar** — *Significa:* traço de criatura **quebra-armadura**: 1× por combate, ao acertar, a peça atingida desce um estado de desgaste mesmo sem crítico. *Onde mora:* `docs/gdd/GDD_Equipamentos.md` §3.2. *Status:* canon (Aprovação 034); **o Touro Mecânico tem**. O outro traço quebra-armadura é o **Crítico 19–20**.
- **Remendo de campo** — *Significa:* reparo de equipamento pela via Gambiarra, em qualquer lugar: Mecânica **CD 13** e **2 Sucata** devolvem um estado, mas a peça **nunca volta acima de Marcada**. *Onde mora:* `docs/gdd/GDD_Equipamentos.md` §4.1. *Não confundir com:* o reparo na **bancada**, que devolve a peça a Intacta e custa conforme a raridade (Épico custa **Liga Pré-Queda**). *Status:* canon (Aprovação 034).
- **Variação** — *Significa:* o item-base com uma **modificação já instalada** ou, só para equipamento, em **outro material**. *Onde mora:* `docs/gdd/GDD_Equipamentos.md` §7. *Não confundir com:* o tier **Modificada**, que é o que o **grupo** fabrica — a variação é a modificação que **alguém** fez e o grupo achou. *Status:* canon (Aprovação 034). **Armas variam só por modificação, nunca por material**, para proteger a tabela de DPR. Herda tier e raridade do base; uma raridade acima se a modificação for de Oficina.
- **Vantagem** — *Significa:* rolar `2d20` e usar o **maior**. *Onde mora:* `docs/gdd/GDD_Combate.md` §1.1. *Não confundir com:* bônus numérico; e a Ação **Ajudar** concede Vantagem que **não acumula com outra Vantagem**. Cancelamento com Desvantagem: uma fonte de cada lado zera as duas. **"20 natural" e "1 natural" leem o dado efetivamente usado**, não o descartado. *Status:* canon.
- **Vigor** — *Significa:* **perícia de CON** — forçar o corpo além do limite **por escolha própria**: marcha forçada, vigília prolongada, apneia, suportar frio ou calor extremos, trabalho braçal contínuo, aguentar uma privação sem desmoronar. *Onde mora:* `docs/gdd/GDD_Pericias.md` §2.7, §1.1 e §4.5. *Não confundir com:* **o teste de resistência de CON contra Infecção — e esta é a fronteira mais importante do sistema de perícias**. *"Vigor é o que você faz com o corpo; o teste de CON contra Infecção é o que a mordida faz com ele."* A perícia **não** entra ali, e o motivo é de balanceamento declarado: o modificador de CON é um **dial fraco de propósito**, e um Construtor treinado chegando a `+6` naquele teste faria a Trilha de Infecção — **uma das duas moedas de atrito do jogo** — deixar de morder. Também não confundir com **Atletismo** (pico, não duração) nem com **Resistir Toxinas** (veneno). *Status:* canon quanto à existência e ao atributo (CANON 021 §1); CDs `[A CALIBRAR]`. **ALERTA DE COLISÃO — ver §2.1:** a palavra está **a uma linha de virar sinônimo** do teste de resistência de CON, e basta alguém escrever *"teste de vigor"* em minúscula para que ela vire. É exatamente o erro que produziu *"teste de furtividade"* em minúscula em `docs/gdd/GDD_Combate.md` §4.
- **Vulnerável** — *Significa:* o grau que faz o dado de dano **subir um degrau** na escada, **respeitando o teto 1d12**. *Onde mora:* `docs/gdd/GDD_Combate.md` §6.3. *Não confundir com:* **Vantagem** (que mexe no d20 de ataque, não no dado de dano) nem com a condição **Caído**. *Status:* canon. Perfis canônicos: **zumbi comum** e **mutante** são Vulneráveis a **Fogo**; **alvo com cibernética** é Vulnerável a **Elétrico/EMP**. É o que *"finalmente dá função ao maçarico, à Ponta Incendiária e à Boca de Forno"*. **Dano extra de Elétrico/EMP contra alvos com cibernética:** `[A CALIBRAR]`.

---

## 4. Palavras QUEIMADAS

Não use nenhuma destas para nomear nada novo. Elas já significam algo, e em muitos casos significam
**mais de uma coisa** — o número entre parênteses é quantos sentidos vivos a palavra tem hoje.

**Gravidade alta — palavras já sobrecarregadas. Nunca reutilizar:**

| Palavra | Sentidos vivos hoje |
|---|---|
| **Sucata** (3) | tier de arma · componente abundante · pior estado de conservação |
| **Oficina** (2) | via de fabricação · Oficina de Campo (assinatura) — *era 3; a Aprovação 023 retirou "Oficina médica", hoje **Enfermaria*** |
| **Estabilizar** (3 mecânicas, **4 contextos**) | fim dos testes de morte · socorrer aliado · assinatura do Médico · **a perícia Medicina, que opera o segundo** — §2.1 |
| **Leve** (4) | propriedade de arma · calibre · família Lâminas Curtas · antigo nome do porte Simples |
| **Pesada** (4) | propriedade de arma · calibre Pesado · família Lâminas Longas · antigo nome do porte Estrutural |
| **Slot** (3) | modificação · inventário · Ação Bônus |
| **Carga** (3) | propriedade **Carga (N)** · Munições Especiais de munição · mecanismo Explosivo — *era 4; a Aprovação 028 dissolveu a **Energia da Célula**, que virou `Carga` comum* |
| **Trilha** (4) | Infecção · Radiação · Sangrando · Trilha de Calor |
| **Limiar** (2) | Infecção (pessoal) · Medidor de Horda (20) |
| **Faixa** (3) | faixa de quebra · faixa de travamento · faixa de crítico |
| **Degrau** (5) | escada de dados · Nível de Ruído · estado de conservação · porte de modificação · **resistência / vulnerabilidade a tipo de dano** |
| **Crítico** (3) | acerto crítico · Estado Crítico · falha crítica de fabricação |
| **Família** (2) | família de arma (proficiência) · família de modificação. **Agravada pela Regra 2 das Especializações**, que lê **exclusivamente família de arma** — usar a palavra nua num pré-requisito torna a regra ilegível |
| **Porte** (2) | porte de **modificação** (Simples / Estrutural) · porte de **Especialização** (Menor / Média / Maior / Assinatura) — **candidata a colisão, §2.1** |
| **Assinatura** (2) | habilidade-assinatura de classe · o **porte** que a compra — **candidata a colisão, §2.1** |
| **Resistência** (2) | **resistência a tipo de dano** (move o dado na escada) · **teste de resistência** (os 6 da ficha, 2 fixos por classe) — **duas coisas sem relação alguma** |
| **Banda** (1, reservada) | as quatro faixas da **Trilha de Infecção** (Saudável / Infectado / Infectado grave / limiar). Um só sentido, **mas é a palavra que o canon usa para a única escala proporcional do jogo** — e o sistema já tem **Faixa** com três sentidos ao lado dela. Não reutilizar, e **não escrever "faixa de Infecção"** |
| **Vigor** (1, quase 2) | **perícia de CON** — e o teste de resistência de CON que **não** é ela. **Candidata a colisão, §2.1** |
| **Improviso / Improvisada** (4) | **tier Improviso** · propriedade **Improvisada** · Recurso *Improviso Rápido* · via **Gambiarra**, com que a palavra é confundida em texto corrido |

**Gravidade média — um sentido só, mas reservado e citado em várias regras:** Ação · Ação Bônus ·
Reação · Interação livre · Vantagem · Desvantagem · Defesa · Cobertura · Atração ·
Conservação · Escada de dados · Especialização · Estado Crítico · Gambiarra · Improvisada ·
Infecção · Katana · Liga Pré-Queda · Medidor · Horda · Leva · Cena · Mirar · Modificação · Munição
Padrão · Nível de Ruído · Porta suave · Precedência · Projéteis · Projéteis Mecânicos ·
Propriedade · Quebra · Rajada · Automático · Raridade extrema · Refúgio · Suporte · Tier ·
Travamento · Utilitária · Ágil · Frágil.

**Queimados pelo sistema de Especializações (Aprovações 021 e 022):** **Cota** (o teto de 2 por
classe) · **Trajetória** (as oito escolhas lidas como um todo) · **Fonte diegética** · **Talento
Geral** · **Recurso de classe** · **Ápice** · **Menor** · **Média** · **Maior** · e os rótulos de
contenção **Regra 1**, **Regra 2** e **Regra 3**, que só significam algo dentro daquele documento.

**Queimados pelo sistema de Perícias (Aprovação 021):** **Perícia** · **Teste de resistência** · e os
**18 nomes**, um a um — Atletismo · Arrombamento · Acrobacia · Furtividade · Prestidigitação ·
Pilotagem · **Vigor** · Resistir Toxinas · Mecânica · Eletrônica · Medicina · Saber Pré-Queda ·
Percepção · Investigação · Sobrevivência · Rastrear · Persuasão · Intimidação.

**Queimados pela escala de resistência a dano:** **Resistente** · **Muito Resistente** ·
**Vulnerável** · **Imune**. Os quatro são **graus de uma escala de tipo de dano** e não devem
aparecer descrevendo nenhuma outra coisa — em particular, **nunca** como sinônimo de *teste de
resistência*.

**Também queimados, por serem valores fechados de listas canônicas:** os **nove tipos de dano**
(Perfurante, Cortante, Concussão, Balístico, Fogo, Químico, Radiação, Elétrico/EMP, Necrótico) · as
**doze condições** de `docs/gdd/GDD_Combate.md` §10 · as **dez ações** de §4 · as **24 propriedades** de
`docs/gdd/GDD_Armas.md` §3 · as **17 modificações** e os **oito componentes** · os **seis pools de munição** ·
as **dez Munições Especiais** · os **seis tiers** · as **dez famílias de arma** · os **quatro estados
de conservação** · as **18 perícias** e os **6 testes de resistência** · os **48 Recursos de classe**,
os **8 Recursos de nível 18** e os **8 Ápices** · os nomes das **oito classes** e das **oito
assinaturas**.

> **Onde ainda há espaço — atualizado.** **Perícias saíram desta lista**: os 18 nomes foram batizados
> pela Aprovação 021 e estão registrados no §3 deste ciclo. O que continua disponível é qualquer
> termo do campo de **Bestiário**, **Veículos** e **Refúgio** — três módulos que **ainda não foram
> desenhados**. Quem os batizar primeiro deve **registrar aqui, no mesmo ato**, para não repetir as
> seis colisões.
>
> **Aviso a quem for desenhar esses três.** Eles são justamente os módulos que já têm palavras
> reservadas apontando para dentro deles: **Enfermaria** (Refúgio) · **Pilotagem**
> e **Modificação Veicular** (Veículos) · **ruído de criaturas** e os **perfis de resistência**
> (Bestiário). Nenhuma dessas palavras está livre.

---

### 4.1 Acrescentadas pela Aprovação 025

| Palavra | Sentidos vivos |
|---|---|
| ~~**Tier** (2)~~ | **Resolvida na Aprovação 031:** o sentido de grupo virou **Patamar** (P1 a P5). **Tier** volta a ter um sentido só — procedência de arma |

| Palavra | Sentidos vivos |
|---|---|
| **CD** | **1 — e assim deve ficar.** Classe de Dificuldade, só. A tentativa de usá-la para criatura foi barrada em §2.0 |
| **Aura** | 1 (efeito de criatura). **Ainda livre**, mas não use para condição, item nem modificação sem declarar |
| **Doutora Zumbi / Enfermaria** | **2, e diferem por uma letra.** Ver §2.2 |
| **Maratonista** | **2** — criatura × passagem do mapa. Ver §2.2 |

**Duas palavras a EVITAR, que apareceram em proposta e não são canon:**

- **DPR** é métrica de balanceamento (*dano por rodada*), **não** dano causado. Não escreva *"a aura
  dá DPR"*; escreva *"sofre 1d6 Químico"*. DPR é o que o **analista** mede, não o que o **personagem**
  sofre.
- **Infestação** não existe neste sistema. O termo é **Infecção**, e a mecânica é a **Trilha de
  Infecção**.

---

## 5. Convenções de nomenclatura

**1. Proficiência lê PROPRIEDADE, nunca nome de arma.** Foi por isso que a "Lança Artesanal" virou
**Lança Artesanal** e o "Arco Artesanal" virou **Arco Artesanal** (CANON 017 §3): nenhuma das duas
tem a propriedade **Improvisada**, e o nome sugeria que tivessem. Nome de arma é sabor; propriedade é
regra.

**2. Família de arma é UMA DIMENSÃO SÓ, e cada arma pertence a exatamente uma.** A taxonomia antiga
misturava propriedades, tipos de dano e famílias como se fossem a mesma coisa — e era isso que
produzia fichas impossíveis de resolver. **Arremessável não é família, é propriedade**; o mesmo vale
para Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil e Flexível.

**3. Contadores distintos NUNCA se somam.** **Quebra** e **travamento** usam a mesma moeda numérica
(faixas de d20) e por isso são **diretamente comparáveis** — mas são **duas checagens independentes na
mesma rolagem**. A Guarda de Ejeção reduz travamento; a Gambiarra piora quebra; **não há
cancelamento**. Qualquer contador novo deve declarar, na primeira linha, com quais contadores
existentes ele **não** interage.

**4. Um documento por função do sistema, e não se duplica regra.** O catálogo (`docs/gdd/GDD_Armas.md`) traz
dados; o módulo de combate traz regras; cada subsistema de economia tem arquivo próprio. Verbete que
descreve regra aponta para onde ela mora — **não a repete**, porque regra repetida diverge.

**5. Qualificador obrigatório quando a palavra é compartilhada.** Escreve-se *limiar de Infecção* ou
*limiar do Medidor*, *via Oficina* ou *Oficina de Campo*, *faixa de quebra* ou *faixa de travamento*,
*slot de modificação* ou *slot de inventário*. Nunca a palavra nua. **Acrescentados neste ciclo:**
*porte de modificação* ou *porte de Especialização* · *habilidade-assinatura* ou *porte Assinatura* ·
*degrau de dado*, *degrau de Ruído* ou *degrau de conservação* · *resistência a tipo de dano* ou
*teste de resistência* · *família de arma* ou *família de modificação*.

**6. Perícia é NOME PRÓPRIO. Maiúscula não é estilo — é a diferença entre duas regras.** O canon já
pagou por isso uma vez: `docs/gdd/GDD_Combate.md` §4 descreve a ação **Esconder** como *"teste de
**furtividade** oposto à PER"*, em minúscula, porque **a perícia ainda não existia** e o autor usou o
substantivo comum. Hoje **Furtividade** existe e o texto continua em minúscula. O risco imediato é
**Vigor**: escrever *"teste de vigor"* em minúscula converte, numa linha, a **perícia de CON** no
**teste de resistência de CON** — e o canon separa os dois por razão de balanceamento declarada
(`docs/gdd/GDD_Pericias.md` §1.1). **Se é uma das 18, é maiúscula. Se é um dos 6 testes de resistência, é
"teste de resistência de X", com o atributo em sigla.**

**7. Não batize uma versão "II" como se fosse um conceito novo.** Os sete Recursos *Tiro Calculado
II*, *Corte Contínuo II*, *Oficina de Campo II*, *Mão Calejada II*, *Esquiva Reflexa II*,
*Estabilizar II* e *Modificação Veicular II* **escalam uma assinatura**, e a Aprovação 022 teve de
mudar o **porte** dos sete de uma vez porque isso não estava visível no nome. Um sufixo numérico
herda tudo do termo-base, inclusive as colisões dele — *Estabilizar II* carrega os quatro contextos de
*Estabilizar* (§2.1).

**8. A lição das seis colisões, em uma frase.** **Não batize um conceito novo com a primeira palavra
que o descreve bem sem verificar se ela está livre.** Todas as seis colisões deste projeto foram
palavras *corretas* aplicadas a um segundo conceito. O custo não foi de desenho: foi de **retrabalho**
— renomear em todos os documentos, reemitir aprovação, reconferir a planilha. Uma consulta a este
glossário custa trinta segundos.

---

## 6. Divergências entre documentos — relatadas, não resolvidas

Este glossário **não escolhe lado**. Onde dois documentos canônicos se contradizem, o registro fica
aqui para decisão do Diretor.

> ### Fechadas neste ciclo — 6 das 8 novas
>
> As divergências **23, 24, 27, 28, 29 e 30** foram **fechadas sem consulta ao Diretor**, porque
> nenhuma delas era escolha de design: todas eram **documento contradizendo canon já aprovado**, e
> fechar significou propagar o canon, não criá-lo.
>
> | # | O que era | Como foi fechada |
> |---|---|---|
> | **23** | Os oito `Classe_*.md` §7 diziam que a lista e os níveis de Especialização eram `[A CALIBRAR]` | Caixa de correção nos oito, apontando para `docs/gdd/GDD_Especializacoes.md` como fonte de níveis; as quatro frases soltas que repetiam o erro foram reescritas |
> | **24** | `docs/gdd/GDD_Especializacoes.md` ainda dava Vantagem de **Utilitária** em **Mecânica** | Removida da tabela de perícias e do §13.3, com a razão: *Utilitária é FOR para arrombar, e arma é alavanca, não ferramenta de precisão* |
> | **27** | "**Sete** delas preenchem buracos" seguido de **oito** nomes | Numeral corrigido para **oito**, com nota de que o erro estava no número, não na lista |
> | **28** | §6 fechava "10 Médias" no topo e "17 opções" oito linhas abaixo | Total reescrito para **10**, explicando que os sete "II" continuam fisicamente na seção mas com porte Assinatura |
> | **29** | A escala de resistência não trazia número de aprovação onde a regra mora | **Aprovação 020** carimbada em `docs/gdd/GDD_Combate.md` §6.3, junto do escopo: os graus são canon, os perfis por criatura dependem do Bestiário |
> | **30** | *Muito Resistente* com a coluna inteira em `—` e *Imune* sem coluna nenhuma | Aviso ao implementador em `docs/gdd/GDD_Combate.md`: os cinco degraus se implementam mesmo assim; quem os usa é matéria do Bestiário |
>
> **Correção ao relato original:** o item 30 dizia que as colunas *Muito Resistente* e *Imune*
> estavam vazias. **Imune não tem coluna** na tabela de perfis — só *Muito Resistente* existe e está
> toda em `—`. O problema é o mesmo; a descrição estava imprecisa.
>
> **Continuam abertas — e são as duas que precisam do Diretor: 25 e 26.** Uma é escolha de nome, a
> outra é escolha de balanceamento. Nenhuma das duas o glossário pode resolver sozinho.

1. ~~**Proficiências de classe: duas taxonomias vivas.**~~ **FECHADA — e ninguém tinha registrado.**
    Auditoria de hoje: **os oito** `Classe_*.md` já usam a taxonomia de famílias na linha
    *"Proficiência (famílias de arma)"*. A migração aconteceu em algum ponto entre o CANON 017 e as
    Aprovações 018–022 e **este glossário continuou relatando o conflito depois de ele ter acabado** —
    exatamente o defeito que a divergência 23 descreve, cometido aqui dentro. O texto original segue
    abaixo como histórico.
    **Histórico:** CANON 017 §2 declara a taxonomia de famílias
   como substituta das proficiências antigas, mas **sete dos oito `Classe_*.md` continuam com os nomes
   antigos** — só `docs/classes/Classe_Ceifador.md` usa a taxonomia nova.
   Médico: *"Leves, Perfurantes"* × *Lâminas Curtas, Dispositivos* · Explorador: *"Ágeis,
   Projéteis"* × *Lâminas Curtas, Projéteis Mecânicos* · Construtor: *"Improvisadas, Utilitárias"* ×
   *Contundentes, Hastes* · Pugilista: *"Desarmado, Concussão"* × *Desarmado, Contundentes* ·
   Cientista: *"Leves"* × *Dispositivos, Lâminas Curtas* · Piloto: *"Pistolas, Utilitárias"* ×
   *Pistolas, Contundentes* · Atirador de Elite: *"Todas as de fogo"* × *Pistolas, Longas,
   Espingardas*. **Nenhum dos sete foi atualizado.**
2. ~~**Proficiências antigas nomeiam propriedades e tipos de dano.**~~ **FECHADA junto com a 1** — nenhum `Classe_*.md` usa mais os nomes antigos. "Perfurantes" e "Concussão" são
   **tipos de dano**; "Leves", "Ágeis", "Improvisadas" e "Utilitárias" são **propriedades**. É
   exatamente o que CANON 017 §2 diz que a taxonomia nova veio corrigir.
3. **Ceifador: nome resolvido em dois documentos, pendente em quatro.** CANON 017 §1 confirma o nome
   e `docs/classes/Classe_Ceifador.md` já existe; mas `docs/gdd/GDD_Combate.md` §8.1 e `docs/gdd/GDD_Infeccao.md` ainda escrevem
   *"Ceifador"*, e `docs/classes/Classe_Construtor.md` e `docs/classes/Classe_Pugilista.md` continuam dizendo
   que *"a oitava classe (…) seu nome ainda não foi decidido pelo Diretor"*.
4. **Oito ou nove classes.** Todo o corpo do canon fala de **oito**; CANON 017 §5 escreve *"todas as
   nove classes"*.
5. ~~**Katana fora do catálogo.**~~ **FECHADA — Aprovação 024.** Entrou em `docs/gdd/GDD_Armas.md` §4.4 (tier Militar) e migrou para **Lâminas Longas**. **Histórico:** Existe só em CANON 017 §1, não em `docs/gdd/GDD_Armas.md` §4.4 (tier Militar).
   O DPR vem escrito `4,72 / 5,38`, contra os `4,725 / 5,375` que o catálogo usa para o mesmo dado —
   arredondamento divergente.
6. **Lança Artesanal / Arco Artesanal.** CANON 017 §3 renomeia; `docs/gdd/GDD_Armas.md` §4.1 e §5,
   `docs/classes/Classe_Medico.md` §5.5 e `docs/classes/Classe_Explorador.md` §5.3 ainda usam *"Lança Artesanal"* e *"Arco
   improvisado"*.
7. **Tiro Calculado exige arma de fogo?** CANON 017 §4 fecha que **sim**, com redação canônica.
   `docs/classes/Classe_AtiradorDeElite.md` §7 afirma o contrário — *"ele **não** exige arma de fogo"* — e deixa a
   restrição como `[A CALIBRAR]`.
8. **Quem destrava a via Oficina.** CANON 017 §4 decide que **a bancada destrava, não a classe**:
   qualquer personagem com Refúgio equipado modifica pela via Oficina. `docs/classes/Classe_Cientista.md` §4
   afirma *"Só o Cientista faz Oficina"*, e §5.1 registra a pendência como `[A CALIBRAR]`.
9. **Corpo a corpo acima de Baixo não está formalizado.** `docs/gdd/GDD_Armas.md` §8.4 (#7) registra que
   Rebarbadora (**Alto**) e Serra "Denteira" (**Médio**) são *"exceções ad-hoc não formalizadas"*,
   enquanto `docs/gdd/GDD_Ruido.md` §1 apresenta a cláusula de motor como cobrindo o caso. Os dois textos não
   se referem um ao outro.
10. **"Cantor": Silencioso × nunca silencia.** `docs/gdd/GDD_Armas.md` §6.4 lista Ruído **Silencioso**, e §8.4
    (#6) registra que isso contraria a nota da própria planilha e o precedente do "Vigília", travado
    em **Baixo** por decisão do Diretor.
11. **Limiar do Medidor de Horda: fechado ou aberto.** `docs/gdd/GDD_Horda.md` §2 fixa **20, em escada**, e
    mede todo o ritmo canônico com ele. `docs/gdd/GDD_Armas.md` §8.1 diz *"Limiar do Medidor de Horda:
    `[A CALIBRAR]`"* e §8.3 o lista entre os *"cinco números que não existem"*.
12. **Pontos de Infecção por golpe: idem.** `docs/gdd/GDD_Infeccao.md` §1 fixa **1** por golpe e **2** no
    crítico; `docs/gdd/GDD_Armas.md` §8.3 lista esse número como inexistente.
13. **Ponteiros de seção quebrados para Ruído.** `docs/gdd/GDD_Modificacoes.md` §3.1, §9.1 e §5.2 citam
    *"§12.1 a §12.5 do Módulo de Combate"* para escala de Ruído, silenciador e precedência. Essas
    subseções **não existem mais**: `docs/gdd/GDD_Combate.md` §12 apenas aponta para `docs/gdd/GDD_Ruido.md` e
    `docs/gdd/GDD_Horda.md`.
14. **Cano c/ Arame Farpado usa o nome antigo do porte e não declara FOR.** `docs/gdd/GDD_Armas.md` §4.3 lê
    *"porte Pesado"* (hoje **Estrutural**) e, conforme §8.4 (#10), tem a célula de FOR mínima vazia
    embora **Pesada exija FOR mínima por definição**.
15. **Nomes e dados divergentes no catálogo** (registrados em `docs/gdd/GDD_Armas.md` §8.4, #2 a #4):
    Baioneta de Encaixe 1d6 × Baioneta-Adaptador M7 1d8 · Pá de Trincheira Afiada 1d8 Cortante × Pá de
    Sapador 1d10 Dupla Face · Soqueira 2d4 × "Volt-9" 1d6+1d6, sem linhagem entre as duas. A grafia
    da Soqueira elétrica também alterna entre **"Volt-9"** e **"Vólt-9"**.
16. **Espingarda 2d6 rompe o teto de DPR sem ser exceção declarada** (6,35 contra 6,025), enquanto a
    planilha afirma que a Rajada é a *"única exceção"* — `docs/gdd/GDD_Armas.md` §8.4 (#1).
17. **Modo "Automático (Classe)" da Metralhadora** não existe na lista de propriedades
    (`docs/gdd/GDD_Armas.md` §8.4, #11). CANON 017 §4 resolve o *acesso* (proficiência de nível superior,
    níveis `[A CALIBRAR]`) mas não a entrada de catálogo.
18. **`Recarga` com F.sust. = 1.** Fisga de Rolamentos e Seringa de Pressão Veterinária têm a
    propriedade **Recarga** mas fração sustentada 1 em vez de 0,5 — `docs/gdd/GDD_Armas.md` §8.4 (#8, #9).
19. **Lâminas Soldadas promete Silencioso e a precedência nega.** `docs/gdd/GDD_Modificacoes.md` §5.2 e §9.2
    (item 5) registram que falta a frase de exceção: soldar lâminas numa arma **Pesada** não a
    silencia.
20. **Cross-reference errado em `docs/gdd/GDD_Combate.md` §1.1**: manda para *"§7.4"* para travamento, e
    travamento é **§7.3** (§7.4 é Alcance).
21. **Cabeçalho de `docs/gdd/GDD_Armas.md` com link malformado**: `[docs/gdd/GDD_Combate.md](`docs/gdd/GDD_Ruido.md` /
    `docs/gdd/GDD_Horda.md`)` — o rótulo e o destino não correspondem.
22. **Colisões latentes, ainda não declaradas por nenhuma aprovação:** **Sucata** (tier · componente ·
    estado de conservação) e **Carga** (propriedade · Munições Especiais · carga de Célula · carga
    pirotécnica). Nenhuma das duas está resolvida nem registrada como colisão — são candidatas a
    sétima e oitava. **Somam-se a elas, a partir deste ciclo, as quatro de §2.1:** Vigor, Estabilizar
    (quarto contexto), **Porte** e **Assinatura**.

### Divergências registradas neste ciclo (Perícias, Especializações e Resistência)

23. ~~**`Classe_*.md` §7 defasados quanto a Especializações — o mesmo erro que este glossário cometia.**~~ **FECHADA.**
    `docs/classes/Classe_Medico.md` §7 e `docs/classes/Classe_Cientista.md` §7 declaram que *"a **lista** por classe e os
    **pré-requisitos de nível** são `[A CALIBRAR]` (canon §4)"*, e `docs/classes/Classe_Pugilista.md` §7 diz que
    *"o canon §4 mantém aberta a lista de **todas** as oito"*. **Não mantém mais:** CANON 021 §2 fixa
    os **oito níveis** (3, 5, 7, 9, 11, 13, 15, 17), os **quatro portes** com mínimos (Menor 3, Média
    7, Maior 13, Assinatura 17) e as **três regras de contenção**; a Aprovação 022 recontou o
    catálogo. Os documentos de classe **não foram atualizados**. *(Este glossário estava no mesmo
    estado e foi corrigido no verbete **Especialização** — a defasagem havia sido apontada em
    `docs/gdd/GDD_Pericias.md` §8.1, item 5, e ficou sete aprovações sem resposta.)*
24. ~~**Utilitária dá Vantagem em quê — declarada resolvida num documento, ainda propagada em outro.**~~ **FECHADA.**
    `docs/gdd/GDD_Armas.md` §3 e o verbete **Utilitária** fecham a propriedade como *"Vantagem em testes de
    **FOR** para arrombar"*. `docs/gdd/GDD_Pericias.md` §8 declara o caso **resolvido** — a extensão a
    **Mecânica** foi *"erro de redação da proposta"*, e a §3.1 daquele documento já traz a correção
    em destaque. Mas `docs/gdd/GDD_Especializacoes.md` **continua propagando a versão errada em dois lugares**:
    a tabela de §5.1 escreve *"**Mecânica** — o teste de INT das Modificações. A propriedade
    **Utilitária** dá Vantagem"*, e §13.3 registra como pendência *"Arrombamento **e Mecânica** ganham
    Vantagem por Utilitária"*. **Mecânica é INT; a propriedade fala de FOR.**
25. ~~**Enfermaria × Oficina médica — dois nomes para a mesma instalação de Refúgio.**~~
    **FECHADA — Aprovação 023.** Venceu **Enfermaria**, e *"Oficina médica"* **saiu do canon**. Não
    foi contagem de votos (dez documentos contra um): foi que *Oficina* é a palavra mais
    sobrecarregada do sistema, e o voto minoritário era justamente o que a sobrecarregava numa
    terceira acepção. A **colisão 6 desceu de 3 para 2 sentidos** — a primeira deste glossário
    resolvida por **renomeação** em vez de qualificador, e o critério que isso estabeleceu está em
    **§2.2**. A Enfermaria é uma das **quatro vias canônicas** de remoção (`docs/gdd/GDD_Infeccao.md`,
    "Remoção"); **a quantidade removida por descanso continua `[A CALIBRAR]`**.
26. ~~**Soro de Campo: raridade extrema × um por descanso longo.**~~
    **FECHADA EM DUAS PARTES DE TRÊS — Aprovação 023.** Não havia contradição: havia **dois itens
    escrevendo-se com o mesmo nome**.
    - **26.1 — são dois.** O **Soro Anti-Infecção** de raridade extrema **zera** a Trilha inteira e
      continua trava de distribuição do Diretor; o **Soro de Campo** do Médico remove **`N` pontos** e
      **nunca zera**. Esperar 14 níveis pela versão **parcial e repetível** do item lendário é a troca.
      **Não devem compartilhar identificador no motor.**
    - **26.3 — produção custa componente.** Regra **geral**, não exceção do soro: *tudo que se fabrica
      consome componente* (`docs/gdd/GDD_Modificacoes.md` §4). O Soro de Campo consome **Química**, o que faz de
      *"um por descanso longo"* um **teto** em vez de piso — sem Química, o descanso passa em branco.
    - **26.2 — AINDA ABERTA, e maior do que parecia.** Ver **divergência 31**.
27. ~~**"Sete" × oito, de novo — corrigido num documento e não no outro.**~~ **FECHADA.** `docs/gdd/GDD_Pericias.md` §8 declara
    a contagem resolvida: são **oito** as perícias que preenchem buracos preexistentes, e o "sete" era
    erro de contagem da proposta. `docs/gdd/GDD_Especializacoes.md` §5.1 **ainda escreve** *"**Sete** delas
    preenchem buracos que já existiam no sistema"* e em seguida **lista oito nomes** na mesma frase —
    Mecânica, Eletrônica, Medicina, Furtividade, Percepção, Arrombamento, Pilotagem e Sobrevivência.
28. ~~**Contagem de Médias contraditória dentro do próprio `docs/gdd/GDD_Especializacoes.md`.**~~ **FECHADA.** O aviso de
    Aprovação 022 no topo do §6 fecha *"contagem corrigida: 9 Médias de classe + Cicatrizado =
    **10 Médias**"*, coerente com a tabela de §2 (Menor 41 · Média 10 · Maior 16 · Assinatura 15 =
    82). Oito linhas abaixo, o corpo do mesmo §6 ainda diz *"**Total: 16 Recursos + Cicatrizado = 17
    opções**"*, que é a contagem **anterior** à reclassificação. As duas frases estão na mesma seção.
29. ~~**A escala de resistência não carrega carimbo de aprovação no arquivo.**~~ **FECHADA.** `docs/gdd/GDD_Combate.md` §6.3
    apresenta Vulnerável / Resistente / Muito Resistente / Imune, o piso de `1d4`, a aplicação por
    dado e os perfis por criatura **sem número de aprovação no texto**, ao contrário de praticamente
    todas as regras vizinhas (`Aprovação 002`, `006`, `009`, `012`, `013` aparecem carimbadas). Este
    glossário registra os quatro graus como **canon pela Aprovação 020**, conforme instrução do
    Diretor; **o carimbo precisa ser gravado no documento onde a regra mora**, porque é lá que ela
    prevalece.
30. ~~**Os quatro perfis de resistência dependem de um módulo que não existe.**~~ **FECHADA.** A tabela de
    `docs/gdd/GDD_Combate.md` §6.3 fixa perfis para **zumbi comum**, **mutante**, **alvo com cibernética** e
    **humano**, e a coluna **Muito Resistente** está **inteiramente vazia** — nenhuma criatura
    canônica a usa hoje. **Imune** também não é atribuído a ninguém. As duas colunas existem para o
    **Bestiário**, que `docs/gdd/GDD_Ruido.md` §6 confirma **não ter sido desenhado**. Não é contradição, mas
    é **regra sem sujeito**, e implementadores devem criar os quatro graus no motor mesmo sem dado
    para dois deles.

---

*Este documento é um índice, não uma fonte de regra. A regra mora nos arquivos citados; em qualquer
divergência entre este glossário e o documento apontado, **o documento apontado prevalece**. Toda
palavra nova acrescentada ao sistema deve ser registrada aqui no mesmo ciclo de aprovação que a criou.*

---

### Divergência 31 — FECHADA POR DECISÃO, não por correção

**Toda Especialização Maior de um Recurso de nível 14 chega um nível antes da classe dona.** O porte
**Maior** abre no **nível 13** e concede *"um Recurso de nível 10 ou 14 de outra classe"* (§2 de
`docs/gdd/GDD_Especializacoes.md`). Para os Recursos de nível 10, tudo bem — chegam três níveis atrasados. Para
os de **nível 14**, o comprador chega **no 13**, um nível **antes** de quem é da classe.

**São oito casos, não um.** *Automático* (Atirador, 7.2) · *Dança* (Ceifador, 7.4) · *Substituto*
(Cientista, 7.6) · *Ponto Fraco* (Construtor, 7.8) · *Some* (Explorador, 7.10) · *Soro de Campo*
(Médico, 7.12) · *Conhece a Máquina* (Piloto, 7.14) · *Couro Grosso* (Pugilista, 7.16).

**Registro de erro:** chegou-se a propor que *Soro de Campo* subisse para o nível 17. Era duas vezes
errado — trata **um caso de oito**, e o nível 17 é o slot da **Assinatura**, que um Maior não deve
ocupar. A proposta corrigida era: *nenhuma Especialização entrega um Recurso antes do nível em que a
classe dona o entrega* (Maior de Recurso de nível 14 exigiria o nível **15**).

> ### Decisão do Diretor (Aprovação 023): **fica como está.**
>
> **Os oito casos permanecem.** Comprar um Recurso de nível 14 no nível **13**, um nível antes da
> classe dona, é **canon deliberado** a partir de agora — não é dívida, não é bug, e **não deve ser
> "corrigido" por implementador nenhum** que tropece nisso no motor.
>
> **A razão:** um nível de antecedência é pouco, e **nenhuma simulação diz que quebra**. A regra que
> resolveria custaria um cardápio separado por nível — maquinaria nova para um problema que ninguém
> mediu. O preço de comprar o Recurso alheio já é alto: consome **uma das duas** aquisições daquela
> classe (Regra 1) e fecha a Assinatura dela para sempre.
>
> **O que reabre esta decisão:** playtest mostrando que algum dos oito chega cedo demais *na prática*.
> Os candidatos a vigiar são *Automático* (Atirador) e *Couro Grosso* (Pugilista), porque são os dois
> que alteram sobrevivência ou DPR diretamente, em vez de abrir uma opção.
