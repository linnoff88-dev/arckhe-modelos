ï»¿# ê°Å¸Â§Â­ Qual Modelo de IA Usar

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


> O modelo certo para cada tarefa êÂ· repositêÂ³rio `modelos`

[![Qual modelo de IA usar](guia/assets/banner.jpg)](https://inematds.github.io/modelos/guia/)

Muitos modelos chegaram ao mesmo tempo. A resposta prêÂ¡tica êÂ© simples:
**use o melhor modelo para cada tarefa, sem lealdade a nenhuma plataforma.**

ê°Å¸ââ **Guia:** [PortuguêÂªs](https://inematds.github.io/modelos/guia/) êÂ· [English](https://inematds.github.io/modelos/guia/en/) êÂ· [EspaêÂ±ol](https://inematds.github.io/modelos/guia/es/)
ê°Å¸Â§Â© **Modelos explicados de forma simples:** [PT](https://inematds.github.io/modelos/guia/modelos/) êÂ· [EN](https://inematds.github.io/modelos/guia/en/modelos/) êÂ· [ES](https://inematds.github.io/modelos/guia/es/modelos/)

---

## VisêÂ£o rêÂ¡pida dos modelos

### ê°Å¸Å¸Â  Claude Opus 5.5 ê¢â¬â o melhor para uso geral
- RêÂ¡pido, direto e econêÂ´mico em tokens.
- Excelente em projetos complexos; precisa de poucas instruêÂ§êÂµes.
- Forte em criativo, design, vêÂ­deo, pesquisa e navegador.
- **Modelo principal para o dia a dia**, em esforêÂ§o baixo.

### ê°Å¸âÂ· GPT-6 Astra ê¢â¬â planejamento e problemas difêÂ­ceis
- Pensar antes de fazer: planejar, decidir arquitetura, simular cenêÂ¡rios.
- EsforêÂ§o mêÂ©dio a alto (acima disso nêÂ£o houve ganho).

### ê¢Ëâ¬ê¯Â¸Â GPT-6 Sol ê¢â¬â execuêÂ§êÂ£o com bom custo
- Bom e econêÂ´mico, mas abaixo do Astra no que êÂ© exigente.
- Faz sentido para tarefas **jêÂ¡ bem definidas** e para consertar cêÂ³digo com testes.
- EstratêÂ©gia: **planejar com Astra ê¢â â executar com Sol**.

### ê°Å¸Åâ¢ GPT-6 Luna ê¢â¬â trabalho braêÂ§al
- Tarefas repetitivas, claras e sem ambiguidade.
- **Luna Low:** simples e rêÂ¡pido. **Luna High / X-High:** pesado e operacional.

### ê¢Åâê¯Â¸Â Grok 4.7 ê¢â¬â fora
- ExperiêÂªncia ruim; inferior ao 4.6. NêÂ£o entrou na pilha.

### ê°Å¸âÅ½ Claude Fable 5.1 ê¢â¬â perdeu espaêÂ§o
- Consome muitos tokens; o Opus 5.5 entrega o mesmo ou mais por menos.
- Para caso ambêÂ­guo, prefira **Astra + Opus 5.5 como segunda opiniêÂ£o**.

### ê¢Å¾â Claude Sonnet 5 e Haiku 4.5 ê¢â¬â pular
- Sonnet 5 gasta demais por tarefa; o Haiku atual êÂ© fraco. Dentro do Claude, use o Opus 5.5 em esforêÂ§o baixo.

---

## A pilha hoje

| Papel | Modelo | EsforêÂ§o |
|---|---|---|
| Planejamento e problemas difêÂ­ceis | **GPT-6 Astra** | mêÂ©dioê¢â¬âalto |
| Uso geral e projetos complexos | **Claude Opus 5.5** | baixo |
| Criativo, design, vêÂ­deo, navegador | **Claude Opus 5.5** | baixoê¢â¬âmêÂ©dio |
| ExecuêÂ§êÂ£o econêÂ´mica / consertar cêÂ³digo | **GPT-6 Sol** | mêÂ©dioê¢â¬âalto |
| Tarefas repetitivas | **GPT-6 Luna** (Low ou High/X-High) | conforme o peso |
| Muitas subtarefas em paralelo | **Opus 5.5 orquestra + Sol/Luna executam** | ê¢â¬â |
| Caso ambêÂ­guo | **Astra propêÂµe + Opus 5.5 revisa** | ê¢â¬â |

Uso e testes **via assinaturas** (plano Claude + plano Codex), nêÂ£o API: "custo" = quanto da cota cada modelo consome.

## Regra principal

**NêÂ£o confie apenas em benchmarks. Teste os modelos nas suas prêÂ³prias tarefas.**

ê¢Å¡Â ê¯Â¸Â **Efeito lua de mel:** modelos novos parecem incrêÂ­veis nos primeiros dias. Espere uma semana,
observe estabilidade, qualidade e custo antes de mudar toda a pilha.
PrêÂ³xima revisêÂ£o: **2026-09-30**.

---

## Como usar este repositêÂ³rio

| Queroê¢â¬Â¦ | Abra |
|---|---|
| Decidir rêÂ¡pido | a tabela acima |
| Detalhe de um modelo | [`modelos/`](modelos/) ê¢â¬â uma ficha por modelo (YAML: status, melhor para, evitar para, esforêÂ§o) |
| Ver dados de esforêÂ§o (Opus 5.5 êâ Astra, com grêÂ¡ficos) | [guia/esforco/](https://inematds.github.io/modelos/guia/esforco/) êÂ· [`referencias/padroes-esforco-2026-09-24.md`](referencias/padroes-esforco-2026-09-24.md) ê¢â¬â referêÂªncia, nêÂ£o regra |
| Usar dois modelos juntos | [`prompts/`](prompts/) ê¢â¬â planejarê¢â âexecutar, segunda opiniêÂ£o, orquestrador+workers, tarefa braêÂ§al |
| Entender as regras | [`regras.md`](regras.md) ê¢â¬â sem lealdade, lua de mel, cota por resultado, um agente por pasta, teste de 30 min |
| Testar nas minhas tarefas | [`avaliacao/bateria.md`](avaliacao/bateria.md) ê¢â¬â 8 casos reais com nota 0ê¢â¬â3 |
| Registrar o que observei | [`log.md`](log.md) ê¢â¬â uma linha por observaêÂ§êÂ£o |
| Virar skill | [`skills/`](skills/) ê¢â¬â rascunho `escolher-modelo` (ainda nêÂ£o instalado) |

O guia (landing) êÂ© gerado por `python3 guia/_src/build.py` ê¢â¬â o texto das 3 lêÂ­nguas fica nesse script.

## RelaêÂ§êÂ£o com outras ferramentas

- **`/maestro-roteador`** decide modelo êâ esforêÂ§o dentro da pilha Claude. Este repositêÂ³rio êÂ© o catêÂ¡logo multi-provedor.
  O maestro ainda recomenda Sonnet/Haiku/Fable, o que conflita com a pilha acima ê¢â¬â revisar apêÂ³s 2026-09-30 (ver [`log.md`](log.md)).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>