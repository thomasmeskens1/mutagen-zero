# MUTAGEN:ZERO — Módulo de Combate

> **Regras Canônicas — Combate Tático.** As regras deste documento foram aprovadas pelo Diretor de
> Criação. Os **valores numéricos de balanceamento NÃO foram aprovados**: todo número em aberto
> aparece como `[A CALIBRAR]`. Implementadores devem tratar esses campos como configuração externa
> e **nunca** inventar valores padrão dentro do motor.

---

## 1. Visão Geral do Combate

Sistema **d20 tático em grid hexagonal**, desenhado para ser resolvido por um VTT. Três premissas:

1. **Uma rolagem decide cada teste.** `d20 + modificadores vs. CD`; sucesso se o total for **≥ CD**.
2. **A ordem do combate é estável.** A iniciativa é rolada uma vez e não muda mais.
3. **O perigo não acaba com o combate.** Dano necrótico deixa Infecção, resolvida *depois* da luta.

### 1.1. Regras de Núcleo

- **Modificador de atributo:** `floor((valor_do_atributo − 10) / 2)`.
- **Resolução:** `d20 + modificador [+ proficiência] ≥ CD` → sucesso.
- **Proficiência:** bônus de treino de **+2 a +6**, conforme o nível. Progressão: `[A CALIBRAR]`.
- **Vantagem:** role `2d20`, use o **maior**. **Desvantagem:** role `2d20`, use o **menor**.
- **Vantagem e Desvantagem NÃO acumulam.** Havendo ao menos uma fonte de cada, ambas se cancelam e
  o personagem rola **1d20 normal**, não importa quantas fontes existam de cada lado.
- **20 natural:** acerto crítico automático, independentemente da Defesa do alvo.
- **1 natural:** falha automática. Se o ataque foi com **arma de fogo**, a arma **trava** (§7.4).

> **Implementação.** "20 natural" e "1 natural" referem-se ao **dado efetivamente usado** depois de
> aplicar Vantagem/Desvantagem — não ao dado descartado.

---

## 2. Sequência de uma Rodada

### 2.1. Iniciativa

Cada combatente rola **`d20 + modificador de AGI`** uma única vez, no início do combate. A ordem
resultante é **FIXA pelo combate inteiro**; não há re-rolagem entre rodadas.

**Desempate**, nesta ordem: (1) maior **AGI** bruta; (2) **jogador antes de NPC**; (3) empate entre
dois jogadores ou dois NPCs — desempate aleatório do VTT.

### 2.2. Emboscada

O lado surpreendido **não age na 1ª rodada**. Os surpreendidos mantêm sua posição na ordem (o turno
apenas passa) e **não têm Reação** até o início do próprio turno na 2ª rodada. O lado emboscador age
normalmente desde a 1ª rodada. CD do teste de PER para detectar a emboscada: `[A CALIBRAR]`.

### 2.3. Estrutura do turno

| Momento | O que acontece |
|---|---|
| **Início do turno** | A Reação é reposta; disparam efeitos de "início de turno" (ex.: Sangrando). |
| **Corpo do turno** | O combatente gasta, em qualquer ordem e podendo intercalar: Movimento, a Ação e a interação livre. |
| **Fim do turno** | Disparam efeitos de "fim de turno"; faz-se o teste de morte, se em Estado Crítico. |

### 2.4. Economia do turno

| Recurso | Por turno | Reposição |
|---|---|---|
| Movimento | 9 m (6 hexágonos) | Início do próprio turno |
| Ação | 1 | Início do próprio turno |
| Reação | 1 | **Início do próprio turno** |
| Interação livre com objeto | 1 | Início do próprio turno |
| **Ação Bônus** | 1 (escopo restrito) | Início do próprio turno |

> **Ação Bônus em MUTAGEN:ZERO — escopo fechado.** Reincorporada por decisão do Diretor
> (Aprovação 003), revertendo a Aprovação 001. No MVP ela tem **um único uso aprovado: Destravar
> uma arma de fogo** (§7.3). Nenhum talento, item, arma ou classe concede outros usos sem aprovação
> explícita do Diretor.
> Implementadores: criar o slot no motor, mas expor somente a ação Destravar.

Como a Reação é reposta no início do *próprio* turno, quem a gasta logo após seu turno fica sem
Reação por quase uma rodada inteira. O movimento pode ser **fracionado** livremente (mover 2 hex,
Atacar, mover 4 hex é legal).

---

## 3. Atributos Aplicados ao Combate

São 6 atributos. Modificador = `(atributo − 10) / 2`, arredondado para baixo.

| Atributo | Sigla | Função geral | Uso direto em combate |
|---|---|---|---|
| Força | **FOR** | Poder físico, capacidade de carga | Ataque e dano corpo a corpo; Agarrar; empurrar |
| Agilidade | **AGI** | Reflexos, coordenação fina | **Iniciativa**; ataque e dano com armas de fogo; **Defesa**; teste contra fogo automático; armas Ágeis |
| Constituição | **CON** | Resistência orgânica | **HP**; resistir a Infecção, Radiação e Veneno |
| Inteligência | **INT** | Raciocínio, técnica | Investigação, tecnologia, hacking; dispositivos técnicos em combate |
| Percepção | **PER** | Atenção sensorial | Detectar ameaças, emboscadas e alvos escondidos |
| Carisma | **CAR** | Presença social | Ações sociais sob pressão (intimidar, parlamentar) |

Referência de modificadores: `8–9 → −1` · `10–11 → +0` · `12–13 → +1` · `14–15 → +2` · `16–17 → +3`
· `18–19 → +4`. Teto de atributo para personagens jogadores: `[A CALIBRAR]`.

---

## 4. Ações Detalhadas

Um combatente executa **exatamente uma Ação por turno**, escolhida desta lista fechada.

| Ação | Efeito mecânico |
|---|---|
| **Atacar** | Um ataque corpo a corpo ou à distância (§5). Uma única rolagem, salvo modo de disparo em contrário (§7.3). Não existe ataque extra neste MVP. |
| **Correr** | Ganha movimento extra igual ao movimento base (total de 18 m / 12 hex no turno). Não permite atacar no mesmo turno, pois Correr *é* a Ação. |
| **Desengajar** | O movimento **deste turno** não provoca ataques de oportunidade de **nenhum** inimigo. |
| **Esquivar** | Até o início do seu próximo turno: ataques contra você têm **Desvantagem** e você tem **Vantagem** em testes de AGI. Cancela-se se você ficar Incapacitado, Inconsciente ou com movimento 0. |
| **Ajudar** | Um aliado a até **1 hex (1,5 m)** — ou ao alcance do dispositivo usado — ganha **Vantagem** no próximo teste ou ataque dele, até o início do seu próximo turno. Não acumula com outra Vantagem. |
| **Esconder** | Teste de furtividade **oposto** à PER dos observadores. Escondido: **Vantagem no próximo ataque**, e o ataque revela você. Alvo que não pode ser visto é atacado com Desvantagem. Modificador por cobertura/terreno: `[A CALIBRAR]`. |
| **Usar Objeto** | Manipula um objeto quando a interação livre não basta: aplicar estimulante, ativar dispositivo, arrombar, estabilizar um aliado. |
| **Mirar** | Custa a **Ação** inteira. Concede **Vantagem** no próximo ataque à distância **e +2 de dano**, se você não se moveu. **Não** pode ser combinado com **Rajada** nem com **Automático** (Aprovação 002). |
| **Recarregar** | Repõe o carregador de uma arma de fogo (§7.2). Consome a Ação inteira. |

### 4.1. Reação

Uma Reação por turno, reposta no início do próprio turno. Cobre:

- **Ataque de oportunidade:** quando um inimigo visível sai do seu alcance corpo a corpo **sem**
  Desengajar, você faz **um** ataque corpo a corpo contra ele.
- Reações concedidas por talentos, cibernética ou equipamento: `[A CALIBRAR]`.

### 4.2. Interação livre com objeto

Uma por turno, sem custo de Ação: sacar ou guardar uma arma, abrir porta destrancada, soltar um
item, pegar um item adjacente no chão, apertar um botão ao alcance. Além disso, exige **Usar Objeto**.

---

## 5. Ataque e Defesa

### 5.1. Fórmula de ataque

```
Rolagem de ataque = d20 + modificador de atributo + proficiência (se proficiente na arma)
Acerta se: rolagem de ataque >= Defesa do alvo
```

| Tipo de ataque | Atributo usado |
|---|---|
| Corpo a corpo | **FOR** |
| Corpo a corpo com arma de propriedade **Ágil** | **FOR ou AGI**, à escolha do jogador |
| Arma de fogo | **AGI** |
| Arma de arremesso | `[A CALIBRAR]` — definir se usa FOR, AGI ou a propriedade da arma |

O atributo escolhido para o ataque é **o mesmo** aplicado ao dano daquele ataque.

### 5.2. Fórmula de Defesa

```
Defesa = 10 + modificador de AGI (limitado pela categoria) + armadura + escudo + cobertura
```

| Componente | Origem | Valor |
|---|---|---|
| Base | Fixa | **10** |
| Modificador de AGI | Atributo | `(AGI − 10) / 2`, **limitado pela categoria de armadura** (§5.3) |
| Armadura | Equipamento | **+1 a +7** (§5.3) |
| **Escudo** | Equipamento, exige **mão livre** | **+1 a +3** (§5.3) |
| Cobertura | Posicionamento | +2 / +5 / intocável (§5.4) |

**A armadura é a soma das peças de Corpo, Cabeça e Pernas**, com teto por espaço, e a categoria do conjunto é a da peça mais pesada (`docs/gdd/GDD_Equipamentos.md` §2, Aprovação 034). **Faixa prática de Defesa: 10 a 22.** Um personagem sem nada e de AGI 10 fica em **10**; um tanque
completo — AGI 14, armadura Pesada +7, escudo +3 — chega a **20**, e com meia cobertura a **22**.

> **O escudo é componente próprio da fórmula e exige mão livre.** Ele é incompatível com a
> propriedade **Duas mãos** (`docs/gdd/GDD_Armas.md` §3): a decisão de empunhadura passa a ser também uma
> decisão de Defesa.

### 5.3. Categorias de armadura (Aprovação 029)

| Categoria | Bônus de Defesa | Limite de mod. AGI | **FOR mínima** | Penalidade |
|---|---|---|---|---|
| **Nenhuma** | +0 | Sem limite | — | — |
| **Leve** | **+1 a +3** | Sem limite | — | — |
| **Média** | **+3 a +5** | Máximo **+2** | **12** | — |
| **Pesada** | **+5 a +7** | Máximo **+0** | **14** | Desvantagem em **Furtividade** |
| **Escudo leve** | **+1 a +2** | — | — | Ocupa uma mão |
| **Escudo pesado** | **+3** | — | **12** | Ocupa uma mão · Desvantagem em Furtividade |

**Sem a FOR mínima, a armadura não pode ser vestida.** Não há versão com penalidade: é um gate, não
um preço.

> ### Por que o limite de AGI é o freio, e não o bônus
>
> Um personagem de **AGI 16 (+3)** que veste **Pesada +7** perde os 3 de AGI e ganha 7: fica em
> **Defesa 17**. O mesmo personagem com **Leve +3** fica em **16**. Ganhou **1 ponto** e pagou com
> Desvantagem em Furtividade e FOR 14.
>
> Já um personagem de **AGI 10 (+0)** com Pesada +7 vai a **17** sem perder nada.
>
> **Armadura pesada não é "melhor": ela é a armadura de quem tem AGI baixa.** O limite faz a escolha
> depender da ficha, e não da tabela de preços.

### 5.3.1 A escala — ataque das criaturas por ND

A Defesa do jogador só significa alguma coisa em relação ao **ataque do inimigo**. Esta é a outra
metade do contrato, e o Bestiário a obedece:

| ND | Ataque | Defesa esperada do patamar | P(acerto) vs **equipado** | P(acerto) vs **pelado** |
|---|---|---|---|---|
| **0** | **+4** | 15 | 50% | 60% |
| **1** | **+5** | 16 | 50% | 65% |
| **2** | **+7** | 17 | 55% | 75% |
| **3** | **+8** | 18 | 55% | 80% |
| **4** | **+10** | 19 | 60% | **90%** |
| **5** | **+11** | 20 | 60% | **95%** |
| **6** *(Bloco 5)* | **+13** | 21 | 65% | 95% *(teto)* |
| **7** *(Bloco 5)* | **+14** | 21 | 70% | 95% *(teto)* |
| **8** *(Bloco 5)* | **+16** | 21 | 80% | 95% *(teto)* |
| **9** *(Bloco 5)* | **+17** | 21 | 85% | 95% *(teto)* |
| **10** *(Bloco 5)* | **+19** | 21 | 95% *(teto)* | 95% *(teto)* |

> **Extensão ND 6–10 (Aprovação 035, Bloco 5).** `Defesa esperada` para de subir em **21** — é o teto
> real de um grupo de Patamar 5 (§4.4); não existe Patamar 6 para "olhar adiante", como as linhas
> anteriores faziam (ND 5 já mirava um degrau acima do Patamar 3 em que vivia). O ataque continua a
> mesma progressão alternada **+1/+2** da tabela original (4·5·7·8·10·11 → 13·14·16·17·19), e o
> P(acerto) vs. equipado sobe de 65% a 95% — a mesma lógica: **quanto mais alto o ND, maior a distância
> entre personagem equipado e pelado**, porque é aí que o equipamento do Bloco 4b precisa provar seu
> valor.

> ### Medido: escalar os DOIS lados preserva a economia de atrito
>
> A Trilha de Infecção conta **acertos**, então subir a Defesa do jogador sem subir o ataque do
> inimigo desarmaria a moeda central do jogo. Medido em 8.000 iterações por linha, encontro padrão de
> 4 Zumbis:
>
> | Cenário | P(acerto) | Dano por PJ | **Infecção** |
> |---|---|---|---|
> | Sem armadura, zumbi **+3** *(a escala antiga)* | 55% | 3,5 | **4,03** |
> | Armadura **+3**, zumbi **+3** | 40% | 2,7 | 3,06 |
> | Armadura **+3**, zumbi **+6** | 55% | 3,5 | **4,01** |
> | Armadura **+6**, zumbi **+9** | 55% | 3,5 | **4,02** |
>
> **Com os dois lados escalando, a Infecção fica idêntica até a segunda decimal.** O que importa nunca
> foi o valor absoluto da armadura — é a **diferença líquida** entre a Defesa e o ataque do patamar.
>
> **E a armadura continua importando muito.** Um ponto líquido de vantagem vale 5% de acerto; sete
> pontos de armadura contra um ataque que não escalou derrubam o acerto de 55% para 40%, e a Infecção
> de 4,03 para 3,01.
>
> **A consequência mais importante está na última coluna da tabela de ND:** contra ND 5, o personagem
> sem armadura é acertado em **95%** das rolagens, enquanto o equipado fica em 60%. **A distância
> entre equipamento completo e improviso cresce com o ND** — é por isso que não existe teto de
> Defesa, e é por isso que o inimigo precisava escalar junto.

> **O teto de 1d12 não limita a criatura.** Ele é o teto do **dado de uma arma**
> (`docs/gdd/GDD_Armas.md` §1.1). Uma criatura pode ter `1d12 + 1d4`, `2d8+5`, ou duas ações — e as de ND
> alto têm. O teto protege a **tabela de armas**, não o Bestiário.

> **Nota importante: a tabela de DPR das ~76 armas NÃO se move.** Ela é calculada contra a Defesa
> **da criatura** (14, o Zumbi comum), que esta aprovação não toca. A escala mexe apenas no lado do
> jogador.

### 5.4. Cobertura

| Grau | Efeito |
|---|---|
| **Meia cobertura** | **+2** na Defesa |
| **Três quartos de cobertura** | **+5** na Defesa |
| **Cobertura total** | **Não pode ser alvo** de um ataque direto |

A cobertura é determinada pela linha de visão no grid hexagonal (§11.3). Apenas o grau **mais
favorável** se aplica; bônus de cobertura **não somam entre si**.

### 5.5. Ordem de resolução de um ataque

1. Declarar a Ação **Atacar**, a arma e o alvo.
2. Verificar linha de visão e alcance (§7.5); além do alcance normal → **Desvantagem**.
3. Somar todas as fontes de Vantagem e Desvantagem e **cancelar** o que se opõe (§1.1).
4. Rolar o ataque. `1` natural → falha automática (e travamento, se arma de fogo).
   `20` natural → acerto crítico automático, pulando o passo 5.
5. Comparar o total com a Defesa do alvo.
6. Em caso de acerto, rolar o dano (§6). Descontar munição (§7.2).
7. Aplicar reduções por tipo de dano, condições e efeitos derivados.

---

## 6. Dano e Crítico

### 6.1. Fórmula de dano

```
Dano = [dados da arma] + modificador do atributo usado no ataque
```

O modificador somado ao dano é **o mesmo** da rolagem de ataque: FOR no corpo a corpo, AGI em armas
de fogo e em armas Ágeis usadas com AGI.

### 6.2. Crítico

**No acerto crítico, DOBRAM-SE OS DADOS DE DANO, NÃO O MODIFICADOR.**

```
Dano crítico = (dados da arma x 2) + modificador (uma única vez)
```

Uma arma que causa `NdX + mod` causa, no crítico, `2NdX + mod` (notação estrutural; `N` e `X` são
`[A CALIBRAR]`). Dados extras de efeito — fogo, veneno, rajada — **também dobram**; bônus fixos **não**.

### 6.3. Tipos de dano

| Tipo | Descrição | Fonte típica | Nota mecânica |
|---|---|---|---|
| **Perfurante** | Penetração concentrada | Lâminas de ponta, lanças, flechas | — |
| **Cortante** | Corte aberto | Facões, serras, lâminas | Pode causar **Sangrando** |
| **Concussão** | Impacto contundente | Marretas, coronhadas, quedas | Pode causar **Atordoado** |
| **Balístico** | Projétil de arma de fogo | Pistolas, rifles, submetralhadoras | Interage com armadura balística |
| **Fogo** | Queimadura | Coquetéis, lança-chamas, incêndios | Permite dano contínuo por turno |
| **Químico** | Corrosão / toxina | Ácidos, gás, reagentes | Pode causar **Envenenado** |
| **Radiação** | Exposição radioativa | Zonas quentes, resíduos, armas sujas | Resistido com **CON**; causa **Irradiado** |
| **Elétrico/EMP** | Descarga ou pulso | Tasers, granadas EMP | Agrava-se contra implantes e drones |
| **Necrótico** | Degeneração de tecido vivo | **Mutantes e zumbis** | **Gera pontos de Infecção** (§9) |

#### Resistência, vulnerabilidade e imunidade — a escada é a moeda

> **Os quatro graus são canônicos (Aprovação 020)**, assim como a aplicação **por dado** e o **piso de
> 1d4**. Os **perfis por criatura** da tabela ao final desta seção são canon apenas para as quatro
> entradas listadas; **o Bestiário ainda não foi desenhado** e é ele que dirá quem mais usa cada grau.

**Resistência não corta o dano pela metade.** Ela move a arma na **escada de dados**:

| Grau | Efeito |
|---|---|
| **Vulnerável** | o dado **sobe um degrau** (respeitando o teto **1d12**) |
| *(normal)* | — |
| **Resistente** | o dado **desce um degrau** |
| **Muito Resistente** | o dado **desce dois degraus** |
| **Imune** | dano **0** |

**Piso:** uma arma já em **1d4** que sofra resistência perde **1 de dano** em vez de descer degrau
(mínimo 1).

> **Por que não a metade, como no d20 clássico.** Medido em 200.000 tiradas: cortar o dano pela
> metade custa **52% a 54%** de DPR, enquanto um degrau da escada vale **12% a 19%** — e a faixa
> inteira do catálogo de 76 armas vai de 2,88 a 6,35, ou seja **2,2×**. Pela regra clássica, um flip
> de resistência custaria **mais do que trocar da pior arma do jogo para a melhor**, e a tabela de
> armas deixaria de existir como decisão. A regra de degrau também **não é regressiva**: uma redução
> fixa de −2 puniria o cano improvisado em 35% e a marreta em 20%, enquanto o degrau trata todas
> proporcionalmente.

#### Resistência aplica-se POR DADO, não ao total

Uma **Soqueira "Vólt-9"** (1d6 Concussão + 1d6 Elétrico) contra alvo **Resistente a Concussão** vira
**1d4 + 1d6** — perde só o primeiro dado.

> É exatamente por isso que o **dado secundário foi travado em 1d6** (Aprovação 009): armas de dois
> tipos **contornam resistência de tipo único**, e agora essa frase tem regra por trás em vez de ser
> só uma intenção.

#### Perfis de resistência por criatura

| Criatura | Vulnerável | Resistente | Muito Resistente |
|---|---|---|---|
| **Zumbi comum** | **Fogo** | **Perfurante**, **Balístico** | — |
| **Mutante** | Fogo | Perfurante, **Necrótico** | — |
| **Alvo com cibernética** | **Elétrico/EMP** | Perfurante, Necrótico, Químico | — |
| **Humano (saqueador)** | — | — *(só o que o material da armadura der)* | — |

> **Aviso ao implementador: dois graus existem sem sujeito.** Nenhuma criatura canônica é **Muito
> Resistente** (coluna inteira em `—`) e **Imune não tem sequer coluna** aqui. Os dois graus são reais
> e devem ser implementados no motor — a escada precisa dos cinco degraus para funcionar —, mas quem
> os usa é matéria do **Bestiário**, que ainda não existe. Não trate a ausência como "grau morto".

O zumbi resiste a Perfurante e Balístico porque **não tem órgão vital para furar** — é a tradução
mecânica do trope do gênero. E ser **Vulnerável a Fogo** é o que finalmente dá função ao maçarico, à
Ponta Incendiária e à **"Boca de Forno"**.

> **Impacto medido.** Com 4 zumbis de 12 HP contra um grupo de 4: resistir a Balístico leva o rifle
> de **3,44 para 3,86 rodadas** (+12%), a Horda de 20,6 para 23,1 pontos por luta, e a Infecção de
> 1,28 para 1,71 (+34%, porque luta mais longa é mais golpe recebido). A marreta, de Concussão, fica
> **inalterada**. A via de fogo não morre — ela paga cerca de 12% a mais, o que é um empurrão real
> na direção do corpo a corpo sem apagar nada. **Foi a escolha da mecânica gentil que tornou o sabor
> do gênero acessível:** com a resistência clássica, dar ao zumbi resistência a Balístico seria
> impossível.

#### Armadura dá Defesa, não resistência

**Armadura comum não concede resistência nenhuma.** Ela já reduz a frequência de acerto pela
**Defesa**, e somar resistência seria cobrar duas vezes pelo mesmo investimento.

Resistência vem de **material**, não de peça: uma placa de **Liga Pré-Queda** enxertada na armadura
concede **Resistente a Balístico**. Isso mantém a Liga como o gargalo que ela é e lhe dá mais uma
função.

> **Emenda da Aprovação 034.** Uma peça **cujo próprio material é específico** — kevlar, borracha,
> malha — concede **uma** resistência (o Colete Balístico Civil, de kevlar, é Resistente a
> Perfurante). Armadura comum continua sem nenhuma. Três travas: **graus não se somam** (vale o maior);
> **resistência a Necrótico nunca vem de equipamento**; **peça Rachada perde a resistência**. Ver
> `docs/gdd/GDD_Equipamentos.md` §6.

#### Dois efeitos colaterais, registrados

- **Prejudica o Explorador.** A **Besta** dele vai de 5,89 para **6,70 rodadas** e a Infecção por
  luta de 4,14 para **5,11**. Ele já era o pior nas duas trilhas. Aceito pelo Diretor: a besta é arma
  de **batedor e de alvo específico**, não de refrega — que já era a intenção dela.
- **Conserta a Lança.** A mesma regra resolve sozinha um desequilíbrio sinalizado muitas rodadas
  atrás: a Lança Artesanal era silenciosa, perfurante e de alcance 2 hex, a melhor relação
  risco/retorno da tabela. Agora cai de 3,86 para **4,07 rodadas** e entra na fila.

Dano extra de Elétrico/EMP contra alvos com cibernética: `[A CALIBRAR]`.

### 6.4. Tabela de Armas

O catálogo completo de armas **não vive mais neste documento**. Ele foi separado para manter cada
arquivo legível:

- **`docs/gdd/GDD_Armas.md`** — as ~74 armas canônicas nos seis tiers (Improviso, Civil, Modificada,
  Militar, Corporativa, Protótipo), com dado, tipo de dano, Nível de Ruído, FOR mínima,
  propriedades e DPR calculado. Inclui os efeitos mecânicos completos das armas de tier alto.
- **`docs/Mutagen_Zero_Armamento.xlsx`** — a mesma informação em planilha, com **fórmulas vivas**:
  alterar um dado ou um parâmetro recalcula DPR, rodadas para derrubar e consumo de munição.
  É a fonte da verdade numérica.

> **Por que separado.** Este documento define as **regras** de combate; o catálogo define os
> **dados**. Misturar os dois tornaria impossível revisar qualquer um dos lados sem reler o outro.

---

## 7. Armas de Fogo

Armas de fogo usam **AGI** para ataque e dano, causam dano **Balístico** por padrão e são o único
tipo de arma sujeito a **travamento** e a **gestão de munição**.

### 7.1. Munição e Recarga

- Cada arma tem um **carregador de capacidade fixa**: `[A CALIBRAR]` por modelo (§6.4).
- Cada modo de disparo consome uma quantidade fixa de munição (§7.2).
- **Recarregar custa 1 Ação inteira**, qualquer que seja a arma.
- Se a munição restante for menor que a exigida pelo modo escolhido, **o modo não pode ser usado**.
  Regra de disparo parcial (rajada com munição insuficiente): `[A CALIBRAR]`.
- Cada disparo desconta do **carregador**, não da reserva de inventário.

### 7.2. Modos de disparo

| Modo | Ataque | Dano | Munição | Resolução |
|---|---|---|---|---|
| **Tiro único** | Ataque normal | Normal | **1** | Uma rolagem de ataque contra a Defesa do alvo |
| **Rajada de 3** | **−2** no ataque | **+1 dado de dano** | **3** | Uma rolagem de ataque contra a Defesa do alvo |
| **Automático** | Não rola ataque | Ver abaixo | **10** | **Cone/área**: cada alvo faz um **teste de AGI vs. CD** |

**Rajada de 3.** Uma única rolagem de ataque com −2. No acerto, o dano é o dado da arma **mais um
dado adicional do mesmo tipo**. Em um crítico, todos os dados — inclusive o extra da rajada — dobram.

**Automático.** Não há rolagem de ataque. O atirador define um **cone/área** a partir de sua posição
e cada criatura dentro dela faz um teste de **AGI** contra uma CD.

- **Falha no teste:** sofre o dano completo da arma.
- **Sucesso no teste:** `[A CALIBRAR]` — definir se é dano reduzido (metade) ou dano nenhum.
- **CD do teste de AGI:** `[A CALIBRAR]` — definir se é fixa ou derivada de
  `8 + mod AGI do atirador + proficiência`.
- **Geometria do cone/área (alcance e abertura em hexágonos):** `[A CALIBRAR]`.
- Sem rolagem de ataque, **não há crítico por 20 natural nem travamento por 1 natural** neste modo.
  Travamento alternativo por sobreaquecimento no fogo automático: `[A CALIBRAR]`.

### 7.3. Travamento

- **Gatilho:** qualquer `1` natural em uma rolagem de ataque com arma de fogo. A arma **trava** e o
  ataque falha automaticamente.
- Uma arma travada **não dispara em nenhum modo** até ser destravada.
- **Destravar custa 1 Ação Bônus** (Aprovação 003), **não** a Ação. Consequência: quem trava perde
  o ataque do turno em que tirou o `1`, mas no turno seguinte destrava **e** ataca. O custo total de
  um travamento é de **1 turno, não 2**. Teste exigido para destravar, se houver, e sua CD:
  `[A CALIBRAR]`.
- **O estado de conservação da arma modula a chance de travamento**: quanto pior o estado, maior a
  faixa de resultados que travam.

**Os quatro estados são canônicos** (Aprovação 006), com os valores fechados:

| Estado de conservação | Trava em | Faixa | P(trava) por ataque |
|---|---|---|---|
| **Calibrada** | `1` natural **confirmado** — rola um 2º d20 e só trava se sair `1` ou `2` | — | **~0,5%** |
| **Boa** | `1` natural | 1 | **5,0%** |
| **Desgastada** | `1` ou `2` | 2 | **10,0%** |
| **Arruinada** | `1`, `2` ou `3` | 3 | **15,0%** |

> **Não existe arma que nunca trava.** A propriedade "Confiável" foi proposta e **rejeitada**
> (Aprovação 009): ela criaria um recurso de turno permanentemente morto — quem nunca trava nunca
> usa a Ação Bônus — e pressionaria a reabertura do escopo fechado em §2.4. O melhor caso possível é
> o estado **Calibrada**, com ~0,5% de risco residual.

> **QUEBRA e TRAVAMENTO são contadores distintos e nunca se somam** (Aprovação 013).
> **Travamento** é a arma emperrar: só arma de fogo, gatilho no `1` natural, modulado pela tabela
> acima, resolvido com 1 Ação Bônus. **Quebra** é a arma se partir: vem da propriedade **Frágil** e
> do `+1` que cada modificação Gambiarra acrescenta (ver `docs/gdd/GDD_Modificacoes.md`). Uma arma pode
> ter faixa de travamento 1 e faixa de quebra 2 ao mesmo tempo, sem que os números interajam.
> Armas de corpo a corpo **nunca travam** — mas modificadas em Gambiarra, **podem quebrar**.

### 7.4. Alcance

Cada arma à distância tem **alcance normal** e **alcance longo**, medidos em hexágonos (§11.2).

| Distância até o alvo | Efeito |
|---|---|
| Até o alcance normal | Ataque sem penalidade de distância |
| Acima do normal, até o longo | **Desvantagem** na rolagem de ataque |
| Acima do alcance longo | **Não pode ser alvo** |

Valores por arma: `[A CALIBRAR]` (§6.4). Penalidade por disparar arma de fogo estando em corpo a
corpo adjacente: `[A CALIBRAR]`.

---

## 8. HP, Estado Crítico e Morte

### 8.1. Pontos de Vida

```
HP por nível = dado de vida (da classe) + modificador de CON
HP total     = soma de todos os níveis
```

**Dado de vida por classe — RESOLVIDO** (Aprovação 016). Ver os documentos `Classe_*.md`:

| Dado | Classes |
|---|---|
| **d10** | Pugilista, Construtor |
| **d8** | Médico, Piloto, Explorador, Ceifador |
| **d6** | Cientista, Atirador de Elite |

- **HP no 1º nível = valor MÁXIMO do dado de vida + modificador de CON** (Aprovação 016). Com
  CON `+2`, isso vai de **8** (d6) a **12** (d10).
- **HP por nível após o 1º:** `[A CALIBRAR]`.

> **Letalidade no nível 1, para você saber antes da mesa.** O crítico médio de uma marreta é **16**
> de dano; de um rifle em Rajada, **19,5**. Ou seja: **um único crítico derruba qualquer personagem
> de nível 1**, sem exceção. Isso é intencional e equivalente ao d20 clássico — o Estado Crítico
> (§8.2) com testes de morte existe exatamente para isso.
- Modificador de CON negativo reduz o ganho por nível; piso mínimo de ganho: `[A CALIBRAR]`.

### 8.2. Estado Crítico (0 HP)

Ao chegar a **0 HP**, o personagem entra em **Estado Crítico**: fica **Inconsciente** e **Caído**,
não age, não se move, não tem Reação, e faz um **teste de morte no fim de cada um de seus turnos**.

### 8.3. Testes de morte

```
Teste de morte = d20 vs. CD 10 (sem modificadores de atributo)
```

| Resultado | Consequência |
|---|---|
| **10 ou mais** | 1 sucesso |
| **9 ou menos** | 1 falha |
| **3 sucessos acumulados** | **Estabiliza** — fica Inconsciente com 0 HP e para de rolar |
| **3 falhas acumuladas** | **Morre** |

Efeito de `20` natural e `1` natural no próprio teste de morte: `[A CALIBRAR]`.

### 8.4. Dano em um personagem caído

| Situação | Consequência |
|---|---|
| Sofre qualquer dano em Estado Crítico | **1 falha automática** no teste de morte |
| Sofre um **acerto crítico** em Estado Crítico | **2 falhas automáticas** |

Sucessos e falhas acumulam até que um dos lados chegue a 3. Ao estabilizar ou voltar a ter HP acima
de 0, a contagem **zera**.

### 8.5. Recuperação

- Qualquer cura que devolva ao menos 1 HP tira o personagem do Estado Crítico e zera a contagem.
- Estabilizar um aliado com **Usar Objeto** ou perícia médica: CD `[A CALIBRAR]`.
- Descanso, cura natural e itens de cura: `[A CALIBRAR]`.

---

## 9. Trilha de Infecção

A Trilha de Infecção foi extraída para arquivo próprio: **`docs/gdd/GDD_Infeccao.md`**.

Ela é uma das duas moedas de atrito do jogo — o preço que o combate corpo a corpo cobra do corpo do
personagem. O essencial para arbitrar em mesa: **golpe necrótico de mutante = 1 ponto** (crítico =
2); ao fim do combate, **teste de CON com CD 10 + pontos ganhos naquele combate**, e o sucesso
remove metade; **limiar base 15**, variável por classe, com bandas proporcionais (Saudável até 1/3,
Infectado até 2/3, Infectado grave até o limiar, mutação ou morte no limiar).


## 10. Condições

Uma condição altera as regras normais. Condições **não acumulam com elas mesmas**, salvo as que têm
trilha de pontos (Sangrando, Irradiado, Infectado).

| Condição | Efeito mecânico |
|---|---|
| **Caído** | Move-se apenas rastejando (custo dobrado por hex). Ataques **corpo a corpo** contra você têm **Vantagem**; ataques **à distância** contra você têm **Desvantagem**. Seus ataques têm **Desvantagem**. Levantar-se custa metade do movimento total do turno. |
| **Agarrado** | Movimento reduzido a **0**; não se beneficia de bônus de movimento. Termina se o agarrador ficar Incapacitado ou se você escapar com um teste oposto de FOR ou AGI. |
| **Atordoado** | **Incapacitado**: não age, não se move, não reage. Ataques contra você têm **Vantagem**. Falha automaticamente em testes de FOR e AGI. Duração padrão: `[A CALIBRAR]`. |
| **Cego** | Falha automaticamente em qualquer teste que exija visão. Seus ataques têm **Desvantagem**; ataques contra você têm **Vantagem**. |
| **Surdo** | Falha automaticamente em qualquer teste que exija audição. Não pode dar nem receber avisos verbais (afeta a Ação Ajudar à distância). |
| **Amedrontado** | **Desvantagem** em ataques e testes enquanto a fonte do medo estiver na sua linha de visão. Não pode se mover voluntariamente **em direção** à fonte. |
| **Envenenado** | **Desvantagem** em rolagens de ataque e em testes de atributo. Dano contínuo, quando a fonte especificar: `[A CALIBRAR]`. |
| **Incapacitado** | Não pode usar **Ação**, **Reação** nem interação livre. Ainda pode ser movido por terceiros. |
| **Inconsciente** | **Incapacitado** + **Caído** + solta o que segura, sem consciência do ambiente. Ataques contra você têm **Vantagem** e qualquer acerto a até 1 hex é **crítico automático**. |
| **Sangrando** | Sofre **1 ponto de dano por camada**, no **início de cada um dos seus turnos**. Acumula em camadas, **teto de 5**. Cessa com **qualquer cura**, ou com a **Ação** de estancamento (Usar Objeto, perícia **Medicina**, **CD 12**), que remove **todas** as camadas. Ver §10.2. |
| **Irradiado** | Trilha de pontos de Radiação, resistida com testes de **CON**. Penalidades progressivas por faixa: `[A CALIBRAR]`. Limite da trilha e sua consequência: `[A CALIBRAR]`. |
| **Infectado** | O personagem tem pontos ativos na Trilha de Infecção (§9). Penalidades por faixa: `[A CALIBRAR]`. Atingir o limite causa **mutação ou morte**. |

### 10.2. Sangrando — por que 1 ponto fixo, e por que ele é anti-chefe

**Aprovação 028.** Sangrando dispara no **início do turno do alvo**. Alvo que morre rápido quase não
sangra; alvo que dura, sangra muito. A consequência é medida, não intencional — e é a propriedade
mais útil que a condição tem.

Ganho em rodadas da serra "Denteira" (1d8 Cortante) **contra ela mesma sem Sangrando**, 40.000
iterações:

| Alvo | Ganho |
|---|---|
| **Zumbi comum** (12 HP) | **+8%** |
| Mutante (28 HP) | +20% |
| Touro Mecânico (35 HP) | +25% |
| Zumbi Venenoso (45 HP) | +28% |
| **Gigante Mutagênico** (80 HP) | **+40%** |

> **Isto é o corretivo exato do problema medido em `docs/gdd/GDD_Bestiario.md` §3.** Lá, a simulação
> mostrou que o chefe é **estruturalmente fraco** contra um sistema cuja Trilha conta acertos, porque
> um corpo só ataca uma vez. **Sangrando é a única mecânica do sistema com a inclinação invertida**:
> quase nada contra bando, muito contra alvo único. Ela não foi desenhada para isso — foi desenhada
> para a serra, e a propriedade apareceu na medição.

**Por que 1 ponto fixo e não `1d4`:**

1. **Não rola dado.** Sangrando já custa contabilidade de camadas; somar uma rolagem por camada por
   turno é custo de mesa sem retorno.
2. **A inclinação fica mais limpa.** Com `1d4` o ganho contra o Zumbi comum sobe para **+15%**, e aí
   a serra começa a virar arma genérica em vez de especialista.
3. **Ela justifica o preço duplo da serra sem dominar.** A "Denteira" é o **único corpo a corpo que
   paga Infecção E Horda** (Ruído Médio). A +8% contra alvo comum, esse preço **não compensa** — e
   está certo que não compense: a serra é ferramenta de chefe.

**O teto de 5 quase nunca morde** (+40% contra +41% sem teto nenhum): é grade de proteção para lutas
longas futuras, não restrição do jogo normal.

**Estancar remove TODAS as camadas.** Uma Ação desfazer cinco rodadas de serra é a tensão correta — a
serra reaplica a cada acerto, e criaturas de suporte podem estancar tanto quanto personagens.

### 10.1. Interações entre condições

- **Inconsciente** engloba **Incapacitado** e **Caído**; aplicá-los à parte é redundante.
- **Atordoado** engloba **Incapacitado**, mas **não** derruba o personagem.
- Vantagem e Desvantagem vindas de condições diferentes seguem o cancelamento de §1.1: uma de cada
  lado zera as duas e o personagem rola 1d20 normal.
- Durações padrão e formas de remoção das condições sem duração explícita: `[A CALIBRAR]`.

---

## 11. Grid Hexagonal e Movimento

### 11.1. A malha

- O campo de batalha é um **grid hexagonal**; **1 hexágono = 1,5 m**.
- **Movimento base por turno = 9 m = 6 hexágonos** (18 m / 12 hex com a Ação Correr).
- Cada hexágono tem **6 vizinhos** e **todos os 6 estão exatamente a 1,5 m**.
- **Não existe regra de diagonal.** É por isso que o grid é hexagonal: todo passo custa o mesmo e
  não há distorção de distância por direção.

### 11.2. Medindo distância

A distância entre dois hexágonos é o **número mínimo de passos** entre hexágonos adjacentes,
multiplicado por 1,5 m: 1 hex = 1,5 m · 2 hex = 3 m · 4 hex = 6 m · 6 hex = 9 m · 12 hex = 18 m.

Ataques corpo a corpo alcançam **1 hexágono (1,5 m)** por padrão. Armas com alcance corpo a corpo
estendido: `[A CALIBRAR]`.

### 11.3. Linha de visão e cobertura

- Traça-se uma linha do centro do hexágono do atacante ao centro do hexágono do alvo.
- Os obstáculos interceptados determinam o grau de cobertura (§5.4): meia (+2), três quartos (+5)
  ou total (não pode ser alvo).
- Quando a linha passa exatamente pela aresta entre dois hexágonos, o desempate **beneficia o
  defensor** (aplica-se o maior grau de cobertura).
- Percentual de bloqueio que define cada grau de cobertura: `[A CALIBRAR]`.

### 11.4. Custos de movimento

| Terreno / situação | Custo |
|---|---|
| Terreno normal | 1 hex de movimento por hexágono |
| **Terreno difícil** | 2 hex de movimento por hexágono |
| Rastejar (condição **Caído**) | 2 hex de movimento por hexágono |
| Levantar-se de **Caído** | Metade do movimento total do turno |
| Escalar / nadar | `[A CALIBRAR]` |
| Atravessar hexágono ocupado por aliado | `[A CALIBRAR]` |
| Atravessar hexágono ocupado por inimigo | `[A CALIBRAR]` |

Um combatente de tamanho padrão ocupa **1 hexágono**. Ocupação de criaturas Grandes ou maiores:
`[A CALIBRAR]`.

### 11.5. Movimento e ataques de oportunidade

Sair do alcance corpo a corpo (1 hex) de um inimigo visível **sem** usar a Ação **Desengajar**
provoca um ataque de oportunidade, que gasta a **Reação** desse inimigo. Mover-se *dentro* do
alcance dele — de um hex adjacente para outro hex adjacente — **não** provoca.

---

## 12. Ruído, Detecção e Horda

Estes dois sistemas foram extraídos para arquivos próprios:

| Documento | O que cobre |
|---|---|
| **`docs/gdd/GDD_Ruido.md`** | Níveis de Ruído e raios, precedência, cláusula de motor, Atração, silenciadores, armas silenciosas nativas, ruído de criaturas |
| **`docs/gdd/GDD_Horda.md`** | O Medidor de Horda: acúmulo por rodada, limiar 20 em escada, as levas, zeragem no fim da cena |

O essencial para arbitrar em mesa: os níveis são **Silencioso (0) · Baixo (4 hex) · Médio (20 hex)
· Alto (50 hex)**; a precedência é **Pesada vence Concussão vence Cortante/Perfurante/Leve**, e
**motor ou mecanismo Explosivo sobrepõe** a precedência. O Medidor soma **o ruído mais alto por
rodada** (0/1/3/6) e traz uma leva a cada **20 pontos**, zerando no fim da cena. O Medidor é
**exclusivo do Mestre** — o jogador nunca vê o número.


## 13. Mapa do canon — onde mora o resto

Este documento cobre as **regras** de combate. Os **catálogos** e os **subsistemas de economia**
foram separados em arquivos próprios para que nenhum deles fique ilegível.

**Princípio de organização: uma função do sistema por arquivo.**

| Documento | O que contém |
|---|---|
| **`docs/gdd/GDD_Combate.md`** *(este)* | Núcleo de resolução, iniciativa, turno, ataque e defesa, dano, armas de fogo, HP e morte, condições, grid hexagonal, **categorias de tamanho (§14)** |
| **`docs/gdd/GDD_Armas.md`** | Catálogo das ~74 armas nos seis tiers, tabela das 24 propriedades, efeitos das armas de tier alto |
| **`docs/gdd/GDD_Modificacoes.md`** | Sistema de Modificações (Gambiarra × Oficina), os oito componentes, as 17 modificações e suas receitas |
| **`docs/gdd/GDD_Infeccao.md`** | **Trilha de Infecção** — o preço que o corpo a corpo cobra do corpo |
| **`docs/gdd/GDD_Ruido.md`** | **Ruído e Detecção** — quanto barulho cada ação faz, quem escuta, silenciadores |
| **`docs/gdd/GDD_Horda.md`** | **Medidor de Horda** — o que acontece quando o barulho acumula |
| **`docs/gdd/GDD_Equipamentos.md`** | **Equipamentos** — espaços, soma da Defesa, desgaste por crítico, reparo, modificação, variações e Vantagem de equipamento *(regras: Aprovação 034; catálogo: Bloco 4b)* |
| **`docs/gdd/GDD_Saque.md`** | **Saque** — a escala de raridade (Abundante a Mítico) e a tabela de saque do grupo |
| **`docs/gdd/GDD_Consumiveis.md`** | **Consumíveis** — reposição de Carga, a tabela de saque de munição, a disputa do gerador do Refúgio |
| **`docs/gdd/GDD_Bestiario.md`** | **Bestiário** — as 18 criaturas, ND e orçamento de encontro, quem gera Infecção, quem uiva, imunidades |
| **`docs/gdd/GDD_Especializacoes.md`** | Catálogo das 82 Especializações adquiríveis, os quatro portes e as três regras de contenção |
| **`docs/gdd/GDD_Pericias.md`** | As 18 perícias, seus atributos e as listas por classe |
| **`docs/gdd/GDD_Glossario.md`** | Termos reservados, colisões declaradas e divergências entre documentos |
| **`docs/Mutagen_Zero_Armamento.xlsx`** | Fonte da verdade numérica, com fórmulas vivas de DPR, consumo de munição e travamento |

> **As duas moedas de atrito.** `docs/gdd/GDD_Infeccao.md` e `docs/gdd/GDD_Horda.md` são as duas faces da mesma
> escolha: corpo a corpo é silencioso mas infecta; arma de fogo mantém o corpo limpo mas chama a
> horda. Elas **não têm o mesmo ritmo** de propósito — a Horda é pressão rápida e recuperável, a
> Infecção é desgaste lento e permanente. `docs/gdd/GDD_Ruido.md` é a entrada de ambas.

### 13.1. Munição — resumo canônico

O módulo completo está na planilha (abas `Municao`, `Munições Especiais`, `Compatibilidade`).
O essencial para arbitrar em mesa:

- **Seis pools:** os quatro calibres de pólvora (**Leve, Pesado, Rifle, Cartucho**), mais
  **Projéteis** (flechas, virotes, dardos — **recuperáveis**) e **Exótica** (limitada a 2 itens no
  jogo inteiro, só se fabrica no Refúgio).
- **Munição Padrão** é o que se saqueia. As **dez Munições Especiais** não se acham: **fabricam-se**,
  com os mesmos oito componentes das Modificações.
- **Munição de Gambiarra soma `+1` à faixa de travamento** enquanto estiver carregada. Munição suja
  emporcalha a arma. A de Oficina não tem penalidade.
- **Flecha recuperada perde a melhoria:** recupera-se o projétil, não a carga.

> **Piso de empilhamento de Ruído.** Silenciador reduz 1 nível e munição **Subsônica** reduz outro,
> mas qualquer combinação **para em Baixo**. **Arma de fogo nunca chega a Silencioso**, por mais que
> se empilhe. A Subsônica também custa **−1 degrau no dado** — silêncio se paga em dano.

### 13.2. As três exceções nomeadas ao teto de DPR

O teto de dano por rodada é **6,025** (marreta 1d12) e vale para armas de alcance normal. Três
coisas passam dele, cada uma pagando com uma restrição própria:

| Exceção | DPR | O preço |
|---|---|---|
| **Espingarda** 2d6 | 6,35 | Alcance 4/12 hex — **6 metros**. Obriga a entrar na faixa de exposição à Infecção |
| **Soqueira "Vólt-9"** carregada | 6,35 | Decai visivelmente para 4,08 quando as 6 cargas acabam |
| **Rajada** | 7,28 | 3× munição e restrição ao calibre **Rifle**, o mais escasso |

---

*Fim do documento. Qualquer alteração nas regras das seções §1 a §12 exige nova aprovação do Diretor
de Criação. Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*

---

## 14. Categorias de tamanho

**Aprovação 025.** Quatro categorias. Elas moram aqui, e não no Bestiário, porque governam
**geometria e regras de combate** — ocupação de hexágono, cobertura, alcance de Enganchar — e não
características de criatura. O `docs/gdd/GDD_Bestiario.md` apenas **usa** esta escala.

| Categoria | Hexágonos ocupados | Exemplos canônicos |
|---|---|---|
| **Miúdo** | 1 (cabem **2** por hexágono) | Cachorro Zumbi, Cachorro Explosivo, Arrastador |
| **Médio** | **1** | Personagens jogadores, Zumbi, Mutante, Saqueador Humano |
| **Grande** | **3** (um hexágono e os adjacentes de um lado) | Touro Mecânico, Casulo |
| **Enorme** | **7** (um hexágono central e os seis vizinhos) | Gigante Mutagênico |

### 14.1 O que o tamanho faz

1. **Ocupação.** Uma criatura Grande ou Enorme **bloqueia linha de visão** para quem está atrás dela,
   e concede **meia cobertura (+2)** a aliados que se abriguem atrás — inclusive aos inimigos dela.
2. **Enganchar e Agarrado.** **Não afetam alvo duas categorias maiores** que quem aplica. Um
   personagem Médio **não** agarra um Gigante Enorme; agarra um Grande com dificuldade e um Miúdo com
   facilidade.
3. **Empurrar.** Efeitos de empurrão (Investida do Touro Mecânico, Escudo Antimotim) **não movem alvo
   duas categorias maiores**.
4. **Movimento através.** Pode-se atravessar o espaço de uma criatura **duas ou mais categorias
   menor**; o espaço de qualquer outra é **terreno difícil** (custa o dobro).

### 14.2 O que o tamanho NÃO faz

**Tamanho não altera dado de dano, HP nem Defesa.** Um Gigante não causa mais dano *por ser Enorme* —
ele causa mais dano porque a ficha dele diz isso. Acoplar tamanho a números criaria uma segunda
dimensão de escalonamento competindo com o ND, e o sistema já tem escadas demais.

> **Destrava o "Extrator".** O arpão de resgate (`docs/gdd/GDD_Armas.md` §7.4) estava **⛔ CONGELADO**
> desde a aprovação de tier alto por depender de categorias de tamanho. Com esta seção, a cláusula
> *"se o alvo for Grande ou mais forte, ELE arrasta você"* passa a ter sujeito: o **Touro Mecânico**
> (Grande), o **Casulo** (Grande) e o **Gigante Mutagênico** (Enorme).

`[A CALIBRAR]`: categoria **Minúsculo** (insetos, enxames) e criaturas **Colossais** — nenhuma das
duas tem sujeito no MVP.
