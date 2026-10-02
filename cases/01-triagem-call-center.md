# Caso 01: Agente de triagem por voz em call center

**Setor:** serviços financeiros | **Papel:** Product Owner

## Contexto

Operação de call center com alto volume de ligações e triagem feita manualmente por atendentes antes de direcionar cada cliente.

## Problema

A triagem consumia tempo de atendente qualificado em tarefa repetitiva, e a classificação das chamadas era inconsistente entre operadores.

## Decisões de produto

- Agente de IA de voz integrado ao discador da operação via SIP Trunk.
- Histórias específicas para **tabulação** (classificação de cada chamada) e **escalonamento** (passagem para atendente humano).
- Após a entrega, conduzi uma **auditoria pós-entrega** contra a Definition of Done. Ela revelou lacunas justamente em tabulação e escalonamento.
- Em vez de tratar como bug avulso, abri um **épico de correções** com histórias próprias e critérios de aceite reescritos para serem binários.
- Migração do motor de voz para nova plataforma durante o ciclo de correções.

## Aprendizado

Entregue não é aceito. A auditoria pós-entrega encontrou o que o QA funcional não pegou, porque os critérios originais permitiam interpretação. Desde então, todo critério que escrevo passa no teste: duas pessoas testando chegam à mesma conclusão?
