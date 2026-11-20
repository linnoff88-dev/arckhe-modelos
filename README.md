# ðŸ§­ Qual Modelo de IA Usar

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


> O modelo certo para cada tarefa Â· repositÃ³rio `modelos`

[![Qual modelo de IA usar](guia/assets/banner.jpg)](https://inematds.github.io/modelos/guia/)

Muitos modelos chegaram ao mesmo tempo. A resposta prÃ¡tica Ã© simples:
**use o melhor modelo para cada tarefa, sem lealdade a nenhuma plataforma.**

ðŸ“– **Guia:** [PortuguÃªs](https://inematds.github.io/modelos/guia/) Â· [English](https://inematds.github.io/modelos/guia/en/) Â· [EspaÃ±ol](https://inematds.github.io/modelos/guia/es/)
ðŸ§© **Modelos explicados de forma simples:** [PT](https://inematds.github.io/modelos/guia/modelos/) Â· [EN](https://inematds.github.io/modelos/guia/en/modelos/) Â· [ES](https://inematds.github.io/modelos/guia/es/modelos/)

---

## VisÃ£o rÃ¡pida dos modelos

### ðŸŸ  Claude Opus 5.5 â€” o melhor para uso geral
- RÃ¡pido, direto e econÃ´mico em tokens.
- Excelente em projetos complexos; precisa de poucas instruÃ§Ãµes.
- Forte em criativo, design, vÃ­deo, pesquisa e navegador.
- **Modelo principal para o dia a dia**, em esforÃ§o baixo.

### ðŸ”· GPT-6 Astra â€” planejamento e problemas difÃ­ceis
- Pensar antes de fazer: planejar, decidir arquitetura, simular cenÃ¡rios.
- EsforÃ§o mÃ©dio a alto (acima disso nÃ£o houve ganho).

### â˜€ï¸ GPT-6 Sol â€” execuÃ§Ã£o com bom custo
- Bom e econÃ´mico, mas abaixo do Astra no que Ã© exigente.
- Faz sentido para tarefas **jÃ¡ bem definidas** e para consertar cÃ³digo com testes.
- EstratÃ©gia: **planejar com Astra â†’ executar com Sol**.

### ðŸŒ™ GPT-6 Luna â€” trabalho braÃ§al
- Tarefas repetitivas, claras e sem ambiguidade.
- **Luna Low:** simples e rÃ¡pido. **Luna High / X-High:** pesado e operacional.

### âœ–ï¸ Grok 4.7 â€” fora
- ExperiÃªncia ruim; inferior ao 4.6. NÃ£o entrou na pilha.

### ðŸ’Ž Claude Fable 5.1 â€” perdeu espaÃ§o
- Consome muitos tokens; o Opus 5.5 entrega o mesmo ou mais por menos.
- Para caso ambÃ­guo, prefira **Astra + Opus 5.5 como segunda opiniÃ£o**.

### âž– Claude Sonnet 5 e Haiku 4.5 â€” pular
- Sonnet 5 gasta demais por tarefa; o Haiku atual Ã© fraco. Dentro do Claude, use o Opus 5.5 em esforÃ§o baixo.

---

## A pilha hoje

| Papel | Modelo | EsforÃ§o |
|---|---|---|
| Planejamento e problemas difÃ­ceis | **GPT-6 Astra** | mÃ©dioâ€“alto |
| Uso geral e projetos complexos | **Claude Opus 5.5** | baixo |
| Criativo, design, vÃ­deo, navegador | **Claude Opus 5.5** | baixoâ€“mÃ©dio |
| ExecuÃ§Ã£o econÃ´mica / consertar cÃ³digo | **GPT-6 Sol** | mÃ©dioâ€“alto |
| Tarefas repetitivas | **GPT-6 Luna** (Low ou High/X-High) | conforme o peso |
| Muitas subtarefas em paralelo | **Opus 5.5 orquestra + Sol/Luna executam** | â€” |
| Caso ambÃ­guo | **Astra propÃµe + Opus 5.5 revisa** | â€” |

Uso e testes **via assinaturas** (plano Claude + plano Codex), nÃ£o API: "custo" = quanto da cota cada modelo consome.

## Regra principal

**NÃ£o confie apenas em benchmarks. Teste os modelos nas suas prÃ³prias tarefas.**

âš ï¸ **Efeito lua de mel:** modelos novos parecem incrÃ­veis nos primeiros dias. Espere uma semana,
observe estabilidade, qualidade e custo antes de mudar toda a pilha.
PrÃ³xima revisÃ£o: **2026-09-30**.

---

## Como usar este repositÃ³rio

| Queroâ€¦ | Abra |
|---|---|
| Decidir rÃ¡pido | a tabela acima |
| Detalhe de um modelo | [`modelos/`](modelos/) â€” uma ficha por modelo (YAML: status, melhor para, evitar para, esforÃ§o) |
| Ver dados de esforÃ§o (Opus 5.5 Ã— Astra, com grÃ¡ficos) | [guia/esforco/](https://inematds.github.io/modelos/guia/esforco/) Â· [`referencias/padroes-esforco-2026-09-24.md`](referencias/padroes-esforco-2026-09-24.md) â€” referÃªncia, nÃ£o regra |
| Usar dois modelos juntos | [`prompts/`](prompts/) â€” planejarâ†’executar, segunda opiniÃ£o, orquestrador+workers, tarefa braÃ§al |
| Entender as regras | [`regras.md`](regras.md) â€” sem lealdade, lua de mel, cota por resultado, um agente por pasta, teste de 30 min |
| Testar nas minhas tarefas | [`avaliacao/bateria.md`](avaliacao/bateria.md) â€” 8 casos reais com nota 0â€“3 |
| Registrar o que observei | [`log.md`](log.md) â€” uma linha por observaÃ§Ã£o |
| Virar skill | [`skills/`](skills/) â€” rascunho `escolher-modelo` (ainda nÃ£o instalado) |

O guia (landing) Ã© gerado por `python3 guia/_src/build.py` â€” o texto das 3 lÃ­nguas fica nesse script.

## RelaÃ§Ã£o com outras ferramentas

- **`/maestro-roteador`** decide modelo Ã— esforÃ§o dentro da pilha Claude. Este repositÃ³rio Ã© o catÃ¡logo multi-provedor.
  O maestro ainda recomenda Sonnet/Haiku/Fable, o que conflita com a pilha acima â€” revisar apÃ³s 2026-09-30 (ver [`log.md`](log.md)).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>