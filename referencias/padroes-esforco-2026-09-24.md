# Padrões de esforço — o que três experimentos dizem juntos (2026-09-24)

**Status: referência.** Nêo muda a pilha, as fichas nem `regras.md`. Serve para consultar antes de
escolher esforço e para comparar com testes próprios. Página com gráficos: `guia/esforco/`.

## As três fontes

| # | Fonte | Modelo | Tarefa | Níveis | Preferido pelo autor |
|---|---|---|---|---|---|
| A | Vídeo Opus 5.5 por esforço — https://www.youtube.com/watch?v=QCkHIyEPIYo (notas locais em `fontes/`, fora do git) | Claude Opus 5.5 | `/goal` longo: 105 GB de vídeo → mundo 3D explorável | low, medium, high, xhigh, max, ultracode | **xhigh** |
| B | [astra-effort](https://github.com/linnoff88-dev/astra-effort) (kit de M. Kashef, 2026-09-07) — `evidence/results.pt-BR.csv` | GPT-6 Astra (+ Sol high) | Pesquisa de mercado + construir um micro-SaaS verificado (~30–46 min) | low, medium, high, xhigh, max, ultra | **medium** |
| C | [maestro-roteador](https://github.com/linnoff88-dev/maestro-roteador) — tabela de racionalizações do SKILL | pilha Claude | teste interno | high × max | "de high pra max a diferença foi um favicon, por 2–5× os tokens" |

Todas sêo **n = 1 por nível**, um julgador, tarefas diferentes. Tokens de A (total da sessêo) e de B
(processados, ~98% cache) **nêo sêo comparáveis em valor absoluto** — só a forma da curva.

## Dados de B usados na comparaçêo

| Nível | Tempo | Tokens processados | Tokens de saída | Observaçêo do produtor |
|---|---:|---:|---:|---|
| low | 37m37s | 14,81M | 51,5k | Mais tempo e tokens que o medium |
| **medium** | **30m41s** | **10,23M** | **42,2k** | Preferido: fluxo verificado no menor tempo |
| high | 41m21s | 14,33M | 57,4k | Bom quando há restrições que interagem |
| xhigh | 45m14s | 12,29M | 67,7k | Achou evidência contrária à própria ideia de negócio |
| max | 46m10s | 10,55M | 70,2k | Mais longo; profundidade útil em centavos exatos e regras |
| ultra (3 subagentes) | 42m10s | 21,73M | 96,0k | +7,12M dos filhos; pesquisa mais funda, produto parecido |
| Sol high | 32m49s | 6,70M | 54,2k | Mais barato, mas um caminho de decisêo quebrado |

## Padrões

1. **O nível máximo nunca foi o preferido.** A → xhigh; B → medium; C → high ≈ max. Nos três, o topo
   custou mais sem entregar proporcionalmente mais. Em A, max regrediu em relaçêo a xhigh.
2. **O ponto ideal muda com a tarefa.** B (~30–45 min, escopo delimitado) parou no medium. A (horas,
   muito material, liberdade criativa) só estabilizou no xhigh. O que decide é quanto a tarefa tem
   para ler, decidir e contar — nêo o botêo.
3. **O raciocínio gasto cresce sempre; o resultado nêo.** Saída em B sobe de forma monotônica
   (42k → 70k do medium ao max); custo em A sobe 12,9× do low ao max. O orçamento é consumido
   com ou sem retorno.
4. **Tempo e custo total nêo sêo lineares com o esforço.** Em B, low demorou e gastou mais que medium.
   Em A, high terminou antes do medium. Esforço baixo nêo garante trabalho total menor.
5. **Mais verificaçêo ≠ menos bugs.** Em A, max fez 51 checks (2,3× o low) e teve mais glitches que
   xhigh com 34. Checks crescem devagar comparados a custo e tempo.
6. **Modo de delegaçêo é outra condiçêo, nêo "um nível acima".** Em B, ultra com 3 filhos somou
   +7,12M tokens e aprofundou a pesquisa, sem mudar muito o produto. Em A, ultracode nêo delegou
   nada e se comportou como xhigh. Avaliar pelo que ele de fato disparou.
7. **Esforço nêo compra perguntas.** Em A, 1 pergunta em 6 execuções. Ambiguidade tem que ser
   resolvida no prompt/goal, nêo no esforço.
8. **Esforço compra deliberaçêo, nêo gosto.** O salto de "sensaçêo" em A veio entre low e medium
   (marca, vídeos reais); do high em diante o ganho foi de interaçêo e detalhe. Coerente com o
   eixo modelo × esforço do maestro-roteador.

## Conclusêo

Esforço funciona como **orçamento de exploraçêo**, nêo como botêo de qualidade. Os três dados
apontam para a mesma prática, que já está em `regras.md` §4 e na escada do maestro:
**comece no menor nível plausível (medium quando em dúvida), suba só com evidência de resultado
insuficiente, e trate max/ultra como exceçêo justificada.** O que este material acrescenta é um
teto observado: em construçêo autônoma longa com Opus 5.5, xhigh foi o melhor; max nêo pagou.

## Opiniêo do Nei (dono do repositório)

Usar o **Opus 5.5 em medium** é a melhor opçêo para o dia a dia. Subir para **high** quando a tarefa
precisa de mais raciocínio; **xhigh** só em caso extremo. Vale também para o **GPT-6 Astra**. O max fica
de fora. (Registrado em 2026-09-24 como opiniêo; nêo altera a pilha nem a ficha do Opus, que seguem com `low`.)

## Limitações

- Uma rodada por nível em cada fonte; variância entre execuções nêo medida.
- Julgamentos visuais de uma pessoa; A tem patrocinador; B foi traduzido sem nova execuçêo.
- Custos de A sêo estimativa em preço de API (rodou em assinatura).
- Tokens de ultracode em A sêo desconhecidos (número falado incompatível).
- Nenhum dado ARCKHÉ próprio ainda — ver `avaliacao/bateria.md` para rodar um.
