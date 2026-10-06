# MUTAGEN:ZERO — Classe: CONSTRUTOR

> **Canon.** Nível 1 fechado por `CANON_CLASSES.md` (Aprovação 016): dado de vida **d10**, limiar de Infecção **16**, proficiências
> **Improvisadas e Utilitárias**, assinatura **Mão Calejada**. O que não estiver lá aparece como `[A CALIBRAR]`.
> **Não duplicado aqui:** `docs/gdd/GDD_Combate.md` §2, §5–§6 · `docs/gdd/GDD_Armas.md` §1.2 e §3 (fórmula de DPR; propriedades
> **Improvisada**, **Utilitária**, **Frágil**, **Pesada**) · `docs/gdd/GDD_Modificacoes.md` · `docs/gdd/GDD_Infeccao.md` ·
> `docs/gdd/GDD_Ruido.md` · `docs/gdd/GDD_Horda.md`.

## 1. Identidade

O Construtor é quem olha um ferro-velho e vê uma parede. Antes do Colapso podia ser pedreiro, soldador, estivador, montador de
andaime — a profissão exata quase nunca importa, porque o que sobreviveu foi o jeito de olhar: peso, ponto de apoio, onde a coisa
cede, onde ela aguenta. Enquanto o resto do grupo aprende a atirar e a fugir, ele aprendeu que o mundo virou uma pilha de material,
e que material é a única riqueza que ainda funciona. Não é o inventor da mesa: é o sujeito que sabe que uma porta reforçada vale
mais que um carregador cheio, porque a porta segura a noite inteira e o carregador segura três rodadas.

É o mais sujo dos oito. Óleo entranhado nas cutículas, tetânico crônico, mãos onde o calo já não distingue onde termina a pele e começa a ferramenta — daí o nome da assinatura. Ele briga com o que estava na mão quando a coisa entrou pela janela: o pé de cabra, o
cano de descarga, a tampa de bueiro, a bateria de carro com garras improvisadas. Não tem uma arma; tem proximidade constante de objetos pesados, e transformou isso em ofício.

O horror dele é lento e profissional. É quem fica no Refúgio depois da incursão medindo se a solda aguenta, e quem entende primeiro que **nada aguenta para sempre** — o serviço dele não é vencer, é comprar semanas. Todo Construtor carrega a mesma neurose: conhece, pessoalmente, cada ponto fraco do lugar onde as pessoas que confiam nele estão dormindo.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d10** — nunca muda, qualquer que seja a Especialização adquirida |
| **HP no nível 1** | **10 + mod. de CON** (12 com CON +2) — máximo do dado, por regra canônica |
| **HP por nível após o 1º** | `[A CALIBRAR]` |
| **Limiar de Infecção** | **16** — uma acima da base 15 |
| **Proficiência (famílias de arma)** | **Contundentes**, **Hastes** |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Perícias e resistências com proficiência** | `[A CALIBRAR]` |
| **Bônus de proficiência no nível 1** | **+2** (progressão até +6 `[A CALIBRAR]`) |

**Bandas de Infecção calculadas para o limiar 16** — frações do limiar pessoal (`docs/gdd/GDD_Infeccao.md` §3):

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 (5,33) | **0–5** | Saudável | Nenhum |
| 1/3 a 2/3 (10,67) | **6–10** | Infectado | Custo **social**: NPCs reagem. Sem penalidade mecânica |
| 2/3 até o limiar | **11–15** | Infectado grave | **Desvantagem** nos testes de CON contra Infecção |
| no limiar | **16** | Mutação ou morte | Critério entre as duas: `[A CALIBRAR]` |

> **Arredondamento:** trunca-se para baixo porque reproduz o exemplo canônico do limiar 15 (0–5 · 6–10 · 11–14 · 15) — formalizar é
> `[A CALIBRAR]`. Com 16, as duas primeiras bandas ficam **idênticas** às da base: o ponto extra aparece todo no fim da faixa grave.
> **Lutas até a mutação com limiar 16:** `[A CALIBRAR]` (o canon mede 12 → 6, 15 → 8 e 18 → 9 pela marreta).

## 3. Habilidade-assinatura: MÃO CALEJADA

**Enunciado canônico:** armas com a propriedade **Improvisada** somam o bônus de proficiência normalmente.

É a assinatura mais econômica das oito porque **não introduz nenhuma mecânica nova**. A propriedade Improvisada, em `docs/gdd/GDD_Armas.md` §3, diz exatamente uma coisa: *"não soma o bônus de proficiência ao ataque"*. Mão Calejada é a **anulação literal dessa cláusula, e nada
mais** — sem recurso novo, sem trilha nova, sem gasto de turno novo: uma exceção de uma linha a uma regra que já existia, cujo resultado é a única classe do jogo que sabe usar lixo como arma.

1. No **bônus efetivo de ataque** (`docs/gdd/GDD_Armas.md` §1.2), a subtração da proficiência por Improvisada **não se aplica** a este
   personagem: onde a regra geral faz `bônus de ataque − proficiência`, ele usa o bônus cheio.
2. O efeito é **só no ataque**. Não altera dado de dano, tipo de dano, Nível de Ruído, **Frágil**, **Lenta**, a FOR mínima de armas
   **Pesadas**, nem o `+1` na faixa de quebra que cada modificação Gambiarra acrescenta.
3. **Nenhum uso novo de Ação Bônus.** É passiva e permanente: não consome Ação, Reação, Ação Bônus nem a interação livre. O escopo
   da Ação Bônus permanece fechado em "Destravar arma de fogo".
4. Improvisadas não são armas de fogo: **não travam**. Podem **quebrar** (Frágil e/ou Gambiarra), e quebra e travamento são
   contadores distintos que nunca se somam (`docs/gdd/GDD_Combate.md` §7.3). Em Improvisadas com **Arremessável**, o atributo do ataque à
   distância segue `[A CALIBRAR]` e a anulação vale qualquer que seja ele. **Teto de dado 1d12:** a assinatura nunca toca o dado.

**Exemplo numérico.** Parâmetros canônicos de aferição (`docs/gdd/GDD_Armas.md` §1.2): ataque **+5**, proficiência **+2**, dano **+3**,
Defesa **14**, HP do alvo **12**. Arma: **Improvisada 1d4** (cano, tijolo), tier Improviso.

```
QUALQUER PERSONAGEM                      CONSTRUTOR (Mão Calejada)
bônus efetivo = 5 - 2 = 3                bônus efetivo = 5
P(acerto) = (21-(14-3))/20 = 50%         P(acerto) = (21-(14-5))/20 = 60%
DPR = 0,50 x (2,5+3) + 0,05 x 2,5        DPR = 0,60 x (2,5+3) + 0,05 x 2,5
    = 2,75 + 0,125 = 2,88                    = 3,30 + 0,125 = 3,42
```

**2,88 nas mãos de qualquer um; 3,42 nas dele** — **+19%**, vindos inteiramente de 10 pontos percentuais de chance de acerto. Derivando a mesma fórmula para o resto do arsenal (coluna "qualquer um" conferida contra o catálogo de `docs/gdd/GDD_Armas.md` §4):

| Arma Improvisada | Dado | Ruído | Qualquer um | Construtor | Equivale a |
|---|---|---|---|---|---|
| Cano / tijolo, Martelo | 1d4 Concussão | Baixo | 2,875 | **3,425** | — |
| Garrafa Quebrada *(Frágil)* | 1d4 Cortante | **Silencioso** | 2,875 | **3,425** | — |
| Tampa de Bueiro *(Pesada, FOR 14)* | 1d6 Concussão | Baixo | 3,425 | **4,075** | Cacetete (Comum) |
| Corrente c/ Gancho *(Lenta, 2 hex)* | 1d6 Perfurante | **Silencioso** | 3,425 | **4,075** | Cacetete (Comum) |
| Cano c/ Arame Farpado *(Gambiarra)* | 1d8 Concussão | Baixo | 3,975 | **4,725** | Taco de Baseball (Comum) |

Em uma frase: **Mão Calejada promove o tier Improviso a tier Civil sem tocar em nenhum dado** — é o que torna a classe jogável num mundo em que arma de verdade é o recurso mais escasso do inventário.

## 4. A porta suave

| Pilar | Qualquer personagem pode | Só o Construtor |
|---|---|---|
| **Refúgio / Base** | **Reparo e construção básica** | **Melhorias estruturais** |

**Qualquer personagem** tapa um buraco, escora uma porta, remenda um telhado, reconstrói o que havia e voltou a ceder: o Refúgio **não depende** do Construtor para continuar existindo. **Só o Construtor** faz **melhoria estrutural** — transformar o Refúgio em algo
que ele não era. Catálogo, custos em componentes, tempos e efeitos mecânicos pertencem ao **módulo de Refúgio, que ainda não foi
desenhado**: `[A CALIBRAR]`. Regra operacional até então: **reparo devolve ao estado anterior; melhoria cria estado novo.**

Atenção ao que **não** é porta dele: **Modificações de arma** é do Cientista (qualquer um faz Gambiarra com `+1` na faixa de quebra; o Cientista faz Oficina sem penalidade) e **Veículos** é do Piloto. Ele é o tier bom de **um** pilar, não de três.

## 5. Interação com os subsistemas

### 5.1. Trilha de Infecção — e a saída geométrica

Limiar **16**: uma tolerância acima da base, com as duas primeiras bandas iguais às de um personagem base. É coerente com o papel — ele **luta corpo a corpo**, logo fica na faixa de 1 hex onde o dano **Necrótico** acontece (**1 ponto por golpe acertado, 2 no
crítico**), mas não é o para-choque contratado do grupo. **A saída que a assinatura abre é geométrica, não de resistência:** dois itens do próprio arsenal Improvisado têm **Alcance 2 hex**, que por `docs/gdd/GDD_Armas.md` §3 permite atacar **sem ficar adjacente ao alvo**.

| Arma | Perfil com Mão Calejada | Por que importa |
|---|---|---|
| **Corrente c/ Gancho** | 1d6 Perfurante · **Silencioso (0)** · 2 hex · DPR **4,075** | Ataca fora do alcance das garras: **0 ponto de Infecção** na rodada em que o mutante não alcança ninguém e **0 ponto** no Medidor. Preço: **Lenta** (perde a Reação após atacar, logo sem ataque de oportunidade) e **Duas mãos** |
| **Antena de Carro** | 1d4 Cortante · **Silencioso (0)** · 2 hex · DPR **3,425** | Mesma geometria com metade do porte, mas **Frágil**: quebra em qualquer `1` natural |

É o ponto de design mais forte da classe: **é a única que consegue, dentro da própria proficiência, atacar em Silencioso, fora do alcance corpo a corpo e com DPR de tier Civil.** Não escapa das duas moedas por resistir melhor a elas — escapa por não entrar no hexágono onde são cobradas, e paga isso com a Reação e com fragilidade.

### 5.2. Ruído e Horda — o único que escolhe a moeda arma por arma

A proficiência dele atravessa dois níveis de Ruído, porque as Improvisadas se dividem entre tipos de dano (`docs/gdd/GDD_Ruido.md` §1,
precedência **Pesada > Concussão > Cortante/Perfurante/Leve**):

| Escolha dentro da proficiência | Nível | Raio de Atração | Pts/rodada no Medidor |
|---|---|---|---|
| Garrafa, Antena, Corrente c/ Gancho *(Cortante/Perfurante, não Pesadas)* | **Silencioso (0)** | nenhum | **0** |
| Cano, tijolo, Martelo, Cano c/ Arame Farpado *(Concussão)* | **Baixo (1)** | **4 hex (6 m)** | **1** |
| Tampa de Bueiro, Extintor, Bateria c/ Garras *(Pesadas)* | **Baixo (1)** | **4 hex (6 m)** | **1** |

Ele é **a única classe cuja lista de proficiências contém as duas pontas da escolha** — o Pugilista está travado em Baixo, o Explorador e o Médico nas pontas silenciosas. O Construtor decide, ao pegar a arma, **qual das duas moedas de atrito vai gastar naquela
cena**, e nenhuma é a segura: o canon mediu que a via silenciosa é a mais infecciosa. Em números: um grupo em via silenciosa gera **0 leva em 6 lutas**; com o Construtor de cano na mão passa a somar **1 ponto por rodada** e, ao vigésimo ponto **na mesma cena** (o
Medidor só zera no **fim da cena**), chega a leva de **2 errantes**.

### 5.3. Modificações

- **Sinergia central:** a Gambiarra é a modificação de campo aberta a qualquer um e cobra **`+1` na faixa de quebra**. O arsenal
  Improvisado é o alvo natural dela, e Mão Calejada é o que faz o resultado valer a pena: **Cano c/ Arame Farpado** sai de **3,975**
  para **4,725** de DPR, igualando um Taco de Baseball de tier Civil — com uma arma feita de lixo.
- **Mão Calejada não paga esse custo:** mexe **só** no ataque, o `+1` de quebra permanece e **Frágil** permanece. Uma Garrafa
  Quebrada modificada em Gambiarra, na mão dele, acerta melhor **e** se parte mais fácil.
- **Ele não é o especialista de Modificações** — o tier bom é do **Cientista** (Oficina sem penalidade, `Oficina de Campo` 1× por
  descanso longo). Ele tem a mesma Gambiarra que todos; o que tem de diferente é o **melhor uso do produto dela**. E **Utilitária**,
  na segunda proficiência, dá **Vantagem em testes de FOR para arrombar**: na ficha dele, arma e ferramenta são o mesmo objeto.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **lixo vira equipamento** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **10 + mod CON** | **16** | Classe, assinatura, proficiências | — |
| **2** | +2 | +6 + mod CON | 16 | **Improviso Rápido** — fabrica uma arma Improvisada num **descanso curto**, sem custo | — |
| **3** | +2 | +6 + mod CON | 16 | — | **Especialização** |
| **4** | +2 | +6 + mod CON | 16 | **Aumento de atributo** | — |
| **5** | +3 | +6 + mod CON | **17** | — | **Especialização** |
| **6** | +3 | +6 + mod CON | 17 | **Mão Calejada II** — armas Improvisadas perdem a propriedade **Frágil** nas suas mãos | — |
| **7** | +3 | +6 + mod CON | 17 | — | **Especialização** |
| **8** | +3 | +6 + mod CON | 17 | **Aumento de atributo** | — |
| **9** | +4 | +6 + mod CON | **18** | — | **Especialização** |
| **10** | +4 | +6 + mod CON | 18 | **Erguer Depressa** — melhoria estrutural do Refúgio custa **metade** do material | — |
| **11** | +4 | +6 + mod CON | 18 | — | **Especialização** |
| **12** | +4 | +6 + mod CON | 18 | **Aumento de atributo** | — |
| **13** | +5 | +6 + mod CON | **19** | — | **Especialização** |
| **14** | +5 | +6 + mod CON | 19 | **Ponto Fraco** — contra estrutura ou objeto, seus ataques causam **dano dobrado** | — |
| **15** | +5 | +6 + mod CON | 19 | — | **Especialização** |
| **16** | +5 | +6 + mod CON | 19 | **Aumento de atributo** | — |
| **17** | +6 | +6 + mod CON | **20** | — | **Especialização** |
| **18** | +6 | +6 + mod CON | 20 | **Arsenal de Sucata** — suas armas Improvisadas sobem **um degrau** na escada de dados | — |
| **19** | +6 | +6 + mod CON | 20 | **Aumento de atributo** | — |
| **20** | +6 | +6 + mod CON | 20 | **ÁPICE — **O Refúgio é Meu** — o Refúgio ganha um nível de fortificação além do que o material permitiria; e o **Medidor de Horda sobe 1 ponto a menos por rodada** enquanto o grupo estiver dentro dele** | — |

**HP total no nível 20:** 124 + (20 × mod CON). Com CON +3, isso dá **184 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 16 para **20** ao fim da carreira.
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

| O que o Construtor oferece | Conteúdo | Pré-requisito |
|---|---|---|
| **Mão Calejada** (assinatura) | Improvisadas somam o bônus de proficiência | `[A CALIBRAR]` — canon: a assinatura é a especialização **mais cara**, só em nível alto |
| **Melhorias estruturais de Refúgio** | O lado especialista da porta suave | `[A CALIBRAR]` (depende do módulo de Refúgio) |
| Especializações menores | `[A CALIBRAR]` | `[A CALIBRAR]` |

**Quem mais quer Mão Calejada:** qualquer classe cuja proficiência **não** cubra Improvisadas e que se veja sem equipamento em campo
— o que, no pós-apocalipse, é todo mundo. Ela não dá uma arma nova: dá **permissão de usar o que já está no chão**.

**O que combina bem com ele** (níveis mínimos valem os de `docs/gdd/GDD_Especializacoes.md`):

| Origem | Por que combina |
|---|---|
| **Cientista** — *Oficina de Campo* | As duas metades da economia de material: o Cientista faz a modificação boa, o Construtor extrai DPR de tier Civil do resultado. Juntas fecham o ciclo componente → arma → Refúgio |
| **Médico** — *Estabilizar*, limiar 18 | Ele fica no corpo a corpo e acumula Infecção; é o contrapeso direto do único recurso permanente que a classe gasta |
| **Explorador** — *Esquiva Reflexa* | Cuidado: a Corrente c/ Gancho é **Lenta** e consome a Reação após atacar. Só vale nas armas não-Lentas (Garrafa, Antena, cano, Martelo) |
| **Piloto** — *Modificação Veicular* | Proficiência compartilhada em Utilitárias e a mesma lógica de ofício: o grupo passa a ter Refúgio **e** veículo em tier bom |

**O que não combina.** *Tiro Calculado* (Atirador de Elite) exige arma de fogo e a Ação **Mirar** inteira, e nenhuma proficiência do
Construtor é de fogo — Mão Calejada não faz nada por arma de fogo. *Combate Desarmado* (Pugilista) é redundante: o punho é 1d6
Concussão, Baixo, DPR 4,075, o mesmo perfil que a Tampa de Bueiro já dá a ele, e ele nunca fica sem objeto na mão.

> A oitava classe do canon não é tratada nesta seção: seu nome ainda não foi decidido pelo Diretor.

*Nível 1 conforme `CANON_CLASSES.md` (Aprovação 016). Todo campo `[A CALIBRAR]` aguarda o próximo ciclo de proposta e aprovação de
balanceamento; alterações no nível 1 exigem nova aprovação do Diretor de Criação.*
