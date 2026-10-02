# Case 06: Discovery em uma empresa de planos assistenciais

**Setor:** planos assistenciais | **Papel:** Product Owner da consultoria, de ponta a ponta | **Período:** jul. a set. de 2026 | **Status:** especificação funcional entregue; projeto repassado a outro PO

> **Resumo.** Empresa de planos assistenciais com venda porta a porta. O discovery quantificou o gargalo em horas e mostrou que parte das dores se resolvia sem IA. A recomendação combinou melhorias de processo de baixo custo com 4 agentes de IA aprovados. Na revisão técnica, a integração com o sistema central se mostrou dependente de APIs que o fornecedor ainda precisava construir.

## Contexto

A empresa crescia reestruturando os processos comerciais. No primeiro contato, estava deslocando o foco de novas vendas para a retenção de clientes.

## Problema

- **Gargalo dominante:** validação manual de contratos, de 1,5 a 2 horas por dia, mais duas tardes inteiras no fim do mês para conciliar comissões.
- Cobrança, comissões e atendimento manuais.
- Atendimento lento fora do horário comercial.

## Responsabilidades

### Minha responsabilidade

| Atividade | Status |
|---|---|
| Product Owner da consultoria de ponta a ponta | Comprovado |
| Kickoff, junto com o gestor | Comprovado |
| Pelo menos cinco entrevistas individuais (gestão geral, liderança comercial, cobrança em campo, vendas internas e conferência) | Comprovado |
| Pacote do diagnóstico: DDE, inventário de processos, sistemas e lacunas, fricções e oportunidades, sugestões de melhoria sem IA, viabilidade das implementações de IA | Comprovado |
| Matriz de priorização ICE | Comprovado |
| Apresentação das oportunidades | Comprovado |
| Especificação funcional (v0.3 e v0.4) | Comprovado |
| Revisão técnica do PRD | Comprovado |
| Mapeamento dos requisitos de API para o cliente levar ao fornecedor | Comprovado |

### Responsabilidade de outras partes

| Parte | Papel documentado |
|---|---|
| Liderança técnica | Revisão técnica do PRD |
| Fornecedor do sistema do cliente | Construção das 4 APIs de que o cronograma passou a depender |
| Cliente | Aprovação dos agentes; contato com o fornecedor |
| Outro Product Owner | Assumiu o projeto na transição |

## Discovery

- Entrevistas operacionais individuais, gravadas e transcritas.
- Classificação das fricções por impacto (alto, médio e baixo).
- **Correção do mapa de sistemas:** o sistema central de vendas não era o que constava no início.

## Insights

- A dor tinha tamanho: horas por dia na validação e tardes inteiras no fechamento do mês.
- Parte das dores se resolvia com ajuste nos sistemas e planilhas que a empresa já usava, sem IA.

## Decisão

| Decisão | Status |
|---|---|
| Apresentar melhorias sem IA junto com os agentes, em vez de vender apenas automação | Comprovado |
| Validação documental por cruzamento de dados (OCR), e não por IA lendo imagens | Comprovado. Justificativa: **[A VALIDAR]** |
| Atendimento com agente próprio, e não chatbot genérico | Comprovado |
| Mapear os requisitos de API para o cliente acelerar o fornecedor | Comprovado |

## Requisitos

Agentes aprovados em 14/09:

1. validação de documentos, que confere os dados do contrato contra o sistema e alerta o vendedor (prioridade máxima);
2. atendimento;
3. retenção e negociação;
4. cross-sell.

> **[CONFLITO ENTRE FONTES: VALIDAR]** Registros anteriores listavam outro conjunto de agentes (atendimento, validação, venda porta a porta e cobrança). Prevalece a lista aprovada na apresentação de 14/09; a diferença mostra a evolução do escopo durante a consultoria.

## Riscos e dependências

| Risco | Como apareceu |
|---|---|
| Sistema do fornecedor sem API | O cronograma passou a depender de 4 APIs a serem construídas pelo fornecedor |
| Validação técnica depois da aprovação | A inviabilidade da integração surgiu na revisão técnica de 23/09, após a aprovação dos agentes |

## Resultado

| Resultado | Status |
|---|---|
| 4 agentes aprovados | Comprovado |
| Especificação funcional v0.4 entregue em 23/09 | Comprovado |
| Economia de 2 a 3 horas por dia com o ajuste da planilha de cobrança | **Estimativa**, não medida |
| Resultado em produção | **[EVIDÊNCIA INSUFICIENTE]** |

## O que não deu certo

A inviabilidade de integração com o sistema central apareceu depois da aprovação dos agentes, porque a validação técnica não aconteceu antes da apresentação.

## Aprendizado

- **A validação técnica precisa acontecer antes da apresentação ao cliente.** Quando o alinhamento técnico não acontece, o PO escala.
- Distinguir o que a IA resolve do que um ajuste de processo resolve mais barato, e quantificar a dor em horas para sustentar a recomendação.
