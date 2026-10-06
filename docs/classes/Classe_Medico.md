# MUTAGEN:ZERO — Classe: MÉDICO

> **O nível 1 é canon** (Aprovação 016, `CANON_CLASSES.md`): dado de vida, limiar de Infecção, proficiências e habilidade-assinatura — nada disso
> muda com especialização. Todo o resto é `[A CALIBRAR]`: **implementadores não inventam valor padrão no motor.** **Não duplicar regras:**
> Infecção em `docs/gdd/GDD_Infeccao.md`; turno, Estado Crítico, grid e condições em `docs/gdd/GDD_Combate.md`; propriedades e catálogo em `docs/gdd/GDD_Armas.md`;
> Gambiarra × Oficina em `docs/gdd/GDD_Modificacoes.md`.

## 1. Identidade

Ele não é médico. Ele **era**. O diploma queimou com o prédio e o conselho que o licenciava deixou de existir junto com o país. Da medicina
sobrou o que dá para carregar nas costas: agulha, fio, pinça hemostática, um garrote que já foi cinto, álcool duvidoso em garrafa de
refrigerante. E a coisa que ninguém consegue saquear — saber **onde** cortar, e saber **quando parar**.

Em MUTAGEN:ZERO a infecção não é ferida que cicatriza: é relógio. O corpo mordido acumula, converte e, no limiar, deixa de ser o corpo de alguém. O
Médico é a única pessoa do grupo que entende o relógio como relógio — que lê a cor do tecido morto na borda da mordida e diz quantas lutas o amigo
ainda tem. É por isso que é ouvido, e é por isso que é odiado: a informação é sempre má, e sempre útil.

Ele trabalha sem assepsia, sem anestesia e sem luz decente: debrida com faca de cozinha, cauteriza com o que estiver quente, mede dose por peso
estimado porque a balança não existe. O que oferece não é cura — é **prorrogação**, e ele sabe que arrancar ponto não é o mesmo que consertar pessoa.
É quem fica acordado depois da luta decidindo em quem vale a pena gastar o pouco que tem.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d8** — CANON, nunca muda, qualquer que seja a especialização |
| **HP no nível 1** | **8 + mod. de CON** (máximo do dado) — CANON. HP por nível 2+: `[A CALIBRAR]` |
| **Limiar de Infecção** | **18** — CANON; **o maior das oito classes** |
| **Proficiência (famílias de arma)** | **Lâminas Curtas**, **Dispositivos**. Perícias e resistências: `[A CALIBRAR]` |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Habilidade-assinatura** | **Estabilizar** (§3) — CANON. **Porta suave: nenhuma** (§4) — CANON |

**Bandas calculadas — limiar 18.** As bandas são frações do limiar pessoal (`docs/gdd/GDD_Infeccao.md` §3):

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 | **0 – 6** | Saudável | Nenhum |
| 1/3 a 2/3 | **7 – 12** | Infectado | Sintomas visíveis; custo **social**, sem penalidade mecânica |
| 2/3 ao limiar | **13 – 17** | Infectado grave | **Desvantagem** nos testes de CON contra Infecção |
| no limiar | **18** | Mutação ou morte | Fim da linha |

Contra a base 15 (`0–5 / 6–10 / 11–14 / 15`), ele ganha **1 ponto de banda Saudável, 2 de aviso e 3 de pista antes da espiral** — mas é **pista de
decolagem, não resolução**: a CD do teste de fim de combate é `10 + pontos ganhos naquele combate` e **não olha o limiar**. Ele não converte menos, só
tem mais espaço antes de o acúmulo doer. (18 é divisível por 3 e as bandas fecham sem arredondamento; isso não vale para todo limiar canônico.)

## 3. Habilidade-assinatura — **Estabilizar**

**Texto canônico:** *remove pontos da Trilha de Infecção de um aliado adjacente.* É tudo o que o canon fixa. A **estrutura** abaixo é proposta de
implementação; os três números que importam ficam abertos de propósito.

| Parâmetro | Valor |
|---|---|
| Alvo e efeito | **um aliado a 1 hexágono (1,5 m)**; remove pontos da **Trilha de Infecção** — CANON (`docs/gdd/GDD_Combate.md` §11.2) |
| **Quantidade removida** | `[A CALIBRAR]` — chamada `N` abaixo |
| **Custo em ação** | `[A CALIBRAR]` — **Ação** ou **Usar Objeto**; **nunca Ação Bônus** (§5.3) |
| **Frequência** | `[A CALIBRAR]` — por combate, por descanso, ou pool de usos |
| Momento de uso, alvejar a si mesmo, componente consumido | `[A CALIBRAR]` em cada caso |

**Precisão de implementação.** (1) Opera sobre a **trilha**, não sobre o dano: não devolve HP, não interage com §8 do Módulo de Combate, não
remove **Sangrando**. (2) Alvo aliado e **adjacente** — entrar em 1 hex contra mutantes é entrar no alcance de quem infectou o aliado; o custo de
posicionamento é embutido e intencional. (3) É **subtração direta** na trilha em ficha, não um teste; **piso zero**, e remoção acima do saldo não
gera crédito. (4) **Ordem contra o teste de fim de combate:** usável durante a luta, reduz os *pontos ganhos naquele combate* e portanto **também
a CD** (`10 + pontos ganhos`) — duas eficiências num uso; usável só depois, tira apenas da trilha acumulada. **Essa ordem é `[A CALIBRAR]` e é a
decisão de balanceamento mais sensível do documento.**

**Exemplo numérico.** Talita (Ceifadora, limiar 14) sai de uma luta com **6 pontos ganhos**. Teste de fim de combate:
`d20 + mod. CON vs. CD 10 + 6 = 16`. Ela falha; os 6 ficam e, somados aos 5 que já carregava, vai a **11** — com limiar 14 a banda **Infectado
grave** começa em 10 (`2/3 de 14`, arredondamento `[A CALIBRAR]`). O Médico Estabiliza:

- `N = 1` → vai a 10 e **continua** na banda grave. A habilidade comprou uma luta.
- `N = 2` → vai a 9, **sai** da banda grave e recupera o teste limpo. Desfez a espiral.
- `N = 4` → vai a 7: a luta ruim inteira **deixou de ter acontecido**. Três jogos diferentes — por isso `N` não pode ser chutado.

> **Não copie o número do item.** O único ponto de comparação canônico é o **Cauterizador "Miséria"**, que remove **2 pontos** (`docs/gdd/GDD_Armas.md`
> §7.3) — mas é **RARIDADE EXTREMA**, custa a **Ação inteira** e causa **1d4 de Fogo irredutível** em quem cauteriza. Aquele `2` foi orçado para um
> item que quase não existe e cobra HP por uso: herdá-lo numa habilidade renovável importa o efeito sem o preço.

## 4. A porta suave — **o Médico não tem**

**Dito explicitamente: o Médico não possui porta suave.** As três portas suaves canônicas são **Modificações** (qualquer um faz Gambiarra; só o
**Cientista** faz Oficina), **Refúgio** (qualquer um repara; só o **Construtor** melhora estruturalmente) e **Veículos** (qualquer um dirige; só
o **Piloto** modifica). Medicina **não é pilar com porta suave** no canon atual — não existe "primeiros socorros de qualquer um × tratamento de
Médico" declarado em lugar nenhum.

Consequência dura: **estabilizar um aliado em Estado Crítico continua aberto a todo mundo** via **Usar Objeto** ou perícia médica, CD `[A CALIBRAR]`
(`docs/gdd/GDD_Combate.md` §8.5) — o Médico **não tranca** o salvamento em combate. O que só ele faz é mexer na **Trilha de Infecção**, e isso não é porta
suave, é **assinatura**, porque não há tier inferior aberto aos outros: as demais vias canônicas de remoção não passam por personagem nenhum, passam
por **item de raridade extrema**, a **Enfermaria do Refúgio** e **descanso longo prolongado**. Transformar medicina em pilar com porta suave é
**decisão nova** e exige aprovação do Diretor.

## 5. Como a classe interage com os subsistemas

### 5.1. Trilha de Infecção — **ALERTA DE CALIBRAGEM**

> ### O Médico pressiona a mesma válvula que a raridade extrema existe para proteger.
>
> O canon já classificou as armas e cargas anti-Infecção como **RARIDADE EXTREMA** (`docs/gdd/GDD_Armas.md` §7.4) e disse por quê, em texto explícito: *é a
> única trava que impede a Trilha de Infecção de ser deflacionada.* A escassez **é** o balanceamento. Mas **Estabilizar é fonte renovável de
> remoção de Infecção**: não depende de saque nem de carga esgotável e não morre quando o item quebra — **volta com o personagem**, luta após luta.
>
> **O risco, nomeado:** se `N`, o custo em ação e a frequência forem generosos, a Trilha deixa de ser **ameaça existencial** e vira **taxa
> administrativa** — um número que o Médico zera no fim da cena. E o efeito não fica contido na Infecção: **o custo do corpo a corpo desaparece do
> jogo.** A Infecção é o preço que o melee paga; se o preço for reembolsável, a **inversão medida** de `docs/gdd/GDD_Ruido.md` — a arma mais silenciosa é a
> mais infecciosa — **deixa de ser uma escolha**, o melee vira dominante por falta de contrapartida, e a Horda fica sendo a única moeda de atrito.
>
> **Este documento não resolve. Sinaliza.** Os três diais são **um único dial conjunto** — remoção por sessão — medido contra o ritmo canônico:
> **marreta chega ao limiar em 8 lutas; rifle, em 14**. A decisão é do Diretor.

Dois efeitos de segunda ordem. **Limiar 18 e Estabilizar se multiplicam:** pista maior *mais* bomba de drenagem é a mesma vantagem duas vezes, e se
ele puder alvejar a si mesmo é o personagem que praticamente não tem Trilha (`[A CALIBRAR]` separado). **E a habilidade recua na espiral, não a
desliga:** a Desvantagem da banda grave é **posicional**, então sair da banda a remove na hora, o que dá a Estabilizar valor **descontínuo** — 1
ponto vale pouco ou vale tudo, dependendo de onde o alvo está. **Calibre por banda, não por ponto.**

### 5.2. Ruído e Horda

Proficiência em **Leves** e **Perfurantes**, e na precedência canônica **Cortante/Perfurante/Leve é o degrau mais baixo**: as armas dele são as
silenciosas, o que o joga no lado errado da inversão — mantém o Medidor de Horda quieto e **paga em Infecção**. É ao mesmo tempo a classe que mais
frequenta a faixa de 1 hexágono (Estabilizar exige adjacência) e a que menos tem como responder a quem está nessa faixa: **o corpo mais exposto à
Infecção do grupo, com a maior tolerância a ela.** Se Estabilizar virar utilizável a distância, essa simetria se rompe.

### 5.3. Economia do turno — escopo fechado

**A Ação Bônus continua fechada em "Destravar arma de fogo"** (`docs/gdd/GDD_Combate.md` §2.4, Aprovação 003). **Estabilizar NÃO é Ação Bônus**, e nada derivado
desta classe concede outro uso: restrição dura. As duas vias legítimas são a **Ação** ou **Usar Objeto** (que *é* a Ação, e cuja descrição canônica já
lista "estabilizar um aliado") — a escolha é `[A CALIBRAR]`. E **não existe ataque extra no MVP**: quem Estabiliza **não ataca naquele turno**, gasta
movimento para chegar a 1 hex e, ao sair de lá, **provoca ataque de oportunidade** sem **Desengajar** — que é, ela também, a Ação inteira.

### 5.4. Estado Crítico — colisão de nomes, resolvida aqui

Há **três** coisas chamadas "estabilizar" no canon e elas não são a mesma: **Estabiliza** (0 HP) é acumular 3 sucessos em testes de morte e parar de
rolar (`docs/gdd/GDD_Combate.md` §8.3); **estabilizar um aliado** é um uso de **Usar Objeto** aberto a qualquer personagem, CD `[A CALIBRAR]` (§4 e §8.5); e
**Estabilizar** com maiúscula é a assinatura desta classe, que **remove pontos da Trilha de Infecção**. **A assinatura não interage com testes de
morte, não concede sucessos e não tira ninguém do Estado Crítico.** Implementadores: **três identificadores distintos no motor.**

### 5.5. Armas e Modificações

d8 e **Leves, Perfurantes** desenham um Médico que não é linha de frente: sem proficiência em **Pesada**, a Marreta (1d12, FOR 15) está fora do
escopo, e o teto **1d12 absoluto** vale igual para todos. Dentro da proficiência dele moram Faca/Facão (1d6 Cortante, Ágil, Leve), Seringa de Pressão
Veterinária (1d4 Perfurante, Leve, Ágil, Frágil, Recarga) e Lança Artesanal (1d8 Perfurante, Alcance 2 hex, Frágil). **A Lança é a leitura correta
da classe:** `Alcance 2 hex` ataca **sem ficar adjacente**, exatamente o oposto do que Estabilizar exige.

O Médico **não tem a via Oficina**; ela é do Cientista (`docs/classes/Classe_Cientista.md`). Ele faz **Gambiarra** como qualquer personagem, ao custo
canônico: **cada modificação Gambiarra soma +1 à faixa de quebra** (`docs/gdd/GDD_Modificacoes.md` §7) — duas gambiarras numa faca são **10% de quebra por
ataque**, e **quebra e travamento nunca se somam** (Aprovação 013). Médico que quer instrumental confiável **precisa do Cientista**.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **manter o grupo de pé** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **8 + mod CON** | **18** | Classe, assinatura, proficiências | — |
| **2** | +2 | +5 + mod CON | 18 | **Mãos Firmes** — estabilizar um aliado em Estado Crítico **não exige teste** | — |
| **3** | +2 | +5 + mod CON | 18 | — | **Especialização** |
| **4** | +2 | +5 + mod CON | 18 | **Aumento de atributo** | — |
| **5** | +3 | +5 + mod CON | **19** | — | **Especialização** |
| **6** | +3 | +5 + mod CON | 19 | **Estabilizar II** — remove mais pontos, e pode ser usado como **Reação** | — |
| **7** | +3 | +5 + mod CON | 19 | — | **Especialização** |
| **8** | +3 | +5 + mod CON | 19 | **Aumento de atributo** | — |
| **9** | +4 | +5 + mod CON | **20** | — | **Especialização** |
| **10** | +4 | +5 + mod CON | 20 | **Diagnóstico** — você vê a Trilha de Infecção de qualquer aliado; o Mestre deve informar a banda | — |
| **11** | +4 | +5 + mod CON | 20 | — | **Especialização** |
| **12** | +4 | +5 + mod CON | 20 | **Aumento de atributo** | — |
| **13** | +5 | +5 + mod CON | **21** | — | **Especialização** |
| **14** | +5 | +5 + mod CON | 21 | **Soro de Campo** — fabrica **um por descanso longo**, consumindo **Química**; remove `N` pontos, **não zera** a Trilha (Aprov. 023) | — |
| **15** | +5 | +5 + mod CON | 21 | — | **Especialização** |
| **16** | +5 | +5 + mod CON | 21 | **Aumento de atributo** | — |
| **17** | +6 | +5 + mod CON | **22** | — | **Especialização** |
| **18** | +6 | +5 + mod CON | 22 | **Estabilizar III** — alcance passa a **3 hex** e afeta **dois** aliados | — |
| **19** | +6 | +5 + mod CON | 22 | **Aumento de atributo** | — |
| **20** | +6 | +5 + mod CON | 22 | **ÁPICE — **Reverter** — **uma vez por campanha**, você reverte uma **mutação já consumada**** | — |

**HP total no nível 20:** 103 + (20 × mod CON). Com CON +3, isso dá **163 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 18 para **22** ao fim da carreira.
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

A **lista** por classe e os **pré-requisitos de nível** estão **fechados** em `docs/gdd/GDD_Especializacoes.md` (Aprovações 021 e 022). O que segue é **leitura de afinidade**, não fonte de níveis. O
Médico é o fornecedor mais caro do sistema: o que tem para vender é o único antídoto renovável de uma moeda de atrito.

| Faixa | Natureza | Pré-requisito | Números |
|---|---|---|---|
| Baixa | leitura diagnóstica — saber saldo e banda de Infecção de um alvo, sem remover | `[A CALIBRAR]` | `[A CALIBRAR]` |
| Média | deslocar o **limiar pessoal** de quem adquire, dentro da faixa canônica `±3` sobre 15 | `[A CALIBRAR]` | `[A CALIBRAR]` |
| **Alta** | **Estabilizar** — a assinatura, "a especialização mais cara, só em nível alto" (canon) | **nível alto**, `[A CALIBRAR]` | `[A CALIBRAR]` |

> **O alerta de §5.1 se repete aqui, multiplicado.** Se Estabilizar vira adquirível, o risco escala com o número de personagens que a compraram: um
> grupo com três Estabilizadores não deflaciona a Trilha, **apaga** a Trilha. As duas travas existentes — gate de nível alto e **fonte diegética** —
> não são numéricas. Considerar um **teto por grupo**, não só por personagem. Decisão do Diretor.

**O que combina.** **Explorador** (limiar 12, **Esquiva Reflexa** de Reação) resolve a fragilidade de chegar a 1 hexágono, e a troca é honesta nos
dois sentidos. **Cientista** (Oficina) transforma instrumental gambiarrado em equipamento que não quebra — é a via Oficina, não uma segunda porta
suave. **Construtor** dá melhorias estruturais, e a **Enfermaria do Refúgio** é via canônica de remoção: industrializar o tratamento pressiona a
válvula de §5.1 **por fora** da habilidade. **Pugilista** (d10, limiar 17, punho 1d6 Concussão Ágil) cobre o corpo a corpo que a proficiência do
Médico não cobre, sem arma que possa quebrar. **O que não combina:** **Tiro Calculado** (Atirador de Elite) exige a Ação **Mirar**, que custa a Ação
inteira e só vale se o personagem **não se moveu** — a antítese de quem precisa se mover até 1 hexágono e provavelmente gastar a Ação.

*Nível 1 é canônico (Aprovação 016). Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento; o alerta de §5.1 é
item de agenda, não decisão tomada.*
