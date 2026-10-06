# MUTAGEN:ZERO — Consumíveis

> **O que este documento é.** A economia de **reposição** de MUTAGEN:ZERO: o que se gasta, quanto
> custa repor e onde se repõe. Ele é o espelho da regra de produção da Aprovação 023 — se *tudo que
> se fabrica consome componente*, então **tudo que se consome precisa de uma via de volta declarada**.

> **Regras relacionadas:** os oito componentes e as duas vias de fabricação em
> `docs/gdd/GDD_Modificacoes.md` §2 e §4 · as propriedades de arma em `docs/gdd/GDD_Armas.md` §3 · os pools
> de munição em `docs/gdd/GDD_Combate.md` §13.1 · o Medidor de Horda, que é o outro freio do tiro, em
> `docs/gdd/GDD_Horda.md`.

> **Aprovação 028.** Canônico salvo onde o campo diz `[A CALIBRAR]`.

---

## 1. O princípio

> **Nada se gasta sem ter uma via de volta declarada.**

Um recurso sem regra de reposição é uma de duas coisas: **infinito na prática** (o Mestre concede
quando lembra) ou **morto na prática** (ninguém usa por medo de acabar). As duas arruínam a decisão,
que é o que o consumível existe para criar.

Este documento fecha **quatro** `[A CALIBRAR]` antigos de uma vez: a reposição da propriedade
`Carga (N)`, o consumo e a recarga da **Energia da Célula**, a disputa dela com o **gerador do
Refúgio**, e o **lote de munição saqueada**.

---

## 2. A unificação — `Carga (N)` absorve combustível e Energia da Célula

**Antes da Aprovação 028 havia três recursos fazendo a mesma coisa com nomes diferentes:**

| Nome antigo | Onde aparecia |
|---|---|
| `Carga (N)` | Soqueira "Vólt-9" (6) · "Ferro de Marca" (10) · Emissor EMP "Apagão" (3) · "Cantor" (2) · Tonfa de Choque (4) · Bateria de Carro c/ Garras (3) |
| *"combustível 6 rodadas"* | Maçarico de Solda Portátil |
| **Energia da Célula** | Eletrodos · Soqueira de Raios |

**Os três passam a ser `Carga (N)`.** O Maçarico tem **`Carga (6)`**; as modificações elétricas gastam
**`Carga`** tirada da Célula de Energia.

> **Esta unificação REMOVE terminologia em vez de acrescentar.** A palavra *carga* tinha **quatro
> sentidos vivos** registrados em `docs/gdd/GDD_Glossario.md` §4 — propriedade `Carga (N)`, Munições
> Especiais, Energia da Célula e mecanismo Explosivo. Agora tem **três**. É a **segunda colisão do
> projeto resolvida por unificação**, depois da *Oficina* na Aprovação 023.

**O que `Carga (N)` continua NÃO sendo:** munição. Ela **não usa pool de calibre**, não se saqueia na
tabela do §5 e não se conta em pente.

---

## 3. Reposição de Carga

> **Repor 1 Carga custa 1 unidade do componente que a alimenta.**

| Tipo de carga | Componente | Escassez | Itens |
|---|---|---|---|
| **Elétrica** | **Célula de Energia** | Incomum | Vólt-9 · EMP "Apagão" · Tonfa de Choque · Bateria de Carro · **Eletrodos** · Soqueira de Raios |
| **Incendiária** | **Química** | Incomum | Maçarico de Solda · "Ferro de Marca" |
| **Chamariz** | **Peças Mecânicas** | Comum | "Cantor" dardo chamariz |

**Onde se repõe:** apenas em **Refúgio com bancada**, ou pela **Oficina de Campo** do Cientista
(1× por descanso longo, sem dispensar o componente).

**Consequência que a mesa vai sentir:** a Soqueira "Vólt-9" tem **6 cargas** e custa **6 Células de
Energia** para encher — e Célula de Energia é **Incomum**. Recarregá-la por completo é uma decisão de
Refúgio, não um gesto de rotina. `docs/gdd/GDD_Combate.md` §6 já registrava que o DPR dela **decai
visivelmente de 6,35 para 4,08** quando as cargas acabam: **agora esse decaimento tem preço de
volta.**

### 3.1 O "Ferro de Marca" é o caso extremo, e de propósito

`Carga (10)`, alimentada por **Química**. Ele é **RARIDADE EXTREMA** (`docs/gdd/GDD_Armas.md` §7.4) e a
habilidade dele — *Cauterizar de Reação, zerando os pontos de Infecção de um ataque sofrido* — é a
coisa mais forte que o sistema oferece contra a Trilha.

**Dez cargas custam dez unidades de Química.** É o item mais caro de manter do jogo, e deve ser.

---

## 4. A disputa com o gerador do Refúgio

`docs/gdd/GDD_Modificacoes.md` §9.2, item 4, registrava esta pendência desde a aprovação das
Modificações: *"a disputa com o gerador do Refúgio"* nunca teve número.

> ### Um pool, duas bocas.
>
> **A Célula de Energia gasta em arma NÃO alimenta o Refúgio, e a gasta no Refúgio não volta para a
> arma.** É o mesmo estoque, e cada unidade vai para um lado só.

**O que o gerador do Refúgio paga:** as instalações que consomem energia — a bancada de **Oficina**,
a **Enfermaria** e o que os módulos futuros acrescentarem. **Quanto cada instalação consome por
descanso longo é `[A CALIBRAR]`** e pertence ao módulo de Refúgio.

O que esta seção fixa é o **princípio**: recarregar a Vólt-9 é decidir que a Enfermaria fica sem
energia naquele ciclo. A escolha é do grupo, e ela existe.

---

## 5. Munição — onde se acha

> **SUBSTITUÍDA na Aprovação 033.** A tabela de munição desta seção — `1d20` **por personagem**,
> **2 pontos de saque por cena**, só munição — foi trocada pela **tabela única de saque do grupo**, em
> `docs/gdd/GDD_Saque.md` §4, que mistura munição, componentes, armas e equipamento numa rolagem só.
>
> **O que sobreviveu daqui:** o princípio de que **a escassez mora no calibre errado**, não na
> ausência de munição no mundo; e a métrica de calibragem — **combates em que o atirador tem munição**.
> Na tabela nova ela ficou **mais dura**: Rifle 20%, Pistola 22%, Espingarda 27% (antes: 31%, 35%,
> 48%), por decisão do Diretor.

### 5.1 Os dois pools que não obedecem à tabela

- **Projéteis é RECUPERÁVEL** (Aprovação 011): recupera-se o projétil depois do combate, mas **não a
  carga especial**. Na prática o arco quase não depende do saque — ele é a via à distância
  **sustentável e silenciosa**, e paga por isso em dado.
- **Exótica não se saqueia.** O limite de **2 itens exóticos no jogo inteiro** continua valendo; a
  munição deles se fabrica no Refúgio.

---

## 6. Consumíveis de uso único

| Item | Regra |
|---|---|
| **Granada de Atordoamento** | Propriedade **Consumível**: um uso, some. Fabricação pelas regras das Munições Especiais |
| **Munições Especiais (as dez)** | Não se acham — **fabricam-se**, com os mesmos oito componentes. Quantidade por receita: ver `docs/gdd/GDD_Modificacoes.md` |
| **Soro Anti-Infecção** | **Raridade extrema.** Não se fabrica por regra nenhuma; distribuição é decisão exclusiva do Diretor |
| **Soro de Campo** | **2 unidades de Química** por soro (fecha o `[A CALIBRAR]` da Aprovação 023). Um por descanso longo, e **sem Química o descanso passa em branco** |

---

## 7. O que continua `[A CALIBRAR]`

| Campo | Estado |
|---|---|
| **Consumo do gerador do Refúgio** por instalação | Pertence ao módulo de **Refúgio**, que não foi desenhado. O §4 fixa o princípio, não os números |
| **Combustível de veículo** | Pertence ao módulo de **Veículos**. **Não** é `Carga (N)` e não deve ser tratado como tal sem aprovação |
| ~~Ponto de saque~~ | **Fechado na Aprovação 033:** o conceito foi aposentado. O saque agora é do **grupo**, ~6 por Patamar, onde o Mestre decidir (`docs/gdd/GDD_Saque.md` §4) |
| **Água, comida e descanso** | Não modelados no MVP. Fome e sede **não existem** como regra |
| **Peso e capacidade de carga** | Não modelados. O sistema usa **slots de inventário** (`docs/gdd/GDD_Armas.md` §3), não quilos |

---

## 8. Notas de balanceamento

1. ~~A tabela de munição da Aprovação 028~~ entregava 31% (Rifle), 35% (Leve) e 48% (Cartucho) de
   combates com arma de fogo. **Substituída na Aprovação 033** pela tabela única do grupo, que entrega
   **20%, 22% e 27%** — mais dura, por decisão do Diretor. A calibragem nova está em
   `docs/gdd/GDD_Saque.md` §4.4.
2. **A espingarda continua a mais sustentável das armas de fogo** (27%): gasta 11 tiros por combate
   contra os 17 do rifle — e continua sendo **Ruído Alto**, então quem atira mais paga mais Horda.
3. **A unificação da Carga não mexeu em DPR nenhum.** Nenhuma arma mudou de dado, alcance ou
   propriedade — mudou só o nome do recurso e a existência de uma via de reposição.
4. **O que estas simulações não modelam:** grupos que dividem munição, saque fora de cena, compra ou
   troca com NPCs, e a decisão de simplesmente não lutar.

---

*Este arquivo é canônico (Aprovação 028). Qualquer alteração exige nova aprovação do Diretor de
Criação. Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*
