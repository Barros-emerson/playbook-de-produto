# Prompt engineering

> **Situação da evidência.** Não há registro documental de "prompt engineering" como atividade profissional com esse nome. **[A VALIDAR]**.
>
> O que está documentado é a **especificação de comportamento de agentes baseados em LLM**: o que o agente faz, o que não faz, como encerra, quando passa para humano e como responde a objeções. Esta página mapeia essas evidências contra os elementos de um prompt, sem afirmar mais do que isso.

## Elementos de um prompt x evidências

| Elemento | Evidência | Status |
|---|---|---|
| Contexto e objetivo do agente | Script de SDR do cliente, focado em qualificação, adotado como base do agente de pré-venda ([case 03](../02-cases/03-gestao-de-escopo-imobiliario/)) | Comprovado |
| Instruções de comportamento | Encerramento proativo da chamada pela IA ([case 04](../02-cases/04-agente-de-voz-call-center/)) | Comprovado |
| Restrições e guardrails | Sinalizar respostas fora da base de conhecimento, em um assistente com base documental | Registrado; detalhes **[A VALIDAR]** |
| Tratamento de exceção | Passagem para humano: finalização da abertura de CNPJ ([case 01](../02-cases/01-automacao-contabil-whatsapp/)) e escalonamento no call center ([case 04](../02-cases/04-agente-de-voz-call-center/)) | Comprovado |
| Variação de resposta | Diversificação de frases em objeções, depois de identificar frases repetitivas ([case 04](../02-cases/04-agente-de-voz-call-center/)) | Comprovado |
| Validação e iteração | Escuta das gravações completas do lote de teste, seguida de novas histórias de correção ([case 04](../02-cases/04-agente-de-voz-call-center/)) | Comprovado |
| Formato de saída | | **[A VALIDAR]** |
| Tratamento de ambiguidade | | **[A VALIDAR]** |
| Critérios de qualidade de resposta | | **[A VALIDAR]** |

## LLMs aplicados ao próprio trabalho de Produto

**[INFERÊNCIA BASEADA EM EVIDÊNCIAS]** Os registros mostram um framework de PRD apoiado em "skills" de LLM, com retorno positivo de clareza dado por um desenvolvedor e por um cliente, registrado pelo gestor em 16/07. A autoria do framework é atribuída a mim por inferência e precisa ser confirmada.

## Posicionamento

Quando a evidência for confirmada: **prompt engineering aplicado à estruturação e evolução de produtos baseados em LLMs**. Não é engenharia de software.
