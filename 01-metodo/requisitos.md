# Requisitos

Como a dor confirmada no discovery vira escopo que o time consegue construir e o cliente consegue aceitar.

## Da necessidade à solução

1. **Necessidade:** o que o usuário precisa conseguir fazer, sem citar tecnologia.
2. **Restrições:** sistemas que já existem, dados disponíveis, limites de integração, prazo e orçamento.
3. **Solução:** o desenho que atende à necessidade dentro das restrições. Quando um sistema de terceiro não suporta o que a solução pressupõe, a solução muda, não a restrição.

Exemplo de restrição que mudou a solução: em um call center, a discadora recebia apenas o áudio da chamada e não processava dados de volta. Em vez de insistir na integração da tabulação, a decisão foi gerar o relatório de tabulação no ambiente próprio da solução ([case 04](../02-cases/04-agente-de-voz-call-center/)).

## PRD

- **Um PRD por projeto**, com vários épicos dentro. É a fonte única da verdade do escopo.
- **Versionado.** Cada versão registra o que mudou e por quê.
- **Congelado antes dos cards.** O PRD é aceito pelo cliente antes de virar backlog. PRD aberto durante o desenvolvimento é retrabalho com data marcada.
- **Decisões e questões abertas registradas.** Cada decisão de escopo recebe um identificador (D-01, D-02...) e cada pendência também (Q-01, Q-02...). Uma questão só fecha quando uma decisão a resolve.

Template: [03-templates/prd.md](../03-templates/prd.md).

## Épicos

- Um épico agrupa histórias que entregam uma capacidade completa do produto.
- Épico também é unidade de negociação: cancelar ou substituir um épico inteiro é uma decisão de escopo legítima, registrada no PRD ([case 03](../02-cases/03-gestao-de-escopo-imobiliario/)).
- Correções pós-entrega ganham um épico próprio, com histórias e critérios reescritos, em vez de bugs avulsos ([case 04](../02-cases/04-agente-de-voz-call-center/)).

## User stories

- Formato: **como** [persona], **quero** [ação], **para** [benefício de negócio].
- Cada história tem contexto, critérios de aceite, fora do escopo e dependências.
- Investigação não é história de produto com critério de aceite: vira tarefa. "Ouvir as gravações completas do lote de teste" foi tratada como tarefa, não como critério.

Template: [03-templates/user-story.md](../03-templates/user-story.md).

## Critérios de aceite

Regra que adotei como padrão: **toda história tem critério de aceite testável. Se o enunciado não fecha, a demanda não avança.**

- **Observável:** alguém consegue ver o resultado acontecer.
- **Binário:** passou ou não passou.
- **Sem interpretação:** duas pessoas testando chegam à mesma conclusão.
- O formato Dado/Quando/Então é opcional. Uso quando ajuda a clareza.

Critério vago típico que essa regra elimina: "responder bem o cliente".

Template com exemplos ruim x bom: [03-templates/criterios-de-aceite.md](../03-templates/criterios-de-aceite.md).
