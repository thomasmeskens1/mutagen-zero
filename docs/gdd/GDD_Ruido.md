# MUTAGEN:ZERO — Ruído e Detecção

> **O que este documento é.** O Ruído define **quanto barulho cada ação faz e quem escuta**. Ele é
> a entrada de dois sistemas: a **Atração** imediata (mutantes se movem na direção do som) e o
> **Medidor de Horda** (`docs/gdd/GDD_Horda.md`), que acumula o barulho ao longo da cena e traz levas
> de errantes. Este arquivo cobre a física do som; o Horda cobre a consequência do acúmulo.

> **Regras relacionadas:** hexágonos e distância em `docs/gdd/GDD_Combate.md` §11 · Nível de Ruído de
> cada arma em `docs/gdd/GDD_Armas.md` · silenciador como modificação em `docs/gdd/GDD_Modificacoes.md` ·
> munição **Subsônica** em `docs/gdd/GDD_Combate.md` §13.1.

Todo combate em MUTAGEN:ZERO cobra um de **dois preços opostos**, e **nenhuma via é gratuita**. O
corpo a corpo é silencioso, mas coloca o personagem ao alcance do dano Necrótico e, portanto, da
**Infecção** (§9). A arma de fogo mantém a distância segura, mas **chama a horda**. Escolher a arma
é, antes de tudo, escolher qual dos dois custos o grupo prefere pagar naquela cena.
## 1. Níveis de Ruído

Toda ação que produz som recebe um **Nível de Ruído** de **0 a 3**. Cada nível define um **raio**
medido em hexágonos (§11.2), contado a partir do hexágono da fonte. Os raios abaixo são
**canônicos**.

| Nível | Nome | Raio | Pts no Medidor | Fontes |
|---|---|---|---|---|
| **0** | **Silencioso** | Sem raio | 0 | Mover-se com cautela; corpo a corpo **Cortante ou Perfurante não Pesado** (faca, facão, machadinha, lança, foice, forcado); arco; besta; dardo |
| **1** | **Baixo** | **4 hex (6 m)** | 1 | Corpo a corpo de **Concussão ou Pesado** (cacetete, taco, pé de cabra, machado, marreta); Ação **Correr**; arma de fogo com silenciador; mecanismo pneumático |
| **2** | **Médio** | **20 hex (30 m)** | 3 | Pistola leve, pistola pesada, SMG; corpo a corpo com **motor leve** (serra de resgate) |
| **3** | **Alto** | **50 hex (75 m)** | 6 | Carabina, rifle, revólver, espingarda, metralhadora, explosão; **motor pesado** (rebarbadora); **mecanismo Explosivo** (pistola de pinos, granada) |

#### Precedência (Aprovação 009)

Uma arma pode cair em mais de uma categoria — uma foice de duas mãos é Cortante **e** pesada; um
taco de golfe é Leve **e** de Concussão. A ordem é fixa:

> **PESADA** vence **CONCUSSÃO**, que vence **CORTANTE / PERFURANTE / LEVE**.

Se a arma é Pesada, o Ruído é **Baixo**, qualquer que seja o tipo de dano. Peso faz mais ruído que
impacto, e impacto faz mais ruído que corte.

#### Cláusula de motor (Aprovação 012) — sobrepõe a precedência

A precedência acima só consegue produzir Silencioso ou Baixo, mas existem armas de mão mais
ruidosas que isso. Esta cláusula **tem prioridade sobre a precedência**, inclusive em corpo a corpo:

| Mecanismo | Nível |
|---|---|
| Tensão mecânica (arco, besta, fisga) | **Silencioso** |
| Pneumático ou motor leve | **Baixo a Médio** |
| Motor pesado | **Alto** |
| Mecanismo Explosivo ou explosiva | **Alto** |

É por isso que a **Rebarbadora** é Alto e a **Serra de Resgate** é Médio, apesar de serem corpo a
corpo — e por que a **Pistola de Pinos** e a **Granada** são Alto, apesar de uma ser de alcance 2 hex
e a outra ser arremessável.

## 2. Atração

Efeito **imediato**, resolvido no instante em que o ruído é produzido:

> **Todo mutante dentro do raio que NÃO esteja já engajado move-se na direção da fonte no próximo
> turno dele.**

- Não há rolagem: a Atração é automática dentro do raio.
- Mutantes **já engajados** ignoram a Atração e continuam seu combate atual.
- Definição precisa de "engajado" para efeito de Atração: `[A CALIBRAR]`.
- Efeito de obstáculos (paredes, portas, desnível) sobre a propagação do raio: `[A CALIBRAR]`.

## 3. Silenciadores

O silenciador é um **modificador de arma**. Ele **reduz o Nível de Ruído em 1 degrau** e **nunca o
zera**.

| Nível de Ruído original | Com silenciador |
|---|---|
| Alto (3) | **Médio (2)** |
| Médio (2) | **Baixo (1)** |
| Baixo (1) | **Baixo (1)** — o piso é Baixo; arma de fogo nunca fica Silenciosa |

**Custo aprovado: durabilidade.** O silenciador aguenta **30 disparos** (Aprovação 006) e então
**se esgota**, comportando-se como **consumível**. Ele também **ocupa o slot de modificação da
arma**, disputando espaço com qualquer outro acessório.

> **O número 30 é valor de playtest, não resultado de simulação.** Ele só será calibrável quando o
> limiar do Medidor de Horda existir, porque a pergunta real é *quantos tiros silenciados cabem
> antes de a horda chegar* — e hoje não se sabe quantos tiros Altos ela tolera.

- **Efeito mecânico do silenciador esgotado** (a arma volta ao nível original; se o item quebra ou
  pode ser recondicionado): `[A CALIBRAR]`.
- Disponibilidade e custo de aquisição: `[A CALIBRAR]`.

#### Empilhamento com munição Subsônica

A munição **Subsônica** (§13.1) reduz outro degrau, e as duas reduções **empilham** — mas o piso
continua sendo **Baixo**:

| Arma | Base | + Silenciador | + Subsônica |
|---|---|---|---|
| Rifle de caça | Alto (3) | Médio (2) | **Baixo (1)** |
| Pistola pesada | Médio (2) | Baixo (1) | **Baixo (1)** — já no piso |

> **Por que a Subsônica custa dano.** Ela impõe **−1 degrau no dado**, e isso não é decoração: sem
> esse custo, um rifle comum com duas modificações fabricáveis igualaria o protótipo **"Vigília"**,
> cujo valor inteiro é justamente atirar em Nível Baixo. Silêncio se paga em dano — o protótipo
> continua melhor porque entrega 1d10 no mesmo nível de Ruído, com munição de sucata infinita.

> **Silenciador não é furtividade grátis.** Uma arma de fogo silenciada continua em Nível 1: ainda
> soma **1 ponto** ao Medidor de Horda a cada disparo e ainda **atrai** todo mutante não engajado
> dentro de 4 hexágonos. Ele compra distância do problema, não a ausência dele.

## 4. Armas silenciosas nativas

São **Silenciosas (Nível 0)** por natureza, sem gastar o slot de modificação e sem durabilidade a
administrar:

- Armas de corpo a corpo **Cortantes ou Perfurantes** que **não** sejam Pesadas — faca, facão,
  machadinha, lança, foice, forcado
- **Arco**, **besta** e **dardo** (tensão mecânica)

> **Atenção: "improvisada" não implica silenciosa.** A precedência da §1 decide pelo **tipo de dano e
> pelo peso**, não pela procedência da arma. Um cano de ferro é Improvisado e de **Concussão**, logo
> é **Baixo**, não Silencioso. Uma garrafa quebrada é Improvisada e **Cortante**, logo é Silenciosa.
> O que torna uma arma silenciosa é **como ela fere**, não de onde ela veio.

> **Corpo a corpo de Concussão NÃO é silencioso.** Cacetete, taco, pé de cabra, machado e marreta
> são **Baixo** (4 hex, 1 ponto por rodada no Medidor). Isto vale também para o **punho** do
> Pugilista, que é arma de Concussão.

O **arco** tem uma vantagem econômica adicional: **as flechas são recuperáveis**, o que o torna a
única arma à distância sustentável em operação longa fora do Refúgio.

- **Regra de recuperação de flechas** (quantas voltam, teste exigido, chance de quebra por acerto,
  por erro ou por crítico): `[A CALIBRAR]`.
- Se a besta compartilha ou não a recuperação de virotes: `[A CALIBRAR]`.

## 5. Modificadores de Ambiente — PÓS-MVP

> **FORA DO ESCOPO DO MVP.** A subseção abaixo está **aprovada como design**, porém **agendada para
> pós-MVP**. Implementadores **não** devem incluí-la no motor do MVP: ela é registrada aqui apenas
> para que o desenho futuro não seja reinventado.

| Ambiente | Efeito sobre o Nível de Ruído |
|---|---|
| Chuva forte ou vento | **−1 nível** para todos, sem exceção |
| Interior fechado (corredor, galpão) | **+1 nível**, pelo eco |

Regras de acúmulo entre modificadores de ambiente, pisos e tetos resultantes, e classificação de
cada tipo de ambiente do mapa: `[A CALIBRAR]` (pós-MVP).

## 6. Ruído de criaturas

Nem todo ruído vem dos jogadores. **Alguns tipos de zumbi emitem ruído e atraem outros** — o uivo
funciona como uma fonte de Atração (§2 deste documento) produzida pelo próprio inimigo. **Os zumbis BÁSICOS não
emitem ruído.**

**Consequência tática:** quando um tipo que uiva está em cena, **ele vira alvo prioritário**.
Silenciá-lo passa a valer mais do que o inimigo mais forte ou mais próximo, e o grupo é forçado a
gastar ações de alto ruído para calar uma fonte de ruído — o dilema de §12 aplicado a si mesmo.

> **RESOLVIDO — Aprovação 025.** O Bestiário existe, e os sujeitos deste mecanismo são **dois**:
>
> | Criatura | Ruído próprio | Efeito |
> |---|---|---|
> | **Uivante** (ND 2) | **Alto (3)**, gastando a Ação | Atração em raio amplo |
> | **Cachorro Explosivo** (ND 2) | **Alto (3)** na aproximação | O guincho denuncia a posição dele — e a sua |
>
> **Todas as demais criaturas do catálogo são Silenciosas (0)**, o que preserva a regra desta seção:
> os zumbis básicos não emitem ruído. Fichas completas em `docs/gdd/GDD_Bestiario.md` §15.
>
> **Ruído de criatura gera Atração, não pontos de Medidor.** O Medidor conta o ruído que **o grupo**
> produziu (`docs/gdd/GDD_Horda.md` §1). A única criatura que mexe no Medidor é o **Vigia** (ND 1): se ele
> escapar do mapa, o Medidor sobe **+10** — não por barulho, mas porque ele foi buscar gente.

---

---

## 7. A inversão que a calibragem produziu

A arma **mais silenciosa** é a **mais infecciosa**. A faca não chama ninguém — e leva o personagem
à mutação em 5 lutas, porque a briga dura mais e ele apanha mais. O rifle enche o mapa de errantes
— e mantém o corpo limpo por 14 lutas.

| Via | Levas em 6 lutas | Lutas até a mutação |
|---|---|---|
| Faca, besta, arco *(Silencioso)* | **0** | **5** |
| Marreta *(Baixo)* | 0,4 | 8 |
| Pistola *(Médio)* | 3,0 | 11 |
| Rifle **com silenciador** | 2,7 | 14 |
| Rifle *(Alto)* | **5,8** | **14** |

Isso não foi desenhado: emergiu da simulação. Quem escolhe furtividade **não escolhe o caminho
seguro** — escolhe qual moeda vai gastar. Ver `docs/gdd/GDD_Infeccao.md` para a outra ponta.

---

*Este arquivo é canônico. Qualquer alteração exige nova aprovação do Diretor de Criação.
Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*
