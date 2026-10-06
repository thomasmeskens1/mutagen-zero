# MUTAGEN:ZERO — Classe: PILOTO

> **Escopo.** Define o **nível 1** do Piloto conforme o canon (Aprovação 016). Não redefine subsistema: turno em
> `docs/gdd/GDD_Combate.md` §2.4 · catálogo em `docs/gdd/GDD_Armas.md` · motor em `docs/gdd/GDD_Ruido.md` §1 · Horda e Infecção
> em `docs/gdd/GDD_Horda.md` e `docs/gdd/GDD_Infeccao.md`.
>
> **AVISO DE DEPENDÊNCIA.** O **módulo de Veículos NÃO EXISTE**: não há catálogo, estatísticas, nem regras de
> condução, combustível, dano estrutural ou perseguição. A §4 é **estrutura, não regra** — tudo que dependeria dele
> está `[A CALIBRAR]`, e **nada foi inventado para preenchê-lo**.

## 1. Identidade

O Piloto é quem entende que o mundo não acabou — apenas ficou grande outra vez. Antes, cem quilômetros eram uma
hora; agora são quatro dias a pé, dois rios sem ponte e uma cidade que ninguém atravessa. Ele é quem ainda comprime
distância, e o grupo o trata com uma mistura de dependência e desconfiança: sem ele não se vai longe, e com ele se
vai longe demais. Não é mecânico de oficina limpa — é o que dorme embaixo do chassi porque é o único lugar com
sombra, o que conhece cada motor pelo som antes de pela marca. Na cintura, uma pistola, porque arma comprida não
cabe atrás de um volante; no cinto, um pé de cabra que abre porta, capô e crânio, nessa ordem de frequência.

E ele é o único dos oito que carrega uma ameaça que não é dele. Motor faz barulho. Muito barulho. Quando o Piloto
liga o que passou dois dias consertando, o som atravessa o mapa e toda coisa morta que ainda anda vira a cabeça. Ele
é **d8 e limiar 15**, a resistência média do jogo; o que tem de excepcional não está no corpo, está estacionado.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d8** — nunca muda, qualquer que seja a Especialização |
| **HP no nível 1** | **8 + mod. de CON** (máximo do dado) — com CON +2, **10 HP** |
| **HP por nível após o 1º** | `[A CALIBRAR]` |
| **Limiar de Infecção** | **15** — exatamente a **base** canônica; resistência média |
| **Proficiência (famílias de arma)** | **Pistolas**, **Contundentes** |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Perícias / resistências com proficiência** | `[A CALIBRAR]` |
| **Habilidade-assinatura** | **Modificação Veicular** + **reparo sob pressão** |

### Bandas de Infecção calculadas para o limiar 15

`1/3 = 5` · `2/3 = 10`. Como o limiar dele **é** a base, as bandas coincidem com o exemplo canônico, sem arredondamento e sem ambiguidade.

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 | **0–5** | Saudável | Nenhum |
| 1/3 a 2/3 | **6–10** | Infectado | Custo **social**, sem penalidade mecânica |
| 2/3 ao limiar | **11–14** | Infectado grave | **Desvantagem** em testes de CON contra Infecção |
| no limiar | **15** | Mutação ou morte | Fim da linha |

Ritmo canônico no limiar 15: marreta em **8 lutas**, pistola em **11**, faca em **5**. O Piloto é o **caso de referência** do sistema: qualquer conta feita sobre a base 15 vale para ele sem correção.

## 3. Habilidade-assinatura

A assinatura tem **duas metades** e só uma é utilizável hoje: a metade **Modificação Veicular** está em §4, e
**nenhuma regra numérica pode ser escrita** sem o módulo de Veículos. **Reparo sob pressão — custo: a Ação inteira.**
No combate, o Piloto repara um sistema mecânico avariado (veículo, gerador, portão, bomba), restaurando a **função**
em vez de consertar a peça.

1. **Custa a Ação, sempre.** Ele **não** recebe uso novo da **Ação Bônus**: o escopo dela segue fechado em
   "Destravar arma de fogo" (§2.4), e nem esta habilidade nem Especialização dela derivada pode abri-lo.
2. **Não é `Usar Objeto` com outro nome** — este já cobre ativar dispositivo e arrombar. Esta é a **Ação de
   reparo**, e só o Piloto a executa sem penalidade; **qualquer personagem faz reparo grosseiro** pela porta suave.
3. **Uma rolagem decide** (§1.1): `d20 + modificador + proficiência` contra uma CD. **Atributo (INT é o candidato
   óbvio), CD e faixas: `[A CALIBRAR]`**, assim como o que **"sem penalidade"** significa (ausência de Desvantagem,
   CD reduzida ou dispensa de ferramenta). Paralelo: a Gambiarra custa `+1` na faixa de quebra, a Oficina não custa.
4. **Usos por descanso: `[A CALIBRAR]`** — a do Cientista é explícita (`1× por descanso longo`), a do Piloto não foi
   fixada e **não deve ser presumida ilimitada**. **Falha crítica** no `1` natural: `[A CALIBRAR]`; o precedente é
   material perdido e queda de um degrau de conservação.

**Exemplo numérico** (só economia do turno e Medidor, então **não depende** do módulo de Veículos). Um reparo de **3
Ações** bem-sucedidas (ilustrativo, `[A CALIBRAR]`) com um motor ligado ao lado, **motor pesado = `Alto` = 6
pts/rodada**, acumula **6 → 12 → 18** e cruza os **20** do limiar na 4ª rodada, com **24**. **Três rodadas de reparo =
3 turnos sem atacar e 18 dos 20 pontos consumidos:** o reparo termina e a leva chega quase junto. Com o motor
**desligado** e o grupo em silêncio, as mesmas 3 rodadas valem **0**. **Ligar o motor antes de terminar o reparo é a
decisão tática central da classe** — tomada **às cegas**, porque o Medidor é invisível ao jogador.

## 4. A porta suave — Veículos

**O Piloto é o dono da terceira porta suave canônica** (`CANON_CLASSES.md` §2): **qualquer personagem dirige,
abastece e faz reparo grosseiro; só o Piloto faz modificação veicular.** Como as outras duas, ela **não tranca o
pilar** — define o tier bom. **Um grupo sem Piloto continua tendo carro:** dirige, abastece, amarra o radiador com
arame e segue. O que não tem é a **modificação**.

### Estrutura da Modificação Veicular — `[A CALIBRAR]`

**Esta subseção existe para que o desenho futuro não seja reinventado, não para ser jogada.** O módulo de Veículos **ainda não foi desenhado**; **nada abaixo é regra.**

| Campo da estrutura | Observação |
|---|---|
| Catálogo de veículos e estatísticas | **Módulo de Veículos — não existe** |
| **Slots de modificação** por veículo, se houver | Paralelo: arma comum 2 slots, especializada 3 |
| Lista de modificações veiculares e seus efeitos | **Nenhuma foi aprovada** |
| Eixo **Gambiarra × Oficina**, componentes e receitas | Candidatos: a assimetria de `CANON_CLASSES.md` §2 e os oito componentes de `docs/gdd/GDD_Modificacoes.md` |
| Teste, atributo, CD, tempo, local, falha crítica | Bancada, Refúgio ou campo — não definido |
| **Nível de Ruído de cada veículo** | **Mas a cláusula de motor já o restringe** — ver §5.1 |
| Plataforma de tiro, cobertura, atropelamento, dano estrutural, combustível | Nada aprovado. Não modelar |

> **Contenção para implementadores.** Até o módulo existir, o motor **não deve** expor modificação veicular como
> funcionalidade. Jogável hoje: o **reparo sob pressão**, as proficiências, o d8 e o limiar 15. Preencher qualquer célula
> acima com palpite invalida a calibragem futura de dois subsistemas — Horda e combustível.

## 5. Como ela interage com os subsistemas

### 5.1. Ruído e Medidor de Horda — a cláusula de motor manda

Isto **já é canon** e não espera pelo módulo. A **cláusula de motor** (`docs/gdd/GDD_Ruido.md` §1, Aprovação 012) **sobrepõe a
precedência de tipo de dano**, inclusive em corpo a corpo: tensão mecânica = **Silencioso (0)** · pneumático ou motor
leve = **Baixo a Médio (1 a 3)** · **motor pesado = Alto (6)** · mecanismo Explosivo = **Alto (6)**. Qual veículo é leve
e qual é pesado é `[A CALIBRAR]`, mas o **mapeamento já está fechado** — o módulo só escolherá dentro dessa escala.
**O pilar do Piloto é, portanto, fonte de Ruído de primeira grandeza:** motor pesado ligado = **6 pontos por
rodada**, o mesmo que um rifle, **sem ninguém ter atirado**, o que dá **uma leva a cada ~4 rodadas**, indefinidamente,
porque o Medidor só zera **no fim da cena**. E a **Atração** é automática num raio de **50 hex (75 m)**.

**A ferramenta de trabalho dele também tem motor.** **Utilitárias** lhe dá a **Rebarbadora**: 1d10 Cortante, **Ruído
ALTO**, FOR mínima **12**, Duas mãos, Pesada, Lenta, bateria de 4 rodadas — corpo a corpo e Alto, pela cláusula de
motor. O Piloto é a única classe cujo arsenal **branco** alimenta a Horda a 6 pontos por rodada. A alternativa
silenciosa na mesma proficiência é o **Pé de cabra** (1d8 Concussão, **Baixo**, 1 ponto); a **Pá de Trincheira
Afiada** (1d8 Cortante, **Silencioso**) serve se o Diretor confirmar que cai em Utilitárias: `[A CALIBRAR]`.

### 5.2. Pistolas — a via do meio, e a única em que o silenciador chega ao piso

Pistolas são **Ruído Médio: 3 pontos por rodada**. Via canônica medida: **3,0 levas em 6 lutas** e **mutação em 11
lutas** — o meio exato entre o Explorador (0 levas, mutação em 5) e o Atirador de Elite (5,8 levas, mutação em 14),
coerente com um limiar que é a própria base. E **Médio (3) − 1 degrau = Baixo (1)**, o **piso** de arma de fogo: um
silenciador basta para levar a pistola dele ao mínimo, o que **não** acontece com o rifle do Atirador de Elite, que
precisa de silenciador **e** Subsônica. Em números: pistola nua cruza os 20 do limiar em **7 rodadas** (21 pontos);
silenciada, em **20**. O silenciador dura **30 disparos**, ocupa o slot, e a pistola pesada gasta **4,23
tiros/alvo** — ~7 alvos, quase **2 lutas**. **Com o motor ligado, nada disso importa**: o Medidor conta só o ruído
mais alto da rodada, e o motor vence a pistola.

### 5.3. Trilha de Infecção

Nenhum ajuste: **limiar 15, a base** — ele é o benchmark. **Reparo sob pressão consome a Ação**, ou seja **rodadas sem
atacar** dentro do alcance de mordida: cada acerto necrótico vale **1 ponto**, crítico **2**, e a Trilha conta
**acertos, não dano** — reparar sob fogo é comprar Infecção com tempo de turno. E **ele não tem defesa reativa
própria**: a Reação só faz ataque de oportunidade (§4.1), e quem precisa reparar **e** se proteger gasta rodadas em
**Esquivar**, que **é** a Ação, logo não repara. É assim que a classe deve se sentir sob pressão.

### 5.4. Modificações de arma e munição

**Sem acesso especial a Modificações de arma:** a porta suave dele é Veículos, não Oficina. Em arma usa **Gambiarra**
com o `+1` na faixa de quebra, e **quebra e travamento nunca se somam** (§7.3). **Pistola trava:** `1` natural →
travamento, e destravar custa **1 Ação Bônus** — **o único uso aprovado dela**, que o Piloto usa de verdade, ao
contrário do Explorador. Faixas: Calibrada ~0,5% · Boa 5% · Desgastada 10% · Arruinada 15%, e **munição de Gambiarra soma
`+1`** à faixa. **Munição:** pistola leve usa o pool **Leve**, pistola pesada usa **Pesado** — ele **não** disputa o
calibre **Rifle** com o Atirador de Elite, virtude real de composição de grupo. **Combustível não é munição:** pool e
consumo são `[A CALIBRAR]`, e **não** se modela como sétimo pool. O **teto de `1d12` é absoluto**.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **mobilidade e máquina** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **8 + mod CON** | **15** | Classe, assinatura, proficiências | — |
| **2** | +2 | +5 + mod CON | 15 | **Reparo Rápido** — reparo sob pressão custa **metade** do tempo | — |
| **3** | +2 | +5 + mod CON | 15 | — | **Especialização** |
| **4** | +2 | +5 + mod CON | 15 | **Aumento de atributo** | — |
| **5** | +3 | +5 + mod CON | **16** | — | **Especialização** |
| **6** | +3 | +5 + mod CON | 16 | **Modificação Veicular II** — segundo slot veicular | — |
| **7** | +3 | +5 + mod CON | 16 | — | **Especialização** |
| **8** | +3 | +5 + mod CON | 16 | **Aumento de atributo** | — |
| **9** | +4 | +5 + mod CON | **17** | — | **Especialização** |
| **10** | +4 | +5 + mod CON | 17 | **Motorista de Fuga** — o grupo inteiro embarca num veículo com **uma única Ação** | — |
| **11** | +4 | +5 + mod CON | 17 | — | **Especialização** |
| **12** | +4 | +5 + mod CON | 17 | **Aumento de atributo** | — |
| **13** | +5 | +5 + mod CON | **18** | — | **Especialização** |
| **14** | +5 | +5 + mod CON | 18 | **Conhece a Máquina** — **Vantagem** contra alvos mecânicos e com cibernética | — |
| **15** | +5 | +5 + mod CON | 18 | — | **Especialização** |
| **16** | +5 | +5 + mod CON | 18 | **Aumento de atributo** | — |
| **17** | +6 | +5 + mod CON | **19** | — | **Especialização** |
| **18** | +6 | +5 + mod CON | 19 | **Modificação Veicular III** — terceiro slot; o veículo ganha resistência | — |
| **19** | +6 | +5 + mod CON | 19 | **Aumento de atributo** | — |
| **20** | +6 | +5 + mod CON | 19 | **ÁPICE — **Aríete Rodante** — o veículo atravessa hexágonos ocupados por mutantes causando dano; e **o Medidor de Horda zera** quando o grupo sai da cena em veículo** | — |

**HP total no nível 20:** 103 + (20 × mod CON). Com CON +3, isso dá **163 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 15 para **19** ao fim da carreira.
> O crescimento é pequeno de propósito, porque a Trilha **não é vitalícia**: ela mede a carga
> infecciosa **atual**, e descanso longo em Refúgio com Enfermaria remove pontos `[A CALIBRAR]`.
> Sem isso, como a Trilha conta **acerto e não dano**, qualquer personagem mutaria antes do nível 10.

> **Especializações** vêm dos níveis 3, 5, 7, 9, 11, 13, 15 e 17, e cada uma exige uma **fonte
> diegética**: um mentor NPC, um manual saqueado, ou prática em campo validada pelo Mestre. O **dado
> de vida nunca muda**, qualquer que seja a especialização adquirida.

## 7. Especializações

> **CORRIGIDO (Aprovações 021 e 022) — esta seção NÃO é mais espaço de desenho.**
>
> O catálogo de Especializações está **fechado e aprovado** em `docs/gdd/GDD_Especializacoes.md`: **8 aquisições
> na carreira inteira**, nos níveis **3 · 5 · 7 · 9 · 11 · 13 · 15 · 17**, em **quatro portes**
> (Menor nv 3 · Média nv 7 · Maior nv 13 · **Assinatura nv 17**, uma única oportunidade), sob **três
> regras de contenção**: cota de **2 por classe de origem**, pré-requisito que lê **proficiência de
> família de arma**, e **Recursos de nível 18 e Ápices não são adquiríveis por ninguém**. Contagem
> vigente: Menor **41** · Média **10** · Maior **16** · Assinatura **15** = **82 adquiríveis**, mais
> **16 inadquiríveis**.
>
> A frase *"a lista e os pré-requisitos de nível são `[A CALIBRAR]`"* que esta seção trazia era
> **defasagem deste documento**, não abertura de canon. O que segue continua valendo como **leitura de
> afinidade** — o que combina com esta classe e por quê —, mas **os níveis mínimos que valem são os do
> catálogo**, não os desta página. Onde os dois discordarem, prevalece `docs/gdd/GDD_Especializacoes.md`.

### O que o Piloto oferece a outras classes

| Especialização | Conteúdo | Nível mínimo |
|---|---|---|
| **Modificação Veicular** (assinatura) | **BLOQUEADA** até o módulo de Veículos existir | Alto — `[A CALIBRAR]` |
| **Reparo sob pressão** | A Ação de §3 | `[A CALIBRAR]` |
| Proficiência em **Pistolas** / em **Utilitárias** | `[A CALIBRAR]` | `[A CALIBRAR]` |

> **Aviso de balanceamento.** **Modificação Veicular não pode ser oferecida como Especialização antes do módulo
> existir** — ceder habilidade de efeito indefinido é ceder cheque em branco. Até lá, a assinatura do Piloto é a
> única das oito **indisponível** no mercado de Especializações, e isso deve estar visível na tabela do jogador. Já
> **Utilitárias** merece atenção: entrega a **Rebarbadora** (Ruído **ALTO**) e a **Pá de Trincheira Afiada** (1d8 em
> uma mão, **Silencioso**), e num Ceifador ou Explorador a Pá é um upgrade barato: `[A CALIBRAR]`.

### O que combina com o Piloto

| Origem | Por quê |
|---|---|
| **Construtor** — *Mão Calejada* | A melhor sinergia do jogo para ele. Parte do arsenal Utilitário é **Improvisada** (Martelo), e Improvisada **não soma proficiência**. Mão Calejada devolve o bônus, e a proficiência dele passa a valer o que parece valer. |
| **Explorador** — *Esquiva Reflexa* | Resolve o problema estrutural de §5.3: protege-se pela **Reação** e mantém a **Ação** livre para o reparo. A compra mais funcional da classe. |
| **Cientista** — *Oficina de Campo* | Silenciador em campo **sem** o `+1` de quebra. Leva a pistola de Médio a **Baixo**, o piso, em um degrau. |
| **Atirador de Elite** — armas de fogo | Tira a limitação de alcance das pistolas (10–12 hex normal). Custo: passa de **Médio (3)** para **Alto (6)** por rodada e vira, somado ao motor, a pior combinação de Ruído possível. |

> **A evitar:** especializações que exijam ficar parado. **Mirar** e **Tiro Calculado** só funcionam se o personagem
> **não se moveu nenhum metro no turno** (§4); um Piloto desenhado em torno de estar em movimento não extrai valor delas, e o d8 não compensa a exposição de ficar imóvel.

*Nível 1 conforme `CANON_CLASSES.md` (Aprovação 016). A metade **Modificação Veicular** está bloqueada por dependência de módulo. Alterar dado, limiar, proficiências, a assinatura ou o escopo da Ação Bônus exige nova aprovação do Diretor.*
