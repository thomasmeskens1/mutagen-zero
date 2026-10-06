# MUTAGEN:ZERO — Classe: CEIFADOR

> **Escopo.** Define o **nível 1** do Ceifador conforme o canon (Aprovação 016 + **CANON 017**, que prevalece). Não redefine subsistema: Infecção em `docs/gdd/GDD_Infeccao.md` · Ruído em `docs/gdd/GDD_Ruido.md` · Horda em `docs/gdd/GDD_Horda.md` · turno, Reação e oportunidade em `docs/gdd/GDD_Combate.md` §2.4/§4.1/§11.5 · propriedades, tiers e parâmetros de DPR em `docs/gdd/GDD_Armas.md` §1.2/§3/§4/§8.1. Valor não fixado pelo canon = `[A CALIBRAR]`.
> **Nome:** em português a forma acompanha o personagem — **Ceifador** ou **Ceifadora**, escolha do jogador.

## 1. Identidade

O Ceifador é quem resolve no silêncio. Não é o mais forte da mesa e não é o que aguenta mais pancada — é o que entendeu que barulho é convite, e que cada tiro que o grupo não dá é uma leva de errantes que não chega. Segura a lâmina como quem segura ferramenta, não como quem segura arma; corta e já está olhando o próximo, porque o primeiro ainda está caindo e tempo de queda é tempo que existe. Não grita, não avisa, não comemora. Quando ele atravessa um corredor, o que se ouve é pano e respiração.

E é por isso mesmo que ele apanha. Ele é a **única classe do jogo que mata em corpo a corpo sem alimentar o Medidor de Horda** — o Pugilista, de punho, faz ruído **Baixo** e soma **1 ponto por rodada**. Mas o preço da via silenciosa está medido e é cruel: quem não faz barulho briga por mais rodadas, e cada rodada extra é mais um golpe necrótico entrando na Trilha. O limiar dele é **14**, um ponto abaixo da base. A assinatura existe para comprar de volta essa exposição, e é só isso que a torna jogável. Um Ceifador que erra o ritmo não morre de mordida: apodrece.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d8** — nunca muda, qualquer que seja a Especialização |
| **HP no nível 1** | **8 + mod. de CON** (máximo do dado) — com CON +2, **10 HP** |
| **HP por nível após o 1º** | `[A CALIBRAR]` |
| **Limiar de Infecção** | **14** — um ponto abaixo da base **15** |
| **Proficiência (famílias de arma)** | **Lâminas Curtas**, **Lâminas Longas** |
| **Perícias / resistências com proficiência** | `[A CALIBRAR]` |
| **Habilidade-assinatura** | **Corte Contínuo** |

> **Proficiência é por FAMÍLIA, nunca por tipo de dano nem por propriedade** (`CANON_017` §2). As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. **Lâminas Curtas:** faca, facão, machadinha, garrafa quebrada, antena de carro, seringa de pressão. **Lâminas Longas:** **katana**, machado de bombeiro, foice de ceifar, pá de sapador, machado corta-anteparo. *(A katana migrou de Curtas para Longas na Aprovação 024 — a taxonomia da Aprovação 018 é por **tamanho da lâmina**, e uma katana é uma lâmina longa. O Ceifador tem proficiência nas duas famílias, então nada muda para ele na ficha.)* *Ágil, Leve, Pesada, Flexível, Arremessável* e *Frágil* são **propriedades**, e nenhuma delas é família.

### Bandas de Infecção calculadas para o limiar 14

Frações do limiar pessoal, **truncadas para baixo** (`docs/gdd/GDD_Infeccao.md` §3): `1/3 = 4` · `2/3 = 9`.

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 | **0–4** | Saudável | Nenhum |
| 1/3 a 2/3 | **5–9** | Infectado | Custo **social**, sem penalidade mecânica |
| 2/3 ao limiar | **10–13** | Infectado grave | **Desvantagem** em testes de CON contra Infecção |
| no limiar | **14** | Mutação ou morte | Fim da linha |

## 3. Habilidade-assinatura — Corte Contínuo

**Ao reduzir um alvo a 0 HP com uma arma Cortante, você pode imediatamente mover 1 hexágono e fazer outro ataque contra um alvo diferente. Uma vez por turno.**

1. **Exige arma Cortante, e Cortante é o tipo de dano da rolagem — não a família.** Facão, machadinha, foice de ceifar, machado de bombeiro e katana disparam. **Corrente c/ Gancho** e **Forcado**, Perfurantes, **não** disparam, mesmo com proficiência. A **Pá de Sapador** tem **Dupla Face** (`docs/gdd/GDD_Armas.md` §7.1): só dispara se o ataque foi declarado **Cortante** — e nesse caso o Ruído também segue Cortante.
2. **1× por turno, teto duro.** Se o ataque extra também reduzir um alvo a 0 HP, **não** dispara de novo. Não há cadeia.
3. **Não é Ação, não é Reação e NÃO É AÇÃO BÔNUS.** É um ataque extra concedido pela assinatura dentro do próprio turno. O escopo da Ação Bônus segue **fechado em "Destravar arma de fogo"** (`docs/gdd/GDD_Combate.md` §2.4) e o Ceifador **não** recebe uso novo dela.
4. **O gatilho é "reduzir a 0 HP", não "matar".** Dano excedente é irrelevante e alvo que já estava a 0 não conta. O alvo do ataque extra tem de ser **diferente**.
5. **O 1 hexágono é movimento, e movimento tem consequência.** Sair do alcance corpo a corpo de outro inimigo visível sem Desengajar **provoca ataque de oportunidade** (§11.5); mover de um hex adjacente para outro hex adjacente ao mesmo inimigo **não** provoca. Se esse hexágono é descontado do orçamento de 9 m / 6 hex ou concedido à parte: `[A CALIBRAR]`.
6. **Resolve-se imediatamente**, antes de qualquer outra criatura agir. Crítico no ataque extra **dobra os dados**, não o modificador (§6.2). Combina com **Mirar**, que custa a Ação inteira: o ataque extra, se vier, é **normal**. Interação com **Lenta** (Foice de Ceifar), **Espalhamento** e **Linha**: `[A CALIBRAR]`.

**Exemplo numérico de uma rodada.** Parâmetros canônicos de DPR (`docs/gdd/GDD_Armas.md` §1.2): ataque **+5**, mod. de dano **+3**, Defesa do alvo **14**, HP do alvo **12**. Katana em duas mãos = **1d10**.

```
P(acerto) = (21 − (14 − 5)) / 20 = 60%   ·   Dano médio no acerto = 5,5 + 3 = 8,5
DPR = 0,60 × 8,5 + 0,05 × 5,5 = 5,375   (canon: 5,38)
```

| Passo | O que acontece |
|---|---|
| Ação Atacar em **A** (5 HP restantes) | Rola 14 → acerto. `1d10+3` = 9 de dano → **A a 0 HP** |
| **Corte Contínuo** dispara | Move **1 hex** para ficar adjacente a **B** e ataca **B** (12 HP) |
| Ataque extra em **B** | 60% de acerto, 8,5 de dano médio → **B a ~3,5 HP** |
| Sem a assinatura | **B** terminaria a rodada **intacto**, com 12 HP em pé |

**O valor esperado do gatilho é um DPR inteiro: 5,375.** A **2,04 gatilhos por luta** (katana em duas mãos, tabela abaixo), são **~11 de dano extra por luta** — um zumbi comum inteiro. Valor derivado dos números canônicos, não é número novo.

### A simulação que fixou o número

**4 zumbis de 12 HP, Defesa 14, grupo de 4, mod. de dano +3** (`CANON_017` §1):

| Configuração | Rodadas | Efeito | Gatilhos por luta |
|---|---|---|---|
| Katana 1 mão, sem Corte | 3,85 | — | — |
| Katana 1 mão, com Corte | 3,30 | **−14%** | 2,21 |
| Katana 2 mãos, sem Corte | 3,45 | — | — |
| Katana 2 mãos, com Corte | **2,94** | **−15%** | 2,04 |
| Contra horda de 8, com Corte | 5,46 | **−16%** | 4,27 |

**A assinatura escala com a densidade de alvos.** Contra 4 inimigos corta 15% das rodadas; contra 8, corta 16% e dispara **4,27** vezes. É a única classe cuja habilidade **melhora** quando a leva de errantes chega — e a leva chega por barulho que não foi ele que fez.

## 4. A porta suave

**O Ceifador NÃO tem uma porta suave.** As três são canônicas e fechadas (`CANON_CLASSES.md` §2): Modificações de arma = **Cientista**, Refúgio = **Construtor**, Veículos = **Piloto**. Ele não destrava pilar nenhum, e **nada de furtividade, execução silenciosa ou remoção de corpos foi aprovado como pilar com porta suave.** Qualquer personagem se move com cautela e ataca em corpo a corpo pelas regras gerais; o silêncio dele vem da **arma**, que qualquer um pode empunhar, e a vantagem dele é **converter esse silêncio em rodadas a menos**. Um quarto pilar (Furtividade / Execução) seria proposta nova do Diretor, não leitura deste documento: até lá, `[A CALIBRAR]` e **por padrão inexistente**.

> **Rebarbadora e Serra "Denteira" NÃO são Lâminas Longas** (Aprovação 018). São ferramentas
> **motorizadas** e pertencem à família **Dispositivos**. A mudança existe para proteger o nicho desta
> classe: as duas são Cortantes, mas a **cláusula de motor sobrepõe a precedência** e as coloca em
> Ruído **Médio** e **Alto**. Deixá-las em Lâminas Longas daria ao Ceifador, por proficiência, duas
> armas que destroem o silêncio que o define — e ambas dispararíam Corte Contínuo.

## 5. Como ela interage com os subsistemas

### 5.1. Trilha de Infecção — o núcleo do design

A Trilha conta **acertos, não dano**: golpe necrótico que acerta = **1 ponto**, crítico necrótico = **2** (`docs/gdd/GDD_Infeccao.md` §1). Corte Contínuo não reduz dano e não impõe Desvantagem a ninguém — ele **encurta a luta**, e como a exposição é proporcional ao número de rodadas em contato, **menos rodadas é menos Trilha**. Katana em duas mãos: **3,45 → 2,94 rodadas**, **−15%**. **Encurtar a luta em 15% significa ~15% menos Infecção.**

É isso que sustenta a afirmação canônica: o limiar dele é **14**, abaixo da base **15**, mas **na prática se comporta como 16**, porque a assinatura compra de volta a exposição que o silêncio custa. A conta por trás: `14 ÷ 0,85 ≈ 16,5`, e o canon arredonda para **16**. O valor exato da equivalência é `[A CALIBRAR]`.

> **A diferença entre ele e o Explorador é a natureza do desconto.** O Explorador paga **3 pontos de teto** de uma vez, para sempre, e recupera ~1 por luta **desde que a Reação esteja livre** — compensação condicional. O Ceifador paga **1 ponto de teto** e recupera **~15% de toda a exposição** sem gastar recurso de turno nenhum: a assinatura não compete com Reação, Ação nem Ação Bônus. A economia dele é **estrutural e recorrente**, e é por isso que 14 aguenta o que 12 não aguentaria. Ritmo canônico: via silenciosa na base leva à mutação em **5 lutas**; no limiar 14, com a assinatura ativa, `[A CALIBRAR]`.

Fim de combate como todos: teste de **CON, CD 10 + pontos ganhos naquele combate**, sucesso remove **metade**. Menos rodadas = menos pontos = **CD mais baixa**: a assinatura reduz a exposição **e** a dificuldade de limpar o que entrou.

### 5.2. Ruído e Medidor de Horda — o nicho, e é aqui que ele é único

Pela precedência canônica (`docs/gdd/GDD_Ruido.md` §1, `docs/gdd/GDD_Armas.md` §8.1), **PESADA vence CONCUSSÃO, que vence CORTANTE / PERFURANTE / LEVE**. Logo: **Cortante não-Pesado é Silencioso (0)** e **Concussão é Baixo (1)**.

| Classe / arma | Tipo | Ruído | Pts no Medidor por rodada | Levas em 6 lutas |
|---|---|---|---|---|
| **Ceifador** — katana, facão, foice | **Cortante** | **Silencioso (0)** | **0** | **0** |
| **Pugilista** — punho `1d6` | Concussão | **Baixo (1)** | **1** | 0,4 *(via Baixo)* |

**Ele é a única classe do jogo que mata em corpo a corpo sem alimentar o Medidor de Horda.** Não é o dano que o define — o DPR da katana em duas mãos (**5,375**) fica abaixo da marreta (**6,025**). O que o define é o **zero**.

1. **Duas mãos NÃO o torna Pesado.** A katana tem **Flexível**, não **Pesada**. A precedência só sobe para Baixo "se é Pesada"; Flexível apenas sobe **um degrau na escada de dados**, teto **1d12 absoluto**. Katana em duas mãos continua **Silenciosa**. Precedente canônico explícito: *"uma foice de duas mãos é Silenciosa; uma marreta é Baixo."*
2. **A família Lâminas Longas NÃO é silenciosa.** O silêncio é propriedade do **golpe**, não da família. O **Machado de Bombeiro** é Cortante e **Pesada** → **Baixo**; a **Rebarbadora** é Cortante e de motor pesado → **ALTO** pela cláusula de motor, que sobrepõe a precedência. Ambos **disparam Corte Contínuo**, porque são Cortantes. É a tensão central do arsenal dele: **a família que entrega mais dado é a que cobra o silêncio.**
3. **Ele não zera o Medidor do grupo.** O Medidor soma **o ruído mais alto do grupo por rodada** (`docs/gdd/GDD_Horda.md` §1): se o Atirador de Elite dispara na mesma rodada, ela vale **6** e o silêncio dele não conta. Limiar **20 pontos**, em escada, zerando no **fim da cena** — fugir de sala não limpa o rastro. O Medidor é **exclusivo do Mestre**.

### 5.3. A Katana — arma nova, tier Militar

| Arma | Dado | Tipo | Ruído | FOR mín. | Propriedades | DPR |
|---|---|---|---|---|---|---|
| **Katana** | 1d8 | Cortante | **Silencioso** | — | **Ágil**, **Flexível** (2 mãos: **1d10**) | **4,72** / **5,38** |

**Tier Militar, não Comum:** uma espada de verdade num mundo de sucata não se acha numa garagem. Família **Lâminas Curtas**. **Ágil** permite usar **AGI** no ataque e no dano (`docs/gdd/GDD_Armas.md` §3) — o Ceifador não precisa de FOR, o que a separa de todo o resto do corpo a corpo de dado alto, que é Pesado e exige FOR 12–16.

**A decisão de empunhadura é a arma.** Uma mão: `1d8`, DPR **4,72**, mão livre para escudo, item ou a interação livre. Duas mãos: `1d10`, DPR **5,38**, e as rodadas caem de 3,45 para **2,94** com a assinatura — mas nada na outra mão. O canon mediu as duas e as duas são jogáveis: a de duas mãos corta 15% da luta, a de uma mão corta 14%. Tier Militar é **confiável e sem efeito exótico**: a katana não tem **Frágil**, e **corpo a corpo nunca trava** (§7.3).

### 5.4. Modificações e munição

Sem acesso especial: **Gambiarra** com `+1` na faixa de quebra, como todos; a via **Oficina** exige bancada em Refúgio, e **a bancada é que destrava, não a classe** (`CANON_017` §4). Como o arsenal dele é de tier **Militar** e **Comum** e não carrega **Frágil**, ele é o corpo a corpo que **menos** sofre com a penalidade de quebra da Gambiarra.

**Sem nenhuma proficiência em arma de fogo, ele nunca usa a Ação Bônus de Destravar com arma própria.** O slot fica vazio, isso é aceitável, e **não** justifica abri-lo. Munição: ele não consome pool nenhum — nem os quatro calibres, nem Projéteis, nem Exótica (`docs/gdd/GDD_Combate.md` §13.1). É a classe mais barata de sustentar em campo e a mais caríssima de sustentar em corpo.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **matar em silêncio** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **8 + mod CON** | **14** | Classe, assinatura, proficiências | — |
| **2** | +2 | +5 + mod CON | 14 | **Golpe Limpo** — mutante abatido por arma **Cortante não gera pontos de Infecção** | — |
| **3** | +2 | +5 + mod CON | 14 | — | **Especialização** |
| **4** | +2 | +5 + mod CON | 14 | **Aumento de atributo** | — |
| **5** | +3 | +5 + mod CON | **15** | — | **Especialização** |
| **6** | +3 | +5 + mod CON | 15 | **Corte Contínuo II** — **duas vezes** por turno | — |
| **7** | +3 | +5 + mod CON | 15 | — | **Especialização** |
| **8** | +3 | +5 + mod CON | 15 | **Aumento de atributo** | — |
| **9** | +4 | +5 + mod CON | **16** | — | **Especialização** |
| **10** | +4 | +5 + mod CON | 16 | **Lâmina Afiada** — armas Cortantes suas ignoram **2 pontos de resistência** | — |
| **11** | +4 | +5 + mod CON | 16 | — | **Especialização** |
| **12** | +4 | +5 + mod CON | 16 | **Aumento de atributo** | — |
| **13** | +5 | +5 + mod CON | **17** | — | **Especialização** |
| **14** | +5 | +5 + mod CON | 17 | **Dança** — ao mover-se entre dois inimigos, ataca um **de graça**, 1× por turno | — |
| **15** | +5 | +5 + mod CON | 17 | — | **Especialização** |
| **16** | +5 | +5 + mod CON | 17 | **Aumento de atributo** | — |
| **17** | +6 | +5 + mod CON | **18** | — | **Especialização** |
| **18** | +6 | +5 + mod CON | 18 | **Corte Contínuo III** — **sem limite** por turno, cada gatilho exigindo um alvo diferente | — |
| **19** | +6 | +5 + mod CON | 18 | **Aumento de atributo** | — |
| **20** | +6 | +5 + mod CON | 18 | **ÁPICE — **Ceifa** — 1× por combate, você ataca **todos os inimigos adjacentes** com uma única rolagem** | — |

**HP total no nível 20:** 103 + (20 × mod CON). Com CON +3, isso dá **163 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 14 para **18** ao fim da carreira.
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

### O que o Ceifador oferece a outras classes

| Especialização | Conteúdo | Nível mínimo |
|---|---|---|
| **Corte Contínuo** (assinatura) | A habilidade de §3, integral | Alto — `[A CALIBRAR]` |
| Proficiência em **Lâminas Curtas** | `[A CALIBRAR]` | `[A CALIBRAR]` |
| Proficiência em **Lâminas Longas** | `[A CALIBRAR]` | `[A CALIBRAR]` |
| Leitura de posicionamento e desengajamento | `[A CALIBRAR]` | `[A CALIBRAR]` |

> **Aviso de balanceamento.** Corte Contínuo é a assinatura mais fácil de exportar do jogo: **não custa recurso de turno**, não pede Reação e funciona com qualquer arma Cortante. Num **d10** com limiar **16–17** — Construtor, Pugilista — entrega a compressão de rodadas **sem** o limiar 14 que a justifica aqui, e num **Machado de Bombeiro** entrega isso com `1d10`. O nível mínimo é o único dial que impede a combinação, e **não deve ser barato**. Nota: o Pugilista puro não a aproveita — punho é **Concussão**, nunca Cortante.

### O que combina com o Ceifador

| Origem | Por quê |
|---|---|
| **Médico** — *Estabilizar* | Remove pontos da Trilha de aliado adjacente: a contramedida direta da única moeda que ele gasta. |
| **Explorador** — *Esquiva Reflexa* | Mesma via Silenciosa. Ele encurta a luta, ela reduz a frequência de acerto dentro dela: atacam a Trilha por vias diferentes e **não** se sobrepõem. |
| **Cientista** — *Oficina de Campo* | Modificação de qualidade Oficina sem bancada: melhora a lâmina sem o `+1` de quebra, em campo. |
| **Construtor** — *Mão Calejada* | Faz a arma Cortante de sucata valer proficiência quando a katana se perde — e a garrafa quebrada é Silenciosa. |

> **A evitar:** qualquer proficiência de **arma de fogo**. Não melhora nada do que ele faz e destrói o único perfil em que ele é único no jogo: um tiro numa rodada põe **3 ou 6 pontos** no Medidor e apaga o zero. **Rebarbadora** é o caso extremo dentro da própria proficiência dele — Cortante, dispara a assinatura, e **ALTO** por motor pesado: ele passa a pagar Horda **e** Infecção na mesma rodada.

*Nível 1 conforme `CANON_017` sobre `CANON_CLASSES.md` (Aprovação 016). Alterar dado, limiar, famílias de proficiência ou a assinatura exige nova aprovação do Diretor.*
