# MUTAGEN:ZERO — Classe: CIENTISTA

> **O nível 1 é canon** (Aprovação 016, `CANON_CLASSES.md`): dado de vida, limiar de Infecção, proficiências e habilidade-assinatura — nada disso muda com
> especialização. Todo o resto é `[A CALIBRAR]`: **implementadores não inventam valor padrão no motor. Não duplicar regras:** Gambiarra × Oficina,
> componentes e as 17 modificações em `docs/gdd/GDD_Modificacoes.md`; turno, travamento e grid em `docs/gdd/GDD_Combate.md`; propriedades e catálogo em `docs/gdd/GDD_Armas.md`;
> Trilha de Infecção em `docs/gdd/GDD_Infeccao.md`.

## 1. Identidade

Ele tem as mãos erradas para este mundo. Mãos de bancada, de pipeta, de parafuso de precisão — mãos que nunca apertaram um pescoço. Antes do Colapso era
alguém com acesso a um prédio com ar-condicionado; hoje é o sujeito que o grupo carrega pelo corredor. Do laboratório sobrou uma bolsa: alicate de bico,
lupa de joalheiro, um multímetro que ainda liga, arame, solda, e um caderno encardido que vale mais que a bolsa inteira.

O caderno é o motivo de ele estar vivo. Todo mundo sabe enrolar arame farpado num cano — isso não é conhecimento, é desespero. O que praticamente ninguém sabe é
**por que** a solda fria racha no terceiro impacto, qual liga aguenta o recuo, quanta folga o ferrolho precisa para não emperrar com poeira. Ele sabe, e por isso
a arma que sai da mão dele não se desfaz na mão de quem a usa.

O Cientista é o único personagem cuja contribuição sobrevive à própria morte: o taco que ele montou continua sendo o melhor taco do grupo depois que ele já era.
Não é bom em ficar vivo — é bom em fabricar as condições para que outros fiquem.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d6** — CANON, o menor do jogo junto com o Atirador de Elite; nunca muda |
| **HP no nível 1** | **6 + mod. de CON** (máximo do dado) — CANON. HP por nível 2+: `[A CALIBRAR]` |
| **Limiar de Infecção** | **15** — CANON; exatamente a **base**, sem deslocamento de classe |
| **Proficiência (famílias de arma)** | **Dispositivos**, **Lâminas Curtas** — a mais estreita das oito. Perícias e resistências: `[A CALIBRAR]` |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Habilidade-assinatura** | **Oficina de Campo** (§3) — CANON. **Porta suave: Oficina** (§4) — CANON |

**Bandas calculadas — limiar 15**, frações do limiar pessoal (`docs/gdd/GDD_Infeccao.md` §3), coincidindo com o exemplo canônico da base:

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 | **0 – 5** | Saudável | Nenhum |
| 1/3 a 2/3 | **6 – 10** | Infectado | Sintomas visíveis; custo **social**, sem penalidade mecânica |
| 2/3 ao limiar | **11 – 14** | Infectado grave | **Desvantagem** nos testes de CON contra Infecção |
| no limiar | **15** | Mutação ou morte | Fim da linha |

**Ele é frágil nos dois eixos, e isso é o desenho.** Com CON `+2` abre com **8 HP** — o piso do jogo, metade do crítico médio de uma marreta (16) — e sem
tolerância extra de Infecção. O Médico compra corpo com limiar 18, o Explorador mobilidade com 12; o Cientista **não compra nada nesse eixo**.

## 3. Habilidade-assinatura — **Oficina de Campo**

**Texto canônico:** *executa uma modificação de Oficina sem bancada, 1× por descanso longo.* A estrutura abaixo é proposta de implementação.

| Parâmetro | Valor |
|---|---|
| Efeito | executa **uma** modificação da via **Oficina** **sem Refúgio e sem bancada** — CANON |
| Frequência | **1× por descanso longo** — CANON. O que *é* um descanso longo: `[A CALIBRAR]`, não definido em documento nenhum |
| **Componentes e Liga Pré-Queda** | **NÃO são dispensados**: a receita de Oficina é cobrada integralmente, e a Liga segue obrigatória e **não-fabricável** (§3.1) |
| Teste de INT; falha crítica consumindo o uso; munição e Munições Especiais; arma de aliado; tempo em campo | `[A CALIBRAR]` em cada caso — e note que o canon diz "modificação", e munição não é modificação (§5.3) |

### 3.1. O que a habilidade dispensa, e o que ela não dispensa

**Oficina de Campo remove exatamente uma coisa: o lugar.** Não é Refúgio portátil e não é atalho de economia. Ela **dispensa a bancada e o Refúgio** — só
isso o texto canônico concede. Ela **NÃO dispensa os componentes**: a coluna "Oficina (Refúgio)" das 17 modificações é cobrada como está, e como a via
Oficina usa **menos unidades de escassez maior**, trocar a bancada pela estrada não converte escassez em nada. E ela **NÃO dispensa a Liga Pré-Queda**, o
**gargalo proposital** do sistema: **não é fabricável por nenhum meio, em nenhum tier, em nenhuma circunstância**, e *quase sempre* aparece nas receitas de
Oficina. Oficina de Campo não gera Liga, não converte Sucata em Liga e não a substitui — se a Liga não está na bolsa, a modificação **não acontece**.
**Consequência de desenho, e é a boa:** a habilidade **não fecha o laço que o canon abriu de propósito**. O grupo continua empurrado para fora do Refúgio, porque
Liga só se encontra saqueando; o Cientista em campo não é um grupo autossuficiente, é um grupo que consegue **gastar em campo o que saqueou em campo**, sem
voltar para casa primeiro. É logística, não independência.

### 3.2. Exemplo numérico — o mesmo taco, dois jogos

`Taco de Baseball` = 1d8 Concussão, Flexível (2 mãos: **1d10**), 2 slots. O grupo quer **Pregos** (+1 degrau, 1 slot) e **Guarda-mão** (+1 de Defesa em corpo a
corpo, não se perde se desarmado, 1 slot). O resultado é idêntico nas duas vias — **1d10 / 1d12 com duas mãos, +1 de Defesa** — e muda uma coluna só:

| Via das duas modificações | Componentes | Faixa de quebra | P(quebra) por ataque |
|---|---|---|---|
| **Gambiarra** (qualquer personagem) | Sucata x2 + (Sucata x2, Peças x1) | **2** | **10%** |
| **Oficina** (Cientista) | (Sucata x1, Peças x1) + (**Liga x1**, Peças x1) | **0** | **0%** |

**Mesma ficha. 10% contra 0%** — uma arma que se parte a cada dez ataques, em média, e **na pior hora possível**. É isto que o Cientista vende. Com **Oficina de
Campo**, em plena estrada: os **Pregos** de Oficina pedem `Sucata x1, Peças x1` e **nenhuma Liga** — saem no primeiro descanso longo, com teste de INT contra
**CD 10**; o **Guarda-mão** pede `Liga x1, Peças x1`, sai no **segundo**, e **só se alguém tiver trazido a Liga de um galpão militar**. Duas noites e um saque
de sorte para um taco que nunca quebra.

## 4.

> **CORRIGIDO pela Aprovação 017 — a bancada é que destrava, não a classe.** Qualquer personagem com
> acesso a um Refúgio com **Oficina instalada** pode fabricar pela via Oficina. A vantagem do
> Cientista passou a ser **dupla e diferente**: ele tem **Vantagem no teste de INT** de fabricação em
> qualquer via, e a **Oficina de Campo** executa trabalho de qualidade Oficina **sem bancada**, 1× por
> descanso longo. Onde este documento disser que "só o Cientista faz Oficina", vale esta nota.
 A porta suave — **Oficina** (e só o Cientista a tem)

> ### Qualquer personagem faz **Gambiarra**. Só o Cientista faz **Oficina**. A diferença **não é de acesso — é de qualidade.**

O canon é explícito em não deixar nenhuma classe trancar um pilar: *"a classe é indispensável para o tier bom, não para o acesso"*. Modificar armas é um pilar,
e **está aberto a todo mundo**: um grupo sem Cientista nenhum monta arsenal inteiro, enche todos os slots, sobe dados, solda lâminas, improvisa silenciador, e
não há uma única modificação que a ausência dele proíba pela via Gambiarra. **Nada trava.** O que muda é o **preço estrutural** (`docs/gdd/GDD_Modificacoes.md` §7):

| Via | Quem | Penalidade | Faixa de quebra por camada |
|---|---|---|---|
| **GAMBIARRA** | qualquer personagem, em qualquer lugar | **+1 à faixa de quebra da arma**, por modificação | 1 → 5% · 2 → 10% · 3 → 15% |
| **OFICINA** | **Cientista** (e Refúgio com Oficina instalada) | **nenhuma** | **0 → 0%, sempre** |

**O efeito mecânico das duas vias é idêntico** — mesmo dado, mesmo tipo de dano, mesmo bônus. A Gambiarra é **acessível e tóxica**, a Oficina é **limpa e
cara**. Sem Cientista, empilhar é **aposta**: a segunda camada já cobra 10% por ataque, e arma que quebra é pior que arma fraca. Com Cientista, empilhar é
**progressão limpa**, limitada só por slots (2 em arma comum, 3 em especializada). **Por isso ele é quem transforma uma arma remendada numa arma
confiável** — e por isso não é fornecedor de dano, é fornecedor de **confiabilidade**: a ficha da arma não melhora quando ele entra no grupo; o que melhora
é a chance de ela ainda existir no fim da luta. Três limites que precisam estar escritos, porque são fáceis de supor errados:

1. **Ele não "limpa" gambiarra já feita.** Modificação é **permanente** e slot gasto não volta; remoção ou substituição é `[A CALIBRAR]` (§9.2). Ele
   **previne** faixa de quebra, não a desfaz: chegar tarde ao grupo não conserta o arsenal que já existe.
2. **Oficina não protege contra mão ruim.** A falha crítica — **`1` natural no teste de INT** — perde **todo** o material e derruba **1 degrau de conservação**
   (`Calibrada → Boa → Desgastada → Arruinada`), **nas duas vias**. A única proteção é **Peças Novas**, e ela é **exclusiva de Oficina**.
3. **A porta suave não o torna imune ao teto.** Modificação ofensiva numa arma já em **1d12** (Marreta) **não faz nada** ao dado: o teto é **1d12 absoluto**. O
   slot é gasto, o material é gasto, e Oficina de Campo gasta o uso do descanso longo. **Poder de tier alto vem de efeito, nunca de dado maior.**

## 5. Como a classe interage com os subsistemas

### 5.1. Modificações e componentes — o laço com o Base Builder

O Cientista é o consumidor final dos **oito componentes**, e a curva de escassez dele é a curva de campanha do grupo: Sucata e Peças são o pão; **Óptica** é o
gargalo da família Precisão; **Eletrônicos** *não se fabrica, só se desmonta de algo que já existia*; **Célula de Energia** disputa com o gerador do Refúgio; e
a **Liga Pré-Queda** é a única coisa que nenhuma habilidade, receita ou recompensa pode gerar. As CDs de INT vão de **8** (Pano Abafador, Alça Tática) a **16**
(Eletrodos, Designador Laser), e as duas mais altas são justamente as que também consomem Célula. **Ele não resolve escassez — ele dá uso a ela.** Pendência
real de escopo: o canon de classes diz que **Oficina é do Cientista**, enquanto `docs/gdd/GDD_Modificacoes.md` a descreve como trava de **lugar** ("somente em Refúgio com
Oficina instalada"), sem mencionar classe. **Se um personagem sem Cientista pode executar uma modificação de Oficina num Refúgio equipado é `[A CALIBRAR]`;**
aqui se assume a leitura conservadora: Oficina de Campo remove o *lugar* para quem já tem a *classe*.

### 5.2. Ruído, Horda e Trilha de Infecção — ele vende silêncio, e é o pior corpo para usá-lo

O **Silenciador** existe nas duas vias, e o canon já disse a diferença: o de Gambiarra *"não é só um consumível de 30 disparos — é uma arma que passa a travar"*,
e o de Oficina é **a única forma de ser silencioso e confiável**. Quem destrava a build furtiva do grupo é o Cientista — e a build furtiva é exatamente a que
**paga em Infecção**: pela **inversão medida** de `docs/gdd/GDD_Ruido.md`, a arma mais silenciosa é a mais infecciosa (faca = mutação em 5 lutas; rifle = 14). **Ele
fabrica a rota que menos o protege** (d6, limiar 15). Dois pisos canônicos que a habilidade **não** move: **arma de fogo nunca chega a Silencioso** por mais que
se empilhe silenciador e Subsônica (a combinação **para em Baixo**), e a Subsônica custa **−1 degrau no dado**.
Do outro lado, **ele não tem interação mecânica nenhuma com a Trilha de Infecção**: limiar 15 é a base crua, e ele não remove pontos nem melhora o teste de fim
de combate (`d20 + mod. CON vs. CD 10 + pontos ganhos`). **Isso é correto e deve continuar assim:** a remoção de Infecção é a válvula que o canon protege com
**raridade extrema** (`docs/gdd/GDD_Armas.md` §7.4), e o **Médico** já é a fonte renovável que a pressiona (`docs/classes/Classe_Medico.md` §5.1). Um Cientista que
**fabricasse** anti-Infecção seria a segunda, e a Trilha não sobrevive a duas: as dez **Munições Especiais** usam os mesmos oito componentes, e **nenhuma delas
pode ser anti-Infecção sem aprovação explícita do Diretor.**

### 5.3. Turno, travamento, armas e munição

**A Ação Bônus continua fechada em "Destravar arma de fogo"** (`docs/gdd/GDD_Combate.md` §2.4, Aprovação 003). Oficina de Campo **não é Ação Bônus**, e nada derivado desta
classe concede outro uso — restrição dura, e a tentação é grande, porque *destravar* parece assunto de Cientista. **QUEBRA e TRAVAMENTO são contadores distintos e
nunca se somam** (Aprovação 013): a Oficina zera o que a Gambiarra acrescentaria à **quebra** e não toca no **travamento** por conservação, e quem mexe em
travamento é a **Guarda de Ejeção** (−1 na faixa) — por isso as duas não se anulam. O melhor caso segue sendo **Calibrada**, com **~0,5%** residual: **não existe
arma que nunca trava**, e "Confiável" foi **rejeitada** (Aprovação 009). Fabricar em combate não está previsto: o tempo por via é `[A CALIBRAR]`.

**Ele constrói o que não sabe usar: proficiência em Leves, e nada mais** — a mais estreita das oito, sem Cortantes, sem Perfurantes, sem Pistolas, sem armas de
fogo. Ele pode levar um rifle de precisão a três slots de Oficina, faixa de quebra 0, Mira Telescópica e Coronha Estabilizada, e **atacar com ele sem somar o
bônus de proficiência**; `Improvisada` também continua **não somando proficiência** depois de modificada, porque *gambiarra não apaga a origem da arma*. Do que
ele usa de fato: Faca/Facão, Garrafa Quebrada, Taco de Golfe, Seringa de Pressão Veterinária, Fisga de Rolamentos. **A arma boa do Cientista é sempre a arma de
outra pessoa.** Sobre **munição**: as Munições Especiais usam os mesmos oito componentes, e **munição de Gambiarra soma +1 à faixa de travamento** enquanto
carregada, enquanto a de Oficina não tem penalidade — se Oficina de Campo cobre munição (`[A CALIBRAR]`), ele é também a fonte de munição limpa em campo.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **fabricar o impossível** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **6 + mod CON** | **15** | Classe, assinatura, proficiências | — |
| **2** | +2 | +4 + mod CON | 15 | **Oficina de Campo II** — **duas** modificações por descanso longo | — |
| **3** | +2 | +4 + mod CON | 15 | — | **Especialização** |
| **4** | +2 | +4 + mod CON | 15 | **Aumento de atributo** | — |
| **5** | +3 | +4 + mod CON | **16** | — | **Especialização** |
| **6** | +3 | +4 + mod CON | 16 | **Mão Precisa** — falha crítica de fabricação **não derruba** o estado de conservação | — |
| **7** | +3 | +4 + mod CON | 16 | — | **Especialização** |
| **8** | +3 | +4 + mod CON | 16 | **Aumento de atributo** | — |
| **9** | +4 | +4 + mod CON | **17** | — | **Especialização** |
| **10** | +4 | +4 + mod CON | 17 | **Engenharia Reversa** — remove uma modificação e **recupera metade** dos componentes | — |
| **11** | +4 | +4 + mod CON | 17 | — | **Especialização** |
| **12** | +4 | +4 + mod CON | 17 | **Aumento de atributo** | — |
| **13** | +5 | +4 + mod CON | **18** | — | **Especialização** |
| **14** | +5 | +4 + mod CON | 18 | **Substituto** — usa um componente no lugar de outro, 1× por fabricação | — |
| **15** | +5 | +4 + mod CON | 18 | — | **Especialização** |
| **16** | +5 | +4 + mod CON | 18 | **Aumento de atributo** | — |
| **17** | +6 | +4 + mod CON | **19** | — | **Especialização** |
| **18** | +6 | +4 + mod CON | 19 | **Sem Liga** — uma modificação de Oficina por sessão **dispensa a Liga Pré-Queda** | — |
| **19** | +6 | +4 + mod CON | 19 | **Aumento de atributo** | — |
| **20** | +6 | +4 + mod CON | 19 | **ÁPICE — **Protótipo** — você fabrica **UMA** arma de tier Protótipo, uma única vez na campanha. É a única fonte de Protótipo que não é saque** | — |

**HP total no nível 20:** 82 + (20 × mod CON). Com CON +3, isso dá **142 HP**.

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

A **lista** por classe e os **pré-requisitos de nível** estão **fechados** em `docs/gdd/GDD_Especializacoes.md` (Aprovações 021 e 022); o que segue é **leitura de afinidade**, não fonte de níveis. A escada natural dele é a distância até a bancada:

| Faixa | Natureza | Pré-requisito | Números |
|---|---|---|---|
| Baixa | leitura técnica — identificar conservação, slots livres e faixa de quebra de uma arma no olho | `[A CALIBRAR]` | `[A CALIBRAR]` |
| Média | fabricação assistida — receitas de **Gambiarra** com CD reduzida, sem tocar na faixa de quebra | `[A CALIBRAR]` | `[A CALIBRAR]` |
| **Alta** | **Oficina de Campo** — a assinatura, "a especialização mais cara, só em nível alto" (canon) | **nível alto**, `[A CALIBRAR]` | `[A CALIBRAR]` |

> **Alerta de escopo.** Uma especialização do Cientista **não pode** conceder Liga Pré-Queda, convertê-la, substituí-la nem torná-la fabricável — ela é marcada no
> motor como recurso **não-fabricável**, e quebrá-la desmonta o laço que puxa o grupo para fora do Refúgio. Também **não pode** conceder usos novos de Ação Bônus,
> elevar dado acima de **1d12**, nem criar carga anti-Infecção (§5.3).

**O que combina.** **Construtor** (d10, limiar 16, **Mão Calejada**) é o par óbvio: ergue o Refúgio que hospeda a Oficina, e as armas `Improvisada` em que só
ele soma proficiência são as que a Gambiarra produz. **Piloto** (**Modificação Veicular**) estende a lógica de modificação para fora da arma e resolve o
transporte da carga saqueada. **Explorador** (**Esquiva Reflexa** de Reação, Ágeis e Projéteis) é a compra de sobrevivência mais direta para um d6 de 8 HP, e
abre arco e besta — armas silenciosas que ele já sabe consertar. **Pugilista** (punho 1d6 Concussão Ágil) dá a ele a única arma que **não quebra, não trava,
não é desarmada e não fica sem munição**. **O que não combina:** **Corte Contínuo** (Ceifador) exige reduzir um alvo a 0 HP com arma **Cortante**, fora da
proficiência dele; e **Tiro Calculado** (Atirador de Elite) é mais cruel ainda — ele constrói o rifle perfeito, e o crítico em **19–20** vem depois de uma Ação
**Mirar** feita com um ataque **sem proficiência**. A arma é dele; o tiro é de outro.

*Nível 1 é canônico (Aprovação 016). Os campos `[A CALIBRAR]` são o próximo ciclo de balanceamento; as travas nomeadas em §4, §5.3 e §7 não são sugestões de
calibragem, são limites herdados do canon.*
