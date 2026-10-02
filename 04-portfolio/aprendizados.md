# Aprendizados

Experiências reais transformadas em regra de trabalho. Cada ciclo indica o que é comprovado e o que é inferência.

```
PROBLEMA  →  CAUSA  →  DECISÃO  →  NOVA REGRA  →  APLICAÇÃO FUTURA
```

## 1. Critério de aceite vago

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | PRDs reabertos e cards devolvidos; histórias aprovadas no QA funcional falhando na auditoria | Comprovado |
| Causa | Critérios de aceite que permitiam interpretação, como "responder bem o cliente" | Comprovado |
| Decisão | Começar pela regra mais objetiva e de efeito mais rápido | Comprovado |
| Nova regra | Toda história tem critério de aceite testável; se o enunciado não fecha, a demanda não avança | Comprovado (regra de minha autoria) |
| Aplicação futura | [Critérios de aceite](../01-metodo/criterios-de-aceite.md) e [template](../03-templates/criterios-de-aceite.md). Conferência da aplicação nas histórias posteriores: **[A VALIDAR]** | |

## 2. Escopo vendido que não chega ao Produto

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | Cliente esperava um agente adaptativo, como na demonstração comercial; o entregue era um roteiro mais rígido ([case 04](../02-cases/04-agente-de-voz-call-center/)) | Comprovado |
| Causa | Desalinhamento entre o que foi vendido e o que foi especificado e entregue | Comprovado |
| Decisão | Criar portões de passagem com checklist | Comprovado |
| Nova regra | Portão de Entrada: o Produto recebe do comercial o escopo vendido completo | Comprovado (plano de minha autoria) |
| Aplicação futura | [Método](../01-metodo/README.md) e [checklist de handoff](../03-templates/handoff-produto-dev.md) | |

A ligação direta entre o case 04 e a criação do portão de Entrada é **[INFERÊNCIA BASEADA EM EVIDÊNCIAS]**: o portão responde exatamente a essa falha, mas o plano não cita o case.

## 3. Teste que não reproduz o ambiente real

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | Quedas de chamada em produção depois de um teste de 40 mil chamadas simuladas ([case 04](../02-cases/04-agente-de-voz-call-center/)) | Comprovado |
| Causa | Teste só de volume, sem o ambiente de produção do cliente | Comprovado |
| Nova regra | Teste no ambiente do cliente, além do simulado, na Definition of Done | **[INFERÊNCIA BASEADA EM EVIDÊNCIAS]**: incorporada a este playbook; adoção formal pela equipe não documentada |

## 4. PRD congelado sem leitura com o time

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | Dúvida do time sobre o plano de WhatsApp e atraso de uma sprint ([case 05](../02-cases/05-consultoria-ia-saude/)) | Comprovado |
| Causa | O repasse ao desenvolvimento não incluiu leitura conjunta do PRD | Comprovado (aprendizado registrado) |
| Decisão | Revisão do PRD com devs e liderança técnica | Comprovado |
| Nova regra | Sessão de leitura conjunta antes da primeira sprint | Incorporada ao [checklist de handoff](../03-templates/handoff-produto-dev.md) |

## 5. Validação técnica depois da apresentação

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | Inviabilidade de integração descoberta depois da aprovação dos agentes ([case 06](../02-cases/06-discovery-planos-assistenciais/)) | Comprovado |
| Causa | A validação técnica não aconteceu antes da apresentação | Comprovado (aprendizado registrado) |
| Nova regra | Validação técnica antes da apresentação; escalar quando o alinhamento técnico não acontece | Incorporada ao [checklist de handoff](../03-templates/handoff-produto-dev.md) |

## 6. Mudança de sistema pelo cliente no meio do projeto

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | Troca de CRM tornou parte do trabalho obsoleta e pausou o projeto ([case 03](../02-cases/03-gestao-de-escopo-imobiliario/)) | Comprovado |
| Nova regra | Migração de sistema do cliente exige tratamento formal como mudança de escopo | Comprovado, como **política da empresa**, criada a partir de casos como este; não é regra de minha autoria |

## 7. Meta sem linha de base

| Etapa | Conteúdo | Status |
|---|---|---|
| Problema | Plano de redução de retrabalho com meta definida | Comprovado |
| Causa | A linha de base do retrabalho nunca foi medida | Comprovado |
| Aprendizado | Meta sem linha de base medida não se sustenta como resultado | Comprovado (aprendizado registrado) |

## Outros aprendizados documentados

- **MVP precisa ser defensável diante de restrições reais**, com o trade-off escrito ([case 01](../02-cases/01-automacao-contabil-whatsapp/)).
- **Corrigir a fonte da verdade vem antes de nova funcionalidade** ([case 02](../02-cases/02-assistente-juridico-rag/)).
- **Mudança de custo da plataforma é decisão de produto**, tomada com números ([case 03](../02-cases/03-gestao-de-escopo-imobiliario/)).
- **Discovery pode redefinir o problema**: a dor de operação era, na verdade, de captação ([case 05](../02-cases/05-consultoria-ia-saude/)).
- **Nem toda dor precisa de IA** ([case 06](../02-cases/06-discovery-planos-assistenciais/)).
