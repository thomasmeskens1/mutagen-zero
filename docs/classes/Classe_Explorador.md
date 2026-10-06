# MUTAGEN:ZERO — Classe: EXPLORADOR

> **Escopo.** Define o **nível 1** do Explorador conforme o canon (Aprovação 016). Não redefine subsistema:
> Infecção em `docs/gdd/GDD_Infeccao.md` · Ruído em `docs/gdd/GDD_Ruido.md` · Horda em `docs/gdd/GDD_Horda.md` · Reação e
> turno em `docs/gdd/GDD_Combate.md` §2.4/§4.1 · propriedades em `docs/gdd/GDD_Armas.md` §3. Valor não fixado pelo canon
> = `[A CALIBRAR]`.

## 1. Identidade

O Explorador é quem sai. Não por coragem — porque alguém tem que ir ver se a estrada ainda existe, se o poço não
secou, se aquela fumaça a três quilômetros é fogueira ou é incêndio de gordura humana. Ele conhece o mapa que
ninguém mais tem, e conhece porque andou nele com os pés. O grupo o manda na frente e finge que isso é
confiança; ele sabe que é logística — é mais barato perder um batedor do que perder o refúgio. Não é o mais
forte nem o mais preciso: é o que vira o corpo meio passo antes do braço chegar. Tudo que carrega pesa pouco e
faz pouco barulho: faca, arco, virote recuperado do cadáver de ontem, um caderno que vale mais que a arma.
Pólvora ele troca por comida; flecha ele recolhe — do mesmo corpo que ela matou, ajoelhado ao lado dele, à
distância de mordida.

E é aí que a conta dele fecha errado. O Explorador é o corpo que menos aguenta Infecção das oito classes —
limiar **12**, três pontos abaixo da base. O organismo dele é rápido, não é resistente. Ele vive a poucos metros
de coisas que apodrecem e depende de nunca ser tocado, porque uma sequência ruim de dois combates o coloca na
banda em que os testes falham em cascata. Não existe Explorador velho. Existe Explorador que parou de sair.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d8** — nunca muda, qualquer que seja a Especialização |
| **HP no nível 1** | **8 + mod. de CON** (máximo do dado) — com CON +2, **10 HP** |
| **HP por nível após o 1º** | `[A CALIBRAR]` |
| **Limiar de Infecção** | **12** — o **menor das oito classes** |
| **Proficiência (famílias de arma)** | **Lâminas Curtas**, **Projéteis Mecânicos** |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Perícias / resistências com proficiência** | `[A CALIBRAR]` |
| **Habilidade-assinatura** | **Esquiva Reflexa** (Reação) |

### Bandas de Infecção calculadas para o limiar 12

Frações do limiar pessoal (`docs/gdd/GDD_Infeccao.md` §3): `1/3 = 4` · `2/3 = 8`.

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 | **0–4** | Saudável | Nenhum |
| 1/3 a 2/3 | **5–8** | Infectado | Custo **social**, sem penalidade mecânica |
| 2/3 ao limiar | **9–11** | Infectado grave | **Desvantagem** em testes de CON contra Infecção |
| no limiar | **12** | Mutação ou morte | Fim da linha |

> A banda de aviso dele tem **4 pontos** (5–8) contra 5 da base: a margem entre "vejo que estou doente" e "a
> espiral começou" é a mais estreita do jogo. Arredondamento não está no canon; usa-se **piso**, por analogia ao
> limiar 15 (0–5 / 6–10 / 11–14): `[A CALIBRAR]`.

## 3. Habilidade-assinatura — Esquiva Reflexa

**Custo: a Reação.** Quando um ataque é feito contra você e você pode ver o atacante, impõe **Desvantagem** àquela rolagem.

1. **É Reação, não Ação Bônus.** O escopo da Ação Bônus segue fechado em "Destravar arma de fogo" (§2.4). O
   Explorador **não** recebe uso novo dela.
2. **Uma por rodada, de fato.** A Reação é reposta no **início do próprio turno**; quem a gasta logo após o
   próprio turno fica sem ela por quase uma rodada inteira.
3. **Compete diretamente com o ataque de oportunidade** (§4.1) — são o mesmo recurso. Ele não pode punir quem
   recua e se proteger de quem avança no mesmo ciclo: **escolhe um.** Essa disputa é o freio da habilidade e não
   deve ser removida.
4. Declarada após o ataque anunciado, **antes da rolagem**; nunca retroativa. Alcance máximo e uso contra
   atacante que ele não pode ver: `[A CALIBRAR]`.
5. **Não empilha, e cancela** (§1.1): se ele já usou a Ação **Esquivar**, ela **não adiciona nada** — gastar a
   Reação ali é desperdício puro. Se o atacante tem Vantagem (ele **Caído**, **Atordoado**, atacante
   **Escondido**), ela devolve a rolagem a **1d20 normal**, sem gerar Desvantagem.
6. **Não funciona contra o modo Automático** (§7.2): ali não há rolagem de ataque para penalizar.

**Exemplo numérico.** Premissas **ilustrativas** (armaduras `[A CALIBRAR]`, Bestiário não existe): AGI 16 (+3), sem armadura → **Defesa 13**; mutante com ataque **+4**.

| Situação | Precisa | P(acerto) | P(crítico) |
|---|---|---|---|
| Ataque normal | 9+ | **60,0%** | 5,00% |
| Com **Esquiva Reflexa** | 9+ em 2d20 pelo menor | **36,0%** (`0,60²`) | **0,25%** (`0,05²`) |

Luta de 4 rodadas, um ataque por rodada, Reação livre sempre: **2,40 acertos** esperados sem ela,
**1,44** com ela.

## 4. A porta suave

**O Explorador NÃO tem uma porta suave.** As três são canônicas e fechadas (`CANON_CLASSES.md` §2):
Modificações de arma = **Cientista**, Refúgio = **Construtor**, Veículos = **Piloto**. Ele não destrava pilar
nenhum, e **nada de navegação, batida de mapa ou rastreio foi aprovado como pilar com porta suave.** Qualquer
personagem viaja, procura caminho e observa à distância pelas regras gerais. Um quarto pilar (Exploração /
Cartografia) seria proposta nova do Diretor, não leitura deste documento: até lá, `[A CALIBRAR]` e **por padrão
inexistente**.

## 5. Como ela interage com os subsistemas

### 5.1. Trilha de Infecção — o núcleo do design

A Trilha conta **acertos, não dano**: golpe necrótico que acerta = **1 ponto**, crítico = **2**
(`docs/gdd/GDD_Infeccao.md` §1). A Esquiva Reflexa não reduz dano nenhum — reduz a **frequência de acerto**, a moeda
real. Com os números acima, numa luta de 4 rodadas:

| | Acertos | Pontos ganhos | CD do teste de CON (`10 + pontos`) |
|---|---|---|---|
| Sem Esquiva Reflexa | 2,40 | **2,40** | ~12 |
| Com Esquiva Reflexa | 1,44 | **1,44** | ~11 |

**Economia: ~1 ponto por luta e 1 ponto de CD.** O crítico necrótico, que vale 2 pontos, cai de 5% para 0,25%
por ataque — praticamente desaparece. A outra ponta: o limiar **12** contra a base **15** é **3 pontos menos de
tolerância absoluta**, para sempre, sem recurso.

> **Ele paga na tolerância e economiza na exposição, e as duas coisas se cancelam parcialmente — nunca
> integralmente.** Perde 3 pontos de teto de uma só vez e recupera ~1 por luta, **desde que a Reação esteja
> livre**: a compensação só fecha a partir da terceira luta seguida em que ele gastou a Reação em defesa. Na luta
> em que precisou dela para o ataque de oportunidade, em que já estava Esquivando, ou em que apanhou de fogo
> automático, ele é simplesmente **a classe mais frágil do jogo à Infecção**. **Isso é design deliberado, não
> acidente:** a fragilidade é permanente e incondicional; a economia é condicional e recorrente. Ritmo canônico:
> no limiar 12 a via marreta mutaciona em **6 lutas**, contra 8 na base 15. **Via Silenciosa no limiar 12: a
> extrapolação linear das 5 lutas da base daria ~4, mas isso NÃO é canon — `[A CALIBRAR]`.**

### 5.2. Ruído e Medidor de Horda

As duas proficiências dele vivem no **Nível 0 — Silencioso** (`docs/gdd/GDD_Ruido.md` §1 e §4): Ágeis
Cortantes/Perfurantes não Pesadas, arco, besta, dardo. Contribuição ao Medidor: **0 pontos por rodada**; via
Silenciosa, **0 levas em 6 lutas**. E aqui a inversão canônica se vira contra ele: a via mais silenciosa é a
**mais infecciosa** (`docs/gdd/GDD_Ruido.md` §7), porque a briga dura mais e ele apanha mais — e ele tem o menor limiar
para absorver isso. **O Explorador é o pior caso possível da inversão medida.** Duas notas: **ele não zera o
Medidor do grupo** — este soma **o ruído mais alto do grupo por rodada**, e se o Atirador de Elite dispara na
mesma rodada ela vale **6**, anulando o silêncio dele; e **a besta tem `Recarga`**, logo atirar e recarregar não
cabem no mesmo turno e o DPR sustentado dela é **2,3625**, menos que uma faca. Luta longa = mais rodadas de
exposição = mais pontos de Trilha, e é por isso que o **arco**, a 1 ataque por turno e com flecha recuperável, é
a escolha coerente com o limiar 12.

### 5.3. Modificações

Sem acesso especial: **Gambiarra** com `+1` na faixa de quebra, como todos. Pesa mais para ele, porque o arsenal
dele é de tier baixo e já vem cheio de **Frágil** (Garrafa Quebrada, Antena de Carro, Lança Artesanal):
empilhar gambiarra em arma Frágil acumula duas faixas de quebra no mesmo `1` natural.
**Quebra e travamento são contadores distintos e nunca se somam** (§7.3) — e como corpo a corpo **nunca
trava**, para ele só existe o contador de quebra, e ele é o mais exposto a ele. A besta é **arma especializada:
3 slots**. Modificações para Ágeis / tensão mecânica: `[A CALIBRAR]`.

### 5.4. Munição

**O pool `Projéteis`** é o único **recuperável** do jogo (§13.1): a única economia de munição sustentável
indefinidamente fora do Refúgio. **Flecha recuperada perde a melhoria** — volta o projétil, não a carga; regra
de recuperação `[A CALIBRAR]` (`docs/gdd/GDD_Ruido.md` §4). Mas recuperar exige ir até onde o corpo caiu, ou seja
**entrar na faixa de mordida do que ainda não morreu**, a 1 ponto de Trilha por acerto: a economia de munição
dele é paga na moeda em que ele é mais pobre. E, **sem proficiência em arma de fogo**, ele nunca usa a Ação
Bônus de Destravar com arma própria — o slot fica vazio, o que é aceitável e **não** justifica abri-lo.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **não ser acertado, e ver primeiro** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **8 + mod CON** | **12** | Classe, assinatura, proficiências | — |
| **2** | +2 | +5 + mod CON | 12 | **Passo Leve** — mover-se **não gera Ruído nenhum**, nem com a Ação Correr | — |
| **3** | +2 | +5 + mod CON | 12 | — | **Especialização** |
| **4** | +2 | +5 + mod CON | 12 | **Aumento de atributo** | — |
| **5** | +3 | +5 + mod CON | **13** | — | **Especialização** |
| **6** | +3 | +5 + mod CON | 13 | **Esquiva Reflexa II** — impõe **Desvantagem a todos** os ataques contra você até o fim da rodada | — |
| **7** | +3 | +5 + mod CON | 13 | — | **Especialização** |
| **8** | +3 | +5 + mod CON | 13 | **Aumento de atributo** | — |
| **9** | +4 | +5 + mod CON | **14** | — | **Especialização** |
| **10** | +4 | +5 + mod CON | 14 | **Olho Adiantado** — age **sempre primeiro** na iniciativa; emboscada não o afeta | — |
| **11** | +4 | +5 + mod CON | 14 | — | **Especialização** |
| **12** | +4 | +5 + mod CON | 14 | **Aumento de atributo** | — |
| **13** | +5 | +5 + mod CON | **15** | — | **Especialização** |
| **14** | +5 | +5 + mod CON | 15 | **Some** — pode se **Esconder mesmo observado**, 1× por combate | — |
| **15** | +5 | +5 + mod CON | 15 | — | **Especialização** |
| **16** | +5 | +5 + mod CON | 15 | **Aumento de atributo** | — |
| **17** | +6 | +5 + mod CON | **16** | — | **Especialização** |
| **18** | +6 | +5 + mod CON | 16 | **Intocável** — quando um ataque erra você, você **move 1 hex** de graça | — |
| **19** | +6 | +5 + mod CON | 16 | **Aumento de atributo** | — |
| **20** | +6 | +5 + mod CON | 16 | **ÁPICE — **Ninguém Me Vê** — você não pode ser alvo de ataque à distância se estiver a mais de **4 hex** de qualquer inimigo; e **não alimenta o Medidor de Horda de forma alguma**** | — |

**HP total no nível 20:** 103 + (20 × mod CON). Com CON +3, isso dá **163 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 12 para **16** ao fim da carreira.
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

### O que o Explorador oferece a outras classes

| Especialização | Conteúdo | Nível mínimo |
|---|---|---|
| **Esquiva Reflexa** (assinatura) | A habilidade de §3, integral | Alto — `[A CALIBRAR]` |
| Proficiência em **Ágeis** | `[A CALIBRAR]` | `[A CALIBRAR]` |
| Proficiência em **Projéteis** | `[A CALIBRAR]` | `[A CALIBRAR]` |
| Movimentação e terreno difícil | `[A CALIBRAR]` | `[A CALIBRAR]` |

> **Aviso de balanceamento.** Esquiva Reflexa num **d10** com limiar **16–17** entrega a redução de frequência
> de acerto **sem** o custo de tolerância que a justifica aqui. O nível mínimo é o único dial que impede isso, e
> não deve ser barato.

### O que combina com o Explorador

| Origem | Por quê |
|---|---|
| **Médico** — *Estabilizar* | Remove pontos da Trilha de aliado adjacente: a contramedida direta do limiar 12. |
| **Cientista** — *Oficina de Campo* | Modificação **sem** o `+1` de quebra — torna sustentável um arsenal cheio de **Frágil**. |
| **Ceifador** — *Corte Contínuo* | Mesma via Silenciosa, proficiências sobrepostas em Cortantes. Encurtar a luta é a única defesa estrutural contra a Trilha. |
| **Piloto** — proficiência em **Pistolas** | Saída de emergência a 10 hex. Custo real: sai de Ruído 0 para **Médio (3 pts/rodada)** e abandona o único perfil em que não alimenta a Horda. |

> **A evitar:** **Ruído Alto** (calibre Rifle) o põe no pior dos dois mundos — alimenta a Horda **e** carrega o
> menor limiar do jogo. E *Combate Desarmado* combina em ficção mas briga em matemática: o punho é **Concussão**,
> Nível **Baixo**, e o corpo a corpo prolongado é exatamente onde o limiar 12 falha.

*Nível 1 conforme `CANON_CLASSES.md` (Aprovação 016). Alterar dado, limiar, proficiências ou a assinatura exige nova aprovação do Diretor.*
