# IA e LLMs

O que fiz com IA generativa como Product Owner: especificar, decidir, testar e validar produtos baseados em LLMs. A implementação foi do time técnico.

## Tipos de produto de IA que gerenciei

| Tipo | O que o produto faz | Onde aparece |
|---|---|---|
| Agente de voz | Atende o lead por telefone, qualifica e tabula antes do atendimento humano | [Case 04](../02-cases/04-agente-de-voz-call-center/) |
| Agente de pré-venda em dois canais | Prospecção e reativação por WhatsApp e voz, com canal escolhido lead a lead | [Case 03](../02-cases/03-gestao-de-escopo-imobiliario/) |
| Assistente com RAG | Responde com base em uma base de conhecimento, dividido em agentes por área | [Case 02](../02-cases/02-assistente-juridico-rag/) |
| Agente de atendimento e automação no WhatsApp | Previsto no PRD: atender, coletar documentos e disparar rotinas integradas a APIs (não implantado) | [Case 01](../02-cases/01-automacao-contabil-whatsapp/) |
| Agentes comerciais definidos em consultoria | Follow-up, prospecção, inteligência comercial, reativação, validação documental, retenção, cross-sell | [Cases 05](../02-cases/05-consultoria-ia-saude/) e [06](../02-cases/06-discovery-planos-assistenciais/) |

## O que especifiquei em produtos com LLM

| Elemento | Exemplo documentado | Status |
|---|---|---|
| Comportamento do agente em conversa | Encerramento proativo da chamada; diversificação de frases em objeções | Comprovado ([case 04](../02-cases/04-agente-de-voz-call-center/)) |
| Script e objetivo do agente | Substituição do script pelo script de SDR do próprio cliente, focado em qualificação | Comprovado ([case 03](../02-cases/03-gestao-de-escopo-imobiliario/)) |
| Passagem para humano (handoff) | Finalização humana na abertura de CNPJ; escalonamento para atendente no call center | Comprovado (cases [01](../02-cases/01-automacao-contabil-whatsapp/) e [04](../02-cases/04-agente-de-voz-call-center/)) |
| Limite do que o agente responde | Sinalizar respostas fora da base de conhecimento, decisão registrada em um assistente com base documental | Registrado; projeto com evidência parcial, detalhes **[A VALIDAR]** |
| Limites técnicos | Latência máxima aceita pela discadora | Comprovado ([case 04](../02-cases/04-agente-de-voz-call-center/)) |
| Escopo real do produto de IA | Revisão de 14 agentes documentados para 5 em produção | Comprovado ([case 02](../02-cases/02-assistente-juridico-rag/)) |
| Custo de operação | Modelo de repasse da infraestrutura como mensalidade; impacto do custo por mensagem no WhatsApp | Comprovado (cases [02](../02-cases/02-assistente-juridico-rag/) e [03](../02-cases/03-gestao-de-escopo-imobiliario/)) |

## Decisões de produto sobre o uso de IA

- **Nem toda dor precisa de IA.** Melhorias de processo sem IA foram propostas junto com os agentes ([case 06](../02-cases/06-discovery-planos-assistenciais/)).
- **Nem toda tarefa de IA precisa de LLM.** Validação documental por cruzamento de dados (OCR), e não por IA lendo imagens ([case 06](../02-cases/06-discovery-planos-assistenciais/)).
- **Agente próprio em vez de chatbot genérico** no atendimento ([case 06](../02-cases/06-discovery-planos-assistenciais/)).

## O que não afirmo

Escolha de modelos, fine-tuning, embeddings, banco vetorial, avaliação automatizada de modelos e infraestrutura de LLM não estão documentados como atividade minha: **[EVIDÊNCIA INSUFICIENTE]**.

Ver também: [prompt engineering](prompt-engineering.md) e [arquitetura conceitual](arquitetura-conceitual.md).
