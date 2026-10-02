# Case 01: Automação contábil via WhatsApp

**Setor:** contábil | **Papel:** Product Owner | **Período:** jul. a ago. de 2026 | **Status:** PRD completo; produto não implantado com o cliente original

> **Resumo.** Um escritório contábil queria uma IA que atendesse as empresas clientes pelo WhatsApp, coletasse documentos e executasse rotinas contábeis. Estruturei o produto em um PRD que evoluiu de 13 para 16 épicos, com 743 horas estimadas para os épicos 1 a 13. Diante de um escopo completo de 6 a 12 meses, propus um MVP focado em MEI. A contratação pelo cliente original não se concretizou, e converti o PRD em uma versão genérica, reaproveitada em uma nova oportunidade comercial.

## 1. Contexto

Escritório de contabilidade que queria usar IA para atender as empresas clientes pelo WhatsApp, coletar documentos e executar rotinas contábeis.

## 2. Problema

Necessidade apresentada pelo cliente: uma IA que atendesse empresas pelo WhatsApp, coletasse documentos e executasse estas rotinas:

- apuração fiscal;
- folha de pagamento;
- admissão e rescisão;
- notas fiscais;
- declarações;
- abertura de CNPJ, com finalização humana.

Quantificação da dor (horas gastas, volume de atendimentos, custo atual): **[EVIDÊNCIA INSUFICIENTE]**.

## 3. Meu papel

### Minha responsabilidade

| Atividade | Status |
|---|---|
| PRD completo, com épicos e histórias | Comprovado |
| Protótipo do painel de atendimento (Épico 12) | Comprovado |
| Proposta de MVP | Comprovado |
| Estimativas de prazo e custo | Comprovado |
| Roadmap por marcos | Comprovado |
| Conversão do PRD em versão genérica | Comprovado |

### Responsabilidade de outras áreas

| Área | Papel documentado |
|---|---|
| Liderança técnica | Integrante do time do projeto. Atividades específicas: **[A VALIDAR]** |
| Outro Product Owner | Revisão do PRD |
| Comercial | Relação comercial com o cliente; apontou que os primeiros documentos estavam fora do padrão institucional |
| Desenvolvimento | Não houve desenvolvimento: o produto não foi contratado |

## 4. Stakeholders

| Stakeholder | Papel |
|---|---|
| Contador do escritório | Conhecimento das rotinas contábeis |
| Representantes do escritório | Decisão sobre escopo e investimento |
| Prospect posterior, de maior porte | Destinatário do roadmap da versão genérica |

## 5. Discovery

- Levantamento do escopo com o contador e com os representantes do escritório.
- O escopo foi registrado como aprovado em reunião diária de 15/07. Quem aprovou: **[A VALIDAR]**.
- Apresentação da primeira versão (13 épicos e 43 histórias) e da proposta de MVP em reunião com o cliente, em 28/07.
- Duas tensões surgiram nessa reunião: o prazo do escopo completo era alto para o investimento do cliente, e o cliente questionou se um MVP reduziria de fato o esforço, já que as integrações centrais continuariam necessárias.

## 6. DDE

Documento de discovery (DDE) específico deste projeto: **[EVIDÊNCIA INSUFICIENTE]**. O registro do discovery está no próprio PRD e nas reuniões com o cliente.

## 7. Escopo

| Necessidade | Origem |
|---|---|
| Atender as empresas clientes no WhatsApp | Pedido do cliente |
| Coletar documentos pelo canal | Pedido do cliente |
| Executar as rotinas contábeis listadas no problema | Pedido do cliente |
| Finalização humana na abertura de CNPJ | Escopo documentado |
| Painel de atendimento para a equipe do escritório | Escopo documentado (Épico 12) |
| Conciliação bancária via Open Finance | Incluída no roadmap para o prospect posterior |

## 8. MVP

**Decisão:** propor um MVP focado em MEI em vez de defender o escopo integral.

**Racional documentado:** o MEI combina público amplo, tributação fixa e no máximo um funcionário.

**Trade-off:** o cliente apontou que as integrações centrais continuariam necessárias no MVP. O recorte reduz regras e rotinas, mas não elimina as dependências mais pesadas.

## 9. Arquitetura conceitual

Diagrama, explicação de entrada, processamento, integrações, regras e saída, e pontos de falha: [arquitetura-conceitual.md](arquitetura-conceitual.md).

## 10. Integrações

Sistemas previstos no PRD. Atuei na especificação do produto integrado a eles; a implementação não chegou a acontecer.

| Sistema | Papel no produto |
|---|---|
| WhatsApp (Meta) e Twilio | Canal de conversa com a empresa cliente |
| SERPRO Integra Contador | Serviços fiscais federais |
| BrasilAPI | Dados públicos |
| Infosimples | Consultas a fontes públicas |
| Pluggy | Open Finance, para conciliação bancária |
| Alterdata | Sistema contábil |
| eSocial e FGTS | Obrigações trabalhistas |
| Google Drive | Armazenamento de documentos |

Contratos de API, autenticação e volumes: **[EVIDÊNCIA INSUFICIENTE]**.

## 11. Épicos

| Versão do PRD | Estrutura |
|---|---|
| v0.8 | 13 épicos, 43 histórias |
| PRD completo | 16 épicos |
| PRD Genérico v1.0, v1.1 e v1.2 (14 a 18/08) | Versão reaproveitável como SaaS |

Épico documentado neste portfólio: **Épico 12, painel de atendimento**, com protótipo. Lista completa dos épicos: **[EVIDÊNCIA INSUFICIENTE neste portfólio]**.

## 12. Requisitos

Regras de negócio documentadas:

- **Perfil do MVP:** MEI, com tributação fixa e no máximo um funcionário.
- **Abertura de CNPJ:** a etapa final é sempre humana.

As histórias originais pertencem ao PRD do cliente. Exemplo no formato que uso, aplicado a uma regra documentada:

**[ILUSTRATIVO]** US-XX: Encaminhar abertura de CNPJ para finalização humana

**Como** contador do escritório,
**quero** receber no painel os pedidos de abertura de CNPJ com os documentos já coletados,
**para** finalizar a abertura sem pedir os documentos de novo à empresa.

## 13. Critérios de aceite

**[ILUSTRATIVO]** para a história acima:

| # | Critério |
|---|---|
| CA-01 | Quando a empresa conclui o envio dos documentos de abertura de CNPJ, o pedido aparece no painel com status "Aguardando finalização humana". |
| CA-02 | O pedido no painel exibe todos os documentos recebidos, cada um com link de abertura. |
| CA-03 | **Dado** um pedido de abertura de CNPJ, **quando** o agente responde à empresa, **então** a mensagem informa que a finalização será feita por um contador. |

## 14. Estimativas

| Item | Valor |
|---|---|
| Horas estimadas para os épicos 1 a 13 | 743 h |
| Prazo do escopo completo | 6 a 12 meses |
| Estimativa dos épicos 14 a 16 | **[EVIDÊNCIA INSUFICIENTE]** |

## 15. Roadmap

Roadmap precificado em **4 marcos**, de 18/08, montado para o prospect posterior, que tinha prazo curto. Incluiu a conciliação bancária via Open Finance. Critérios de ordenação dos marcos: **[EVIDÊNCIA INSUFICIENTE]**.

## 16. Riscos

| Risco | Origem |
|---|---|
| Prazo do escopo completo alto para o investimento do cliente | Documentado na reunião com o cliente |
| MVP ainda dependente das integrações centrais | Levantado pelo cliente |
| Alta complexidade regulatória das rotinas fiscais e trabalhistas | Documentado |

## 17. Dependências

- Acesso às APIs listadas em [Integrações](#10-integrações). Requisitos de autorização de cada uma: **[A VALIDAR]**.
- Conta do WhatsApp Business.
- Acesso ao sistema contábil do escritório.

## 18. Decisões

| Decisão | Por quê |
|---|---|
| Propor o MVP de MEI em vez de defender o escopo integral | Prazo e investimento do escopo completo |
| Converter o trabalho em ativo reutilizável quando a venda não fechou | Aproveitar o PRD em novas oportunidades |
| Incluir conciliação bancária via Open Finance no roadmap do prospect | Demanda do prospect. Detalhamento: **[A VALIDAR]** |

## 19. Resultado

**Resultado documentado:** PRD evoluído de 13 para 16 épicos, com 743 horas estimadas para os épicos 1 a 13; PRD convertido em versão genérica (v1.0 a v1.2); roadmap em 4 marcos usado em uma nova oportunidade comercial.

**Resultado pós-implantação:** não existe; o produto não foi implantado. Receita gerada pela versão genérica: **[EVIDÊNCIA INSUFICIENTE]**.

## 20. O que não deu certo

- A contratação pelo cliente original não se concretizou.
- Os primeiros documentos saíram fora do padrão institucional da empresa e foram refeitos depois do apontamento do comercial.

## 21. O que eu faria diferente hoje

Com base no que está documentado:

- **Seguir o padrão institucional desde o primeiro documento.**

Reflexões ainda não registradas em nenhum documento, para revisão do autor:

- **[A VALIDAR]** Apresentar o recorte de MVP antes de detalhar o escopo completo, para testar mais cedo a disposição de investimento do cliente.

## 22. Aprendizados

- Dimensionar um produto de alta complexidade regulatória e recortar um MVP defensável, com o trade-off escrito.
- Transformar um negócio perdido em ativo reaproveitável.

## Matriz de evidências

| Afirmação | Status |
|---|---|
| 16 épicos e 743 h para os épicos 1 a 13 | Comprovado |
| Evolução de 13 épicos e 43 histórias para 16 épicos | Comprovado (versões diferentes do PRD) |
| MVP focado em MEI proposto em 28/07 | Comprovado |
| PRD genérico v1.0 a v1.2 e roadmap em 4 marcos | Comprovado |
| Integrações previstas no PRD | Comprovado |
| Exemplo de user story e critérios de aceite | Ilustrativo |
| Quem aprovou o escopo em 15/07 | A validar |
| Receita da versão genérica | Evidência insuficiente |
