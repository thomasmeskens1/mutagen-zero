# MUTAGEN:ZERO — Classe: ATIRADOR DE ELITE

> **Escopo.** Define o **nível 1** do Atirador de Elite conforme o canon (Aprovação 016). Não redefine subsistema:
> Mirar, crítico e travamento em `docs/gdd/GDD_Combate.md` §4/§6.2/§7.3 · catálogo e Ruído por arma em
> `docs/gdd/GDD_Armas.md` · Infecção, Ruído e Horda em `docs/gdd/GDD_Infeccao.md`, `docs/gdd/GDD_Ruido.md` e
> `docs/gdd/GDD_Horda.md`. Valor não fixado pelo canon = `[A CALIBRAR]`.

## 1. Identidade

O Atirador de Elite escolheu a única forma de violência que não exige encostar em nada. Ele passa a luta a quarenta
hexágonos, deitado num telhado quente, o corpo imóvel porque mover-se custa o tiro. O que ele faz não parece
combate: parece contabilidade — vento, distância, quantos cartuchos de calibre Rifle sobraram, quantos deles voltam
como comida. Não é herói de ninguém: é quem decide, sem consultar, qual dos três que correm lá embaixo cai
primeiro, e depois desce e revista o corpo, porque cartucho de Rifle é a moeda mais escassa do mundo.

O preço está no corpo. **Dado d6** — ele e o Cientista são os mais frágeis do jogo, **6 + CON** de HP no nível 1,
oito pontos com CON +2. Um golpe médio de marreta o leva à metade; um crítico o derruba, sempre. E o limiar **13**
não é generoso: o corpo dele é treinado para ficar parado, não para aguentar apodrecer. Ele compra cada metro de
alcance com carne que não tem — tirem-no da posição elevada, encostem um mutante nele, e ele é o alvo mais barato
da mesa.

## 2. Ficha rápida

| Campo                                                 | Valor                                                                                              |
| ----------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Dado de vida**                                | **d6** — o menor do jogo, junto do Cientista; nunca muda                                    |
| **HP no nível 1**                              | **6 + mod. de CON** (máximo do dado) — com CON +2, **8 HP**                          |
| **HP por nível após o 1º**                   | `[A CALIBRAR]`                                                                                   |
| **Limiar de Infecção**                        | **13**                                                                                       |
| **Proficiência (famílias de arma)** | **Pistolas**, **Longas**, **Espingardas** — as três famílias de fogo, acesso integral |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Perícias / resistências com proficiência** | `[A CALIBRAR]`                                                                                   |
| **Habilidade-assinatura** | **Tiro Calculado**: usando a Ação **Mirar** **com uma arma de fogo**, o crítico acontece em **19–20** |

### Bandas de Infecção calculadas para o limiar 13

Frações do limiar pessoal (`docs/gdd/GDD_Infeccao.md` §3): `1/3 = 4,33` · `2/3 = 8,67`.

| Faixa         | Pontos          | Estado             | Efeito                                                   |
| ------------- | --------------- | ------------------ | -------------------------------------------------------- |
| até 1/3      | **0–4**  | Saudável          | Nenhum                                                   |
| 1/3 a 2/3     | **5–8**  | Infectado          | Custo **social**, sem penalidade mecânica        |
| 2/3 ao limiar | **9–12** | Infectado grave    | **Desvantagem** em testes de CON contra Infecção |
| no limiar     | **13**    | Mutação ou morte | Fim da linha                                             |

> Convenção de arredondamento não está no canon; usa-se **piso** (`floor(13/3)=4`, `floor(26/3)=8`), por analogia
> ao limiar 15: `[A CALIBRAR]`. A banda grave dele tem **4 pontos** (9–12) — muito tempo rolando CON com Desvantagem.

## 3. Habilidade-assinatura — Tiro Calculado

**Enquanto o ataque é resolvido sob a Ação Mirar, a faixa de crítico passa de `20` para `19–20`.**

1. **Mirar continua custando a Ação inteira** (§4): exige **não ter se movido nenhum metro** e o ataque mirado
   ocorre **no turno seguinte**. **O Atirador de Elite não barateia isso** — nenhuma classe pode, sem aprovação
   explícita do Diretor. E **nada de Ação Bônus**: o escopo em "Destravar arma de fogo" permanece intacto.
2. **A faixa 19–20 vem do uso de Mirar, não da Vantagem.** Se a Vantagem for cancelada por Desvantagem (alvo além
   do alcance normal, Cego, Envenenado — §1.1), o ataque rola **1d20 normal e ainda crita em 19–20**: 10% em vez
   dos 5% padrão. **Lê-se sempre no dado efetivamente usado**, após Vantagem/Desvantagem (§1.1).
3. **`19` não é crítico automático.** Só o `20` natural ignora a Defesa. Um `19` que não alcance a Defesa é
   **falha**; alcançando-a, é crítico. Formalização exata: `[A CALIBRAR]`.
4. **Não combina com Rajada nem Automático**, porque Mirar não combina. O Atirador de Elite mirado é um homem de
   **tiro único**. O crítico segue §6.2: **dobram-se os dados, não o modificador.**

**O número.** Mirar concede **Vantagem** (2d20, o maior). P(o maior cair na faixa) = `1 − (1 − p)²`:

| Configuração                                 | Cálculo                         | P(crítico)      |
| ---------------------------------------------- | -------------------------------- | ---------------- |
| Sem Mirar, faixa 20                            | `1/20`                         | **5,00%**  |
| Mirar, faixa 20 (qualquer classe)              | `1 − (19/20)² = 1 − 0,9025` | **9,75%**  |
| **Mirar + Tiro Calculado, faixa 19–20** | `1 − (18/20)² = 1 − 0,81`   | **19,00%** |

**A habilidade praticamente dobra a chance de crítico do tiro mirado: 9,75% → 19,00%, `+9,25` pontos percentuais.**
Com **rifle de precisão 1d12** (média 6,5; o crítico dobra os dados, somando outros 6,5), o ganho médio é
`0,0925 × 6,5 =` **+0,60 de dano por ataque mirado**, com pico de 24+mod cinco vezes mais frequente.

**Efeito colateral derivado do canon, não regra nova:** com Vantagem, a chance de `1` natural no dado efetivo cai
ao quadrado — **Boa** 5% → **0,25%**, **Desgastada** 10% → **1,00%**, **Arruinada** 15% → **2,25%** (§7.3). Ele quase
nunca trava, o que deixa a Ação Bônus dele ainda mais ociosa: aceitável, e **não** é argumento para reabrir o escopo.

**Custo de cadência:** Mirar consome a Ação, logo o ciclo real é **1 ataque a cada 2 turnos**. O DPR canônico de
**6,025** do rifle de precisão pressupõe ataque todo turno; o do ciclo mirado, já com Vantagem, `+2` de dano e
faixa ampliada, é `[A CALIBRAR]`. **Tiro Calculado não é mais dano por rodada; é mais variância concentrada em
menos rodadas.**

## 4. A porta suave

**O Atirador de Elite NÃO tem uma porta suave.** As três são canônicas e fechadas (`CANON_CLASSES.md` §2):
Modificações = **Cientista**, Refúgio = **Construtor**, Veículos = **Piloto**. **Tiro de longo alcance não é um
pilar com porta suave:** qualquer personagem proficiente atira à distância pelas regras gerais de §7.4, com a mesma
curva de alcance e Desvantagem. Não invente para ele monopólio de "posição elevada", "observação" ou "designação de
alvo": o que ele tem é proficiência em **todas as armas de fogo** e **Tiro Calculado**, e isso já é o tier bom.
Quarta porta suave: `[A CALIBRAR]`, e **por padrão inexistente**.

## 5. Como ela interage com os subsistemas

### 5.1. Medidor de Horda — a contrapartida pesada

**Ele vive do rifle, e rifle é Ruído `Alto` — 6 pontos por rodada no Medidor.** Carabina, rifle de caça, rifle de
precisão, revólver, espingarda e metralhadora: todos **Alto**. O limiar é **20, em escada**. Aritmética direta:
**4 rodadas de Alto = 24 pontos**, uma leva dentro de uma única luta, e o Medidor segue em 4.

Ritmo canônico medido, em levas por 6 lutas: **rifle (Alto) 5,80** · **rifle silenciado 2,70** · pistola (Médio)
3,00 · faca, arco e besta (Silencioso) 0. Lutas até a mutação, na mesma ordem: 14 · 14 · 11 · 5.

> **Um grupo construído em torno dele enfrenta cerca de 5,8 levas a cada 6 lutas. Com silenciador, 2,7.** Ele é, sem
> concorrência, **a classe que mais alimenta a Horda**: o d6 e o limiar 13 são o preço no corpo, as 5,8 levas são o
> preço no ambiente, e pagam-se os dois.

**Ele cancela o silêncio dos outros.** O Medidor soma **só o ruído mais alto do grupo por rodada**: um Explorador
com arco e três facas na rodada em que o rifle dispara fazem uma rodada de **6**, não de 0 — e o grupo descobre
tarde, porque o Medidor é **invisível ao jogador** e a chegada da leva *é* o aviso. **A cadência de Mirar não reduz
o custo por rodada**, só o número de rodadas ruidosas, e as rodadas em que ele **não** atira só valem 0 se
**ninguém mais** fizer ruído. E a **Atração** é imediata: cada disparo Alto move todo mutante não engajado num raio
de **50 hex (75 m)** na direção dele — e ele está a 40 hex do grupo, sozinho, com 8 HP.

### 5.2. Silenciador — corta pela metade e acaba

Reduz **1 degrau** (Alto → Médio, 6 → 3 pts/rodada), **nunca zera**, dura **30 disparos** e **ocupa o slot de
modificação** (`docs/gdd/GDD_Ruido.md` §3). É ele que leva as levas de 5,8 para 2,7. Derivação canônica: rifle de caça gasta
**3,72 tiros/alvo**, uma luta típica de 4 errantes custa ~**14,9 disparos**, logo **30 disparos ≈ 2 lutas de
silenciador**. Numa carabina de 2 slots ele disputa espaço com a Baioneta-Adaptador M7, e essa disputa **é** a
decisão de personagem. **Revólver e espingarda não aceitam silenciador**, por razão física.

### 5.3. Trilha de Infecção

O rifle mantém o corpo limpo: via Alto, **mutação em 14 lutas** contra 5 da faca (`docs/gdd/GDD_Ruido.md` §7). Mas esse 14 é
medido no **limiar base 15**; no limiar **13** o teto é 2 pontos menor e o ritmo recalculado é `[A CALIBRAR]` — a
referência canônica escala apenas o caso da marreta. O que é certo: a Trilha conta **acertos, não dano**, e ele está
a 40 hexágonos de onde os acertos acontecem, então enquanto a distância se mantém a Trilha fica quase parada. O
risco não é acumular devagar — é **a leva que ele mesmo chamou entrar pela borda mais próxima da última fonte de
ruído** (`docs/gdd/GDD_Horda.md` §3), que é a posição dele: aí ele está em corpo a corpo, com 8 HP, alcance mínimo de arma
de fogo indefinido (`[A CALIBRAR]`) e a Trilha avançando 1 ponto por mordida.

### 5.4. Modificações e munição

**Sem acesso especial:** Gambiarra com `+1` na faixa de quebra. **Quebra e travamento são contadores distintos e
nunca se somam** (§7.3) — mas ele é a única classe que administra os dois ao mesmo tempo, porque é a única que
vive de arma de fogo. **Munição de Gambiarra soma `+1` à faixa de travamento** enquanto carregada (§13.1): sob
Mirar o efeito é abafado (a Vantagem eleva ao quadrado); em qualquer tiro **não** mirado, morde cheia.

**Calibre Rifle é o mais escasso do jogo** e é onde ele vive: pentes de **5** significam **Recarregar consumindo a
Ação inteira** a cada 5 tiros, um terceiro turno improdutivo no ciclo Mirar / Atirar / Recarregar. **Munição
Subsônica** desce outro degrau de Ruído mas custa **−1 degrau no dado** (§13.1): 1d12 → 1d10, e o crítico perde 1
ponto de média por dado dobrado — **silêncio se paga em dano**. E o **teto de `1d12` é absoluto**: o rifle de
precisão já está nele, então nenhuma progressão dele sobe dado; o que vem adiante é **efeito**.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **um tiro, um alvo** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **6 + mod CON** | **13** | Classe, assinatura, proficiências | — |
| **2** | +2 | +4 + mod CON | 13 | **Respiração** — Mirar **não exige** ter ficado parado | — |
| **3** | +2 | +4 + mod CON | 13 | — | **Especialização** |
| **4** | +2 | +4 + mod CON | 13 | **Aumento de atributo** | — |
| **5** | +3 | +4 + mod CON | **14** | — | **Especialização** |
| **6** | +3 | +4 + mod CON | 14 | **Tiro Calculado II** — crítico em **18–20** sob Mirar (**27,8%** com Vantagem) | — |
| **7** | +3 | +4 + mod CON | 14 | — | **Especialização** |
| **8** | +3 | +4 + mod CON | 14 | **Aumento de atributo** | — |
| **9** | +4 | +4 + mod CON | **15** | — | **Especialização** |
| **10** | +4 | +4 + mod CON | 15 | **Alcance Estendido** — o alcance normal das suas armas de fogo **dobra** | — |
| **11** | +4 | +4 + mod CON | 15 | — | **Especialização** |
| **12** | +4 | +4 + mod CON | 15 | **Aumento de atributo** | — |
| **13** | +5 | +4 + mod CON | **16** | — | **Especialização** |
| **14** | +5 | +4 + mod CON | 16 | **Automático** — desbloqueia o modo **Automático** | — |
| **15** | +5 | +4 + mod CON | 16 | — | **Especialização** |
| **16** | +5 | +4 + mod CON | 16 | **Aumento de atributo** | — |
| **17** | +6 | +4 + mod CON | **17** | — | **Especialização** |
| **18** | +6 | +4 + mod CON | 17 | **Tiro Calculado III** — crítico em **17–20** sob Mirar (**36%** com Vantagem) | — |
| **19** | +6 | +4 + mod CON | 17 | **Aumento de atributo** | — |
| **20** | +6 | +4 + mod CON | 17 | **ÁPICE — **Um Tiro** — 1× por combate, um ataque à distância **acerta automaticamente e é crítico**** | — |

**HP total no nível 20:** 82 + (20 × mod CON). Com CON +3, isso dá **142 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 13 para **17** ao fim da carreira.
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

### O que o Atirador de Elite oferece a outras classes

| Especialização                                 | Conteúdo                        | Nível mínimo          |
| ------------------------------------------------ | -------------------------------- | ----------------------- |
| **Tiro Calculado** (assinatura)            | A faixa 19–20 sob Mirar, de §3 | Alto —`[A CALIBRAR]` |
| Proficiência em armas de fogo, por subcategoria | `[A CALIBRAR]`                 | `[A CALIBRAR]`        |

> **RESOLVIDO pela Aprovação 017 — Tiro Calculado EXIGE arma de fogo.**
> O vazamento que este aviso descrevia está fechado na regra, não só na nota. Sem a restrição, um
> **Explorador** que adquirisse a assinatura por Especialização teria **19% de crítico com Ruído 0**
> usando arco ou besta — a variância do crítico sem o d6 que a paga e sem as **5,8 levas a cada 6
> lutas** que o rifle cobra. A Ação **Mirar** continua servindo a qualquer ataque à distância; o que
> não serve é **Tiro Calculado** fora de arma de fogo.

### O que combina com o Atirador de Elite

| Origem                                          | Por quê                                                                                                                                                                                                                   |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cientista** — *Oficina de Campo*     | O silenciador é a diferença entre 5,8 e 2,7 levas, dura 30 disparos e some. Fabricar em campo**sem** o `+1` de quebra é, para ele, a especialização mais valiosa do jogo.                                     |
| **Explorador** — *Esquiva Reflexa*     | A melhor compra defensiva possível para 8 HP: reduz a**frequência** de acerto, que é o que mata quem tem pouco HP e limiar baixo. E ele quase nunca faz ataque de oportunidade, então a Reação dele é barata. |
| **Construtor** — cobertura e estrutura   | Três quartos de cobertura valem**+5** de Defesa (§5.4). Para um d6 imóvel, `+5` vale mais que qualquer dado.                                                                                                    |
| **Médico** — limiar 18, *Estabilizar* | Não conserta o d6, mas cobre o flanco pior: quando a leva chega, ele apanha necrótico com 8 HP e limiar 13.                                                                                                              |

> **A evitar:** qualquer coisa que o empurre para o corpo a corpo. *Combate Desarmado* ou *Corte Contínuo* num d6 com
> limiar 13 convida a Trilha a andar sobre quem tem menos teto para aguentá-la. **O alcance é a defesa dele.**

*Nível 1 conforme `CANON_CLASSES.md` (Aprovação 016). Alterar dado, limiar, proficiências, a assinatura, o custo de Mirar ou o escopo da Ação Bônus exige nova aprovação do Diretor.*
