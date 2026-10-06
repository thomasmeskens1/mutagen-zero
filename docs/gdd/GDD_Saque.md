# MUTAGEN:ZERO — Saque

> **O que este documento é.** Onde as coisas vêm do mundo: a escala de **raridade** — quão difícil é
> achar algo — e as regras de **saque**. É o documento da escassez, e a escassez é o tema central do
> MUTAGEN.

> **Regras relacionadas:** o catálogo de armas e a raridade de cada uma em `docs/gdd/GDD_Armas.md` §2.1 ·
> os componentes em `docs/gdd/GDD_Modificacoes.md` §4 · a reposição de Carga e munição em
> `docs/gdd/GDD_Consumiveis.md` · o dinheiro e as facções neutras *(Bloco 6, a desenhar)*.

> **Aprovações 032 e 033.** Canônico salvo onde o campo diz `[A CALIBRAR]`.

---

## 1. O tom — escassez como princípio

**O MUTAGEN é deliberadamente punitivo.** Nas palavras do Diretor: *"a escassez será o tema principal
do contexto global — vacilou, morreu; matou um monstro, você não é deus."*

Três consequências que todo o resto deste documento obedece:

1. **Recompensa nunca é automática.** Matar uma criatura não gera tesouro por si só.
2. **A escassez é desigual.** O grupo pode ter muita munição e nenhuma arma. Isso é desenho, não azar
   de balanceamento.
3. **A saída para a escassez não é mais saque.** É furtividade, estratégia, e **troca com facções
   neutras** (Bloco 6).

---

## 2. A escala de raridade

**Uma escala só**, para itens **e** componentes. Antes da Aprovação 032 os componentes tinham
"escassez" e os itens não tinham nada; as palavras eram as mesmas e os conceitos também, então viraram
uma coisa só.

| Raridade | Itens | Componentes | Cai em tabela? |
|---|---|---|---|
| **Abundante** | Lixo improvisado | Sucata | Sim |
| **Comum** | Equipamento civil | Peças Mecânicas · Fiação | Sim |
| **Incomum** | Excedente militar · armas de fogo | Química · Óptica · Eletrônicos · Célula de Energia | Sim |
| **Raro** | Militar pesado · Corporativa | **Liga Pré-Queda** | Sim |
| **Épico** | Protótipos — peças únicas | — | Sim, a partir do Patamar 2 |
| **Mítico** | A antiga **"raridade extrema"** | — | **Nunca.** Decisão exclusiva do Diretor |

> **Raridade não é qualidade.** Uma arma Rara não é necessariamente melhor que uma Incomum: é mais
> difícil de achar. A correlação existe, mas a hierarquia não é direta — é o mesmo princípio da
> tabela de tesouro do d20 clássico.

> **O termo "raridade extrema" foi aposentado.** Ele vira o topo da escala, **Mítico**, com a mesma
> regra: as armas que mexem na Trilha de Infecção e o Soro Anti-Infecção não caem de tabela nenhuma.

---

## 3. Raridade por tier

A raridade padrão de cada tier de arma e as onze exceções estão em `docs/gdd/GDD_Armas.md` §2.1. Os
equipamentos recebem raridade no Bloco 4, pela mesma escala.

---

## 4. O saque do grupo (Aprovação 033)

> **Saque é uma oportunidade que o Mestre concede ao grupo — nunca uma recompensa automática de
> combate.** Uma rolagem **por grupo**, não por jogador, numa **tabela única** que mistura munição,
> componentes, armas e equipamento. O grupo pode sair com muita munição e nenhuma arma, e isso é o
> sistema funcionando.

**Ritmo de referência: ~6 saques por Patamar.** O Mestre decide onde e quando — um depósito saqueado,
o abrigo de um grupo morto, a sala que ninguém tinha aberto. A abordagem conta: um grupo que chega em
silêncio e com plano pode merecer a oportunidade que um grupo barulhento perdeu.

### 4.1 Quanto se acha — teste de Sobrevivência do grupo

Antes de rolar, o grupo faz **um** teste de **Sobrevivência, CD 13**. Rola o personagem mais apto; os
outros podem usar a ação **Ajudar** (Vantagem).

| Resultado | Quantidade de itens | Média |
|---|---|---|
| **Sucesso** | `3d6`, mantém os **2 maiores** | ~8,5 |
| **Falha** | `3d6`, mantém os **2 menores** | ~5,5 |

**Medido: 7,1 itens por rolagem, entre 2 e 12.** A perícia Sobrevivência — que o canon liga a
*"encontrar os componentes de fabricação no saque"* desde a Aprovação 021 — passa a ter número.

### 4.2 A tabela — `1d100` por item, na coluna do Patamar

| Resultado | P1 | P2 | P3 | P4 | P5 | Quantidade |
|---|---|---|---|---|---|---|
| **Nada aproveitável** | 01–12 | 01–10 | 01–08 | 01–06 | 01–07 | — |
| Sucata | 13–24 | 11–19 | 09–16 | 07–12 | 08–12 | 1d6 |
| Peças Mecânicas **ou** Fiação | 25–32 | 20–27 | 17–23 | 13–18 | 13–17 | 1d3 |
| Componente Incomum | 33–37 | 28–33 | 24–30 | 19–26 | 18–25 | 1 |
| **Liga Pré-Queda** | 38 | 34–35 | 31–33 | 27–30 | 26–30 | 1 |
| Munição Leve | 39–50 | 36–47 | 34–45 | 31–42 | 31–42 | 1d6 × 3 |
| Munição Pesado | 51–56 | 48–53 | 46–51 | 43–48 | 43–48 | 1d6 × 5 |
| Munição Cartucho | 57–62 | 54–59 | 52–57 | 49–54 | 49–54 | 1d6 × 4 |
| **Munição Rifle** | 63–66 | 60–63 | 58–61 | 55–58 | 55–58 | 1d6 × 7 |
| Projéteis | 67–69 | 64–66 | 62–64 | 59–61 | 59–61 | 1d6 × 3 |
| Consumível | 70–72 | 67–69 | 65–67 | 62–64 | 62–64 | 1 |
| **Item Comum** | 73–88 | 70–81 | 68–75 | 65–70 | 65–68 | 1 |
| **Item Incomum** | 89–98 | 82–94 | 76–88 | 71–82 | 69–78 | 1 |
| **Item Raro** | 99–100 | 95–99 | 89–97 | 83–94 | 79–91 | 1 |
| **Item Épico** | — | 100 | 98–100 | 95–100 | 92–100 | 1 |

### 4.3 Sub-rolagens

| Resultado | Sub-rolagem |
|---|---|
| **Item** (qualquer raridade) | `1d6`: **1–3 arma**, **4–6 equipamento**. Sorteia-se da lista daquela raridade. *Até o catálogo de equipamentos existir (Bloco 4), equipamento vira arma.* |
| **Componente Incomum** | `1d4`: Química · Óptica · Eletrônicos · Célula de Energia |
| **Peças Mecânicas ou Fiação** | `1d2` |
| **Consumível** | `1d6`: **1–3** Munição Especial pronta (sorteada) · **4–5** Granada de Atordoamento · **6** Soro de Campo |

Três regras fixas:

- **Armas Abundantes não estão na tabela.** Um cano ou um tijolo não se *acha* num saque; o Mestre os
  põe no cenário, e qualquer personagem pode improvisar com eles.
- **Mítico nunca** — nem o Soro Anti-Infecção, nem as quatro armas da antiga raridade extrema.
- **Os lotes de munição são maiores nos calibres escassos, de propósito.** Achar munição de rifle é
  raro; quando acontece, é uma caixa, não três balas.

### 4.4 Ritmo medido

8.000 campanhas simuladas, grupo de 4, 12 combates e 6 saques por Patamar.

**Arma ou equipamento — acumulado do grupo ao fim de cada Patamar:**

| Fim do | Incomum | Raro | Épico | Liga Pré-Queda | Meta |
|---|---|---|---|---|---|
| **P1** | 4,3 | 0,9 | — | 0,4 | ~1 Incomum por personagem; Raro é sorte |
| **P2** | 9,9 | 3,0 | 0,4 | 1,3 | ~1 Raro por personagem |
| **P3** | 15,4 | 6,9 | 1,7 | 2,6 | ~2 Raros por personagem; o primeiro Épico |
| **P4** | 20,6 | 12,0 | 4,3 | 4,3 | ~1 Épico por personagem |
| **P5** | 24,8 | 17,6 | 8,2 | 6,4 | 1 a 2 Épicos por personagem |

**Combates em que o atirador tem munição:** Rifle **20%** · Pistola **22%** · Espingarda **27%**,
estáveis do P2 ao P5 (no P1 o rifle fica em 27% só por causa do pente com que o personagem começa).
É **mais punitivo** que os 31% da tabela anterior, por decisão do Diretor.

**O azar:**

| | Chance |
|---|---|
| Grupo termina o P2 **sem nenhum item Raro** | 5% |
| Grupo termina o P3 **sem nenhum item Épico** | **17%** |
| Grupo termina o P1 **sem nenhuma Liga Pré-Queda** | **65%** |

### 4.5 A consequência que foi aceita — e onde está a válvula

A tabela é dura com **componentes Incomuns**: o grupo inteiro acha cerca de **2 no P1 inteiro**,
divididos entre quatro tipos. Isso atinge três classes na estrutura:

| Classe | Depende de | O que a tabela sozinha entrega |
|---|---|---|
| **Médico** | Química (Soro de Campo custa 2) | Até o nível 14, ~2,8 de Química **na campanha inteira** |
| **Cientista · Construtor** | Liga Pré-Queda para a via Oficina | 65% dos grupos não veem Liga no P1 — a Oficina fica fechada no começo |
| Portador da **Vólt-9** | 6 Células de Energia por recarga | Praticamente impossível antes do P3 |

> **Decisão do Diretor (Aprovação 033): a tabela fica dura, e a válvula é o Bloco 6.** Facções neutras
> vendem componentes **de forma confiável, mas caro**. A escassez continua sendo o tema; a diferença é
> que ela passa a ter **preço**, em vez de trancar uma classe. **Até o Bloco 6 existir, o Mestre deve
> saber que o Recurso de nível 14 do Médico depende de uma fonte de Química que ainda não foi
> desenhada.**

### 4.6 O que a tabela substitui

A tabela de munição da Aprovação 028 (`docs/gdd/GDD_Consumiveis.md` §5) era **por personagem**, `1d20`,
**2 por cena**, e só dava munição. Ela foi **substituída** por esta. O conceito de **"ponto de saque"**
foi aposentado: o que existe agora é **o saque do grupo**.

---

*Este arquivo é canônico (Aprovações 032 e 033). Qualquer alteração exige nova aprovação do Diretor de
Criação.*
