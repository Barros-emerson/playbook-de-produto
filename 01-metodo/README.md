# Método

Como conduzo um produto do primeiro contato ao aceite. O método nasceu da prática em projetos de IA sob medida. Os quatro portões e a regra de critério de aceite testável foram formalizados em um plano de redução de retrabalho de minha autoria. O funil de triagem da priorização é o processo de consultoria da empresa em que atuei, que apliquei nos projetos.

## Fluxo ponta a ponta

| # | Etapa | Pergunta que a etapa responde | Onde está |
|---|---|---|---|
| 01 | Discovery | Qual dor resolver, como ela acontece hoje e o que mede o sucesso? | [discovery.md](discovery.md) |
| 02 | Entendimento do problema | Quanto a dor custa, e a solução precisa mesmo de IA? | [discovery.md](discovery.md#entendimento-do-problema) |
| 03 | Levantamento de requisitos | O que o produto precisa fazer, para quem e com quais regras? | [requisitos.md](requisitos.md) |
| 04 | Definição da solução | Qual desenho atende à dor com os dados e sistemas disponíveis? | [requisitos.md](requisitos.md#da-necessidade-à-solução) |
| 05 | Priorização | O que entra primeiro e o que fica fora? | [priorizacao.md](priorizacao.md) |
| 06 | MVP | Qual o menor escopo que entrega valor e testa a hipótese? | [definicao-de-mvp.md](definicao-de-mvp.md) |
| 07 | PRD | Onde está a fonte única da verdade do escopo? | [requisitos.md](requisitos.md#prd) e [template](../03-templates/prd.md) |
| 08 | User stories | Como o escopo vira unidade de trabalho para o time? | [requisitos.md](requisitos.md#user-stories) e [template](../03-templates/user-story.md) |
| 09 | Critérios de aceite | Como o time sabe que a entrega está correta? | [criterios-de-aceite.md](criterios-de-aceite.md) e [template](../03-templates/criterios-de-aceite.md) |
| 10 | DoR e DoD | Quando a história pode entrar no desenvolvimento e quando está pronta? | [handoff-e-validacao.md](handoff-e-validacao.md) e [template](../03-templates/dor-dod.md) |
| 11 | Desenvolvimento | Como o PO sustenta o time durante a execução? | [handoff-e-validacao.md](handoff-e-validacao.md#durante-o-desenvolvimento) |
| 12 | Validação | Como confirmo com o cliente que o critério passou? | [handoff-e-validacao.md](handoff-e-validacao.md#validação-e-aceite) |
| 13 | Tomada de decisão | Com quais critérios mantenho, troco ou retiro escopo? | [tomada-de-decisao.md](tomada-de-decisao.md) |
| 14 | Gestão de riscos | O que pode derrubar a entrega e como mitigar? | [gestao-de-riscos.md](gestao-de-riscos.md) |
| 15 | Melhoria contínua | O que a entrega ensinou e o que muda no processo? | [handoff-e-validacao.md](handoff-e-validacao.md#melhoria-contínua) |

## Os quatro portões

O fluxo é organizado em quatro etapas encadeadas. Cada uma tem checklist, e a demanda só avança quando o checklist fecha.

1. **Entrada:** receber do comercial o escopo vendido completo, inclusive o que foi prometido ou demonstrado ao cliente.
2. **Discovery:** confirmar dor, processo atual, dados disponíveis e métrica de sucesso com quem decide e com quem opera.
3. **Congelamento:** PRD revisado e aceito pelo cliente antes da criação dos cards.
4. **Handoff:** entrega ao desenvolvimento com DoR completa, incluindo acessos, credenciais de teste e dependências resolvidas.

Entre as etapas, os três pontos de passagem mais críticos são Comercial para Produto, Produto para Congelamento (com o cliente) e Produto para Desenvolvimento.
