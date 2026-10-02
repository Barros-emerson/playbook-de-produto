# Priorização

Quando há mais oportunidades do que capacidade, priorizo em duas camadas.

**Autoria:** o funil de triagem é o processo de consultoria da empresa em que atuei. Apliquei esse funil nas consultorias dos [cases 05](../02-cases/05-consultoria-ia-saude/) e [06](../02-cases/06-discovery-planos-assistenciais/).

> **[CONFLITO ENTRE FONTES: VALIDAR]** A versão anterior deste playbook descreve o filtro com 3 perguntas. Os registros das consultorias descrevem um funil de 5 perguntas, com "existem dados?" como critério eliminatório. As 3 perguntas abaixo precisam ser conferidas contra o funil de 5.

## Camada 1: filtro eliminatório

Antes de pontuar qualquer coisa, a oportunidade precisa passar por três perguntas. Um "não" elimina.

1. **Resolve uma dor que o cliente confirmou?** Hipótese nossa não conta.
2. **Existem dados para sustentar a solução?** Sem dado, agente de IA vira adivinhação.
3. **Existe um responsável do lado do cliente?** Sem dono, a entrega morre no aceite.

## Camada 2: ICE Score

As oportunidades que passaram no filtro recebem nota de 1 a 10 em:

| Critério | Pergunta |
|---|---|
| **Impacto** | Quanto isso move a métrica que o cliente definiu como sucesso? |
| **Confiança** | Quão sólida é a evidência de que vai funcionar? |
| **Facilidade** | Quão simples é entregar? (nota alta = menor esforço) |

**ICE = Impacto x Confiança x Facilidade**

Na prática, o esforço entra invertido: quanto menor o esforço, maior a nota de facilidade.

## Regras de uso

- A nota é ponto de partida para a conversa com o cliente, não veredito.
- Empate se resolve por dependência técnica: o que destrava outras entregas vem primeiro.
- Reavaliar a cada ciclo. Confiança muda conforme a evidência aparece.

## Priorização durante o projeto

Com o projeto em andamento, a pergunta muda de "o que construir" para "o que manter". Quatro critérios orientam a decisão:

| Critério | Pergunta |
|---|---|
| **Valor** | A entrega move a métrica que justificou o projeto? |
| **Esforço** | Quanto custa terminar, considerando o que já foi investido? |
| **Risco** | O que pode impedir a entrega: limite técnico, dependência externa, custo de operação? |
| **Impacto no prazo** | Manter essa entrega compromete a previsibilidade do restante? |

Aplicação real: [case 03, gestão de escopo no setor imobiliário](../02-cases/03-gestao-de-escopo-imobiliario/).

Template: [03-templates/priorizacao.md](../03-templates/priorizacao.md).
