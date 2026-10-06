# MUTAGEN:ZERO — Perícias

> **O que este documento é.** A camada de **competência treinada** do sistema: as 18 perícias, a quem
> elas pertencem e — sobretudo — **quais regras que já existiam passaram a ter dono**. Antes delas,
> meia dúzia de regras canônicas pediam "um teste" sem dizer de quê. Este documento fecha isso e nada
> mais: ele **não cria** ação nova, **não** mexe na economia do turno e **não** concede usos de Ação
> Bônus.
>
> **Fonte canônica:** CANON 021 §1. Onde o canon não fechou um número, o campo aparece como
> `[A CALIBRAR]` — **implementadores não inventam padrão no motor**.

> **Regras relacionadas — não duplicadas aqui:** núcleo de resolução, ações e economia do turno em
> `docs/gdd/GDD_Combate.md` §1.1, §2.4 e §4 · propriedade **Utilitária** em `docs/gdd/GDD_Armas.md` §3 · teste de INT
> de fabricação e os oito componentes em `docs/gdd/GDD_Modificacoes.md` §4, §5 e §7.4 · Trilha de Infecção em
> `docs/gdd/GDD_Infeccao.md` · Níveis de Ruído e Atração em `docs/gdd/GDD_Ruido.md` §1 e §2 · colisões de nome e
> palavras queimadas em `docs/gdd/GDD_Glossario.md` §2 e §4.

---

## 1. O que é uma perícia aqui

Uma perícia é um **campo de competência treinada** que se soma a um atributo quando o personagem faz
algo que exige prática, e não só talento bruto. A resolução é a de sempre (`docs/gdd/GDD_Combate.md` §1.1) —
**uma rolagem decide cada teste**:

```
Teste de perícia = d20 + modificador de atributo + proficiência (SE treinado) vs. CD
Sucesso se o total for >= CD
```

- O **modificador de atributo** vem do atributo ao qual a perícia pertence (§2), pela fórmula
  canônica `floor((atributo − 10) / 2)`.
- A **proficiência** é o bônus de treino de **+2 a +6** conforme o nível (`docs/gdd/GDD_Combate.md` §1.1). Ela
  só entra se o personagem **tem** aquela perícia. A progressão continua `[A CALIBRAR]`.
- **Não ter a perícia não impede o teste.** O personagem rola `d20 + atributo` e nada mais. Perícia é
  a diferença entre **tentar e saber** — não entre poder e não poder.
- **Vantagem e Desvantagem** valem em perícias exatamente como em ataques, inclusive o cancelamento:
  uma fonte de cada lado zera as duas e rola-se `1d20` normal, por mais fontes que existam.
- **Efeito de `20` e `1` natural em teste de perícia:** `[A CALIBRAR]`. O canon só fecha os efeitos
  de `20`/`1` em **rolagem de ataque** (§1.1) e em **teste de INT de fabricação**
  (`docs/gdd/GDD_Modificacoes.md` §7.4).
- **Teste oposto:** quando duas criaturas disputam, cada lado rola sua perícia e o maior total vence.
  O canon usa esta forma na ação **Esconder** (`docs/gdd/GDD_Combate.md` §4) e em escapar de **Agarrado**
  (§10). **Regra de empate em teste oposto:** `[A CALIBRAR]`.

### 1.1. Teste de resistência NÃO é perícia

> **Regra canônica (CANON 021 §1).** Testes de resistência são separados de perícias, como no d20
> clássico. **O teste de CON contra Infecção NÃO é a perícia Vigor: é um teste de resistência puro.**

São dois instrumentos com funções opostas, e confundi-los quebra o balanceamento de duas trilhas:

| | **Perícia** | **Teste de resistência** |
|---|---|---|
| Quem começa | **Você**, por escolha | O **mundo**, contra você |
| Quando rola | Quando tenta fazer algo | Quando algo é feito com você |
| Falhar significa | Você não conseguiu | Algo aconteceu com você |
| Quantos você tem | **3** de uma lista de 6, por classe | **2 por classe**, fixos |
| Exemplo canônico | Vigor: forçar o corpo além do limite | CON vs. Infecção (`docs/gdd/GDD_Infeccao.md` §2) |

**Por que a separação importa aqui, e não é preciosismo.** O modificador de CON é, por medição, um
**dial fraco de propósito** na Trilha de Infecção: dobrar de `+2` para `+4` quase não altera o ritmo,
porque o sucesso só remove **metade** dos pontos e a CD **cresce** com o que foi levado
(`docs/gdd/GDD_Infeccao.md` §2). O canon é explícito: *"a diferenciação entre personagens deve vir do limiar,
não do atributo"*.

Se a perícia **Vigor** somasse proficiência àquele teste, um Construtor treinado chegaria a `+6` num
dial que o canon projetou para ser fraco — e a Trilha de Infecção, que é **uma das duas moedas de
atrito do jogo**, deixaria de morder. A perícia não pode entrar ali. **Vigor é o que você faz com o
corpo; o teste de CON contra Infecção é o que a mordida faz com ele.**

O mesmo vale para **Resistir Toxinas**: é a **perícia** de lidar com veneno, gás e reagente de forma
**ativa e voluntária** — identificar, diluir, dosar, aguentar uma dose conhecida. Ela **não** é o
teste de resistência que a condição **Envenenado** ou o dano **Químico** exigem (`docs/gdd/GDD_Combate.md`
§6.3 e §10), nem o teste de CON contra **Radiação**.

**Resumo para a mesa, em uma linha:** *se o Mestre pediu o teste, é resistência; se o jogador pediu,
é perícia.*

---

## 2. As 18 perícias, por atributo

| Atributo | Perícias |
|---|---|
| **FOR** | Atletismo · Arrombamento |
| **AGI** | Acrobacia · Furtividade · Prestidigitação · Pilotagem |
| **CON** | Vigor · Resistir Toxinas |
| **INT** | Mecânica · Eletrônica · Medicina · Saber Pré-Queda |
| **PER** | Percepção · Investigação · Sobrevivência · Rastrear |
| **CAR** | Persuasão · Intimidação |

> **Contagem:** FOR 2 · AGI 4 · CON 2 · INT 4 · PER 4 · CAR 2 = **18**. A distribuição é
> deliberadamente desigual: INT e PER concentram as perícias porque MUTAGEN:ZERO é um jogo de
> **investigação e fabricação**, não de esporte. FOR e CON são curtos de propósito — o corpo aparece
> mais nas regras de combate e na Trilha de Infecção do que na ficha de perícias.

> **Nenhuma CD deste documento é canônica.** Cada verbete traz **faixas de exemplo** para dizer que
> *tipo* de situação pede a perícia. Todos os números são `[A CALIBRAR]` e serão fechados num ciclo
> próprio, junto com a progressão de proficiência.

### 2.1. Atletismo — FOR

- **Cobre:** escalar, saltar, nadar, correr contra o tempo, empurrar e arrastar peso, arrombar **pela
  força bruta do corpo** (ombro na porta), segurar um companheiro que escorrega, e o lado de **FOR**
  do teste oposto para escapar de **Agarrado** (`docs/gdd/GDD_Combate.md` §10).
- **NÃO cobre:** equilíbrio e queda controlada, que são **Acrobacia** (§4.4); aplicar ferramenta a
  uma tranca, que é **Arrombamento** (§2.2); aguentar esforço **prolongado**, que é **Vigor** (§2.7).
- **Exemplos de cena:** subir pela fachada de um estacionamento vertical antes que a leva chegue ·
  segurar a porta de um vagão enquanto o grupo passa · atravessar a nado um canal de água parada.
- **Quando é a perícia errada:** quando o problema é **tempo, não pico**. Marcha de dois dias com
  carga é Vigor. Também é errada contra uma fechadura: força sem ferramenta arromba o batente, não o
  mecanismo — e o Mestre deve deixar isso explícito antes da rolagem.
- **Faixas de exemplo:** muro de galpão · corrente de portão · escalada sob fogo inimigo:
  `[A CALIBRAR]`.

### 2.2. Arrombamento — FOR

- **Cobre:** portas, grades, cadeados, correntes, tampas de bueiro, grelhas de ventilação, caixas
  lacradas, veículos trancados — **abrir o que foi feito para não abrir**, com ferramenta, alavanca
  ou técnica.
- **NÃO cobre:** fechadura **eletrônica** ou painel de acesso corporativo, que é **Eletrônica**
  (§2.10); o mecanismo interno de um dispositivo que se quer preservar intacto e funcional, que é
  **Mecânica** (§2.9); abrir algo sem ser notado **enquanto alguém olha**, que exige um teste de
  **Furtividade** ou **Prestidigitação** em paralelo (§7.5).
- **Vantagem canônica:** a propriedade de arma **Utilitária** (`docs/gdd/GDD_Armas.md` §3) dá **Vantagem** —
  ver §3.6, onde a regra é tratada por inteiro.
- **Exemplos de cena:** pé de cabra na porta de serviço de uma farmácia · arrancar a grade de um
  respiro · abrir o porta-malas de um carro amassado.
- **Quando é a perícia errada:** quando a porta **não está trancada** — abrir porta destrancada é
  **interação livre com objeto**, sem teste nenhum (`docs/gdd/GDD_Combate.md` §4.2). Rolar ali é gastar tensão
  de mesa à toa.
- **Faixas de exemplo:** porta de madeira inchada · grade de loja · porta corta-fogo corporativa:
  `[A CALIBRAR]`.

### 2.3. Acrobacia — AGI

- **Cobre:** equilíbrio em superfície estreita ou instável, queda controlada, rolamento, passar por
  vão apertado, recuperar-se de um tropeço, e o lado de **AGI** do teste oposto para escapar de
  **Agarrado** (`docs/gdd/GDD_Combate.md` §10).
- **NÃO cobre:** potência — escalar e saltar distância bruta é **Atletismo** (§2.1); mover-se **sem
  ser notado** é **Furtividade** (§2.4). Acrobacia é sobre **não cair**, não sobre não ser visto.
- **Exemplos de cena:** atravessar uma viga entre dois prédios · cair de um andar sem entrar em
  Estado Crítico · passar por um duto de ventilação sem ficar preso.
- **Quando é a perícia errada:** quando não há risco de perda de controle. Andar num corredor largo
  não é teste. E ela **não** substitui a Ação **Esquivar** em combate: Esquivar é ação, não perícia
  (`docs/gdd/GDD_Combate.md` §4).
- **Faixas de exemplo:** viga molhada · queda de um andar · vão de duto com equipamento no corpo:
  `[A CALIBRAR]`.
- **Redução de dano de queda por sucesso em Acrobacia, se houver:** `[A CALIBRAR]` — o canon não tem
  tabela de dano de queda fechada.

### 2.4. Furtividade — AGI

- **Cobre:** mover-se sem ser visto nem ouvido, permanecer parado e despercebido, sustentar a ação
  **Esconder** (`docs/gdd/GDD_Combate.md` §4), acompanhar um alvo sem ser notado, atravessar um pátio
  patrulhado.
- **NÃO cobre:** esconder um **objeto** — isso é **Prestidigitação** (§2.5); silenciar uma **arma**,
  que é modificação e munição, nunca perícia (§6.1); e ela **não anula o raio de Ruído**: o Nível de
  Ruído alcança quem alcança, sem rolagem (`docs/gdd/GDD_Ruido.md` §1 e §2).
- **Exemplos de cena:** contornar uma horda dormente para chegar ao outro lado do viaduto · entrar num
  acampamento de saqueadores pela cerca dos fundos · reposicionar-se em combate depois de Esconder.
- **Quando é a perícia errada:** **depois do primeiro tiro.** Uma arma de Nível **Alto** tem raio de
  50 hexágonos e produz **Atração automática**; nenhum teste de Furtividade cancela isso. A furtividade
  morre no instante em que o grupo escolhe a outra moeda de atrito.
- **Faixas de exemplo:** sentinela distraída · zumbi · sensor corporativo: `[A CALIBRAR]`.
- **Detalhe canônico aberto:** modificador por cobertura e terreno na ação Esconder já constava como
  `[A CALIBRAR]` em `docs/gdd/GDD_Combate.md` §4, e **continua**.

### 2.5. Prestidigitação — AGI

- **Cobre:** mãos rápidas e finas — furtar de um bolso ou mochila, plantar um item em alguém, ocultar
  objeto no corpo, trocar um item por outro, manipular um mecanismo delicado **sob observação**,
  truque de mão para distrair.
- **NÃO cobre:** esconder **o próprio corpo**, que é **Furtividade** (§2.4); montar ou consertar um
  mecanismo, que é **Mecânica** (§2.9) mesmo quando exige dedo fino; abrir tranca, que é
  **Arrombamento** (§2.2).
- **Exemplos de cena:** tirar o cartão de acesso do cinto de um segurança corporativo · plantar um
  rastreador na mochila de um contato · esconder uma lâmina antes de uma revista na entrada de um
  assentamento.
- **Quando é a perícia errada:** quando **ninguém está olhando**. Sem observador, manipular objeto é
  narrativa ou interação livre; Prestidigitação existe para o risco de **ser pego**, e por isso
  costuma ser **teste oposto** contra a **Percepção** de quem observa.
- **Faixas de exemplo:** bolso de aliado distraído · revista superficial na porta · revista corporal
  metódica: `[A CALIBRAR]`.

### 2.6. Pilotagem — AGI

- **Cobre:** conduzir veículo terrestre sob pressão, manobra evasiva, trafegar em entulho e terreno
  difícil, atravessar barricada, controlar derrapagem, embarcações improvisadas se a mesa as usar.
- **NÃO cobre:** **consertar** o veículo, que é **Mecânica** (§2.9); modificá-lo, que depende do
  módulo de Veículos e da assinatura **Modificação Veicular**, hoje **bloqueada**
  (`docs/gdd/GDD_Glossario.md` §3); e ler o terreno para escolher a rota, que é **Sobrevivência** (§2.15).
- **Exemplos de cena:** sair de um cerco de errantes com uma caminhonete · descer uma rampa de
  estacionamento com o freio comprometido · manter o veículo entre o grupo e a fonte de ruído.
- **Quando é a perícia errada:** hoje, em quase toda cena mecânica de veículo — **o módulo de Veículos
  ainda não foi desenhado** (§3.7). Pilotagem é plenamente rolável em condução narrada, mas velocidade,
  colisão, dano de veículo e perseguição em grid são `[A CALIBRAR]` e pertencem àquele módulo.
- **Faixas de exemplo:** estrada limpa · rua entulhada · perseguição: `[A CALIBRAR]`.

### 2.7. Vigor — CON

- **Cobre:** forçar o corpo além do limite **por escolha própria** — marcha forçada, vigília
  prolongada, apneia, suportar frio ou calor extremos, trabalho braçal contínuo, aguentar uma
  privação sem desmoronar.
- **NÃO cobre — e esta é a fronteira mais importante do documento:** o **teste de CON contra
  Infecção** (`docs/gdd/GDD_Infeccao.md` §2), que é **teste de resistência puro** e **não recebe proficiência
  de Vigor**. Também não cobre esforço de **pico**, que é Atletismo (§2.1), nem veneno, que é
  Resistir Toxinas (§2.8).
- **Exemplos de cena:** três dias de estrada com ração cortada · segurar uma viga por uma hora
  enquanto o Construtor escora · nadar em água gelada até a outra margem.
- **Quando é a perícia errada:** **sempre que o Mestre foi quem pediu o teste.** Se a fonte é externa
  — mordida, gás, radiação, exaustão imposta — é resistência, não Vigor.
- **Faixas de exemplo:** turno dobrado de escavação · noite exposta sem abrigo · apneia longa:
  `[A CALIBRAR]`.

### 2.8. Resistir Toxinas — CON

- **Cobre:** identificar, diluir, neutralizar e tolerar veneno, gás, solvente e reagente de forma
  **ativa**: julgar se a água serve, reconhecer uma fumaça pelo cheiro, dosar um estimulante
  conhecido, trabalhar perto de **Química** sem se intoxicar (`docs/gdd/GDD_Modificacoes.md` §4).
- **NÃO cobre:** o **teste de resistência** que a condição **Envenenado** e o dano **Químico** exigem
  (`docs/gdd/GDD_Combate.md` §6.3 e §10) — esse é resistência de CON, não perícia. Também não cobre tratar o
  envenenado depois de instalado, que é **Medicina** (§2.11).
- **Exemplos de cena:** avaliar um barril de líquido num galpão industrial antes de tocá-lo · saber
  quanto de um estimulante saqueado pode ser usado sem risco · manusear ácido para uma receita.
- **Quando é a perícia errada:** quando a toxina **já entrou**. A partir daí o problema é do teste de
  resistência e do tratamento; a perícia serve para **não chegar lá**.
- **Faixas de exemplo:** água duvidosa · fumaça química não identificada · dose conhecida de
  estimulante: `[A CALIBRAR]`.

### 2.9. Mecânica — INT

- **Cobre:** tudo que tem **peça** — fabricar, consertar, adaptar, desmontar. **É o teste de INT das
  Modificações** (`docs/gdd/GDD_Modificacoes.md` §5.1, §7.4), consertos de arma, escoras e estruturas do
  Refúgio, mecanismos de porta, armadilhas mecânicas, manutenção de veículo.
- **NÃO cobre:** o que tem **corrente** — placa, sensor, chip, energia — que é **Eletrônica** (§2.10);
  saber **para que servia** um equipamento pré-Queda, que é **Saber Pré-Queda** (§2.12); e **conduzir**
  o que consertou, que é Pilotagem (§2.6).
- **CDs já canônicas:** as 17 modificações têm CD de INT fechada entre **8 e 16**
  (`docs/gdd/GDD_Modificacoes.md` §5.1). Este documento **não as altera**; apenas declara que a perícia que as
  rola é Mecânica.
- **Exemplos de cena:** instalar Arame Farpado num cano em campo · recalibrar uma pistola Desgastada ·
  escorar um teto que cedeu.
- **Quando é a perícia errada:** quando o objeto é eletrônico **por dentro** mesmo parecendo mecânico
  por fora — ver §7.2, que trata a fronteira caso a caso.
- **Falha crítica canônica:** `1` natural no teste de fabricação perde **todo** o material **e** derruba
  a arma 1 degrau de conservação (`docs/gdd/GDD_Modificacoes.md` §7.4). Resultado de falha **não-crítica**:
  `[A CALIBRAR]`.

### 2.10. Eletrônica — INT

- **Cobre:** placa, sensor, chip, fiação viva, baterias e **Célula de Energia**, painéis, câmeras,
  terminais e **interfaces corporativas**; desmontar aparelhos para extrair o componente
  **Eletrônicos**, que **não se fabrica — só se desmonta de algo que já existia**
  (`docs/gdd/GDD_Modificacoes.md` §4).
- **NÃO cobre:** a parte física do encaixe, que é **Mecânica** (§2.9); interpretar o **conteúdo** de
  um arquivo obtido, que é **Investigação** (§2.14) ou **Saber Pré-Queda** (§2.12) conforme o que se
  quer saber.
- **Exemplos de cena:** montar o Designador Laser · desviar a energia de uma porta automática ·
  extrair uma placa intacta de um micro-ondas · abrir um terminal corporativo sem disparar o alarme.
- **Quando é a perícia errada:** quando o alvo é **puramente mecânico**. Um cadeado de latão não tem
  placa; é Arrombamento (§2.2).
- **Faixas de exemplo:** receitas com Eletrônicos — CD canônica em `docs/gdd/GDD_Modificacoes.md` §5.1 ·
  terminais e interfaces corporativas: `[A CALIBRAR]`.

### 2.11. Medicina — INT

- **Cobre:** ferimento, hemorragia, **estabilizar um aliado em Estado Crítico**, estancar
  **Sangrando**, tratamento da **Trilha de Infecção**, aplicação do **Soro de Campo**, farmácia
  improvisada, diagnóstico.
- **NÃO cobre:** a **assinatura Estabilizar do Médico**, que é habilidade de classe e **não** depende
  desta perícia; o teste de resistência contra Infecção, que é CON puro (§1.1); e a **Enfermaria** do
  Refúgio, que é instalação, não perícia (Aprovação 023 — o nome *"Oficina médica"* foi retirado).
- **Exemplos de cena:** trazer de volta um companheiro em Estado Crítico antes da terceira falha ·
  fechar um corte que está drenando HP por turno · conduzir o tratamento de um personagem em
  **Infectado grave**.
- **Quando é a perícia errada:** quando o problema é **toxina antes de entrar** (§2.8) ou quando a
  resposta é a assinatura do Médico. Ver o aviso de colisão em §3.3.
- **Faixas de exemplo:** estabilizar aliado (`docs/gdd/GDD_Combate.md` §8.5) · estancar Sangrando (§10) ·
  tratar Infecção (`docs/gdd/GDD_Infeccao.md`, "Remoção"): todas `[A CALIBRAR]` e **herdadas**, não criadas
  aqui.

### 2.12. Saber Pré-Queda — INT

- **Cobre:** o mundo que acabou — siglas, logotipos, protocolos, hierarquias corporativas, para que
  servia um prédio, como se lia um formulário, o que significava um símbolo de risco, onde numa
  fábrica ficava o almoxarifado.
- **NÃO cobre:** operar a coisa reconhecida — isso é Mecânica ou Eletrônica; deduzir o que aconteceu
  **naquele local recentemente**, que é **Investigação** (§2.14); e o mundo **atual**, que é
  Sobrevivência, Rastrear ou informação de facção obtida socialmente.
- **Exemplos de cena:** reconhecer no crachá de que divisão era aquele laboratório · saber que a **Liga
  Pré-Queda** aparece onde havia estrutura militar · identificar um selo de contenção biológica numa
  porta.
- **Quando é a perícia errada:** quando a pergunta é **"o que houve aqui?"** e não **"o que isto era?"**.
  Essa é a fronteira exata com Investigação.
- **Faixas de exemplo:** marca comum · protocolo militar · arquivo corporativo restrito: `[A CALIBRAR]`.
- **Nota de glossário:** **Saber Pré-Queda** é termo novo, ainda **sem verbete** em
  `docs/gdd/GDD_Glossario.md` (§8.1).

### 2.13. Percepção — PER

- **Cobre:** notar o que **está lá agora** — emboscada, alvo escondido, som fora de lugar, fio de
  armadilha, cheiro de fumaça, movimento na periferia. É o lado defensivo do teste oposto de
  **Esconder** e de **Prestidigitação**.
- **NÃO cobre:** **raciocinar** sobre o que se notou, que é **Investigação** (§2.14); seguir um rastro
  até a origem, que é **Rastrear** (§2.16); ler o terreno para decidir rota e abrigo, que é
  **Sobrevivência** (§2.15).
- **Regra canônica que ela resolve:** a **CD do teste de PER para detectar emboscada**, aberta desde
  `docs/gdd/GDD_Combate.md` §2.2 — ver §3.5.
- **Exemplos de cena:** perceber que o corredor está silencioso demais · ver o cano da espingarda
  antes que ele apareça · notar a tábua solta antes de pisar.
- **Quando é a perícia errada:** quando a informação **exige tempo e análise**. Percepção é o instante;
  Investigação é o minuto.
- **Faixas de exemplo:** emboscada (`docs/gdd/GDD_Combate.md` §2.2, **`[A CALIBRAR]` e canônica em aberto**) ·
  alvo escondido · armadilha bem montada: `[A CALIBRAR]`.

### 2.14. Investigação — PER

- **Cobre:** deduzir o que **esteve** lá — vasculhar cena, ler indício, reconstruir sequência de
  eventos, encontrar o compartimento falso, cruzar documentos, identificar inconsistência num relato.
- **NÃO cobre:** perceber no instante (Percepção, §2.13); reconhecer o que uma sigla significava
  (Saber Pré-Queda, §2.12); seguir a trilha que sai da cena (Rastrear, §2.16).
- **Exemplos de cena:** entender pela disposição dos corpos quem atirou primeiro · achar o esconderijo
  atrás do painel · concluir que o grupo anterior saiu com pressa e deixou componentes para trás.
- **Quando é a perícia errada:** em combate. Investigação é perícia de **cena**, e o canon não abre
  nenhum uso dela dentro do turno. Se a mesa quiser um, é `[A CALIBRAR]`.
- **Faixas de exemplo:** quarto revirado · cena deliberadamente encoberta · fraude documental
  corporativa: `[A CALIBRAR]`.

### 2.15. Sobrevivência — PER

> **Aprovação 033 — o saque do grupo.** Antes de cada saque, o grupo faz **um** teste de
> Sobrevivência, **CD 13**: sucesso rola `3d6` itens mantendo os **2 maiores**, falha mantendo os
> **2 menores** (`docs/gdd/GDD_Saque.md` §4.1). É o número que esta perícia não tinha. **Componente
> específico não se procura mais por teste** — ele sai da tabela única de saque.

- **Cobre:** ler terreno, achar água potável e abrigo, forragear, orientar-se, prever o tempo, montar
  acampamento, evitar zona quente — **e encontrar os oito componentes de fabricação no saque**
  (§3.8), que é o que liga esta perícia direto na economia.
- **NÃO cobre:** seguir um alvo específico, que é **Rastrear** (§2.16); julgar se a água encontrada é
  tóxica, que é **Resistir Toxinas** (§2.8); e **fabricar** com o que achou, que é Mecânica ou
  Eletrônica.
- **Vantagem canônica:** o talento geral **Faro para Sucata** (CANON 021 §2) dá **Vantagem em
  Sobrevivência para encontrar componentes**.
- **Exemplos de cena:** escolher em que ala do hospital vale gastar a hora de busca · achar um ponto
  de água numa cidade morta · encontrar **Peças Mecânicas** numa oficina já saqueada duas vezes.
- **Quando é a perícia errada:** quando o recurso é **Liga Pré-Queda** e o local não a tem. Nenhuma
  Sobrevivência **produz** Liga: ela é **não-fabricável** e a taxa de aparição por tipo de local é
  `[A CALIBRAR]` (`docs/gdd/GDD_Modificacoes.md` §4.1).
- **Faixas de exemplo:** achar água · encontrar componente por escassez (Abundante / Comum / Incomum /
  **RARO**): `[A CALIBRAR]`.

### 2.16. Rastrear — PER

- **Cobre:** seguir pegada, sangue, arrasto e trilha de horda; estimar **número, direção e há quanto
  tempo**; distinguir rastro humano de mutante; perceber que estão **seguindo o grupo**.
- **NÃO cobre:** a busca ampla por recursos, que é **Sobrevivência** (§2.15); notar o rastro pela
  primeira vez quando ele não era procurado, que pode ser **Percepção** (§2.13).
- **Exemplos de cena:** contar quantos saqueadores passaram pela ponte · seguir o arrasto de sangue de
  um mutante ferido até o ninho · descobrir que o rastro do grupo está sendo acompanhado.
- **Quando é a perícia errada:** em terreno que **não guarda marca** — asfalto seco, concreto, chuva
  forte. O Mestre deve declarar a impossibilidade antes, não transformá-la em CD impossível.
- **Faixas de exemplo:** terra molhada · asfalto seco · rastro após chuva: `[A CALIBRAR]`.

### 2.17. Persuasão — CAR

- **Cobre:** negociar, convencer, acalmar, mentir de forma plausível, conseguir passagem ou informação
  **sem arma na mão**, mediar entre facções, comprar tempo.
- **NÃO cobre:** ameaçar, que é **Intimidação** (§2.18); ler se o outro está mentindo, que é
  **Percepção** (§2.13) ou **Investigação** (§2.14) conforme seja instinto ou análise.
- **Exemplos de cena:** convencer um posto avançado a abrir o portão de noite · negociar **Liga
  Pré-Queda** por munição · impedir que dois grupos de sobreviventes se matem por um gerador.
- **Quando é a perícia errada:** contra quem **não negocia**. Zumbis e mutantes não têm reação social,
  e um NPC com ordem explícita costuma exigir outra abordagem.
- **Custo social da Infecção visível:** a banda **Infectado** da Trilha impõe **custo social, não
  mecânico** — *"NPCs reagem"* (`docs/gdd/GDD_Infeccao.md` §3). **Se isso vira Desvantagem em Persuasão:**
  `[A CALIBRAR]`.
- **Faixas de exemplo:** sobrevivente neutro · facção hostil · guarda corporativo com ordem:
  `[A CALIBRAR]`.

### 2.18. Intimidação — CAR

- **Cobre:** ameaçar, impor presença, extrair informação pelo medo, dispersar um grupo sem violência,
  sustentar um blefe armado.
- **NÃO cobre:** a condição **Amedrontado**, que é condição de combate com fonte própria
  (`docs/gdd/GDD_Combate.md` §10) — **a perícia não a aplica sozinha**, e se pode aplicá-la é `[A CALIBRAR]`.
  Também não cobre convencer, que é Persuasão (§2.17).
- **Exemplos de cena:** fazer um saqueador isolado largar a arma · arrancar o paradeiro de um depósito ·
  segurar um grupo na porta enquanto os outros carregam o veículo.
- **Quando é a perícia errada:** quando o grupo vai **voltar àquele lugar**. Intimidação é a perícia
  cujo sucesso a mesa lembra — ela resolve a cena e cobra depois, e o Mestre deve deixar o preço
  visível.
- **Faixas de exemplo:** saqueador isolado · líder na frente do próprio grupo · corporativo protegido:
  `[A CALIBRAR]`.

---

## 3. As que preenchem buracos que já existiam

Esta é a seção que justifica o módulo inteiro existir. Cada uma destas perícias **não foi inventada
para existir**: ela foi criada porque **uma regra canônica anterior pedia "um teste" e não dizia de
quê**. O padrão é sempre o mesmo — a regra estava fechada, a consequência estava fechada, e faltava o
nome da coisa que se rola.

> **Divergência de contagem, registrada e não corrigida.** CANON 021 §1 intitula esta lista **"Sete
> delas preenchem buracos"** e em seguida tabela **oito** perícias. Este documento reproduz as oito
> que a tabela canônica declara, e registra a divergência em §8.1.

### 3.1. Mecânica → o teste de INT das Modificações

| | |
|---|---|
| **Regra órfã** | *"Fabricar exige um **teste de Inteligência** contra a CD da modificação"* |
| **Onde estava** | `docs/gdd/GDD_Modificacoes.md` §5.1 (tabela das 17) e §7.4 (falha crítica) |
| **O que já era canônico** | As **17 CDs**, de **8 a 16**; a falha crítica em `1` natural; as duas vias |
| **O que faltava** | **Qual perícia soma proficiência naquele teste** |
| **Dono agora** | **Mecânica (INT)** |

O sistema de Modificações é o **tier "Modificada"** — o **único tier que o grupo fabrica em vez de
saquear** (`docs/gdd/GDD_Modificacoes.md` §1). Ele tinha receitas, componentes, slots, portes, duas vias, uma
regra central de custo e uma tabela de falha crítica. Tinha tudo **menos a linha da ficha que se
consulta para rolar**. Um Construtor e um sobrevivente qualquer rolavam o mesmo `d20 + INT`, e a
diferença entre o especialista e o amador não existia mecanicamente.

Com Mecânica, a distância aparece: até `+6` de proficiência sobre uma escada de CDs que vai de **8**
(Alça Tática, Pano Abafador) a **16** (Eletrodos, Designador Laser). **As CDs não mudam** — este
documento não toca nelas. E a falha crítica continua canônica: `1` natural perde **todo** o material
**e** derruba a arma um degrau de conservação.

> **CORRIGIDO — a propriedade Utilitária NÃO se aplica aqui.** O CANON 021 §1 sugeria que
> **Utilitária** daria Vantagem também em Mecânica, e isso era **erro de redação da proposta**, não
> uma ampliação aprovada. A definição canônica é e continua sendo *"vantagem em testes de **FOR**
> para arrombar"* (`docs/gdd/GDD_Armas.md` §3, Aprovação 006) — ou seja, **Arrombamento** e nada mais.
> Mecânica é **INT** e não recebe Vantagem de propriedade de arma nenhuma.
>
> A distinção importa: **Utilitária descreve a arma como alavanca**, não como ferramenta de precisão.
> Um pé de cabra abre uma porta; ele não calibra um silenciador.

### 3.2. Eletrônica → Precisão, Eletrodos e as interfaces corporativas

| | |
|---|---|
| **Regra órfã** | Receitas que consomem **Eletrônicos** e **Célula de Energia**; acesso a sistemas corporativos |
| **Onde estava** | `docs/gdd/GDD_Modificacoes.md` §4 (componentes) e §5.1 (Precisão, Eletrodos) |
| **O que já era canônico** | *"**Eletrônicos** não se fabrica: só se desmonta de algo que já existia"* |
| **O que faltava** | **Quem sabe desmontar sem destruir** |
| **Dono agora** | **Eletrônica (INT)** |

O componente **Eletrônicos** é, junto com a Liga Pré-Queda, um dos dois recursos que o canon declara
impossíveis de produzir. Mas os dois são impossíveis por razões **diferentes**, e essa diferença é
inteiramente uma questão de perícia: **Liga não se produz porque não existe processo** — só se
encontra. **Eletrônicos não se produz porque se extrai** — e extrair é uma operação, feita por alguém,
com chance de estragar a peça.

Sem Eletrônica, essa extração era narração. Com ela, é decisão: desmontar um painel achado é um teste,
e falhar custa o componente mais disputado das receitas de **Precisão** (Mira Telescópica, Designador
Laser, Coronha Estabilizada) e dos **Eletrodos** — a modificação que produz a **Soqueira "Vólt-9"**,
item-assinatura do sistema.

Eletrônica também é o único vetor de **invasão não-violenta** do cenário cyberpunk: terminais,
câmeras, portas automáticas, telemetria corporativa. **CDs de interface corporativa:** `[A CALIBRAR]`
— nenhum documento canônico as fixou, porque nenhum documento canônico tinha a perícia.

### 3.3. Medicina → três regras órfãs de uma vez

| Regra órfã | Onde estava | Texto que ficou pendurado |
|---|---|---|
| Estabilizar aliado em Estado Crítico | `docs/gdd/GDD_Combate.md` §4 e §8.5 | *"Estabilizar um aliado com **Usar Objeto** ou **perícia médica**: CD `[A CALIBRAR]`"* |
| Estancar **Sangrando** | `docs/gdd/GDD_Combate.md` §10 | *"Cessa com cura ou com uma ação de estancamento de CD `[A CALIBRAR]`"* |
| Tratar Infecção e aplicar o **Soro de Campo** | `docs/gdd/GDD_Infeccao.md`, "Remoção" | *"As quantidades e os tempos são `[A CALIBRAR]`"* |

**O caso mais literal do documento.** `docs/gdd/GDD_Combate.md` §8.5 escreve a expressão **"perícia médica"**
em texto corrido, apontando para uma perícia que **não existia em lugar nenhum do canon**. A regra
estava escrita contra uma coisa ausente.

As três agora têm dono: **Medicina (INT)**. E as três continuam com CD `[A CALIBRAR]` — **este
documento dá dono às regras, não valor a elas.** A distinção é deliberada: dono é estrutura e pode ser
fechado agora; valor é balanceamento e depende do ciclo de calibragem, sobretudo porque a CD de
estabilizar interage diretamente com a letalidade de nível 1 declarada em `docs/gdd/GDD_Combate.md` §8.1
(*"um único crítico derruba qualquer personagem de nível 1"*).

> **Cuidado com a palavra "Estabilizar" — colisão 5 do glossário.** `docs/gdd/GDD_Glossario.md` §2 registra
> **três sentidos vivos e sem relação entre si**:
> **(a)** *Estabiliza* = acumular 3 sucessos em testes de morte e parar de rolar (`docs/gdd/GDD_Combate.md` §8.3);
> **(b)** *estabilizar um aliado* = um uso da ação **Usar Objeto**, aberto a qualquer personagem;
> **(c)** *Estabilizar* = a **assinatura do Médico**, que remove pontos da Trilha de Infecção.
>
> **Medicina destrava apenas (b).** Ela **não** concede sucessos em teste de morte, **não** tira
> ninguém do Estado Crítico por si só e **não** substitui nem alimenta a assinatura. Implementadores:
> `docs/classes/Classe_Medico.md` §5.4 instrui **três identificadores distintos no motor** — Medicina é um quarto
> contexto da mesma palavra, e não deve compartilhar identificador com nenhum dos três (§8.1).

### 3.4. Furtividade → a ação Esconder finalmente rola contra algo

| | |
|---|---|
| **Regra órfã** | A ação **Esconder** da lista fechada de ações |
| **Onde estava** | `docs/gdd/GDD_Combate.md` §4 |
| **Texto canônico** | *"Teste de **furtividade** oposto à PER dos observadores"* — em minúscula |
| **Dono agora** | **Furtividade (AGI)**, contra **Percepção (PER)** |

A minúscula é o sintoma. **Esconder** é uma das dez ações canônicas, com consequência inteiramente
fechada — *"Escondido: Vantagem no próximo ataque, e o ataque revela você. Alvo que não pode ser visto
é atacado com Desvantagem"* — e o teste que a governa era descrito por um substantivo comum, porque
não havia substantivo próprio. Agora há, dos dois lados:

```
Esconder = d20 + AGI + proficiência (Furtividade)  vs.  d20 + PER + proficiência (Percepção)
```

**Interação com o Ruído — o que é canônico e o que não é.** CANON 021 §1 declara que Furtividade
*"interage com o Nível de Ruído"*. O que já está fechado em `docs/gdd/GDD_Ruido.md`:

- O Ruído é medido em **raio de hexágonos**, não em teste: Silencioso (sem raio) · Baixo (4 hex) ·
  Médio (20 hex) · Alto (50 hex).
- A **Atração** dentro do raio é **automática, sem rolagem** (§2).
- **Arma de fogo nunca chega a Silencioso**, por mais que se empilhe silenciador e munição Subsônica
  (§3) — o piso é **Baixo**.

Ou seja: uma arma **Alta** disparada a 3 hexágonos de uma patrulha **não é um teste de Furtividade
ganho**; é um raio de 50 hexágonos que não consulta ninguém. **A forma exata da interação — se o
Nível de Ruído impõe Desvantagem, uma penalidade numérica, ou falha automática dentro do raio — é
`[A CALIBRAR]`** (§8, item 3). O que este documento fixa é a direção: **o Ruído age sobre a
Furtividade, e a Furtividade nunca age sobre o Ruído.**

### 3.5. Percepção → a CD de emboscada, aberta desde `GDD_Combate` §2.2

| | |
|---|---|
| **Regra órfã** | Detectar uma emboscada |
| **Onde estava** | `docs/gdd/GDD_Combate.md` §2.2 |
| **Texto canônico** | *"CD do teste de **PER** para detectar a emboscada: `[A CALIBRAR]`"* |
| **Dono agora** | **Percepção (PER)** — **o número continua `[A CALIBRAR]`** |

§2.2 é uma das seções mais fechadas do módulo de combate. Ela define **toda** a consequência da
emboscada: o lado surpreendido **não age na 1ª rodada**, mantém sua posição na ordem de iniciativa (o
turno apenas passa) e **não tem Reação** até o início do próprio turno na **2ª rodada**; o lado
emboscador age normalmente desde a 1ª. É uma das punições mais duras do sistema — uma rodada inteira
de exposição sem Reação, num jogo em que *"um único crítico derruba qualquer personagem de nível 1"*.

E a última linha da seção era uma frase pendurada: o teste que decide tudo isso citava um **atributo**,
não uma perícia. Um Explorador treinado em vigilância e um Cientista distraído tinham exatamente a
mesma chance de ver a armadilha.

**Agora a perícia é Percepção, e o número continua `[A CALIBRAR]`.** Esta distinção é o método deste
documento inteiro: **dar dono não é calibrar.** Percepção é também o lado defensivo do teste oposto de
**Esconder** (§3.4) e de **Prestidigitação** (§2.5), e o talento geral **Ouvido Treinado**
(CANON 021 §2) opera na mesma camada sensorial — percebe a **direção** da última fonte de ruído fora
do campo de visão, sem teste.

### 3.6. Arrombamento → a propriedade Utilitária, que esperava há seis aprovações

| | |
|---|---|
| **Regra órfã** | A propriedade de arma **Utilitária** |
| **Onde estava** | `docs/gdd/GDD_Armas.md` §3; verbete em `docs/gdd/GDD_Glossario.md` §3 |
| **Texto canônico** | *"A arma serve como ferramenta — **Vantagem em testes de FOR para arrombar**"* |
| **Dono agora** | **Arrombamento (FOR)** |

**Este é o buraco mais antigo e mais visível do canon.** A propriedade **Utilitária** concedia
**Vantagem** numa coisa que **não existia na ficha de nenhum personagem**. Não havia linha de
Arrombamento, não havia CD de arrombar, não havia nada — e mesmo assim a propriedade era tão
estruturante que provocou a **colisão 2** do glossário: a família de modificação que também se chamava
"Utilitária" teve de ser renomeada para **Suporte** (Aprovação 013) para lhe ceder a palavra. O canon
renomeou uma família inteira para proteger o nome de uma propriedade que apontava para o vazio.

Agora ela aterrissa. **Arrombamento (FOR)** existe, e um pé de cabra, um machado ou uma pá de sapador
dão **Vantagem** nela por serem **Utilitárias** — sem regra nova, sem exceção, sem aprovação
adicional. É a regra de `docs/gdd/GDD_Armas.md` §3 funcionando pela primeira vez como escrita.

> **Isto não concede nada além do que já estava concedido.** A Vantagem é a mesma, a fonte é a mesma,
> e ela **não acumula** com outra Vantagem (`docs/gdd/GDD_Combate.md` §1.1). Uma arma Utilitária usada por
> alguém com a ação **Ajudar** de um aliado continua rolando **um** `2d20`, não dois.

**Divergência registrada:** CANON 021 §1 estende a Vantagem de Utilitária **também a Mecânica**, que é
perícia de **INT** — enquanto `docs/gdd/GDD_Armas.md` §3 e o glossário limitam a propriedade a *"testes de
**FOR** para arrombar"*. Relatado em §8.1, item 2; **não corrigido aqui**.

### 3.7. Pilotagem → a porta suave do Piloto

| | |
|---|---|
| **Regra órfã** | A terceira **porta suave** do sistema |
| **Onde estava** | `CANON_CLASSES.md` §2, replicado em todos os `Classe_*.md` §4; verbete em `docs/gdd/GDD_Glossario.md` §3 |
| **Texto canônico** | *"Qualquer personagem acessa em tier ruim; a classe especialista é indispensável para o tier bom, não para o acesso"* |
| **Dono agora** | **Pilotagem (AGI)** |

O canon declara **três portas suaves**: Modificações (**Cientista**), Refúgio (**Construtor**) e
Veículos (**Piloto**). As duas primeiras já tinham teste — o de INT das Modificações (hoje Mecânica) e
a construção do Refúgio. **A do Piloto era a única sem teste declarado**, o que significa que o pilar
inteiro dependia de arbítrio.

Pilotagem fecha isso do lado da ficha: *qualquer personagem* conduz, rolando `d20 + AGI`; o Piloto
treinado soma proficiência. É exatamente o desenho de porta suave — **acesso para todos, tier bom para
o especialista**.

> **Dependência de módulo, declarada e não escondida.** O **módulo de Veículos ainda não foi
> desenhado**, e a assinatura **Modificação Veicular** do Piloto consta como **bloqueada** por causa
> disso (`docs/gdd/GDD_Glossario.md` §3). Pilotagem é plenamente rolável em qualquer condução narrada em mesa;
> mas **velocidade, colisão, dano de veículo, capacidade, combustível e perseguição em grid hexagonal
> são `[A CALIBRAR]` e pertencem àquele módulo**, não a este. Registrar a perícia agora evita que o
> módulo futuro invente uma segunda.

### 3.8. Sobrevivência → a perícia que liga direto na economia

| | |
|---|---|
| **Regra órfã** | **Como se acham os oito componentes** |
| **Onde estava** | `docs/gdd/GDD_Modificacoes.md` §4 (os oito) e §4.1 (Liga não se fabrica, só se encontra) |
| **O que faltava** | Toda a operação de **busca** — o canon dizia *o que* se acha, nunca *como* |
| **Dono agora** | **Sobrevivência (PER)** |

Esta é a mais consequente das oito, e a razão é **econômica, não temática**.

> ### **É com Sobrevivência que se encontram os oito componentes de fabricação.**

Os componentes — **Sucata** (Abundante), **Peças Mecânicas** e **Fiação** (Comum), **Química**,
**Óptica**, **Eletrônicos** e **Célula de Energia** (Incomum) e **Liga Pré-Queda** (**RARO**) — são o
insumo das **17 modificações** e das **dez Munições Especiais**, que *"não se acham: fabricam-se, com
os mesmos oito componentes"* (`docs/gdd/GDD_Combate.md` §13.1). Sem componentes não há tier **Modificada**, e
sem ele o poder de fogo do grupo volta a ser refém da sorte de saque — exatamente o problema
estrutural que `docs/gdd/GDD_Modificacoes.md` §1 diz que o sistema existe para resolver.

E a cadeia canônica de `docs/gdd/GDD_Modificacoes.md` §7.2 — a que *"puxa o grupo inteiro para fora do
Refúgio sem incentivo artificial"* — termina numa operação que não tinha perícia:

```
Quer stack limpo  ->  precisa de OFICINA
Oficina           ->  precisa de LIGA PRÉ-QUEDA
Liga Pré-Queda    ->  não se fabrica, só se SAQUEIA
Saque             ->  sair do Refúgio
Sair do Refúgio   ->  SOBREVIVÊNCIA          <-- o elo que faltava
```

**Sobrevivência é o último elo dessa corrente.** O talento geral **Faro para Sucata** (CANON 021 §2)
— *"Vantagem em Sobrevivência para encontrar componentes"* — é a confirmação canônica: o canon já
sabia qual perícia seria, porque escreveu o talento antes de a perícia existir.

**Consequência de design.** A perícia transforma o saque de **sorte** em **decisão**. Um grupo sem
Sobrevivência não fica sem componentes — rola `d20 + PER` e acha menos, com mais tempo e mais
exposição. Um grupo com Sobrevivência escolhe **onde** gastar a hora de busca. É a mesma lógica das
portas suaves aplicada à economia.

**Limites duros, que a perícia não move:**

- **Liga Pré-Queda continua não-fabricável**, em nenhum tier e nenhuma circunstância. Uma
  Sobrevivência excelente **encontra** Liga; nenhuma Sobrevivência a **produz**. Implementadores:
  manter a marcação de **recurso não-fabricável** no motor.
- **Taxa de aparição de Liga por tipo de local:** `[A CALIBRAR]`, já aberta em
  `docs/gdd/GDD_Modificacoes.md` §4.1 e **não** resolvida aqui.
- **CD para encontrar cada componente**, por escassez e por tipo de local: `[A CALIBRAR]` (§8, item 4).
- **Se a busca consome tempo de cena, de descanso ou de downtime:** `[A CALIBRAR]` — relacionado à
  pendência de **tempo de fabricação** de `docs/gdd/GDD_Modificacoes.md` §9.2.

---

## 4. Fronteiras entre perícias parecidas

É aqui que mesa real trava. Cada par abaixo tem um **critério de uma frase** que decide a dúvida sem
consulta a documento nenhum.

### 4.1. Percepção × Investigação

> **Percepção é o instante. Investigação é o minuto.**

| Pergunta na mesa | Perícia |
|---|---|
| "Eu noto alguma coisa?" | **Percepção** |
| "Eu procuro o que aconteceu aqui" | **Investigação** |
| "Tem alguém nos esperando?" | **Percepção** (emboscada, §3.5) |
| "Onde eles esconderiam o depósito?" | **Investigação** |
| "Ele está mentindo?" | **Percepção** se é instinto; **Investigação** se é cruzar o relato com fatos |

**A regra prática:** se o personagem **pode fazer isso andando**, é Percepção. Se ele precisa **parar**,
é Investigação. Por isso Percepção tem uso canônico em combate (§6) e Investigação não tem nenhum.

### 4.2. Mecânica × Eletrônica

> **Mecânica é o que tem peça. Eletrônica é o que tem corrente.**

| Objeto | Perícia | Por quê |
|---|---|---|
| Arame Farpado, Pregos, Cabeça Lastrada | **Mecânica** | Só matéria |
| Guarda de Ejeção, Recalibragem, Coronha Estabilizada | **Mecânica** | Mecanismo de arma |
| Lanterna Acoplada, Designador Laser, Eletrodos | **Eletrônica** | Consomem **Célula de Energia** |
| Mira Telescópica | **Mecânica** — óptica sem circuito | Lente e encaixe, sem corrente |
| Terminal, câmera, porta automática | **Eletrônica** | Sistema alimentado |
| Cadeado, grade, corrente | **Arrombamento** | Nem uma nem outra (§2.2) |

**O caso misto é real e comum:** instalar um Designador Laser exige encaixar (**Mecânica**) e ligar
(**Eletrônica**). O canon não define qual das duas o Mestre pede, nem se pede as duas em sequência —
**`[A CALIBRAR]`** (§8, item 5). Convenção sugerida enquanto não se calibra, e **explicitamente não
canônica**: pedir **uma** perícia por receita, escolhida pelo **componente mais escasso** da lista
(`docs/gdd/GDD_Modificacoes.md` §5.1) — se há Eletrônicos ou Célula, é Eletrônica; senão, Mecânica.

### 4.3. Sobrevivência × Rastrear

> **Sobrevivência busca uma categoria. Rastrear segue um indivíduo.**

| Situação | Perícia |
|---|---|
| "Procuro componentes nesta oficina" | **Sobrevivência** |
| "Sigo o que levou o componente daqui" | **Rastrear** |
| "Onde acho água nesta região?" | **Sobrevivência** |
| "Para onde foi a horda que passou?" | **Rastrear** |
| "Escolho a rota mais segura até lá" | **Sobrevivência** |
| "Alguém está nos seguindo?" | **Rastrear** (ou **Percepção**, se for no instante) |

**A regra prática:** Sobrevivência responde **"onde"**; Rastrear responde **"quem, quantos e quando"**.
As duas são PER e convivem na mesma lista de classe em **Explorador** e **Atirador de Elite** — o que é
proposital: são os dois lados do trabalho de batedor.

### 4.4. Atletismo × Acrobacia

> **Atletismo é força aplicada ao corpo. Acrobacia é controle do corpo.**

| Situação | Perícia |
|---|---|
| Escalar um muro alto | **Atletismo** |
| Atravessar uma viga estreita | **Acrobacia** |
| Saltar a maior distância possível | **Atletismo** |
| Cair de um andar sem se arrebentar | **Acrobacia** |
| Empurrar um carro enguiçado | **Atletismo** |
| Passar por um vão apertado | **Acrobacia** |
| Escapar de **Agarrado** | **Ambas** — o canon dá a escolha: teste oposto de **FOR ou AGI** (`docs/gdd/GDD_Combate.md` §10) |

**A regra prática:** se falhar significa **não conseguir**, é Atletismo. Se falhar significa **cair**,
é Acrobacia. A linha do **Agarrado** é a única em que o canon abre as duas, e a escolha é do jogador —
o que faz a fronteira ser uma decisão de ficha, não de arbítrio.

### 4.5. Vigor × Resistir Toxinas × o teste de resistência de CON

Três coisas de CON, e só duas são perícias.

| Situação | O que se rola |
|---|---|
| Marchar a noite inteira | **Vigor** (perícia) |
| Decidir se aquela água é potável | **Resistir Toxinas** (perícia) |
| Aguentar uma dose conhecida de estimulante | **Resistir Toxinas** (perícia) |
| Gás tóxico estourou na sala | **Teste de resistência de CON** |
| Condição **Envenenado** aplicada | **Teste de resistência de CON** |
| Fim do combate com pontos de Infecção | **Teste de resistência de CON** (`docs/gdd/GDD_Infeccao.md` §2) |

**A regra prática, já dita em §1.1:** *se o Mestre pediu o teste, é resistência; se o jogador pediu, é
perícia.*

### 4.6. Furtividade × Prestidigitação

> **Furtividade esconde a pessoa. Prestidigitação esconde a coisa.**

Atravessar um posto sem ser visto é Furtividade; atravessá-lo sendo visto **com uma lâmina no casaco**
é Prestidigitação. As duas são AGI e podem ser pedidas na mesma cena, em sequência — e nesse caso são
**dois testes**, não um.

### 4.7. Persuasão × Intimidação

> **Persuasão deixa a porta aberta. Intimidação a fecha atrás de você.**

Mecanicamente são simétricas; a diferença é o **rastro**. Intimidação tende a resolver a cena e a
criar a próxima; Persuasão custa mais para começar e não cobra depois. O canon **não** fixa penalidade
mecânica para o rastro de Intimidação — **é consequência narrativa**, e transformá-la em regra exigiria
aprovação do Diretor.

### 4.8. Saber Pré-Queda × Investigação

> **Saber Pré-Queda é o que a coisa era. Investigação é o que aconteceu com ela.**

Reconhecer que o símbolo na porta é de contenção biológica corporativa: **Saber Pré-Queda**. Concluir
que alguém a abriu há poucos dias e não fechou: **Investigação**. Numa mesma sala, as duas perguntas
podem ser feitas em sequência, e as duas são PER/INT diferentes — **INT para Saber Pré-Queda, PER para
Investigação** —, o que é proposital: o arquivo é memória, a cena é atenção.

---

## 5. Perícias por classe

**Cada classe escolhe 3 perícias de uma lista de 6** e tem **2 testes de resistência fixos**
(CANON 021 §1).

| Classe | Lista de 6 (escolhe **3**) | Resistências |
|---|---|---|
| **Pugilista** | Atletismo · Intimidação · Vigor · Acrobacia · Percepção · Resistir Toxinas | **FOR, CON** |
| **Construtor** | Mecânica · Arrombamento · Atletismo · Sobrevivência · Saber Pré-Queda · Vigor | **FOR, CON** |
| **Médico** | Medicina · Percepção · Investigação · Saber Pré-Queda · Persuasão · Resistir Toxinas | **CON, INT** |
| **Piloto** | Pilotagem · Mecânica · Eletrônica · Acrobacia · Percepção · Arrombamento | **AGI, INT** |
| **Explorador** | Furtividade · Acrobacia · Percepção · Rastrear · Sobrevivência · Prestidigitação | **AGI, PER** |
| **Ceifador** | Furtividade · Atletismo · Percepção · Rastrear · Intimidação · Acrobacia | **AGI, FOR** |
| **Cientista** | Eletrônica · Mecânica · Saber Pré-Queda · Investigação · Medicina · Prestidigitação | **INT, AGI** |
| **Atirador de Elite** | Percepção · Furtividade · Rastrear · Acrobacia · Sobrevivência · Investigação | **AGI, PER** |

### 5.1. Leitura das listas

- **Percepção aparece em 6 das 8 listas** — só Construtor e Cientista não a têm. É a perícia mais
  disponível do sistema, o que é coerente com o fato de ela governar a **emboscada** (§3.5): o canon
  não quis que a surpresa dependesse de uma única classe estar viva.
- **Duas perícias aparecem em uma lista só:** **Pilotagem** (Piloto) e **Medicina**… que na verdade
  aparece em duas — Médico e Cientista. A única de lista única é **Pilotagem**, o que reforça que ela
  é a porta suave de um pilar (§3.7).
- **Explorador e Atirador de Elite têm listas quase idênticas** (4 de 6 em comum: Percepção,
  Furtividade, Rastrear, Acrobacia) e as **mesmas resistências, AGI e PER**. A diferenciação deles
  **não vem das perícias** — vem do dado de vida (d8 × d6), do limiar de Infecção (12 × 13) e da
  assinatura.
- **Nenhuma lista tem mais de uma perícia de CAR.** Persuasão e Intimidação nunca aparecem juntas,
  o que impede um "personagem social" construído só por perícia.

### 5.2. Nenhuma perícia é obrigatória

> ### **Um Médico sem Medicina é um personagem, não um erro.** (CANON 021 §1)

A lista de 6 é **oferta**, não requisito. Um Médico que escolha Percepção, Investigação e Persuasão é
um clínico que virou investigador de campo — e **continua tendo a assinatura do Médico**, que é
habilidade de classe e não depende de perícia nenhuma, **continua com limiar de Infecção 18**, o mais
alto do jogo, e **continua com as resistências CON e INT**. Nada do que define a classe passa pela
perícia. Um Ceifador sem Furtividade é um açougueiro que entra pela porta da frente; um Construtor sem
Mecânica é um sujeito que ergue paredes e paga outro para calibrar a arma.

Quatro consequências que o Mestre e o motor devem respeitar:

1. **Nenhuma regra canônica exige perícia como pré-requisito.** Pré-requisito de **Especialização** lê
   **proficiência de arma** (CANON 021 §2, regra de contenção 2) — o exemplo canônico é *Tiro
   Calculado exige arma de fogo*, e a solução é gastar uma Menor comprando a família **Longas**, não
   uma perícia.
2. **Quem não tem, rola mesmo assim** — `d20 + atributo`, sem proficiência (§1). A CD é a mesma. O
   personagem sem a perícia não está proibido: está em desvantagem estatística.
3. **O grupo nunca fica sem a função.** Sem ninguém com Medicina, estabilizar um aliado continua sendo
   um uso da ação **Usar Objeto**, aberta a qualquer personagem (`docs/gdd/GDD_Combate.md` §4). Sem ninguém com
   Sobrevivência, ainda se acham componentes. Paga-se em **chance**, não em impossibilidade.
4. **Implementadores: a perícia ausente não pode bloquear a ação no motor.** Nenhuma interface deve
   esconder ou desabilitar uma opção por falta de perícia — ela apenas deixa de somar proficiência.

### 5.3. Aquisição fora da classe

Uma **Especialização de porte Menor** (a partir do **nível 3**) compra **uma perícia** (CANON 021 §2),
com a **fonte diegética** que todo porte exige: mentor NPC, manual saqueado ou prática em campo
validada pelo Mestre. É a **única** via canônica de adquirir perícia fora da própria lista.

- As Menores disputam entre si: o mesmo porte compra **uma perícia · uma família de arma · um teste de
  resistência · um Talento Geral**. Comprar Medicina é não comprar **Nervos de Aço**, e vice-versa.
- **Teto de perícias adquiridas por Especialização, se houver:** `[A CALIBRAR]`.
- **Se uma Especialização pode conceder uma perícia que a classe já oferece na lista:** `[A CALIBRAR]`.
- Os talentos gerais **Faro para Sucata** (Vantagem em Sobrevivência para componentes) e **Ouvido
  Treinado** (direção da última fonte de ruído) são as duas interações canônicas entre Talentos e
  perícias.

---

## 6. Usar uma perícia em combate

A economia do turno **não muda** por causa deste documento. Vale, sem alteração, `docs/gdd/GDD_Combate.md`
§2.4: **1 Movimento (9 m / 6 hex) · 1 Ação · 1 Reação · 1 interação livre · 1 Ação Bônus de escopo
fechado**.

> ### **A Ação Bônus continua fechada em Destravar arma de fogo.**
> Nenhuma perícia deste documento concede, consome ou cria outro uso de Ação Bônus. Implementadores:
> criar o slot no motor e expor **somente** Destravar (`docs/gdd/GDD_Combate.md` §2.4 e §7.3).

| Uso em combate | Perícia | Custo |
|---|---|---|
| Ação **Esconder** — teste oposto à PER dos observadores | **Furtividade** | **A Ação** (`docs/gdd/GDD_Combate.md` §4) |
| Resistir à ação Esconder de um inimigo | **Percepção** | **Livre** — é o lado passivo do teste oposto |
| Notar emboscada no início do combate | **Percepção** | **Livre** — ocorre antes da 1ª rodada (§2.2) |
| Notar alvo escondido durante o turno | **Percepção** | `[A CALIBRAR]` — livre, parte do Movimento ou a Ação |
| Estabilizar aliado em Estado Crítico | **Medicina** | **A Ação**, via **Usar Objeto** (§4 e §8.5) |
| Estancar **Sangrando** | **Medicina** | **A Ação**, via **Usar Objeto** |
| Arrombar porta ou grade em cena de combate | **Arrombamento** | **A Ação**, via **Usar Objeto** |
| Ativar dispositivo técnico no meio da luta | **Eletrônica** | **A Ação**, via **Usar Objeto** |
| Escapar de **Agarrado** | **Atletismo** ou **Acrobacia** | Teste oposto de FOR ou AGI (§10); **se custa a Ação:** `[A CALIBRAR]` |
| Resistir a uma Prestidigitação inimiga | **Percepção** | **Livre** |
| Conduzir veículo em cena de combate | **Pilotagem** | `[A CALIBRAR]` — depende do módulo de Veículos (§3.7) |
| Fabricar qualquer coisa | **Mecânica** / **Eletrônica** | **Fora de combate**; tempo por via: `[A CALIBRAR]` |
| Encontrar componentes | **Sobrevivência** | **Fora de combate**, em saque ou expedição |
| Investigar uma cena | **Investigação** | **Fora de combate** — sem uso canônico em turno |

### 6.1. O que é livre e por quê

O critério é simples e segue a lógica já canônica da **interação livre com objeto** (`docs/gdd/GDD_Combate.md`
§4.2): **é livre o que o personagem não escolheu fazer.**

- **Percepção do lado defensivo é sempre livre.** Quando outro se esconde, você não gastou nada — ele
  gastou a Ação dele. O mesmo vale contra Prestidigitação.
- **Percepção de emboscada é livre** porque acontece **antes** da 1ª rodada, quando ninguém tem turno
  ainda (§2.2).
- **Tudo que o personagem escolhe fazer com as mãos custa a Ação**, via **Usar Objeto** — a ação que o
  canon define como *"manipula um objeto quando a interação livre não basta: aplicar estimulante,
  ativar dispositivo, arrombar, estabilizar um aliado"*. Repare que a própria redação de §4 já
  antecipava três perícias deste documento.
- **O que resta em aberto** é o caso intermediário: procurar ativamente um alvo escondido no meio do
  turno. É escolha do jogador (logo, deveria custar algo) mas é sensorial (logo, poderia ser livre).
  **`[A CALIBRAR]`** — e o canon **não** deve resolver isso abrindo a Ação Bônus.

### 6.2. O que interage com Ruído

Duas perícias tocam o sistema de `docs/gdd/GDD_Ruido.md`, e é útil saber **em que direção**:

- **Furtividade** é afetada pelo Ruído que o **próprio personagem** produz (§3.4). O raio do Nível de
  Ruído **não faz teste**: alcança quem alcança, e a **Atração** é automática dentro dele
  (`docs/gdd/GDD_Ruido.md` §2). **Forma exata da penalidade:** `[A CALIBRAR]`.
- **Percepção** é como se **escuta** o Ruído alheio. O talento **Ouvido Treinado** (CANON 021 §2) é o
  caso canônico — direção da última fonte fora do campo de visão, sem rolagem. **Se Percepção
  substitui, modifica ou apenas complementa o raio automático de Atração:** `[A CALIBRAR]`.
- **Nenhuma perícia reduz o Nível de Ruído de uma arma.** Isso é **modificação** (Silenciador,
  `docs/gdd/GDD_Modificacoes.md` §5.1) ou **munição** (Subsônica), e o piso continua **Baixo** — *arma de fogo
  nunca chega a Silencioso*.
- **Nenhuma perícia mexe no Medidor de Horda.** Ele é **recurso exclusivo do Mestre**, nunca exposto
  ao jogador (`docs/gdd/GDD_Glossario.md` §3), e soma apenas o **ruído mais alto por rodada**.

### 6.3. O que este documento explicitamente NÃO faz

Registrado para que nenhum ciclo futuro reabra por engano:

1. **Não cria ação nova.** A lista de ações continua fechada em dez (`docs/gdd/GDD_Combate.md` §4).
2. **Não concede uso de Ação Bônus.** Escopo fechado em Destravar, sem exceção.
3. **Não concede Reação nova.** Reações de talento, cibernética e equipamento seguem `[A CALIBRAR]`
   em §4.1 do módulo de combate.
4. **Não altera nenhuma CD já canônica** — as 17 CDs de fabricação (8 a 16) valem como estão.
5. **Não adiciona proficiência a teste de resistência nenhum** (§1.1).
6. **Não substitui assinatura de classe** por perícia, em nenhum caso.

---

## 7. Resumo de uma página — para o Mestre

| Se a cena é sobre… | Role… |
|---|---|
| Subir, saltar, empurrar, nadar | **Atletismo** (FOR) |
| Abrir o que está trancado, com ferramenta | **Arrombamento** (FOR) — Vantagem com arma **Utilitária** |
| Não cair, não ficar preso | **Acrobacia** (AGI) |
| Não ser visto nem ouvido | **Furtividade** (AGI) — afetada pelo **Ruído** |
| Mãos rápidas sob observação | **Prestidigitação** (AGI) |
| Conduzir veículo | **Pilotagem** (AGI) — módulo pendente |
| Aguentar esforço longo por escolha | **Vigor** (CON) — **não** é o teste contra Infecção |
| Veneno, gás e reagente, antes de entrar | **Resistir Toxinas** (CON) |
| Fabricar, consertar, adaptar o que tem peça | **Mecânica** (INT) — CDs **8 a 16**, já canônicas |
| O que tem placa, sensor ou corrente | **Eletrônica** (INT) |
| Ferimento, Estado Crítico, Infecção | **Medicina** (INT) |
| O que aquilo era antes da Queda | **Saber Pré-Queda** (INT) |
| O que está aqui **agora** | **Percepção** (PER) — **emboscada** |
| O que **aconteceu** aqui | **Investigação** (PER) |
| Onde acho água, abrigo, **componentes** | **Sobrevivência** (PER) |
| Quem passou, quantos, há quanto tempo | **Rastrear** (PER) |
| Convencer sem arma na mão | **Persuasão** (CAR) |
| Ameaçar e cobrar depois | **Intimidação** (CAR) |
| **O Mestre pediu o teste** | **Não é perícia. É teste de resistência.** |

---

## 8.

> **RESOLVIDAS DEPOIS DA ENTREGA — duas divergências desta lista já têm resposta:**
>
> - **Utilitária × Mecânica.** Era **erro de redação da Queen** na proposta do CANON 021, não uma
>   ampliação da propriedade. A definição canônica permanece: Vantagem em testes de **FOR** para
>   arrombar, ou seja **Arrombamento** apenas. A §3.1 já foi corrigida.
> - **"Sete" × oito.** São **oito** as perícias que preenchem buracos preexistentes. O "sete" do
>   cabeçalho da proposta era erro de contagem da Queen; a tabela de oito estava certa.
 Pendências — os `[A CALIBRAR]` criados aqui

1. **Todas as faixas de CD de §2**, para as 18 perícias. **Exceção:** as CDs de fabricação já são
   canônicas (**8 a 16**, `docs/gdd/GDD_Modificacoes.md` §5.1) e não são recalibradas por este documento.
2. Efeito de **`20` e `1` natural** em teste de perícia, se houver (§1).
3. **Forma da interação entre Furtividade e Nível de Ruído** — Desvantagem, penalidade numérica ou
   falha automática dentro do raio (§3.4 e §6.2).
4. **CD para encontrar cada componente**, por escassez e por tipo de local (§3.8).
5. **Qual perícia o Mestre pede em receitas mistas** de Mecânica e Eletrônica, e se pede as duas em
   sequência (§4.2).
6. Se **notar alvo escondido durante o turno** é livre, parte do Movimento ou custa a Ação (§6.1).
7. Se **escapar de Agarrado** custa a Ação (§6).
8. **Teto de perícias adquiridas por Especialização Menor**, se houver, e se ela pode conceder perícia
   já presente na lista da própria classe (§5.3).
9. **Teste de Pilotagem em combate**, bloqueado pela ausência do módulo de Veículos (§3.7).
10. Se **Percepção** altera de algum modo o raio automático de **Atração** (§6.2).
11. **Regra de empate em teste oposto** de perícias (§1).
12. Se a banda **Infectado** da Trilha impõe **Desvantagem em Persuasão**, ou permanece custo puramente
    social como `docs/gdd/GDD_Infeccao.md` §3 declara (§2.17).
13. Se **Intimidação** pode aplicar a condição **Amedrontado** (§2.18).
14. Se sucesso em **Acrobacia** reduz dano de queda — depende de uma tabela de queda que o canon não
    tem (§2.3).
15. Se a **busca por componentes** consome tempo de cena, de descanso ou de downtime (§3.8).

**Herdados — este documento apenas passa a apontar, não resolve:** CD de detectar emboscada
(`docs/gdd/GDD_Combate.md` §2.2) · CD de estabilizar aliado (§8.5) · CD de estancar **Sangrando** (§10) ·
modificador por cobertura e terreno na ação Esconder (§4) · progressão do bônus de proficiência
(§1.1) · quantidades e tempos de remoção de Infecção (`docs/gdd/GDD_Infeccao.md`, "Remoção") · taxa de aparição
de **Liga Pré-Queda** em saque (`docs/gdd/GDD_Modificacoes.md` §4.1) · resultado de falha **não-crítica** no
teste de fabricação (`docs/gdd/GDD_Modificacoes.md` §9.2) · tempo de fabricação por via (idem).

### 8.1. Divergências no canon — relatadas, não corrigidas

Na convenção de `docs/gdd/GDD_Glossario.md` §6, este documento **não escolhe lado**.

1. **Sete ou oito.** CANON 021 §1 intitula a lista **"Sete delas preenchem buracos que já existiam"**
   e em seguida tabela **oito** perícias: Mecânica, Eletrônica, Medicina, Furtividade, Percepção,
   Arrombamento, Pilotagem e Sobrevivência. §3 reproduz as oito, que é o que a tabela declara.
2. **Utilitária dá Vantagem em quê.** `docs/gdd/GDD_Armas.md` §3 e o verbete de `docs/gdd/GDD_Glossario.md` §3 fecham a
   propriedade como **"Vantagem em testes de FOR para arrombar"**. CANON 021 §1 a estende a **duas**
   perícias: **Arrombamento** (FOR — compatível) **e Mecânica** (INT — **incompatível** com a
   redação "testes de FOR"). Ou a propriedade foi ampliada sem reemissão, ou a linha de Mecânica
   descreve outra coisa. **Decisão do Diretor.**
3. **As 18 perícias ainda não estão no glossário.** `docs/gdd/GDD_Glossario.md` §4 lista **"perícias"** entre
   as palavras **disponíveis**, com instrução explícita de que quem as batizar primeiro **registre
   ali, no mesmo ato**. Os 18 nomes precisam de verbete. Dois termos novos aparecem sem verbete
   algum: **Saber Pré-Queda** (perícia) e **Soro de Campo** (citado em CANON 021 §1 e em §2.11 deste
   documento).
4. **Colisões de nome que as perícias criam ou agravam:**
   - **"Estabilizar"** ganha um **quarto contexto** — a colisão 5 do glossário declara três sentidos
     vivos, e Medicina passa a ser a perícia que opera o sentido (b). Nada foi renomeado.
   - **"Vigor"** é palavra nova e não colide hoje, mas fica **a uma linha de colidir** com o teste de
     resistência de CON toda vez que alguém escrever "teste de vigor" em minúscula — exatamente o
     erro que produziu a colisão de *furtividade* em `docs/gdd/GDD_Combate.md` §4.
   - **"Mecânica"** convive com o componente **Peças Mecânicas** e com a família de arma **Projéteis
     Mecânicos**; **"Percepção"** convive com o atributo **PER**. Nenhuma das três é colisão de
     regra, mas todas são candidatas a confusão de busca.
5. **Especialização: listas fechadas ou abertas.** `docs/gdd/GDD_Glossario.md` §3 afirma que **"todas as listas
   e pré-requisitos de nível são `[A CALIBRAR]`"**, enquanto CANON 021 §2 fixa os níveis
   (3, 5, 7, 9, 11, 13, 15, 17), os quatro portes com mínimos (Menor 3, Média 7, Maior 13, Assinatura
   17) e as três regras de contenção. O glossário está defasado em relação ao CANON 021.
6. **Médico: perícia de Medicina × assinatura Estabilizar.** `docs/gdd/GDD_Glossario.md` §3 registra que os
   números da assinatura — quantidade removida, custo em ação, frequência — são `[A CALIBRAR]`.
   Enquanto isso não fechar, **não é possível saber se a perícia Medicina e a assinatura se sobrepõem
   no tratamento de Infecção**, ou se são caminhos distintos. Registrado, não resolvido.
7. **Piloto: a única classe cuja porta suave depende de um módulo inexistente.** Cientista e
   Construtor têm pilares com regra escrita; o Piloto tem **Pilotagem** e um módulo de Veículos que
   não existe, mais a assinatura **Modificação Veicular** bloqueada. Não é contradição, mas é
   **assimetria declarada** entre as três portas suaves.

---

*Este documento é canônico quanto à estrutura (CANON 021 §1). Qualquer alteração na lista de 18
perícias, nas listas por classe ou nos testes de resistência exige nova aprovação do Diretor de
Criação. Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*
