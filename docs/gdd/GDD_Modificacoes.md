# MUTAGEN:ZERO — Módulo de Modificações de Arma

> **Regras Canônicas — Modificações.** As modificações, os componentes e a regra central de custo são
> **CANON** (Aprovações 001 a 010). Os **valores numéricos pendentes** aparecem como `[A CALIBRAR]`:
> implementadores devem tratá-los como configuração externa e **nunca** inventar valores padrão no motor.
>
> **Fonte da verdade:** `docs/Mutagen_Zero_Armamento.xlsx`, abas `Modificacoes` e `Componentes`. Este
> documento transcreve a planilha; em qualquer divergência, a planilha prevalece.

---

## 1. O Que É o Sistema e Por Que Ele Existe

O sistema de Modificações é o **tier "Modificada"** da escada de armamento — o único tier que o
grupo **fabrica**, em vez de saquear. Dos seis tiers (Improviso, Civil, **Modificada**, Militar,
Corporativa, Protótipo), Militar para cima só se encontra. Modificada só se constrói.

Isso resolve um problema estrutural do pós-apocalipse: sem fabricação, o poder de fogo do grupo é refém
da sorte de saque. O sistema dá uma **alavanca de progressão própria** — e cobra em material, tempo e risco.

### 1.1. A ligação com o Base Builder

Ele existe **em cima do Base Builder**, não ao lado: é a razão mecânica de construir um Refúgio.

| Elemento do Base Builder | O que ele destrava nas Modificações |
|---|---|
| **Refúgio com Oficina** | Acesso à via **Oficina** — a única sem penalidade de fragilidade (§7) |
| **Estoque de componentes** | O material que as duas vias consomem (§4) |
| **Gerador** | Disputa direta pelas **Células de Energia** (§4) |
| **Expedições de saque** | A **única** fonte de Liga Pré-Queda, insumo obrigatório da Oficina |

O laço fecha-se assim: **quem quer empilhar modificações precisa de Oficina; Oficina precisa de Liga
Pré-Queda; Liga Pré-Queda não se fabrica, só se encontra.** A cadeia inteira puxa o grupo **para fora** do
Refúgio. O Base Builder não é onde o grupo se esconde — é o que o obriga a sair.

---

## 2. As Duas Vias: Gambiarra e Oficina

Toda modificação existe em duas formas. **O efeito mecânico é idêntico nas duas.** Muda o custo em
material e o custo em risco.

| | **GAMBIARRA** (campo) | **OFICINA** (Refúgio) |
|---|---|---|
| **Onde** | Em qualquer lugar, em campo, na estrada | Somente em Refúgio com Oficina instalada |
| **Componentes** | Mais unidades, de escassez menor | Menos unidades, de escassez maior |
| **Liga Pré-Queda** | **Nunca** exige | **Quase sempre** exige |
| **Efeito mecânico** | Idêntico ao da Oficina | Idêntico ao da Gambiarra |
| **Penalidade** | **+1 à faixa de quebra da arma** (§7) | **Nenhuma** |
| **Empilhamento** | Aposta: cada camada fragiliza mais | Progressão limpa, limitada só por slots |
| **Falha crítica** | Material perdido + −1 degrau de conservação | Material perdido + −1 degrau de conservação |

**Leitura de design.** A Gambiarra é acessível e tóxica; a Oficina é limpa e cara. Um grupo nômade modifica
tudo e anda com um arsenal que se desfaz na mão. Um grupo sedentário com Oficina tem armas confiáveis e uma
lista de compras que o obriga a viajar. Não existe via superior: existe a via que o grupo pode pagar.

Duas modificações são **exclusivas de uma via**, deliberadamente: **Pano Abafador** só existe em Gambiarra
(é um trapo amarrado, não há o que industrializar) e **Peças Novas** só em Oficina (peça nova é peça nova).

---

## 3. Slots de Modificação

Cada arma tem um número fixo de **slots**. Slots gastos não voltam: modificação é permanente.

| Tipo de arma | Slots |
|---|---|
| **Arma comum** | **2** |
| **Arma especializada** (rifle de precisão, besta, metralhadora) | **3** |

**Ocupação de slots — canônica (Aprovação 013):**

| Tipo de modificação | Slots |
|---|---|
| Ofensiva de porte **Simples** | **1** |
| Ofensiva de porte **Estrutural** | **2** |
| Qualquer modificação **não ofensiva** (Precisão, Furtiva, Confiabilidade, Suporte) | **1**, salvo indicação contrária |

> **Este era um buraco que travava o sistema.** Até a Aprovação 013, só a família Ofensiva declarava
> porte, e as outras onze modificações não diziam quantos slots ocupavam — o que tornava impossível
> fechar qualquer build que usasse silenciador, mira ou guarda-mão. Agora fecha.

### 3.1. O silenciador é um caso particular disto

O **silenciador não é uma regra separada** — é uma modificação da família Furtiva como qualquer
outra, e o §12.4 do Módulo de Combate já diz o essencial: ele ocupa o slot de modificação da arma e disputa
espaço com qualquer outro acessório. Este documento só fecha o que faltava: o silenciador tem **receita,
componentes, CD de INT e via de fabricação** (§5), e, se feito como Gambiarra, **soma +1 à faixa de quebra**
(§7). Um silenciador improvisado não é só um consumível de 30 disparos — é uma arma que passa a travar.

> **Não duplicar.** Degraus de redução de Ruído, piso "Baixo" e comportamento do silenciador
> esgotado estão em **§12.4 do Módulo de Combate**; a escala de Ruído, em **§12.1**.

---

## 4. Os Oito Componentes

A lista é curta de propósito: **componente demais vira contabilidade em vez de decisão.**

| Componente | Escassez | O que é | Nota de economia |
|---|---|---|---|
| **Sucata** | Abundante | Metal torto, madeira, entulho, lata | Base de quase toda gambiarra |
| **Peças Mecânicas** | Comum | Molas, parafusos, engrenagens, canos, roscas | O componente mais versátil das cinco famílias |
| **Fiação** | Comum | Cabo, fio de cobre, isolamento | Porta de entrada das modificações elétricas |
| **Química** | Incomum | Solvente, adesivo, propelente, ácido | Consumida **por uso** na Ponta Incendiária |
| **Óptica** | Incomum | Lente, vidro tratado, visor | Gargalo das modificações de Precisão |
| **Eletrônicos** | Incomum | Placa, sensor, chip | **Não se fabrica:** só se desmonta de algo que já existia |
| **Célula de Energia** | Incomum | Bateria que ainda segura carga | Disputa com o gerador do Refúgio |
| **Liga Pré-Queda** | **RARO** | Aço e titânio de qualidade militar | **O GARGALO PROPOSITAL:** separa Gambiarra de Oficina. Não se fabrica, só se encontra |

> ### Reposição mora em outro arquivo (Aprovação 028)
>
> **O que se GASTA — Cargas, munição, soros — tem regras próprias em `docs/gdd/GDD_Consumiveis.md`.**
> Este documento é dono da **fabricação**; aquele é dono da **reposição**. A Aprovação 028 fechou ali
> três pendências que nasceram aqui: a reposição de `Carga (N)`, o consumo da **Energia da Célula**
> (que deixou de existir como termo separado e virou `Carga`) e a **disputa com o gerador do Refúgio**
> registrada em §9.2, item 4 — hoje resolvida em princípio: **um pool, duas bocas.** A Célula de
> Energia gasta em arma não alimenta o Refúgio, e vice-versa.

> ### Regra geral de produção (Aprovação 023)
>
> **Tudo que se fabrica consome componente.** Não existe produção gratuita no MUTAGEN, e isso vale
> **fora** das Modificações: vale para o **Soro de Campo** do Médico (**Química**), para munição
> artesanal, e para qualquer receita que módulos futuros venham a abrir.
>
> **Por que é regra e não caso a caso.** Uma habilidade que produz *"um por descanso longo"* sem custo
> de material tem, na prática, **produção infinita** — o descanso longo é renovável e o componente não
> é. O componente é o que transforma a frequência em **teto** em vez de piso, e é o que mantém a
> escassez como pressão de jogo em vez de decoração de ficha.
>
> **Consequência para implementadores:** nenhuma receita, presente ou futura, deve ter lista de
> componentes vazia. Uma receita sem custo declarado é **`[A CALIBRAR]`**, nunca "de graça".
>
> **Quantidades por receita são `[A CALIBRAR]`** — a regra fixa que existe custo, não quanto.

### 4.1. A Liga Pré-Queda é o gargalo, e é proposital

A Liga Pré-Queda **não é fabricável por nenhum meio, em nenhum tier, em nenhuma circunstância.** Não existe
receita, substituto nem conversão de Sucata em Liga. Ela só entra no estoque de um jeito: **alguém foi lá
fora e a trouxe.** Essa única restrição carrega três funções de design:

1. **Separa as vias.** Sem Liga não há Oficina de verdade, só gambiarra com teto melhor.
2. **Dá valor a território.** Um depósito militar, um hospital, uma fábrica viram objetivos de
   campanha, não cenário.
3. **Impede o Refúgio fechado.** Um grupo que nunca sai estagna mecanicamente, sem que o Mestre
   precise punir ninguém. A regra faz o trabalho.

> **Implementadores:** marcar Liga Pré-Queda no motor como recurso **não-fabricável**. Nenhuma
> receita, talento, evento ou recompensa automática pode gerá-la sem aprovação do Diretor. Taxa de
> aparição em saque por tipo de local: `[A CALIBRAR]`.

---

## 5. As Cinco Famílias e as 17 Modificações

São **17 modificações** em cinco famílias: **Ofensiva** (6 — sobe dado, muda tipo de dano ou anexa
dado extra), **Precisão** (3 — alcance e rolagem de ataque a distância), **Furtiva** (2 — Nível de
Ruído), **Confiabilidade** (3 — conservação e faixa de travamento) e **Suporte** (3 — defesa,
iluminação e economia de turno).

> **Por que "Suporte" e não "Utilitária".** "Utilitária" já é o nome de uma **propriedade de arma**
> (vantagem em testes de FOR para arrombar — ver Módulo de Combate). Usar a mesma palavra para uma
> família de modificação confundia busca e implementação, então a família foi renomeada na
> Aprovação 013.

### 5.1. Tabela completa — as 17 modificações

> Notação: `Sucata x2` = duas unidades de Sucata; `-` = a via não existe. A **CD INT** é a CD do
> teste de Inteligência exigido para fabricar (§7.4).

| Família | Modificação | Porte | Efeito | Gambiarra (campo) | Oficina (Refúgio) | CD INT |
|---|---|---|---|---|---|---|
| Ofensiva | **Pregos / Parafusos** | Simples | +1 degrau de dado | Sucata x2 | Sucata x1, Peças x1 | **10** |
| Ofensiva | **Cabeça Lastrada** | Simples | +1 degrau; a arma ganha **Lenta** | Sucata x2, Peças x1 | Peças x2, Liga x1 | **12** |
| Ofensiva | **Lâminas Soldadas** | Simples | +1 degrau; dano passa a **Cortante** (e o Ruído a Silencioso) | Sucata x2, Peças x1 | Liga x1, Peças x1 | **14** |
| Ofensiva | **Arame Farpado** | **ESTRUTURAL** | **+2 degraus de dado** | Sucata x3, Peças x1 | Sucata x2, Liga x1 | **12** |
| Ofensiva | **Ponta Incendiária** | Simples | +1d4 **Fogo**; consome 1 Química por combate | Química x2, Fiação x1 | Química x2, Peças x1 | **15** |
| Ofensiva | **Eletrodos** | Simples | +1d4 **Elétrico**; gasta Energia da Célula | Fiação x2, Eletrônicos x1, Célula x1 | Eletrônicos x1, Célula x1, Liga x1 | **16** |
| Precisão | **Mira Telescópica** | - | +50% no alcance normal | Óptica x2, Peças x1 | Óptica x1, Liga x1 | **14** |
| Precisão | **Designador Laser** | - | +1 no ataque a distância | Óptica x1, Eletrônicos x1, Célula x1 | Eletrônicos x1, Célula x1 | **16** |
| Precisão | **Coronha Estabilizada** | - | Remove a desvantagem no alcance longo | Sucata x2, Peças x2 | Peças x2, Liga x1 | **12** |
| Furtiva | **Silenciador** | - | −1 nível de Ruído, por **30 disparos** | Peças x2, Química x1 | Liga x1, Peças x1, Química x1 | **15** |
| Furtiva | **Pano Abafador** | - | −1 nível de Ruído, **só** em corpo a corpo de concussão | Sucata x1 | **- (não existe)** | **8** |
| Confiab. | **Recalibragem** | - | +1 degrau de conservação | Peças x2, Química x1 | Peças x1, Química x1 | **12** |
| Confiab. | **Peças Novas** | - | +1 degrau de conservação e **imune a queda por 1 sessão** | **- (só Oficina)** | Liga x1, Peças x2 | **15** |
| Confiab. | **Guarda de Ejeção** | - | Reduz em 1 a faixa de travamento | Peças x2 | Peças x1, Liga x1 | **14** |
| Suporte | **Guarda-mão** | - | +1 de Defesa em corpo a corpo; não perde a arma se desarmado | Sucata x2, Peças x1 | Liga x1, Peças x1 | **10** |
| Suporte | **Lanterna Acoplada** | - | Ilumina 4 hex à frente | Fiação x1, Célula x1 | Eletrônicos x1, Célula x1 | **10** |
| Suporte | **Alça Tática** | - | Trocar de arma deixa de custar a interação livre | Sucata x1 | Sucata x1, Peças x1 | **8** |

### 5.2. Notas de leitura da tabela

- **Lâminas Soldadas e Ruído.** A mudança para Cortante muda o Ruído **pela precedência canônica** (§12 do
  Módulo de Combate): PESADA vence CONCUSSÃO, que vence CORTANTE/PERFURANTE/LEVE. Soldar lâminas numa arma
  **Pesada** não a torna Silenciosa — o peso continua ganhando.
- **Ponta Incendiária** consome 1 Química **por combate**: único custo recorrente de componente do
  sistema. Sem Química no bolso, a modificação continua instalada e não funciona.
- **Eletrodos** e **Designador Laser** dependem de carga de Célula — o recurso que o gerador do
  Refúgio também quer. Consumo e recarga de Célula: `[A CALIBRAR]`.
- **Alça Tática** mexe na **interação livre com objeto** (§4.2 do Módulo de Combate); não concede
  Ação Bônus, cujo escopo continua fechado em um único uso (§7.3).

---

## 6. Os Dois Portes de Modificação Ofensiva: Simples e Estrutural

A escada de dados é **d4 → d6 → d8 → d10 → d12**, e o **teto é 1d12 ABSOLUTO** — acima dele os
degraus ficam irregulares (d12→2d6 rende só +5% de DPR; 2d6→2d8 salta 20% e trivializa o zumbi
comum). Consequência: **poder de tier alto vem de efeito, nunca de dado maior.**

| Porte | Slots | Efeito | Modificações |
|---|---|---|---|
| **Simples** | **1** | **+1 degrau** de dado | Pregos, Cabeça Lastrada, Lâminas Soldadas, Ponta Incendiária, Eletrodos |
| **ESTRUTURAL** | **2** | **+2 degraus** de dado | Arame Farpado |

> **Os portes mudaram de nome na Aprovação 012.** Antes chamavam-se "Leve" e "Pesada", o que colidia
> com as **propriedades de arma** de mesmo nome. São conceitos sem relação: a propriedade **Leve**
> diz que a arma ocupa meio slot de *inventário*; a propriedade **Pesada** exige **FOR mínima**. O
> porte **Estrutural** apenas consome 2 slots de *modificação*. Nada disso interage.

### 6.1. Os dois exemplos que fecham o sistema sozinhos

Os números de slot e de degrau foram escolhidos para que as duas armas canônicas do tier Modificada
saiam da aritmética sem regra especial nenhuma:

```
Taco de Baseball   1d8 Concussão, Flexível (2 mãos: 1d10), 2 slots
+ Pregos (Simples)    +1 degrau, 1 slot
= Taco c/ Pregos   1d10 Concussão, Flexível (2 mãos: 1d12)
                   Slots: 1 de 2 — SOBRA 1 SLOT

Improvisada (cano) 1d4 Concussão, Improvisada, 2 slots
+ Arame Farpado    +2 degraus, 2 slots (PESADA)
= Cano c/ Arame    1d8 Concussão, Improvisada (mantém: continua um cano)
                   Slots: 2 de 2 — CONSOME OS DOIS
```

**Por que isso é bonito.** O taco já era uma arma: modificá-lo é melhorá-lo, e ainda há espaço para
uma segunda decisão. **O cano enrolado em arame É a arma inteira** — um pedaço de tubo virou 1d8
porque não sobrou nada a mais para ser. A ficha conta a história sem que o texto precise contar.

O cano também **não perde Improvisada**: continua sem somar proficiência. Um 1d8 improvisado tem
DPR **3,975** contra os **4,725** de uma lança 1d8 não-improvisada. Gambiarra não apaga a origem da
arma.

### 6.2. O teto morde

Aplicar uma modificação ofensiva a uma arma já em **1d12** (Marreta) **não faz nada** ao dado: o
teto é absoluto. O slot é gasto, o material é gasto, e — se foi Gambiarra — a faixa de quebra sobe
do mesmo jeito. **Isto não é um defeito; é o freio.**

---

## 7. A Regra Central de Custo

> ### **Cada modificação GAMBIARRA soma +1 à FAIXA DE QUEBRA da arma.**
> ### **A modificação de OFICINA não tem penalidade alguma.**

Esta é a regra mais importante do documento. Tudo o mais é tabela.

### 7.1. Como a faixa de quebra funciona

> **QUEBRA e TRAVAMENTO são contadores distintos e nunca se somam** (Aprovação 013).
> **Travamento** é a arma emperrar: só arma de fogo, gatilho no `1` natural, modulado pelo estado de
> conservação, resolvido com 1 Ação Bônus. **Quebra** é a arma se partir: vem da propriedade
> **Frágil** e do `+1` que cada modificação Gambiarra acrescenta. Uma arma pode ter faixa de
> travamento 1 e faixa de quebra 2 ao mesmo tempo, sem que os números interajam. Armas de corpo a
> corpo **nunca travam** — mas modificadas em Gambiarra, **podem quebrar**.

A **faixa de quebra** é o intervalo de resultados naturais do d20 de ataque nos quais a arma
modificada **quebra ou trava**. Usa a mesma moeda numérica das faixas de travamento por
conservação, e por isso as probabilidades são diretamente comparáveis:

| Gambiarras na arma | Faixa de quebra | Quebra em (d20 natural) | P(quebra) por ataque |
|---|---|---|---|
| **0** (arma base, ou só Oficina) | **0** | **Nunca** | **0%** |
| **1** | **1** | `1` | **5%** |
| **2** | **2** | `1` ou `2` | **10%** |
| **3** | **3** | `1`, `2` ou `3` | **15%** |

A faixa aplica-se **inclusive em corpo a corpo**.

#### Uma rolagem, duas checagens independentes

Quebra e travamento **nunca se somam num número só**. O ataque é **uma** rolagem de d20, e o
resultado natural é conferido contra **duas faixas separadas**:

| Checagem | De onde vem | Vale para | Consequência |
|---|---|---|---|
| **Travamento** | Estado de conservação (§7.3 do Módulo de Combate) | **Só arma de fogo** | A arma emperra. Destravar custa **1 Ação Bônus** |
| **Quebra** | Propriedade **Frágil** + `+1` por modificação **Gambiarra** | Qualquer arma | A arma **se parte** |

**As duas podem acontecer no mesmo `1` natural.** Uma pistola Desgastada com uma gambiarra tem faixa
de travamento 2 e faixa de quebra 1: num `1` natural ela **trava e quebra ao mesmo tempo**; num `2`,
só trava. Isso não é acúmulo de números — são dois eventos distintos disparados pelo mesmo dado, e é
exatamente o que se espera de uma arma remendada que ninguém consertou de verdade.

> **A Guarda de Ejeção não entra em conflito com a Gambiarra.** Ela reduz em 1 a faixa de
> **travamento**; a Gambiarra soma `+1` à faixa de **quebra**. São contadores diferentes, então não
> há cancelamento: a arma fica mais confiável para disparar e mais frágil para durar, ao mesmo
> tempo.

### 7.2. O que essa única regra compra

**Primeiro: preserva a assimetria canônica de que armas de corpo a corpo nunca travam.** Esse privilégio é
deliberado e está na aba `Conservacao` como texto canônico. A regra de gambiarra **não o revoga** — abre uma
exceção estreita e voluntária: a arma **BASE** continua **imune**, sempre (um facão é um facão e não trava);
só a arma **MODIFICADA** fragiliza; e só se a modificação foi **GAMBIARRA**. A fragilidade **não é imposta
pelo sistema** — é comprada, de livre vontade, em troca de dano. Quem nunca improvisa nunca a sente.

**Segundo: transforma empilhar gambiarras numa APOSTA em vez de progressão linear.** Sem esta regra, a
estratégia ótima seria trivial: encher todos os slots de gambiarra, sempre, em tudo. Com ela, a segunda
camada já custa 10% de quebra por ataque — e uma arma que quebra em combate é pior do que uma arma fraca,
porque quebra **na pior hora possível**. A decisão deixa de ser "quanto posso encaixar" e passa a ser
"quanto risco aceito carregar hoje".

**Terceiro: é aqui que o sistema se fecha sobre o Base Builder.** A saída da aposta é única:

```
Quer stack limpo  →  precisa de OFICINA
Oficina           →  precisa de LIGA PRÉ-QUEDA
Liga Pré-Queda    →  não se fabrica, só se SAQUEIA
Saque             →  sair do Refúgio
```

Uma regra de uma linha, aplicada no lugar certo, **puxa o grupo inteiro para fora do Refúgio** sem incentivo
artificial, missão obrigatória nem castigo do Mestre.

### 7.3. Destravar custa Ação Bônus, não a Ação

Quando a faixa de quebra é cruzada em arma de fogo, aplica-se **§7.3 do Módulo de Combate** sem alteração:
**destravar custa 1 Ação Bônus** (Aprovação 003), não a Ação. Quem trava perde o ataque do turno, mas no
seguinte **destrava E ataca**: o custo total é de **1 turno, não 2**.

> **Escopo fechado da Ação Bônus.** A Ação Bônus existe no MVP com **um único uso aprovado:
> Destravar**. Nenhuma modificação deste documento concede, consome ou cria outro uso de Ação
> Bônus. Implementadores: criar o slot no motor e expor **somente** Destravar.

### 7.4. Falha crítica de fabricação

Fabricar exige um **teste de Inteligência** contra a CD da modificação (§5). Num **`1` natural** no
teste de INT:

> **O material é perdido E a arma cai 1 degrau de conservação.**

- Perde-se **todo** o material da receita. A modificação **não** é aplicada e os slots **não** são gastos.
- A queda segue a escada da aba `Conservacao`: **Calibrada → Boa → Desgastada → Arruinada**. Essa escada tem
  **quatro** estados, e a tabela de §7.3 do Módulo de Combate **também** — com os quatro nomes e
  valores fechados desde a Aprovação 006: Calibrada (~0,5%), Boa (5%), Desgastada (10%) e Arruinada
  (15%). A divergência de três nomes provisórios que existia aqui foi corrigida.
- Vale para **as duas vias**: Oficina não protege contra mão ruim, protege contra fragilidade estrutural.
- **Peças Novas** concede imunidade a queda de conservação por 1 sessão — a única proteção
  existente contra o segundo efeito da falha crítica.
- Resultado de uma falha **não-crítica** (teste falhado sem `1` natural): `[A CALIBRAR]`.

---

## 8. Exemplos de Construção Passo a Passo

### 8.1. A soqueira de raios — Soqueira + Eletrodos

O item assinatura do sistema, e o exemplo de que a Oficina vale a viagem.

```
PASSO 1 — Arma base
  Soqueira (tier Civil)   2d4 Concussão | Ruído Baixo | 2 slots
                          Duas rolagens de acerto; mod. de dano SÓ no 1º golpe
PASSO 2 — Escolher via
  GAMBIARRA: Fiação x2, Eletrônicos x1, Célula x1   → +1 à faixa de quebra
  OFICINA:   Eletrônicos x1, Célula x1, Liga x1     → sem penalidade
PASSO 3 — Teste de fabricação
  Teste de INT contra CD 16 (a CD mais alta do sistema, com o Designador Laser)
  Num 1 natural: material perdido + soqueira cai 1 degrau de conservação
PASSO 4 — Resultado
  SOQUEIRA DE RAIOS       2d4 Concussão + 1d4 Elétrico | gasta Energia da Célula
                          Slots: 1 de 2 usados — sobra 1
```

**Por que ela importa.** A Soqueira é 2d4, não 1d6: ganha o dado extra por **duas rolagens de acerto**, não
por dado maior. Acoplar Eletrodos adiciona um **segundo tipo de dano** — e tipo de dano é o que vale contra
resistências. É o princípio do teto de dado em ação: o poder veio de **efeito**, não de d12. Pela Gambiarra,
ela sai em campo com fio de cobre e uma placa de micro-ondas, e passa a quebrar em `1` natural — num item de
**duas rolagens por turno**, o que dobra a exposição ao risco. Pela Oficina, custa uma unidade de Liga que
alguém foi buscar num galpão militar, e nunca quebra. Mesmo item, dois jogos diferentes.

- **Aplicação do +1d4 Elétrico em arma com duas rolagens de acerto** (um golpe ou ambos):
  `[A CALIBRAR]`. Ver §9.

### 8.2. O taco do veterano — progressão em duas decisões

```
Taco de Baseball          1d8 Concussão | Flexível (2 mãos: 1d10) | 2 slots
+ Pregos, via OFICINA     Sucata x1, Peças x1 | CD 10 | 1 slot
= Taco c/ Pregos          1d10 Concussão | Flexível (2 mãos: 1d12) | faixa de quebra 0
+ Guarda-mão, via OFICINA Liga x1, Peças x1 | CD 10 | custo em slot: 1 (Aprovação 013)
= Taco completo           1d10 / 1d12 | faixa de quebra 0 | +1 de Defesa em corpo a
                          corpo; não se perde se desarmado
```

Arma de fim de campanha em corpo a corpo, sem um único ponto de fragilidade — e custou **1 Liga** e
duas CDs baixas. O caminho existe; só passa pelo Refúgio.

### 8.3. O cano do desesperado — a aposta assumida

```
Improvisada (cano)          1d4 Concussão | Improvisada | 2 slots
+ Arame Farpado, GAMBIARRA  Sucata x3, Peças x1 | CD 12 | 2 slots (PESADA)
= Cano c/ Arame Farpado     1d8 Concussão | Improvisada | slots 2 de 2 — cheio
                            Faixa de quebra 1 → quebra em 1 natural (5%)
```

Dano de arma Comum a partir de entulho, sem Refúgio. O preço: 5% de quebra por ataque e nenhum slot restante
para consertar isso depois. **É esse o negócio que a Gambiarra oferece.**

### 8.4. A pistola que o grupo não deveria ter modificado

```
Pistola leve, conservação Desgastada  →  faixa de travamento 2 (10%)
+ Silenciador, GAMBIARRA   Peças x2, Química x1 | CD 15 | 30 disparos e esgota
                           Ruído Médio → Baixo (§12.4 do Módulo de Combate)
                           +1 à faixa de quebra
= PLANILHA DECLARA:        faixa 3 → 15% de travamento por disparo
```

Uma em cada sete rolagens trava a arma. O grupo ganhou furtividade e comprou uma arma que para de funcionar
sozinha. **A leitura de design:** furtividade improvisada é caríssima, e a versão de Oficina do silenciador
— **Liga x1, Peças x1, Química x1** — é a única forma de ser silencioso **e** confiável.

---

## 9. Referências Cruzadas e Pendências

### 9.1. Regras que vivem em outro documento — não duplicar

| Assunto | Onde está |
|---|---|
| Travamento, gatilho e custo de destravar | **§7.3, Módulo de Combate** |
| Escopo fechado da Ação Bônus | **§2.4, Módulo de Combate** |
| Escala de Ruído, raios, Atração, Medidor de Horda | **§12.1 a §12.3, Módulo de Combate** |
| Silenciador (degraus, piso, esgotamento) e armas silenciosas nativas | **§12.4 e §12.5, Módulo de Combate** |
| Precedência de Ruído (Pesada > Concussão > Cortante) | Aba `Ruido`; §12, Módulo de Combate |
| Estados de conservação e P(trava) | Aba `Conservacao` |
| Propriedades de arma; pools de calibre; fórmula de DPR e teto de dado | Abas `Propriedades`, `Municao`, `Leia-me` |

### 9.2. Campos `[A CALIBRAR]` deste módulo

1. Resultado de uma falha **não-crítica** no teste de INT de fabricação.
2. **Tempo** de fabricação por via (turnos, cena, downtime) — não definido em lugar nenhum.
3. Se uma modificação pode ser **removida**, e a que custo.
4. Consumo e recarga de **Célula de Energia**, e a disputa com o gerador do Refúgio; taxa de
   aparição de **Liga Pré-Queda** em saque, por tipo de local.
5. **Lâminas Soldadas** promete tornar a arma Silenciosa, mas a precedência canônica faz arma
   **Pesada** ser sempre Baixo — soldar lâminas numa marreta não a silencia. Falta a frase de
   exceção que resolva a interação.

### 9.3. Pendências resolvidas pela Aprovação 013

Três itens que constavam como abertos foram fechados e estão incorporados ao texto acima:

- **Custo em slots das não ofensivas** → **1 slot**, salvo indicação contrária (§3).
- **Quebra × travamento** → são **contadores distintos que nunca se somam** (§7.1). Por isso a
  **Guarda de Ejeção** não se anula: ela reduz o **travamento**, enquanto a Gambiarra piora a
  **quebra**.
- **Eletrodos e Ponta Incendiária em armas de múltiplas rolagens** → o dado extra entra **uma vez
  só**, não a cada golpe. Uma Soqueira com Eletrodos é 2d4 Concussão **+ 1d4** Elétrico, não +2d4.
> **Nota:** o teto de modificações **por família** numa mesma arma, se houver, também segue aberto —
> está coberto pelo item 3 da lista de §9.2, junto com a questão da remoção.

---

*Fim do documento. As regras deste módulo são canônicas (Aprovações 001 a 010) e qualquer alteração exige
nova aprovação do Diretor de Criação. Os campos `[A CALIBRAR]` são o próximo ciclo de balanceamento.*
