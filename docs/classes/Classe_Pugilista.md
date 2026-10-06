# MUTAGEN:ZERO — Classe: PUGILISTA

> **Canon.** Nível 1 fechado por `CANON_CLASSES.md` (Aprovação 016): dado de vida **d10**, limiar de Infecção
> **17**, proficiências nas famílias **Desarmado e Contundentes**, assinatura **Combate Desarmado**. O que não estiver lá
> aparece aqui como `[A CALIBRAR]`. **Não duplicado aqui:** `docs/gdd/GDD_Combate.md` §2, §5–§6 (ataque, dano,
> economia do turno) · `docs/gdd/GDD_Armas.md` §1.2 e §3 (propriedades e DPR) · `docs/gdd/GDD_Infeccao.md` ·
> `docs/gdd/GDD_Ruido.md` · `docs/gdd/GDD_Horda.md`.

---

## 1. Identidade

Ninguém escolhe ser Pugilista. Você é Pugilista porque a arma acabou, porque o cano entupiu de areia, porque o
facão ficou preso na caixa torácica de alguma coisa que ainda estava se mexendo e não houve tempo de puxar de
volta. É o sobrevivente que aprendeu a lição mais suja do pós-Colapso: o equipamento falha e o corpo continua.
Ele treinou o único instrumento que não pode ser saqueado nem confiscado e não precisa de munição — e o preço
foi descobrir, golpe por golpe, quanto de si mesmo ele gasta antes de parar de ser gente.

É a pessoa mais marcada da mesa: metacarpos remendados, nós dos dedos com calo de osso sobre osso, antebraços
de tecido cicatricial endurecido. As mordidas e os arranhões não estão nos antebraços por acidente — estão ali
porque lutar de perto é oferecer os braços como escudo, e cada oferta dessas é um depósito na Trilha de
Infecção. O histórico de ferimentos dele é o registro literal da própria ficha.

Não há heroísmo nisso. Um Pugilista bom não escolheu a via nobre do combate honesto: calculou, com frieza, que
aguenta mais carga infecciosa que os outros e vendeu essa tolerância como serviço ao grupo. É o que fica no
corredor enquanto os outros recuam — não por coragem, mas porque demora mais para virar uma das coisas dele.

## 2. Ficha rápida

| Campo | Valor |
|---|---|
| **Dado de vida** | **d10** — nunca muda, qualquer que seja a Especialização adquirida |
| **HP no nível 1** | **10 + mod. de CON** (12 com CON +2) — máximo do dado, por regra canônica |
| **HP por nível após o 1º** | `[A CALIBRAR]` |
| **Limiar de Infecção** | **17** — o segundo maior das oito, atrás só do Médico (18) |
| **Proficiência (famílias de arma)** | **Desarmado**, **Contundentes** |

> **Proficiência é por FAMÍLIA DE ARMA** (Aprovação 017), nunca por tipo de dano nem por propriedade. As dez famílias são uma dimensão única e cada arma pertence a **exatamente uma**. *Ágil, Leve, Pesada, Improvisada, Utilitária, Frágil, Flexível e Arremessável* são **propriedades**, e nenhuma delas é família. Ver `docs/gdd/GDD_Glossario.md`.

| **Perícias e resistências com proficiência** | `[A CALIBRAR]` |
| **Bônus de proficiência no nível 1** | **+2** (progressão até +6 `[A CALIBRAR]`) |

**Bandas de Infecção calculadas para o limiar 17** — frações do limiar pessoal (`docs/gdd/GDD_Infeccao.md` §3):

| Faixa | Pontos | Estado | Efeito |
|---|---|---|---|
| até 1/3 (5,67) | **0–5** | Saudável | Nenhum |
| 1/3 a 2/3 (11,33) | **6–11** | Infectado | Custo **social**: NPCs reagem. Sem penalidade mecânica |
| 2/3 até o limiar | **12–16** | Infectado grave | **Desvantagem** nos testes de CON contra Infecção |
| no limiar | **17** | Mutação ou morte | Critério entre as duas: `[A CALIBRAR]` |

> **Arredondamento:** o canon fixa a proporção, não o arredondamento; trunca-se para baixo porque reproduz o
> exemplo canônico do limiar 15 (0–5 · 6–10 · 11–14 · 15) — formalizar é `[A CALIBRAR]`. **Lutas até a mutação
> com limiar 17:** `[A CALIBRAR]`; o canon mede 12 → 6, 15 → 8 e 18 → 9 pela marreta.

## 3. Habilidade-assinatura: COMBATE DESARMADO

**Enunciado canônico:** o punho conta como arma **1d6 Concussão** com a propriedade **Ágil**.

1. Registrar uma arma virtual `PUNHO`, sempre presente, sem slot de inventário, sem munição e sem estado de
   conservação: dado **1d6**, tipo **Concussão**, propriedade **Ágil**, Ruído **Baixo (1)** (§5.2), categoria
   de proficiência **Desarmado**.
2. O portador **é proficiente** e o punho **não** tem a propriedade Improvisada: o bônus de proficiência
   **soma normalmente** ao ataque. Por ser **Ágil**, escolhe-se **FOR ou AGI**, e o atributo escolhido é o
   mesmo aplicado ao dano; o crítico dobra os dados, não o modificador (`2d6 + mod.`).
3. O punho **não é arma de fogo** (nunca trava, sem munição, sem Recarregar), **não é Frágil** e **não tem
   slot de modificação**: não quebra e não recebe silenciador.
4. **Nenhum uso novo de Ação Bônus.** Consome a **Ação Atacar** normal; o escopo da Ação Bônus permanece
   fechado em "Destravar arma de fogo" (`docs/gdd/GDD_Combate.md` §2.4). Um ataque por Ação — não existe ataque extra
   neste MVP. Ataque de oportunidade com o punho é legal e custa a **Reação**. E não há Ação de **Desarmar** na
   lista fechada de §4, logo não existe regra de perda de arma a resolver para o punho no MVP.

**Exemplo numérico.** Parâmetros canônicos de aferição (`docs/gdd/GDD_Armas.md` §1.2): ataque **+5**, dano **+3**,
Defesa **14**, HP do alvo **12**.

```
Punho = 1d6 Concussão, NÃO Improvisada  ->  bônus efetivo = 5
P(acerto)  = (21 - (14 - 5)) / 20 = 12/20 = 60%
Dano médio = 1 x (6+1)/2 = 3,5
DPR        = 0,60 x (3,5 + 3) + 0,05 x 3,5 = 3,90 + 0,175 = 4,075
Rodadas para abater o zumbi comum de 12 HP = 12 / 4,075 = 2,94
```

**4,075 é exatamente o DPR do Cacetete** (`docs/gdd/GDD_Armas.md` §4, tier Civil): o Pugilista carrega, de graça e para
sempre, uma arma de tier Civil que ninguém tira dele. Ela não é boa — o teto do jogo é **6,025** (marreta
1d12) — ela é **incondicional**.

## 4. A porta suave

**O Pugilista não tem porta suave, e isso é deliberado.** As três do canon (`CANON_CLASSES.md` §2) cobrem
**Modificações de arma**, **Refúgio** e **Veículos**: ele não é o especialista de nenhuma, não abre uma quarta
e não é o tier bom de nenhuma das três. Ele não precisa de uma porque a assinatura é o inverso de uma: porta
suave garante que **qualquer um** acesse o pilar em tier ruim; Combate Desarmado garante que **ele** nunca perca
acesso ao pilar do combate, em nenhuma escassez. Não inventar uma porta suave para fechar a simetria da ficha é
decisão de design, não lacuna — **fora de combate o Pugilista é um personagem comum**.

## 5. Interação com os subsistemas

### 5.1. Trilha de Infecção — por que 17 não é generosidade

O limiar 17 é **compensação medida, não bônus**, e a cadeia causal é fechada: o punho tem alcance corpo a corpo
padrão de **1 hexágono** e não existe Alcance 2 hex nele; para atacar, o Pugilista **termina o turno adjacente
ao mutante** e continua adjacente no turno do mutante, que é quando as garras respondem; dano de mutante é
**Necrótico**, única fonte de Infecção (**1 ponto por golpe que acerta, 2 no crítico**); e a conversão é **por
ataque acertado, não proporcional ao dano**, de modo que quem passa o combate a 1 hex maximiza exatamente a
variável que alimenta a trilha. A exposição dele não é um risco que ele corre: é a **precondição de ele agir**.

Com o limiar base 15 ele entraria em Infectado grave — e portanto em **Desvantagem nos próprios testes de CON contra Infecção** — antes de qualquer outro combatente de linha de frente, e a espiral canônica (CD que cresce
com o que foi levado, sucesso que só remove metade) o fecharia em poucas sessões. **Sem o limiar alto, a classe é injogável.** Os 2 pontos acima da base compram as rodadas de adjacência que a assinatura obriga.

**Exemplo de um combate.** Quatro rodadas adjacente, o mutante acerta duas vezes sem crítico → **2 pontos**.
Teste de CON contra **CD 10 + 2 = 12**; com CON +2, sucesso em **10 ou mais (55%)**, que remove metade
arredondando para baixo, isto é **1 ponto** — sobra 1 na trilha no sucesso, 2 na falha. A conta importa porque
**12 pontos** é onde a Desvantagem começa para ele. E o modificador de CON não resolve nada disso: o canon é
explícito que dobrar CON de +2 para +4 quase não move o ritmo. A diferenciação está **no limiar**, e ele já
gastou todo esse orçamento.

### 5.2. Ruído e Medidor de Horda — o Pugilista não é furtivo

Pela precedência canônica (`docs/gdd/GDD_Ruido.md` §1), **Concussão vence Cortante/Perfurante/Leve**, e corpo a corpo de
Concussão é **Nível Baixo (1)**:

| Efeito | Valor |
|---|---|
| Nível de Ruído do punho | **Baixo (1)** |
| Raio de Atração | **4 hex (6 m)** — todo mutante não engajado dentro dele move-se na direção do som |
| Pontos no Medidor de Horda | **1 por rodada** em que o punho seja o ruído mais alto do grupo |
| Rodadas de punho para uma leva, em grupo silencioso | **20** (limiar 20, em escada) |

`docs/gdd/GDD_Horda.md` §5 garante que a via **puramente silenciosa** nunca chama leva. **Um Pugilista quebra essa
garantia:** num grupo que só usa faca, facão, arco ou besta (Nível 0), toda rodada em que ele soca converte a
rodada de **0 para 1 ponto**. Vinte rodadas depois — que podem ser cinco combates de quatro rodadas na **mesma
cena**, porque o Medidor só zera no **fim da cena** — chega a primeira leva de **2 errantes**.

Ele **não é a versão furtiva do corpo a corpo**: paga a moeda da Infecção em cheio *e* a moeda da Horda em Nível Baixo, e a inversão medida do canon não o protege. A proficiência não oferece saída: **toda** arma de Concussão é Baixo, e Pesada também cai em Baixo — **nada na proficiência do Pugilista o deixa em Nível 0**.

### 5.3. Modificações

- O punho não tem slot, não é arma de fogo e não é Frágil: não recebe silenciador nem Gambiarra, não herda o
  **`+1` na faixa de quebra** que cada Gambiarra acrescenta (`docs/gdd/GDD_Combate.md` §7.3) e **não pode quebrar** — a
  arma principal dele não consome componentes. Em troca, é o único que **não pode melhorar a arma principal de
  forma alguma**: o punho continua 1d6 até o fim da campanha, e um avanço da assinatura é `[A CALIBRAR]`.
- Ele mantém a porta suave como qualquer um: **Gambiarra em campo com `+1` de quebra**, tier bom com o
  Cientista — aplicável às armas de Concussão que carregue *além* do punho, como a Soqueira. **Teto de dado
  1d12 absoluto**: poder de tier alto vem de efeito, nunca de dado maior.

## 6. Progressão — níveis 1 a 20

> **Nível máximo é 20** (Aprovação 019). O ritmo é **idêntico nas oito classes**, para a mesa nunca
> precisar consultar qual nível dá o quê. Ao fim da carreira: **8 Especializações · 5 Aumentos de
> atributo · 5 Recursos de classe · 1 Ápice**.

A linha desta classe é **o corpo como arma** — os cinco Recursos escalam essa ideia, não somam bônus soltos.

| Nível | Prof. | HP ganho | Limiar Inf. | Ganho de classe | Especialização |
|---|---|---|---|---|---|
| **1** | +2 | **10 + mod CON** | **17** | Classe, assinatura, proficiências | — |
| **2** | +2 | +6 + mod CON | 17 | **Punho Endurecido** — o punho passa a **1d8** | — |
| **3** | +2 | +6 + mod CON | 17 | — | **Especialização** |
| **4** | +2 | +6 + mod CON | 17 | **Aumento de atributo** | — |
| **5** | +3 | +6 + mod CON | **18** | — | **Especialização** |
| **6** | +3 | +6 + mod CON | 18 | **Agarrão** — ao acertar, pode **Agarrar** sem gastar ação extra | — |
| **7** | +3 | +6 + mod CON | 18 | — | **Especialização** |
| **8** | +3 | +6 + mod CON | 18 | **Aumento de atributo** | — |
| **9** | +4 | +6 + mod CON | **19** | — | **Especialização** |
| **10** | +4 | +6 + mod CON | 19 | **Punho Endurecido II** — **1d10**; e o punho ignora **meia cobertura** | — |
| **11** | +4 | +6 + mod CON | 19 | — | **Especialização** |
| **12** | +4 | +6 + mod CON | 19 | **Aumento de atributo** | — |
| **13** | +5 | +6 + mod CON | **20** | — | **Especialização** |
| **14** | +5 | +6 + mod CON | 20 | **Couro Grosso** — cada golpe necrótico recebido gera **1 ponto de Infecção a menos** (mínimo 0) | — |
| **15** | +5 | +6 + mod CON | 20 | — | **Especialização** |
| **16** | +5 | +6 + mod CON | 20 | **Aumento de atributo** | — |
| **17** | +6 | +6 + mod CON | **21** | — | **Especialização** |
| **18** | +6 | +6 + mod CON | 21 | **Punho Endurecido III** — **1d12** | — |
| **19** | +6 | +6 + mod CON | 21 | **Aumento de atributo** | — |
| **20** | +6 | +6 + mod CON | 21 | **ÁPICE — **Nunca Desarmado** — o punho conta como arma de tier **Protótipo**; você ataca **duas vezes** com a Ação, e a segunda não soma o modificador de dano** | — |

**HP total no nível 20:** 124 + (20 × mod CON). Com CON +3, isso dá **184 HP**.

> **O limiar de Infecção sobe +1 nos níveis 5, 9, 13 e 17** — de 17 para **21** ao fim da carreira.
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

**O que o Pugilista oferece.** `Combate Desarmado` (o punho como 1d6 Concussão, Ágil) é a assinatura e,
portanto, a especialização **mais cara**, só em nível alto: pré-requisito `[A CALIBRAR]`. Especializações
menores da classe: `[A CALIBRAR]` — o canon §4 mantém aberta a lista de **todas** as oito.

**O que combina bem com ele** (níveis mínimos valem os de `docs/gdd/GDD_Especializacoes.md`):

| Origem | Por que combina |
|---|---|
| **Médico** — *Estabilizar* | Remove pontos da Trilha de um aliado **adjacente**, e adjacência é onde ele já está por obrigação. Somando o limiar 17 ao maior do jogo (18), ataca de frente o único recurso que a classe gasta sem parar |
| **Médico** — Leves e Perfurantes | Abre o Nível **Silencioso (0)**, que a proficiência de Concussão nunca dá |
| **Explorador** — *Esquiva Reflexa* | Reação que impõe Desvantagem a um ataque contra você. O punho **não é Lenta**, então ele mantém a Reação depois de atacar: menos golpe recebido é menos ponto de Infecção |
| **Piloto**, **Construtor**, **Cientista** | Portas suaves: cobrem tudo que a classe não faz fora de combate |

**O que não combina.** *Tiro Calculado* (Atirador de Elite) exige a Ação **Mirar** inteira, válida só se o
personagem não se moveu, e exige arma de fogo — fora das duas proficiências: quem vale por estar a 1 hex não
gasta turnos parado mirando. *Oficina de Campo* (Cientista) é inerte para a arma principal, que não tem slot.

> A oitava classe do canon não é tratada nesta seção: seu nome ainda não foi decidido pelo Diretor.

*Nível 1 conforme `CANON_CLASSES.md` (Aprovação 016). Todo campo `[A CALIBRAR]` aguarda o próximo ciclo de
proposta e aprovação de balanceamento; alterações no nível 1 exigem nova aprovação do Diretor de Criação.*
