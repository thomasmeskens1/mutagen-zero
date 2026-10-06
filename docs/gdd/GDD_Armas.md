# MUTAGEN:ZERO — Catálogo de Armamento

> **Dados Canônicos — Armamento.** Este documento é o **catálogo de armas**: dado, tipo de dano,
> Ruído, FOR mínima, propriedades e DPR de cada peça. As **regras** de combate que operam esses
> dados vivem em [`docs/gdd/GDD_Combate.md`](docs/gdd/GDD_Combate.md), e as três funções de atrito em
> [`docs/gdd/GDD_Ruido.md`](docs/gdd/GDD_Ruido.md), [`docs/gdd/GDD_Horda.md`](docs/gdd/GDD_Horda.md) e [`docs/gdd/GDD_Infeccao.md`](docs/gdd/GDD_Infeccao.md).
> **Não são repetidas aqui.**
>
> Fonte da verdade: `Mutagen_Zero_Armamento.xlsx` (v0.3). Armas, propriedades, modificações,
> componentes e escala de Ruído são **CANON** (Aprovações 001 a 010). Valores marcados
> `[A CALIBRAR]` e os números de FOR mínima continuam **abertos**. Implementadores devem tratar
> `[A CALIBRAR]` como configuração externa e **nunca** inventar padrões dentro do motor.

---

## 1. O que este documento é

Um catálogo, não um livro de regras. Para cada arma ele fixa: quantos dados e de quantas faces,
que tipo de dano entrega, quanto Ruído gera, que FOR mínima exige, que propriedades carrega e qual
o DPR de referência.

**Referências cruzadas obrigatórias** (não duplicamos essas regras):

| Assunto | Onde está a regra |
|---|---|
| Fórmula de ataque e Defesa | GDD_Combate §5.1, §5.2 |
| Cobertura (e o que Transfixante reduz) | GDD_Combate §5.4 |
| Dano, crítico e tipos de dano | GDD_Combate §6.1, §6.2, §6.3 |
| Munição, Recarga, modos de disparo | GDD_Combate §7.1, §7.2 |
| Travamento e destravar | GDD_Combate §7.3 |
| Alcance normal e longo | GDD_Combate §7.4 |
| Trilha de Infecção | `docs/gdd/GDD_Infeccao.md` |
| Condições (Atordoado, Sangrando, Agarrado, Envenenado) | GDD_Combate §10 |
| Grid hexagonal, distância, linha de visão | GDD_Combate §11 |
| Níveis de Ruído, Medidor de Horda, silenciadores | `docs/gdd/GDD_Ruido.md` / `docs/gdd/GDD_Horda.md` |

A tabela vazia de GDD_Combate §6.4 é **substituída por este arquivo**.

### 1.1. O princípio do teto de dado

A escada de dados é **d4 → d6 → d8 → d10 → d12** e o **teto é 1d12 ABSOLUTO**.

Acima disso os degraus deixam de ser regulares:

- d12 → 2d6 rende apenas **+5% de DPR** — um degrau imperceptível na mesa;
- 2d6 → 2d8 salta **20%**, o que trivializa o zumbi comum.

**Consequência de design:** o poder de tier alto vem de **EFEITO**, nunca de dado maior. Uma arma
lendária com dado maior **não existe neste jogo**. Dado secundário (armas de dois tipos de dano)
tem teto de **1d6**.

### 1.2. Parâmetros do DPR

Todos os DPR deste catálogo saem de cinco alavancas globais (aba `Parametros`):

| Parâmetro | Valor | Observação |
|---|---|---|
| Bônus de ataque do personagem | **5** | Modificador de atributo + proficiência. Personagem de nível baixo típico. |
| Modificador de dano | **3** | Modificador do atributo usado pela arma. |
| Defesa do alvo | **14** | **Zumbi comum — CANON** (Aprovação 025, `docs/gdd/GDD_Bestiario.md` §1) |
| HP do alvo | **12** | **Zumbi comum — CANON** (Aprovação 025, `docs/gdd/GDD_Bestiario.md` §1) |
| Bônus de proficiência | **2** | Descontado do ataque em armas Improvisadas. Progressão +2 a +6 `[A CALIBRAR]` |

Fórmula usada na planilha:

```
P(acerto)   = (21 - (Defesa - bônus efetivo)) / 20, limitado entre 5% e 95%
              bônus efetivo = bônus de ataque MENOS a proficiência se a arma for Improvisada
Dano médio  = número de dados × (faces + 1) / 2
DPR         = P(acerto) × (dano médio + mod) + 5% × dano médio
              o termo de 5% é o crítico, que dobra os dados
```

Validada contra Monte Carlo de 200.000 tiradas: **a fórmula é exata**; a simulação era aproximada.

**Exceção canônica (Aprovação 009):** em modo **Rajada** o crítico soma **UM dado adicional** em vez
de dobrar. Ver GDD_Combate §7.2.

**Colunas derivadas:** `Rodadas para abater` = HP do alvo ÷ DPR. `DPR sust.` = DPR × fração de
turnos em que a arma consegue atacar (0,5 para armas com Recarga). `Tiros/alvo` = munição esperada
para derrubar um alvo.

---

## 2. Os seis tiers

| Tier | O que é |
|---|---|
| **Improviso** | Lixo improvisado. Quase sempre com **Improvisada** e/ou **Frágil**. |
| **Civil** *(era "Comum" até a Aprovação 032)* | Equipamento civil funcional: ferramenta, esporte, utilidade, material hospitalar, agrícola. |
| **Modificada** | Resultado do sistema de Modificações, feita pelo próprio grupo (ver §9). |
| **Militar** | Excedente militar pré-Queda. Confiável, bem feito, **sem efeito exótico**. É o piso do tier alto. |
| **Corporativa** | Tecnologia de quem causou o Colapso. **TODAS** têm efeito ativo, bateria, DRM ou telemetria. |
| **Protótipo** | Peça única. Efeito marcante com custo marcante. O equivalente a lendária, sem magia. |

---

## 2.1. Raridade — quão difícil é ACHAR (Aprovação 032)

**Tier e raridade medem coisas diferentes.** O tier responde *de onde a arma veio e quão bem foi
feita*; a raridade responde *quão difícil é encontrá-la*. As duas se correlacionam, mas não são
hierarquia: uma katana é Militar e **Rara**; uma Carabina M-24 é Militar e só **Incomum**, porque
excedente militar existe aos montes. A escala completa e as tabelas de saque moram em
`docs/gdd/GDD_Saque.md`.

| Tier | Raridade padrão |
|---|---|
| Improviso | **Abundante** |
| Civil | **Comum** |
| Modificada | *não se acha — o grupo fabrica* |
| Militar | **Incomum** |
| Corporativa | **Raro** |
| Protótipo | **Épico** |

**Exceções** — onde achar é mais difícil do que o tier sugere:

| Arma | Tier | Raridade | Por quê |
|---|---|---|---|
| Pistola pesada · SMG · Carabina · Rifle de caça · Espingarda | Civil | **Incomum** | Arma de fogo é escassa no mundo; atirar é decisão |
| **Rifle de precisão** | Civil | **Raro** | Civil de origem, raríssimo de achar |
| Besta de Caça · Arpão Pneumático de Pesca | Civil | **Incomum** | Equipamento de nicho |
| **Katana** | Militar | **Raro** | *"Uma espada de verdade num mundo de sucata não se acha numa garagem"* |
| Metralhadora · Besta Pesada | Militar | **Raro** | Pesadas e disputadas |
| **Fuzil "Testemunha"** | Corporativa | **Épico** | O topo do arsenal corporativo |
| **"Miséria" · "Boca de Forno"** | Corporativa | **Mítico** | A antiga raridade extrema (§7.4) |
| **"Segunda Boca" · "Ferro de Marca"** | Protótipo | **Mítico** | A antiga raridade extrema (§7.4) |

**Pistola leve e Revólver ficam Comum** — são a arma de fogo que o sobrevivente comum carrega. O
**Punho** não tem raridade.

> **Mítico nunca cai de tabela.** É o nome novo da **raridade extrema**: as quatro armas que mexem
> na Trilha de Infecção continuam sendo **decisão exclusiva do Diretor**, como o canon fixou.

---

## 3. Propriedades de arma (24 canônicas)

| Propriedade | Efeito mecânico | Origem |
|---|---|---|
| **Ágil** | Pode usar AGI no lugar de FOR no ataque e no dano. | Aprov. 006 |
| **Leve** | Ocupa meio slot de inventário. | Aprov. 006 |
| **Pesada** | Exige FOR mínima (12 a 16, por arma). Abaixo dela, desvantagem no ataque. | Aprov. 009 |
| **Duas mãos** | Ocupa as duas mãos. Sem escudo nem item na outra. | Aprov. 006 |
| **Lenta** | Após atacar, perde a Reação até o início do próximo turno. | Aprov. 006 |
| **Improvisada** | Não soma o bônus de proficiência ao ataque. | Aprov. 006 |
| **Utilitária** | Serve como ferramenta: vantagem em testes de FOR para arrombar. | Aprov. 006 |
| **Arremessável (X/Y)** | Arremessável a X/Y hexágonos, usando o mesmo atributo do ataque corpo a corpo. | Aprov. 006 |
| **Alcance 2 hex** | Ataca a até 2 hexágonos, SEM ficar adjacente ao alvo. | Aprov. 006 |
| **Frágil** | Em um 1 natural, a arma quebra. | Aprov. 006 |
| **Flexível** | Uma ou duas mãos. Com duas mãos sobe UM degrau na escada de dados (teto 1d12). | Aprov. 007 |
| **Enganchar** | No acerto, em vez de somar o dano, mova o alvo 1 hexágono ou derrube-o. Alvos 2 categorias maiores são imunes. | Aprov. 009 |
| **Recarga** | Após atirar, exige 1 Ação para rearmar. Não pode atacar e recarregar no mesmo turno. | Aprov. 009 |
| **Cone (X hex)** | Afeta um cone de X hex. Sem rolagem de ataque: cada alvo testa resistência; falha = dano cheio, sucesso = metade. | Aprov. 009 |
| **Acoplada** | Ocupa o slot de modificação de uma arma de fogo hospedeira. Ataca em corpo a corpo sem gastar a interação livre. | Aprov. 009 |
| **Dupla Face** | Escolha entre dois tipos de dano ao declarar. O Nível de Ruído segue o tipo escolhido. | Aprov. 009 |
| **Transfixante (X)** | Reduz em X o bônus de cobertura do alvo, mínimo 0. NÃO permite atacar quem está em cobertura total. | Aprov. 009 |
| **Estacar** | Como Reação: quando uma criatura entra no seu alcance de 2 hex, ataca-a. Só se você não se moveu no turno anterior. | Aprov. 009 |
| **Enxertada** | Não pode ser desarmada, guardada, roubada nem trocada. Você conta como SEMPRE armado. | Aprov. 009 |
| **Carga (N)** | Recurso do item, N cargas. **NÃO** é munição e não usa pool de calibre. **Repor 1 Carga custa 1 unidade do componente que a alimenta** — Célula de Energia (elétricas), Química (incendiárias), Peças Mecânicas (chamariz) — **só em Refúgio com bancada** ou pela Oficina de Campo do Cientista (`docs/gdd/GDD_Consumiveis.md` §3). **Absorveu *combustível* e *Energia da Célula* na Aprovação 028.** | Aprov. 009 · 028 |
| **Trilha de Calor (N)** | Cada disparo soma 1. Ventilar custa a Ação e remove 2. No teto, a arma desliga pela cena e causa o dano de sobrecarga. | Aprov. 009 |
| **Munição Exótica** | Consome pool próprio, fora dos 4 calibres. Só se fabrica no Refúgio. **LIMITE DE 2 ITENS NO JOGO INTEIRO.** | Aprov. 009 |
| **Espalhamento (X hex)** | Ao atacar alvo a 1–X hex, escolhe um segundo alvo adjacente e aplica a MESMA rolagem; metade dos dados, sem modificador. | Aprov. 009 |
| **Linha** | Ao acertar, a mesma rolagem se aplica a uma segunda criatura no hexágono imediatamente atrás. | Aprov. 009 |

> **NÃO EXISTE a propriedade "Confiável"** (nunca trava). Foi **rejeitada na Aprovação 009** e
> substituída por faixa reduzida a 1 natural confirmado — para não criar um recurso de turno morto
> nem pressionar a reabertura da Ação Bônus. Ver GDD_Combate §7.3.

---

## 4. Armas de corpo a corpo

Legenda: **Impr.** = a arma tem Improvisada, logo **não** soma proficiência — a coluna DPR já
desconta isso. (Esse defeito existia na v0.2 e superestimava armas improvisadas em ~16%.)

### 4.1. Tier Improviso

| Arma | Dado | Tipo de dano | Ruído | FOR mín. | Propriedades | Impr. | DPR |
|---|---|---|---|---|---|---|---|
| Improvisada (cano, tijolo) | 1d4 | Concussão | Baixo | — | Improvisada | sim | 2,875 |
| Martelo | 1d4 | Concussão | Baixo | — | Improvisada, Utilitária | sim | 2,875 |
| Garrafa Quebrada | 1d4 | Cortante | Silencioso | — | Ágil, Leve, Improvisada, Frágil, Arremessável (2/4) | sim | 2,875 |
| Antena de Carro | 1d4 | Cortante | Silencioso | — | Ágil, Leve, Improvisada, Frágil, Alcance 2 hex | sim | 2,875 |
| Corrente c/ Gancho | 1d6 | Perfurante | Silencioso | — | Duas mãos, Alcance 2 hex, Improvisada, Lenta, Enganchar | sim | 3,425 |
| Tampa de Bueiro | 1d6 | Concussão | Baixo | **14** | Duas mãos, Pesada, Improvisada, Lenta; cobertura parcial se não atacar | sim | 3,425 |
| Bateria de Carro c/ Garras | 1d6 | Elétrico/EMP | Baixo | **13** | Duas mãos, Pesada, Improvisada, Lenta, 3 cargas | sim | 3,425 |
| Lança Artesanal | 1d8 | Perfurante | Silencioso | — | Alcance 2 hex, Frágil | — | 4,725 |
| Extintor Vazio | 1d8 | Concussão | Baixo | **12** | Duas mãos, Pesada, Improvisada, Lenta | sim | 3,975 |

### 4.2. Tier Civil

| Arma | Dado | Tipo de dano | Ruído | FOR mín. | Propriedades | DPR |
|---|---|---|---|---|---|---|
| Cacetete | 1d6 | Concussão | Baixo | — | — | 4,075 |
| Faca / Facão | 1d6 | Cortante | Silencioso | — | Ágil, Leve | 4,075 |
| Machadinha | 1d6 | Cortante | Silencioso | — | Ágil, Arremessável (4/12) | 4,075 |
| Taco de Golfe (Ferro 7) | 1d6 | Concussão | Baixo | — | Ágil, Leve, Frágil | 4,075 |
| Tesoura de Poda de Altura | 1d6 | Cortante | Silencioso | — | Duas mãos, Alcance 2 hex, Utilitária, Frágil | 4,075 |
| Maçarico de Solda Portátil | 1d6 | Fogo | Baixo | — | Duas mãos, Alcance 2 hex, Utilitária, **Carga (6)** | 4,075 |
| Soqueira | 2d4 | Concussão | Baixo | — | Duas rolagens de acerto; mod. de dano SÓ no 1º golpe | 5,05 ⚠ |
| Pulverizador Costal | 1d4 | Químico | Baixo | — | Duas mãos, Cone (2 hex), Lenta | 3,425 |
| Seringa de Pressão Veterinária | 1d4 | Perfurante | Silencioso | — | Leve, Ágil, Frágil, Recarga | 3,425 |
| Taco de Baseball | 1d8 | Concussão | Baixo | — | Flexível (2 mãos: 1d10) | 4,725 |
| Pé de cabra | 1d8 | Concussão | Baixo | — | Utilitária | 4,725 |
| Foice de Ceifar | 1d8 | Cortante | Silencioso | — | Duas mãos, Lenta, Enganchar | 4,725 |
| Forcado de Feno | 1d8 | Perfurante | Silencioso | — | Duas mãos, Alcance 2 hex | 4,725 |
| Machado de bombeiro | 1d10 | Cortante | Baixo | **13** | Pesada, Duas mãos | 5,375 |
| Cilindro de Oxigênio | 1d10 | Concussão | Baixo | **14** | Duas mãos, Pesada, Lenta, Frágil (rompe: 2d6 em área) | 5,375 |
| Rebarbadora | 1d10 | Cortante | **ALTO** | **12** | Duas mãos, Pesada, Lenta, Utilitária, **Carga (4)** *(era "bateria 4 rodadas"; unificada pelo princípio da Aprov. 028)* | 5,375 |
| Marreta | 1d12 | Concussão | Baixo | **15** | Pesada, Duas mãos, Lenta | 6,025 |

⚠ A **Soqueira** usa 2d4 com **DUAS rolagens de acerto**; a coluna DPR trata o caso simplificado e
portanto **não é diretamente comparável** às demais.

A **Marreta** em 1d12 é o **topo mecânico do corpo a corpo**: DPR 6,025 no teto de dado absoluto.

### 4.3. Tier Modificada

Armas produzidas pelo grupo via sistema de Modificações (§9).

| Arma | Dado | Tipo de dano | Ruído | FOR mín. | Propriedades | Impr. | DPR |
|---|---|---|---|---|---|---|---|
| Cano c/ Arame Farpado | 1d8 | Concussão | Baixo | — | Improvisada (cano 1d4 + Arame Farpado, porte Pesado) | sim | 3,975 |
| Taco c/ Pregos | 1d10 | Concussão | Baixo | — | Flexível (2 mãos: 1d12); taco 1d8 + Pregos | — | 5,375 |

Os exemplos do Diretor fecham sozinhos no sistema de slots: taco 1d8 + Pregos (leve, 1 slot) = 1d10,
sobra 1 slot; cano 1d4 + Arame Farpado (pesada, 2 slots) = 1d8, consumindo os dois.
**Um cano enrolado em arame É a arma inteira.**

### 4.4. Tier Militar

| Arma | Dado | Tipo de dano | Ruído | FOR mín. | Propriedades | DPR |
|---|---|---|---|---|---|---|
| **Katana** | **1d8** | Cortante | Silencioso | — | **Ágil**, **Flexível** (duas mãos: 1d10) | 4,725 |
| Baioneta de Encaixe | 1d6 | Perfurante | Silencioso | — | Leve, Ágil; no rifle ataca sem gastar ação para sacar | 4,075 |
| Tonfa de Choque Antimotim | 1d6 | Concussão | Baixo | — | Ágil, 4 cargas: alvo perde Reação, cibernética falha 1 rodada | 4,075 |
| Escudo Antimotim Eletrificado | 1d6 | Concussão | Baixo | **13** | Pesada, Lenta; empurra 1 hex; cobertura parcial | 4,075 |
| Cambão de Contenção | 1d4 | Concussão | Baixo | — | Duas mãos, Alcance 2 hex, Enganchar (imobiliza sem dano) | 3,425 |
| Pá de Trincheira Afiada | 1d8 | Cortante | Silencioso | — | Utilitária, Arremessável (2/4) — 1d8 em UMA mão | 4,725 |
| Pistola de Pinos de Sapador | 1d8 | Perfurante | **ALTO** | — | Alcance 2 hex, Recarga, Enganchar (prega na superfície) | 4,725 |
| Granada de Atordoamento | 1d4 | Concussão | **ALTO** | — | Arremessável (4/8), Consumível; cega e ensurdece área | 3,425 |

> **A Katana entrou aqui na Aprovação 024, e estava faltando desde o CANON 017.** Ela existia em
> `docs/classes/Classe_Ceifador.md` §5.3 e na planilha, com DPR simulado, mas **nunca no catálogo** — foi a primeira
> vez neste projeto que a planilha esteve à frente dos documentos. Família: **Lâminas Longas**
> (migrou de Lâminas Curtas na mesma aprovação; a taxonomia da Aprovação 018 é por **tamanho de
> lâmina**). Justificativa canônica do tier: *"uma espada de verdade num mundo de sucata não se acha
> numa garagem"*.
>
> **Consequência medida, e ela não é neutra:** a **Foice de Ceifar** (§4.2) é **1d8 Cortante
> Silencioso** com *Duas mãos, Lenta, Enganchar*. A Katana é **o mesmo 1d8 Cortante Silencioso**, mas
> **Ágil** (usa AGI em vez de FOR), **sem Lenta**, e **1d10 em duas mãos** por Flexível. Em dado puro
> a Katana **domina a Foice**. O que salva a Foice é **Enganchar** — imobilizar sem dano é função que
> a Katana não tem, e é a única razão para continuar carregando uma. **Fica registrado como escolha
> consciente**, não como desequilíbrio a descobrir: a Foice é utilidade, a Katana é dano.

### 4.5. Notas de corpo a corpo

- **FOR mínima escala com MASSA E RECUO, não com dano.** A Rebarbadora de 1d10 exige 12; a Tampa de
  Bueiro de 1d6 exige 14.
- As células de FOR estão **editáveis**: o Diretor autorizou a faixa **12–16** e pode reajustar sem
  nova rodada de aprovação.
- **Armas de corpo a corpo NUNCA travam** — assimetria deliberada a favor delas (GDD_Combate §7.3).
  Exceção: cada modificação **Gambiarra** soma +1 à faixa de **quebra**, inclusive em corpo a corpo.
- Corpo a corpo de tiers **Corporativa** e **Protótipo** não tem linha de DPR na planilha: aparece
  apenas em §7, por efeito.

---

## 5. Armas silenciosas à distância

Legenda: **F.sust.** = fração dos turnos em que a arma consegue atacar. **0,5** significa Recarga =
1 Ação, disparando em turnos alternados.

| Tier | Arma | Dado | Tipo | Ruído | Propriedades | DPR | F.sust. | DPR sust. |
|---|---|---|---|---|---|---|---|---|
| Improviso | Fisga de Rolamentos | 1d4 | Perfurante | Silencioso | Leve, Duas mãos, Recarga, 6/12 hex | 3,425 | 1 | 3,425 |
| Comum | Arco Artesanal | 1d6 | Perfurante | Silencioso | 16/48 hex, munição recuperável | 4,075 | 1 | 4,075 |
| Comum | Dardo de Atletismo | 1d6 | Perfurante | Silencioso | Alcance 2 hex empunhado, Arremessável (6/12) | 4,075 | 1 | 4,075 |
| Comum | Besta de Caça | 1d8 | Perfurante | Silencioso | Duas mãos, Recarga, 10/20 hex | 4,725 | 0,5 | **2,3625** |
| Comum | Arpão Pneumático de Pesca | 1d8 | Perfurante | Baixo | Duas mãos, Recarga, 5/10 hex, projétil por cabo | 4,725 | 0,5 | **2,3625** |
| Militar | Besta Pesada | 1d10 | Perfurante | Silencioso | Duas mãos, Recarga, 20/60 hex, munição recuperável | 5,375 | 0,5 | **2,6875** |
| Militar | Lançador de Cabo de Abordagem | 1d6 | Perfurante | Baixo | Duas mãos, Recarga, 8/16 hex; cabo sustenta uma pessoa | 4,075 | 0,5 | **2,0375** |

- **O DPR bruto de uma arma com Recarga engana.** Use sempre a coluna **DPR sust.** para comparar com
  armas que atacam todo turno: a Besta Pesada de 1d10 rende **2,6875 sustentado**, menos que uma faca.
- A **Fisga de Rolamentos** tem Recarga mas F.sust. = 1 na planilha (ver §8.4, inconsistência
  registrada).
- **Besta Pesada** era chamada apenas "Besta" no canon original; **renomeada na Aprovação 010** para
  conviver com a Besta de Caça.

---

## 6. Armas de fogo

Legenda: **Tiros/alvo** = consumo esperado de munição para derrubar um alvo. **É a métrica que
importa para a economia, não o DPR.** Regras de munição, recarga e modos: GDD_Combate §7.1–§7.2.
(Valores de Tiros/alvo arredondados a duas decimais.)

### 6.1. Tier Civil

| Arma | Dado | Ruído | Alc. normal | Alc. longo | Pente | Modos | Silenciável | Munição | DPR | Tiros/alvo |
|---|---|---|---|---|---|---|---|---|---|---|
| Pistola leve | 1d6 | Médio | 12 | 36 | 12 | Único | Sim | Leve | 4,075 | 4,91 |
| SMG | 1d6 | Médio | 8 | 24 | 30 | Único | Sim | Leve | 4,075 | 4,91 |
| Pistola pesada | 1d8 | Médio | 10 | 30 | 8 | Único | Sim | Pesado | 4,725 | 4,23 |
| Carabina | 1d8 | Alto | 20 | 60 | 20 | Único, **Rajada** | Sim | Rifle | 4,725 | 4,23 |
| Revólver | 1d10 | Alto | 8 | 24 | 6 | Único | **NÃO** | Pesado | 5,375 | 3,72 |
| Rifle de caça | 1d10 | Alto | 24 | 72 | 5 | Único | Sim | Rifle | 5,375 | 3,72 |
| Rifle de precisão | 1d12 | Alto | 40 | 120 | 5 | Único | Sim | Rifle | 6,025 | 3,32 |
| Espingarda | 2d6 | Alto | 4 | 12 | 6 | Único | **NÃO** | Cartucho | 6,35 ⚠ | 3,15 |

⚠ Ver §8.2: a Espingarda em 2d6 é o único item base acima do teto de DPR de 6,025.

### 6.2. Tier Militar

| Arma | Dado | Ruído | Alc. normal | Alc. longo | Pente | Modos | Silenciável | Munição | DPR | Tiros/alvo |
|---|---|---|---|---|---|---|---|---|---|---|
| Metralhadora | 1d8 | Alto | 24 | 72 | 50 | Automático (Classe) | **NÃO** | Rifle | 4,725 | 4,23 |
| Carabina M-24 "Régua" | 1d10 | Alto | 24 | 72 | 20 | Único, **Rajada** | Sim | Rifle | 5,375 | 3,72 |
| SMG M-11 "Costura" | 1d6 | Médio | 10 | 30 | 32 | Único, **Rajada (-1)** | Sim | Leve | 4,075 | 4,91 |
| Espingarda "Portaria" | 1d10 | Alto | 6 | 18 | 8 | Único, Espalhamento | **NÃO** | Cartucho | 5,375 | 3,72 |

### 6.3. Tier Corporativa

Todas têm efeito ativo, bateria, DRM ou telemetria. Efeitos completos em §7.2.

| Arma | Dado | Ruído | Alc. normal | Alc. longo | Pente | Modos | Silenciável | Munição | DPR | Tiros/alvo |
|---|---|---|---|---|---|---|---|---|---|---|
| Pistola "Fiador" | 1d10 | Médio | 12 | 36 | 10 | Único; DRM + Telemetria | Sim | Pesado | 5,375 | 3,72 |
| Fuzil "Testemunha" | 1d10 | Alto | 30 | 90 | 10 | Único; Marcação | Sim | Rifle | 5,375 | 3,72 |
| Lança-agulhas "Costureira" | 1d6 | Baixo | 12 | 36 | 12 | Único; +1d6 Químico | Sim | **Exótica** | 4,075 | 4,91 |
| Espingarda "Cordão" | 1d8 | Alto | 6 | 18 | 6 | Único; cartucho de contenção | **NÃO** | Cartucho | 4,725 | 4,23 |
| Emissor EMP "Apagão" | 1d8 | Baixo | 3 | 3 | 3 | Cone 3 hex; Carga (3) | n/a | Carga | 4,725 | 4,23 |

### 6.4. Tier Protótipo

| Arma | Dado | Ruído | Alc. normal | Alc. longo | Pente | Modos | Silenciável | Munição | DPR | Tiros/alvo |
|---|---|---|---|---|---|---|---|---|---|---|
| "Vigília" eletromagnético | 1d10 | Baixo | 24 | 72 | 0 | Único; Trilha de Calor (5) | n/a | Sucata ferrosa | 5,375 | 3,72 |
| "Cantor" dardo chamariz | 1d6 | Silencioso | 12 | 12 | 2 | Chamariz; Carga (2) | n/a | Carga | 4,075 | 4,91 |
| "Ariete" antimaterial 20mm | 1d12 | Alto | 40 | 120 | 1 | Único, Lenta, Linha | **NÃO** | **Exótica** | 6,025 | 3,32 |

### 6.5. Notas de armas de fogo

- **Rajada é restrita a armas de calibre RIFLE** (Aprovação 009). Em Rajada o DPR chega a **7,28** —
  **única exceção deliberada** ao teto, contida pela escassez do calibre.
- Em Rajada o crítico soma **UM dado adicional** em vez de dobrar: reduz o pico de **43 para 33** sem
  mexer na média.
- **Revólver não aceita silenciador por razão física:** o vão entre tambor e cano vaza gás e som.
- **"Vigília" teve o Ruído Silencioso NEGADO pelo Diretor** e ficou em **Baixo**, preservando a regra
  de que arma de fogo nunca silencia.

### 6.6. Calibres — pools compartilhados

| Calibre | Armas que usam | Nota de economia |
|---|---|---|
| **Leve** | Pistola leve, SMG, SMG M-11 "Costura" | Abundante. O calibre do sobrevivente comum. |
| **Pesado** | Pistola pesada, Revólver, Pistola "Fiador" | Intermediário. |
| **Rifle** | Carabina, Carabina M-24, Metralhadora, Rifle de caça, Rifle de precisão, Fuzil "Testemunha" | Escasso e disputado. **Único calibre que permite RAJADA** — a escassez é o freio do DPR de 7,28. |
| **Cartucho** | Espingarda, Espingarda "Portaria", Espingarda "Cordão" | Pool isolado. Achar cartucho só serve para quem tem espingarda. |
| **Exótica** | Lança-agulhas "Costureira", "Ariete" | **LIMITE DE 2 ITENS NO JOGO INTEIRO.** Não se saqueia: só se fabrica no Refúgio. |

Pools compartilhados transformam saque em decisão: 20 de calibre Rifle vale muito para quem tem
carabina e nada para quem só tem revólver.

> **Módulo pendente (pedido do Diretor):** *tipos* de munição (balas, dardos, flechas, cartuchos) e
> *melhorias* de munição (dardos explosivos, flechas envenenadas). A planilha cobre apenas os
> **pools de calibre**.

---

## 7. Tier alto — efeitos mecânicos

O poder aqui é **efeito**, não dado. Texto de efeito e de custo/risco preservados integralmente.

> **Status:** `CANON` = liberado. `PENDENTE` / `CONGELADO` = **NÃO liberado para mesa** até a
> dependência existir.

### 7.1. Tier Militar

| Arma | Dado | Dano | Efeito mecânico | Custo / Risco | Status |
|---|---|---|---|---|---|
| Baioneta-Adaptador M7 | 1d8 | Perfurante | **Acoplada:** ocupa o slot de modificação da carabina. | Disputa o slot com o silenciador. A decisão É a arma. | **CANON** |
| Pá de Sapador | 1d10 | Cortante ou Concussão | **Dupla Face:** escolhe o tipo ao declarar o ataque; o Ruído segue o tipo escolhido. | Duas mãos, sem alcance estendido. | **CANON** |
| Machado "Corta-Anteparo" | 1d8/1d10 | Cortante | **Transfixante (2):** reduz em 2 o bônus de cobertura do alvo. Flexível. | Só se aplica se você estiver adjacente ao obstáculo — ou seja, a 1 hex do dano Necrótico. | **CANON** |
| Piqueta de Cerco M-3 | 1d8 | Perfurante | **Estacar:** ataque de Reação contra quem entra no seu alcance de 2 hex. | Lenta e Estacar são mutuamente exclusivos no mesmo turno. Só funciona parado. | **CANON** |

### 7.2. Tier Corporativa

| Arma | Dado | Dano | Efeito mecânico | Custo / Risco | Status |
|---|---|---|---|---|---|
| Soqueira "Volt-9" | 1d6 + 1d6 | Concussão + Elétrico | **Carga (6).** Gasta carga na interação livre ao acertar para somar o dado Elétrico. Contra alvo com cibernética o dado sobe um degrau e o alvo testa CON ou fica Atordoado. | DPR **6,35** carregada contra **4,08** vazia — o decaimento visível É o design. Em hexágono molhado a descarga atinge também você: 1d6 sem teste. | **CANON** |
| Cauterizador "Miséria" | 1d8 | Fogo | **Modo campo:** remove 2 pontos da Trilha de Infecção de si ou de aliado a 1 hex. | Custa a Ação inteira e causa 1d4 de Fogo irredutível. **RARIDADE EXTREMA.** | **CANON** |
| Serra "Denteira" | 1d8 | Cortante | **Serrilha:** aplica 1 camada de Sangrando ao acertar, 2 no crítico. Cada camada = **1 de dano** no início do turno do alvo, **teto 5** (Aprov. 028). | Ruído **MÉDIO**: é o único corpo a corpo que paga Infecção E Horda. **+8% contra alvo comum, +40% contra o Gigante** — é arma de chefe. | ✅ **CANON** |
| Pistola "Fiador" | 1d10 | Balístico | **DRM neural:** autenticada dá +1 no ataque e travamento reduzido; negada dá Desvantagem e faixa de travamento 1–5. Telemetria soma ponto ao contador de Rastreio do Mestre. | O token expira e precisa ser rearrombado. A melhor pistola do jogo denuncia sua posição a quem a fabricou. | **CANON** |
| Fuzil "Testemunha" | 1d10 | Balístico | **Marcação:** usando a Ação Mirar e gastando carga, o alvo fica Marcado e todo aliado com linha de visão trata o bônus de cobertura dele como 0. | Mirar custa a Ação inteira. E a marca é um ponto vermelho visível: NPC inteligente corre para cobertura total. | **CANON** |
| Lança-agulhas "Costureira" | 1d6 + 1d6 | Perfurante + Químico | Aplica Envenenado ao acertar alvo orgânico. Munição Exótica. | Contra alvo não orgânico o dado Químico não é rolado. Munição só se fabrica no Refúgio. | **CANON** |
| Espingarda "Cordão" | 1d8 | Concussão | **Cartucho de contenção:** sem dano; o alvo testa FOR ou fica Agarrado com movimento 0. | Cartucho de contenção e letal compartilham o tubo; trocar exige a Ação Recarregar. Agarrado NÃO impede garras. | **CANON** |
| Emissor EMP "Apagão" | 1d8 | Elétrico/EMP | **Carga (3).** Cone de 3 hex; alvos com cibernética que falharem perdem a Reação e ficam com implantes offline. | NÃO distingue amigo de inimigo. Se você tem cibernética e o cone começa em você, você está na área. | **CANON** |

### 7.3. Tier Protótipo

| Arma | Dado | Dano | Efeito mecânico | Custo / Risco | Status |
|---|---|---|---|---|---|
| "Cantor" dardo chamariz | 1d6 | Perfurante | Cria evento sonoro Nível 2 a partir de OUTRO hexágono por 3 rodadas. Enquanto ativo, o Medidor de Horda não sobe por ruído do grupo e o Mestre subtrai 2 pontos por rodada. | Puxa a horda para um ponto do mapa — que pode ficar entre o grupo e a saída. Pode trazer MAIS inimigos do que você enfrentaria sem ele. | **CANON** |
| "Vigília" eletromagnético | 1d10 | Perfurante | Munição = qualquer sucata ferrosa, sem consumir pool de calibre. **Trilha de Calor (5):** ventilar custa a Ação e remove 2; no teto a arma desliga pela cena e causa 2d6 de Fogo no portador. | Ruído **BAIXO**, não Silencioso — o Diretor negou a exceção para preservar a regra canônica. | **CANON** |
| "Segunda Boca" braço-serra | 1d8 + 1d4 | Cortante + Necrótico | **Enxertada:** não pode ser desarmada nem guardada. **Absorção:** abater um mutante cura 1d6 HP e dá 2 pontos de Infecção. | Você conta como sempre armado, inclusive quando quer parecer desarmado. E seus testes de CON contra Infecção passam a ter Desvantagem PARA SEMPRE. **RARIDADE EXTREMA.** | **CANON** |
| "Boca de Forno" lança-chamas | 1d8 | Fogo | Cone de 3 hex; cria hexágonos em chamas por 2 rodadas que mutantes não entram voluntariamente. Cadáver queimado não gera Infecção no saque. | O tanque está nas suas costas: dano de Fogo ou um crítico o rompe, causando 2d6 em raio de 2 hex. **RARIDADE EXTREMA.** | **CANON** |
| "Ariete" antimaterial 20mm | 1d12 | Balístico | **Linha:** ao acertar, a mesma rolagem se aplica a uma segunda criatura no hexágono atrás. | Pesada FOR 16, Lenta, Munição Exótica, 1 tiro a cada 2 turnos. A Perfuração Estrutural foi CORTADA do MVP. | **CANON (reduzida)** |
| "Jugo" bastão neural | 1d6 + 1d8 | Concussão + Elétrico | **Subjugar:** força alvo com cibernética a se mover 2 hex na direção escolhida. | Cada uso causa 1d4 em você e soma 1 Eco; em 3 Ecos seus próprios implantes ficam Atordoados. Você desliga junto com o alvo. | **CANON** |
| "Ferro de Marca" lâmina indutiva | 1d8 + 1d4 | Cortante + Fogo | **Carga (10). Cauterizar de Reação:** zera os pontos de Infecção de um ataque sofrido. | Custa 1d6 de Fogo irredutível e a Reação — competindo com o ataque de oportunidade. **RARIDADE EXTREMA.** | **CANON** |
| "Extrator" arpão de resgate | 1d8 | Perfurante | **Cabo:** ao acertar, arrasta o alvo 4 hex ou puxa você para junto dele. | Se o alvo for **Grande ou Enorme**, ELE arrasta você e você fica **Agarrado**. | ✅ **LIBERADO** (Aprov. 025) |

### 7.4. As quatro armas que mexem na Trilha de Infecção — RARIDADE EXTREMA *(hoje: **Mítico**, §2.1)*

**Miséria, Segunda Boca, Boca de Forno e Ferro de Marca** são de **RARIDADE EXTREMA**
(Aprovação 009). Isso **não é sabor**: é a única trava que impede a Trilha de Infecção (GDD_Combate
§9) de ser deflacionada.

> **Três removem, uma faz o contrário.** Miséria, Boca de Forno e Ferro de Marca são ferramentas
> de **remoção** ou de **prevenção** de Infecção. A **"Segunda Boca"** não é: ela **concede 2 pontos
> de Infecção por abate** e impõe **Desvantagem permanente** nos testes de CON contra Infecção. Ela
> está neste grupo porque **interage** com a Trilha e porque a interação é forte o bastante para
> exigir raridade extrema — não porque alivie a Trilha. É a única das quatro que **piora** a condição
> de quem a usa, e isso é o desenho dela: horror corporal traduzido em matemática.

**A distribuição dessas quatro armas é decisão exclusiva do Diretor.** A escassez resolve a deflação
sem criar regra proibitiva e sem parecer que o sistema está contra o jogador.

### 7.5. Teto do tier alto

- **Teto de dado 1d12 absoluto.** O poder de tier alto vem de EFEITO, nunca de dado maior.
- **Dado secundário tem teto de 1d6.**
- **Nenhuma arma de dois tipos de dano pode ser calibrada antes de a TABELA DE RESISTÊNCIAS existir**
  (GDD_Combate §6.3, `[A CALIBRAR]`) — porque dois tipos de dano **contornam resistência de tipo
  único**, que é o mecanismo da armadura balística.

---

## 8. Notas de balanceamento

### 8.1. Precedência de Ruído (CANON, Aprovação 009)

Para armas que caem em mais de uma categoria:

> ### **PESADA vence CONCUSSÃO, que vence CORTANTE / PERFURANTE / LEVE.**

Ou seja: **se é Pesada, o Ruído é Baixo**, qualquer que seja o tipo de dano. Peso faz mais ruído que
impacto, e impacto faz mais ruído que corte. **Uma foice de duas mãos é Silenciosa; uma marreta é
Baixo.**

| Nível | Valor | Raio (hex) | Raio (m) | Pts no Medidor |
|---|---|---|---|---|
| Silencioso | 0 | — | — | 0 |
| Baixo | 1 | 4 | 6 | 1 |
| Médio | 2 | 20 | 30 | 3 |
| Alto | 3 | 50 | 75 | 6 |

Regras de atração, Medidor de Horda e silenciadores: `docs/gdd/GDD_Ruido.md` / `docs/gdd/GDD_Horda.md`. Para armas de curta distância
**não** corpo a corpo: tensão mecânica = Silencioso, pneumático/motorizado = Baixo, carga
pirotécnica/explosiva = Alto. **Silenciador reduz 1 degrau e NUNCA zera** — arma de fogo silenciada
continua mais barulhenta que uma faca. Limiar do Medidor de Horda: `[A CALIBRAR]`.

### 8.2. O teto de DPR

Com os parâmetros de §1.2, o teto prático de DPR de item base é **6,025** (Marreta 1d12, Rifle de
precisão 1d12, "Ariete" 1d12).

| Caso | DPR | Situação |
|---|---|---|
| Teto de dado (1d12, item base) | **6,025** | Referência |
| **Rajada** (calibre Rifle) | **7,28** (+21%) | **Exceção canônica autorizada**, contida pela escassez do calibre Rifle |
| Espingarda (2d6) | **6,35** | Acima de 6,025 e **não** declarada como exceção na planilha — ver §8.4 |
| Soqueira "Volt-9" carregada | **6,35** | O decaimento de carga (6,35 → 4,08) é declaradamente o design |
| Soqueira comum (2d4) | **5,05** | Não comparável: duas rolagens de acerto |

### 8.3. Itens congelados, pendentes e cortados — NÃO liberados

| Item | Status | Bloqueio |
|---|---|---|
| Serra "Denteira" | ✅ **LIBERADA** (Aprovação 028) | Sangrando fechado em `docs/gdd/GDD_Combate.md` §10 e §10.2: **1 ponto por camada, teto 5** |
| "Extrator" arpão de resgate | ✅ **LIBERADO** (Aprovação 025) | As categorias de tamanho existem em `docs/gdd/GDD_Combate.md` §14; alvos Grande e Enorme existem em `docs/gdd/GDD_Bestiario.md` |
| "Ariete" — Perfuração Estrutural | ✂ **CORTADA do MVP** | A arma é CANON apenas na versão reduzida |
| Propriedade "Confiável" | ❌ **REJEITADA (Aprov. 009)** | Substituída por faixa reduzida a 1 natural confirmado |
| Todas as armas de **dois tipos de dano** | ⚠ **Não calibráveis** | Dependem da Tabela de Resistências (GDD_Combate §6.3) |

**Três dos cinco gargalos originais foram fechados. Ficaram dois:**

| Número | Estado |
|---|---|
| Pontos de Infecção por golpe de mutante | ✅ **FECHADO** — 1 ponto; 2 no crítico (Aprov. 014) |
| Limiar do Medidor de Horda | ✅ **FECHADO** — 20, em escada (Aprov. 014) |
| HP por classe | ✅ **FECHADO** — dado de vida por classe, HP nível 1 = máximo do dado + mod. CON (Aprov. 016) |
| **Tabela de resistências** por tipo de dano | ⛔ **ABERTO** — trava todas as armas de dois tipos de dano |
| **Dano por camada de Sangrando** | ✅ **FECHADO** (Aprovação 028) — **1 ponto por camada, teto 5**, no início do turno do alvo |

Para os dois que continuam abertos, **afirmações sobre "X está forte demais" seguem sendo opinião, não
medição.** Para os três fechados, a medição existe: ver `docs/gdd/GDD_Infeccao.md`, `docs/gdd/GDD_Horda.md` e os
documentos `Classe_*.md`.

### 8.4. Inconsistências registradas na planilha (não corrigidas)

Divergências entre abas, deixadas como estão para decisão do Diretor:

| # | Divergência |
|---|---|
| 1 | **Espingarda 2d6 → DPR 6,35** rompe o teto de 6,025 sem ser declarada exceção; a aba `Leia-me` afirma que a Rajada é a "única exceção". |
| 2 | **Baioneta:** `Corpo a Corpo` traz "Baioneta de Encaixe" em **1d6**; `Tier Alto` traz "Baioneta-Adaptador M7" em **1d8**. Nome e dado divergem. |
| 3 | **Pá:** `Corpo a Corpo` traz "Pá de Trincheira Afiada" em **1d8** (Cortante); `Tier Alto` traz "Pá de Sapador" em **1d10** (Dupla Face). Nome e dado divergem. |
| 4 | **Soqueira:** `Corpo a Corpo` traz a Soqueira comum em **2d4**; `Tier Alto` traz a "Volt-9" em **1d6 + 1d6**. Sem linha de linhagem entre as duas. |
| 5 | **Sem linha de stats em nenhuma aba de DPR:** Machado "Corta-Anteparo", Piqueta de Cerco M-3, Serra "Denteira", Cauterizador "Miséria", "Segunda Boca", "Boca de Forno", "Jugo", "Ferro de Marca", "Extrator". Existem só em `Tier Alto`. |
| 6 | **"Cantor" tem Ruído Silencioso** na aba `Armas de Fogo`, contra a nota da própria aba de que "arma de fogo nunca silencia" (razão pela qual o "Vigília" foi travado em Baixo). |
| 7 | **Rebarbadora = ALTO** e **"Denteira" = MÉDIO** são corpo a corpo acima de Baixo. A precedência de §8.1 não cobre corpo a corpo motorizado; ambos são exceções ad-hoc não formalizadas. |
| 8 | **Fisga de Rolamentos** tem **Recarga** nas propriedades mas **F.sust. = 1** (deveria ser 0,5 como as demais com Recarga). O DPR sust. de 3,425 provavelmente está superestimado. |
| 9 | **Seringa de Pressão Veterinária** também tem Recarga e F.sust. = 1 na aba `Corpo a Corpo`. |
| 10 | **Cano c/ Arame Farpado** declara "porte Pesado" nas propriedades mas tem a célula de **FOR mín. vazia** — Pesada exige FOR mínima por definição. |
| 11 | **Metralhadora** usa o modo "Automático (Classe)", que **não existe** na aba `Propriedades`. |
| 12 | **Espingarda "Portaria"** usa Espalhamento sem declarar o **X** em hex que a propriedade exige. |
| 13 | **"Ariete" FOR 16** aparece só no texto de custo/risco de `Tier Alto`; a aba `Armas de Fogo` não tem coluna de FOR mínima, então nenhuma arma de fogo tem FOR registrada de forma estruturada. |
| 14 | A aba `Corpo a Corpo` **não cobre os tiers Corporativa e Protótipo**, então nenhuma arma branca de tier alto tem DPR calculado. |

---

## 9. Modificações — resumo e ponteiro

> **Variações (Aprovação 034).** Uma arma achada com modificação já instalada é uma **variação** do
> item-base — o Taco c/ Pregos é uma variação do Taco de Baseball. **Armas variam só por modificação,
> nunca por material**, para que esta tabela de DPR continue sendo a fonte da verdade. A variação
> herda tier e raridade do base, e fica uma raridade acima se a modificação for de Oficina. Regras
> completas em `docs/gdd/GDD_Equipamentos.md` §7.

O tier **Modificada** (§4.3) é produzido pelo sistema de Modificações (aba `Modificacoes` da
planilha), aqui apenas resumido para explicar os degraus de dado:

- **Slots:** arma comum **2 slots**; arma especializada **3 slots** (rifle de precisão, besta,
  metralhadora).
- **Modificação ofensiva LEVE** = 1 slot, **+1 degrau** de dado. **PESADA** = 2 slots, **+2 degraus**.
- **REGRA CENTRAL DE CUSTO:** cada modificação **Gambiarra** (campo) soma **+1 à faixa de quebra** da
  arma. A de **Oficina** (Refúgio) **não** tem penalidade. Isso preserva a assimetria canônica de que
  corpo a corpo nunca trava: a arma **base** continua imune, só a **modificada** fragiliza.
- **Empilhar gambiarras é uma APOSTA, não uma progressão linear.** Quem quer stack precisa de
  Oficina, e Oficina precisa de **Liga Pré-Queda** — o gargalo proposital.
- **Falha crítica** (1 natural no teste de INT): material perdido e a arma cai 1 degrau de
  conservação.
- **Silenciador:** −1 nível de Ruído, por **30 disparos**. **Pano Abafador:** −1 nível, **só** em
  corpo a corpo de concussão.
- A Soqueira de raios se fabrica aqui: **Soqueira + Eletrodos = 2d4 Concussão + 1d4 Elétrico.**

Estado de conservação e faixas de travamento: aba `Conservacao` da planilha e GDD_Combate §7.3.

---

*Fim do catálogo. Regras em `docs/gdd/GDD_Combate.md`. Planilha-fonte: `Mutagen_Zero_Armamento.xlsx` v0.3.*
