# Tomada de decisão

Como decido escopo, prioridade e solução, e como uma falha vira regra de processo.

## Critérios que uso

| Critério | Pergunta | Onde aparece |
|---|---|---|
| **Valor** | A entrega move a métrica que justificou o projeto? | [Case 03](../02-cases/03-gestao-de-escopo-imobiliario/) |
| **Esforço** | Quanto custa terminar, considerando o prazo? | [Case 03](../02-cases/03-gestao-de-escopo-imobiliario/), [case 01](../02-cases/01-automacao-contabil-whatsapp/) |
| **Risco** | Limite técnico, dependência externa, risco operacional ou de custo? | [Case 03](../02-cases/03-gestao-de-escopo-imobiliario/), [case 06](../02-cases/06-discovery-planos-assistenciais/) |
| **Viabilidade técnica** | O sistema do cliente ou de terceiro suporta o desenho? | [Case 04](../02-cases/04-agente-de-voz-call-center/), [case 06](../02-cases/06-discovery-planos-assistenciais/) |
| **Necessidade de IA** | Um ajuste de processo resolve mais barato? | [Case 06](../02-cases/06-discovery-planos-assistenciais/) |

Não uso pesos numéricos nessas decisões. A pontuação numérica (ICE) entra na priorização de oportunidades novas: ver [priorização](priorizacao.md).

## Decisões documentadas

| Situação | Decisão | Critério determinante | Case |
|---|---|---|---|
| Épico inviável no cronograma | Cancelar e reinvestir nos épicos que já geravam valor | Esforço sem entrega no prazo | [03](../02-cases/03-gestao-de-escopo-imobiliario/) |
| Aumento de custo por mensagem no WhatsApp | Não recomendar API não oficial | Risco de banimento do número | [03](../02-cases/03-gestao-de-escopo-imobiliario/) |
| Discadora não processava dados de volta | Relatório de tabulação no ambiente próprio da solução | Viabilidade técnica | [04](../02-cases/04-agente-de-voz-call-center/) |
| Escopo completo de 6 a 12 meses | Propor MVP focado em MEI | Esforço e prazo frente ao investimento | [01](../02-cases/01-automacao-contabil-whatsapp/) |
| Negócio não fechou | Converter o PRD em versão genérica reaproveitável | Valor do trabalho já feito | [01](../02-cases/01-automacao-contabil-whatsapp/) |
| Documentação com 14 agentes; 5 em produção | Corrigir a fonte da verdade antes de qualquer funcionalidade | Documento desatualizado distorce a conversa comercial | [02](../02-cases/02-assistente-juridico-rag/) |
| Validação documental | Cruzamento de dados (OCR), e não IA lendo imagens | [A VALIDAR: justificativa não documentada] | [06](../02-cases/06-discovery-planos-assistenciais/) |
| Dores com solução simples | Propor melhorias sem IA junto com os agentes | Necessidade de IA | [06](../02-cases/06-discovery-planos-assistenciais/) |

## De falha a regra

```
PROBLEMA  →  CAUSA  →  DECISÃO  →  NOVA REGRA  →  APLICAÇÃO FUTURA
```

Os ciclos completos, com a indicação do que é comprovado e do que é inferência, estão em [aprendizados](../04-portfolio/aprendizados.md).
