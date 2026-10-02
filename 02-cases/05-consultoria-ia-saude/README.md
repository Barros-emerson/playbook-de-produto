# Case 05: Consultoria de IA em uma clínica de saúde

**Setor:** saúde | **Papel:** Product Owner da consultoria, de ponta a ponta | **Período:** jul. a set. de 2026 | **Status:** desenvolvimento iniciado; não está em produção

> **Resumo.** Uma clínica de reabilitação, com um programa de mentoria, queria IA para resolver um problema que parecia operacional. O discovery mostrou que a dor central era captação de pacientes. Conduzi a consultoria das entrevistas ao termo de aceite: 9 fluxos de processo mapeados, triagem de oportunidades, 4 agentes de IA aprovados pela decisora, PRD, especificação funcional e 25 histórias.

## Contexto

Clínica de reabilitação com capacidade ociosa. A cliente queria substituir uma agência de marketing com desempenho abaixo do esperado.

## Problema

O discovery deslocou o problema: **a dor central não era operação, e sim captação.** Quatro fricções foram registradas:

1. follow-up manual, que esquecia leads;
2. prospecção manual em cerca de 300 grupos de WhatsApp;
3. marketing sem medição de retorno;
4. base histórica de pacientes subutilizada.

## Responsabilidades

### Minha responsabilidade

| Atividade | Status |
|---|---|
| Product Owner da consultoria de ponta a ponta, por atribuição do gestor | Comprovado |
| Entrevistas do diagnóstico | Comprovado |
| Mapeamento de 9 fluxos de processo | Comprovado |
| Triagem e priorização das oportunidades | Comprovado |
| Apresentação das propostas à decisora | Comprovado |
| PRD e especificação funcional (EFS) | Comprovado |
| Termo de aceite formal | Comprovado |
| Board com 4 épicos e 25 histórias | Comprovado |
| Revisão do PRD com os devs e a liderança técnica | Comprovado |

### Responsabilidade de outras partes

| Parte | Papel documentado |
|---|---|
| Time de desenvolvimento (dois devs) e liderança técnica | Revisão conjunta do PRD; desenvolvimento iniciado em 21/09. Desenho da arquitetura híbrida alinhada na revisão: **[A VALIDAR]** quem definiu e em que consiste |
| Customer Success | Acompanhamento do cliente |
| Cliente | Decisora única; configuração de contas e acessos (WhatsApp, Twilio, agenda e sistema da clínica) |

## Discovery

- Entrevistas operacionais com as áreas comercial, financeira e de mídia social da clínica.
- 9 fluxos de processo mapeados.
- Artefatos: fricções e oportunidades, inventário de processos, sistemas e lacunas.
- Foi o primeiro projeto a rodar o novo processo de triagem da consultoria.

## Insights

- A dor central era captação, não operação: a clínica tinha capacidade ociosa.
- **[INFERÊNCIA BASEADA EM EVIDÊNCIAS]** As quatro fricções têm em comum o funil comercial, e não o atendimento clínico.

## Decisão

**Triagem em duas camadas** (funil de perguntas e ICE): 4 agentes priorizados e aprovados pela decisora em 24/08.

**Ordem de implementação:**

1. follow-up comercial;
2. prospecção da mentoria;
3. inteligência comercial;
4. reativação da base.

A cliente via a prospecção da mentoria como prioridade própria. Colocar o follow-up à frente foi escolha minha. A justificativa não está documentada.

**[INFERÊNCIA BASEADA EM EVIDÊNCIAS]** O follow-up atua sobre leads que já existem e depende de menos integrações do que a prospecção em grupos.

## Requisitos

- PRD do primeiro agente (follow-up) e especificação funcional oficial.
- Termo de aceite formal (documentos de 04/09 e 08/09).
- Board com 4 épicos (um por agente) e 25 histórias.
- O produto utiliza WhatsApp (Z-API e Twilio), agenda e o CRM citado nas histórias. Atuei na especificação, não na implementação.

## MVP

O primeiro agente, de follow-up comercial, é a primeira entrega. **[INFERÊNCIA BASEADA EM EVIDÊNCIAS]** Atua sobre leads que já existem, o ponto do funil mais próximo da receita. Tratamento formal como MVP: **[A VALIDAR]**.

## Riscos e dependências

| Risco ou dependência | Tratamento | Resultado |
|---|---|---|
| Configuração de contas e acessos do lado da cliente | Passo a passo de criação de contas e acessos | Entregue como próximo passo formal |
| Projeto bloqueado aguardando aprovação do PRD e acesso de desenvolvimento | Termo de aceite formal | Documentos gerados em 04/09 e 08/09 |
| Time confuso sobre o plano de WhatsApp, com risco de retrabalho | Revisão do PRD com devs e liderança técnica | 4 épicos e arquitetura híbrida alinhados em 15/09 |

## Validação

- 4 agentes aprovados pela decisora.
- Escopo formalizado em especificação funcional e termo de aceite.

## Resultado

| Resultado | Status |
|---|---|
| 4 agentes de IA aprovados pela decisora | Comprovado |
| 25 histórias escritas | Comprovado |
| Desenvolvimento iniciado em 21/09 | Comprovado |
| Resultado de negócio (pacientes captados, conversão) | **[EVIDÊNCIA INSUFICIENTE]**: o projeto ainda não entrou em produção |

## O que não deu certo

- A passagem para o desenvolvimento gerou dúvida sobre o plano de WhatsApp.
- O Épico 1 foi adiado para a Sprint 3, atrasando os épicos dependentes.

## Aprendizado

- **PRD congelado não substitui a leitura conjunta com o time antes da primeira sprint.**
- Uma consultoria completa, da entrevista ao termo de aceite, converte fricções operacionais em agentes priorizados por critérios explícitos.
