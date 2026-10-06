# MUTAGEN:ZERO — Medidor de Horda

> **O que este documento é.** O Medidor de Horda é o contador que transforma barulho em
> consequência: o grupo faz ruído, o ruído acumula na cena, e ao cruzar o limiar chega uma leva de
> errantes. É uma das duas moedas de atrito de MUTAGEN:ZERO — o preço que o combate à distância
> cobra do ambiente. A outra é a **Trilha de Infecção** (`docs/gdd/GDD_Infeccao.md`), o preço que o
> corpo a corpo cobra do corpo.

> **Dependência direta.** A única entrada deste sistema é o **Nível de Ruído**, definido em
> `docs/gdd/GDD_Ruido.md`. Nenhuma regra aqui faz sentido sem aquela escala.

> **Regras relacionadas:** hexágonos e bordas do mapa em `docs/gdd/GDD_Combate.md` §11 · Atração
> imediata em `docs/gdd/GDD_Ruido.md` · silenciador e munição Subsônica, que reduzem o acúmulo.

O Medidor de Horda é um **contador de cena** mantido pelo Mestre.

## 1. Acúmulo — por rodada, não por evento

**Ao fim de cada rodada**, o Mestre soma ao Medidor **apenas o ruído mais alto que o grupo produziu
naquela rodada**:

| Nível de Ruído mais alto da rodada | Pontos |
|---|---|
| Silencioso (0) | **0** |
| Baixo (1) | **1** |
| Médio (2) | **3** |
| Alto (3) | **6** |

Se um personagem dispara um rifle e três usam faca, a rodada vale **6**: é o rifle que se ouve.

> **Por que por rodada e não por ação.** Contado por evento, quatro personagens atirando durante
> três rodadas geram treze eventos, e um rifle acumulava **73,6 pontos por luta** — qualquer limiar
> razoável disparava no meio da primeira briga, sempre. Por rodada cai para **20,66**. Além de
> viável, é mais leve na mesa: o Mestre soma **um número por rodada**, não um por ação.

## 2. Limiar: 20, em escada

Ao cruzar **20 pontos**, chega uma leva de errantes. **Subtraia 20 e continue contando** — uma luta
longa e barulhenta pode gerar duas levas, e deve.

## 3. A leva

**Piso: 2 errantes na primeira leva, `+1` a cada leva subsequente na mesma cena.** Entram pela borda
do mapa mais próxima da **última fonte de ruído**.

> **Este valor é piso, não teto.** A leva é explicitamente um **recurso do Mestre** para balancear o
> combate ou aumentar a dificuldade: ele pode escalar o tamanho e a composição acima do piso quando
> a cena pedir. O que o piso garante é que a consequência **sempre** exista.

## 4. Zeragem

O Medidor **zera no fim da cena**, não no fim do combate. Fugir de uma sala para outra **não limpa o
rastro** — o barulho que você fez continua valendo enquanto você estiver naquele lugar.

## 5. Ritmo medido

Com limiar 20, contando por rodada, numa luta típica de quatro errantes:

| Via | Levas em 6 lutas |
|---|---|
| Faca, besta, arco *(Silencioso)* | **0** |
| Marreta *(Baixo)* | 0,4 |
| Pistola *(Médio)* | 3,0 |
| Rifle **com silenciador** | 2,7 |
| Rifle *(Alto)* | **5,8** |

> **O silenciador corta as levas pela metade** — de 5,8 para 2,7 — sem alterar mais nada. Ele não
> remove o custo, reduz. E a via puramente silenciosa **nunca** chama leva: é possível atravessar a
> cena sem acordar ninguém, ao preço que a §9 cobra.

> **Regra de visibilidade — não é sugestão.** O Medidor de Horda é **recurso EXCLUSIVO DO MESTRE**.
> Os jogadores **não veem o contador**: não sabem o valor atual, não sabem quanto falta para o
> limiar e não recebem aviso de que um limiar foi cruzado — a chegada da leva *é* o aviso.
> Implementadores: o Medidor **nunca** é exposto na interface do jogador, nem como número, nem como
> barra, nem como alerta. A tensão da regra depende da incerteza.

---

*Este arquivo é canônico. Qualquer alteração exige nova aprovação do Diretor de Criação.
Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*
