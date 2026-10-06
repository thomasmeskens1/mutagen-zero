# MUTAGEN:ZERO — Trilha de Infecção

> **O que este documento é.** A Trilha de Infecção é uma das duas moedas de atrito de
> MUTAGEN:ZERO — o preço que o combate corpo a corpo cobra do corpo do personagem. A outra moeda é
> o **Medidor de Horda** (`docs/gdd/GDD_Horda.md`), que é o preço que o combate à distância cobra do
> ambiente. Nenhuma das duas vias é gratuita, e as duas **não têm o mesmo ritmo**: a Horda é
> pressão rápida e recuperável; a Infecção é desgaste lento e **permanente**.

> **Regras relacionadas:** dano Necrótico e tipos de dano em `docs/gdd/GDD_Combate.md` §6.3 · condição
> **Infectado** em §10 · armas anti-Infecção de raridade extrema em `docs/gdd/GDD_Armas.md` §7.4 ·
> a inversão entre silêncio e infecção em `docs/gdd/GDD_Ruido.md`.


## 1. Acúmulo

**Todo dano do tipo Necrótico causado por mutantes ou zumbis gera pontos de Infecção.**

| Evento | Pontos de Infecção |
|---|---|
| Golpe necrótico que acerta | **1** |
| Acerto **crítico** necrótico | **2** |

Os pontos acumulam **durante o combate** e ficam registrados na ficha. Note que a conversão é **por
ataque acertado**, não proporcional ao dano: um mutante que arranha muitas vezes é mais perigoso
para a sua trilha que um que acerta um golpe forte.

## 2. Resolução ao fim do combate

**Ao fim do combate**, todo personagem com pontos de Infecção faz um **teste de CON**:

```
Teste de Infecção = d20 + modificador de CON vs. CD de Infecção
```

- **CD de Infecção = 10 + pontos ganhos naquele combate.** Ela **escala**, e isso é o coração da
  mecânica: quanto mais golpe necrótico você levou, menor a chance de não converter aquilo em dano
  permanente. Uma luta ruim se torna duas vezes ruim.
- **Sucesso:** remove **metade** dos pontos ganhos naquele combate, arredondando para baixo.
- **Falha:** os pontos ganhos permanecem **integralmente** na trilha.

> **O modificador de CON é um dial fraco de propósito.** Medido por simulação: dobrar o modificador
> de CON de `+2` para `+4` quase não altera o ritmo — a marreta continua chegando ao limiar em 8
> lutas, o rifle passa de 14 para 15. A razão é que o sucesso só remove metade e a CD cresce com o
> que foi levado. **A diferenciação entre personagens deve vir do limiar (§9.3), não do atributo.**

## 3. O limiar

**Atingir o limiar da trilha de Infecção causa mutação ou morte.**

**Limiar base: 15.** O limiar é **pessoal** e varia por classe (ver abaixo).

#### As bandas são proporcionais ao limiar pessoal

Como o limiar muda de personagem para personagem, as bandas são frações dele, não valores fixos:

| Faixa | Estado | Efeito |
|---|---|---|
| até **1/3** do limiar | **Saudável** | Nenhum. O corpo aguenta |
| **1/3 a 2/3** | **Infectado** | Sintomas visíveis. NPCs reagem — custo **social**, não mecânico |
| **2/3 até o limiar** | **Infectado grave** | **Desvantagem** nos testes de CON contra Infecção. A espiral começa |
| **no limiar** | **Mutação ou morte** | Fim da linha |

> **Convenção de arredondamento.** As frações `1/3` e `2/3` são **truncadas para baixo**. Com
> limiar 15 elas caem em números inteiros; com outros limiares, não. Exemplos canônicos:
>
> | Limiar | Saudável | Infectado | Infectado grave | Fim |
> |---|---|---|---|---|
> | 12 | 0–4 | 5–8 | 9–11 | 12 |
> | 13 | 0–4 | 5–8 | 9–12 | 13 |
> | 14 | 0–4 | 5–9 | 10–13 | 14 |
> | **15** | **0–5** | **6–10** | **11–14** | **15** |
> | 16 | 0–5 | 6–10 | 11–15 | 16 |
> | 17 | 0–5 | 6–11 | 12–16 | 17 |
> | 18 | 0–6 | 7–12 | 13–17 | 18 |

Com o limiar base de 15, isso dá: **0–5** Saudável · **6–10** Infectado · **11–14** Infectado
grave · **15** mutação ou morte.

> **A banda do meio não morde de propósito.** É a **banda de aviso**: você vê que está ficando
> doente, os outros à mesa veem, os NPCs reagem — e ainda dá tempo de agir. A espiral mecânica só
> começa em 2/3, e quando começa ela é cruel, o que é exatamente o ponto.

#### Modificador de classe

A classe do personagem **desloca o limiar**, na faixa de aproximadamente `±3` sobre a base 15.
A intenção de design é que resistência física seja um eixo real de diferenciação: um personagem
voltado a medicina e biologia aguenta mais carga infecciosa; um batedor aguenta menos, e compra
essa fragilidade com mobilidade e esquiva.

| Exemplo | Limiar | Lutas até a mutação (marreta) |
|---|---|---|
| Batedor / Explorador | **12** | 6 |
| Base | **15** | 8 |
| Médico | **18** | 9 |

> **Os valores por classe JÁ estão fixados** (Aprovação 016). Ver os documentos `Classe_*.md`:

| Classe | Limiar | Classe | Limiar |
|---|---|---|---|
| **Médico** | **18** | Piloto | 15 |
| **Pugilista** | 17 | Ceifador | 14 |
| Construtor | 16 | **Atirador de Elite** | **13** |
| Cientista | 15 | **Explorador** | **12** |

> O que continua `[A CALIBRAR]` é a **progressão** desses valores em níveis 2+.

#### Ainda aberto

- **Critério entre mutação e morte** (rolagem, decisão do Diretor, ou tipo da criatura): `[A CALIBRAR]`.
- **Efeitos mecânicos de uma mutação:** `[A CALIBRAR]`.

#### Remoção

> **Aprovação 023 — duas mudanças de canon nesta seção.** (1) A instalação de Refúgio chama-se
> **Enfermaria**; *"Oficina médica"* **deixa de ser nome canônico** e não deve aparecer em documento
> nenhum. (2) O soro de remoção são **dois itens distintos**, não um.

São **quatro** as vias canônicas de remoção de pontos da Trilha:

| Via | O que é | Quem destrava |
|---|---|---|
| **Soro Anti-Infecção** | Item de **raridade extrema**. **Zera a Trilha inteira**, de qualquer banda | Ninguém. É **trava de distribuição**: só entra em jogo por decisão do Diretor (`docs/gdd/GDD_Armas.md` §7.4) |
| **Soro de Campo** | Fabricado pelo **Médico a partir do nível 14**. Remove **`N` pontos** — parcial, nunca zera | O Recurso de nível 14 do Médico, e a Especialização Maior que o exporta |
| **Enfermaria do Refúgio** | Descanso longo em Refúgio com Enfermaria | **Personagem nenhum.** É instalação, e é por isso que ela existe: o grupo sem Médico precisa de uma saída |
| **Armas anti-Infecção** | Raridade extrema, já canônicas (`docs/gdd/GDD_Armas.md` §7.4) | Ninguém; mesma trava do Soro |

**Os dois soros não são o mesmo item** e não devem compartilhar identificador no motor. O de raridade
extrema **zera**; o de Campo **reduz**. Esperar 14 níveis para ter a versão parcial e **repetível** do
item lendário é a troca — e é o que impede o Médico de anular a trava de distribuição sem tornar a
classe inútil.

**Toda produção consome componente** (Aprovação 023, regra geral em `docs/gdd/GDD_Modificacoes.md` §4): o
Soro de Campo consome **Química** por unidade fabricada. Isso torna *"um por descanso longo"* um
**teto**, não um piso — o Médico fabrica um **se tiver Química**, e no pós-apocalipse ele
frequentemente não tem.

As **quantidades e os tempos** continuam `[A CALIBRAR]`: quanto o Soro de Campo remove (`N`), quanto a
Enfermaria remove por descanso, e quantas unidades de Química cada soro custa.

---

---

*Este arquivo é canônico. Qualquer alteração exige nova aprovação do Diretor de Criação.
Os campos `[A CALIBRAR]` são o próximo ciclo de proposta e aprovação de balanceamento.*
