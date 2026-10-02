# Case 01: Automação contábil via WhatsApp

**Setor:** contábil | **Papel:** Product Owner | **Período:** jul. a ago. de 2026 | **Status:** PRD completo; produto não implantado com o cliente original

> **Resumo.** Um escritório contábil queria uma IA que atendesse as empresas clientes pelo WhatsApp, coletasse documentos e executasse rotinas contábeis. Estruturei o produto em um PRD de 16 épicos, com 743 horas estimadas para os épicos 1 a 13 e integrações com APIs governamentais, de dados públicos, de Open Finance e com o sistema contábil. Diante de um escopo completo de 6 a 12 meses, propus um MVP focado em MEI. A contratação pelo cliente original não se concretizou, e o PRD foi convertido em uma versão genérica, reaproveitável como produto SaaS.

## 01. Contexto

Escritório de contabilidade que atende empresas e queria escalar o atendimento e a execução de rotinas com IA, usando o WhatsApp como canal com as empresas clientes.

**Meu papel:** PO do produto. Escrevi o PRD completo, elaborei o protótipo do painel de atendimento, propus o MVP, fiz as estimativas de prazo e custo e montei o roadmap por marcos.

## 02. Problema

Necessidade apresentada pelo cliente: uma IA que atendesse empresas pelo WhatsApp, coletasse documentos e executasse rotinas contábeis.

Rotinas no escopo:

- apuração fiscal;
- folha de pagamento;
- admissão e rescisão;
- notas fiscais;
- declarações;
- abertura de CNPJ, com finalização humana.

Quantificação da dor (horas gastas, volume de atendimentos, custo atual): **[NÃO DOCUMENTADO]**.

## 03. Discovery

- Levantamento do escopo com o contador e com os representantes do escritório.
- Apresentação da primeira versão do escopo (13 épicos e 43 histórias) e da proposta de MVP em reunião com o cliente.
- O discovery revelou duas tensões que orientaram as decisões seguintes: o prazo do escopo completo era alto para o investimento do cliente, e o cliente questionou se um MVP reduziria de fato o esforço, já que as integrações centrais continuariam necessárias.

Roteiro completo de entrevistas e participantes de cada sessão: **[NÃO DOCUMENTADO]**.

## 04. Necessidades identificadas

| Necessidade | Origem |
|---|---|
| Atender as empresas clientes no WhatsApp | Pedido do cliente |
| Coletar documentos das empresas pelo canal | Pedido do cliente |
| Executar as rotinas contábeis listadas no problema | Pedido do cliente |
| Manter um humano na finalização de etapas sensíveis, como a abertura de CNPJ | Escopo documentado |
| Painel de atendimento para a equipe do escritório acompanhar e intervir | Escopo documentado (Épico 12, com protótipo) |
| Conciliação bancária via Open Finance | Incluída no roadmap para um segundo prospect |

## 05. Objetivo do produto

Automatizar, pelo WhatsApp, o ciclo de atendimento, coleta de documentos e execução de rotinas contábeis, com intervenção humana nas etapas que exigem responsabilidade profissional.

Métrica de sucesso acordada com o cliente: **[NÃO DOCUMENTADO]**.

## 06. Perfis envolvidos

| Perfil | Papel no produto |
|---|---|
| Empresa cliente do escritório | Usuária final: conversa com o agente no WhatsApp e envia documentos |
| Equipe contábil do escritório | Acompanha atendimentos no painel, valida e finaliza etapas sensíveis |
| Representantes do escritório | Decisores sobre escopo, investimento e prioridade |

## 07. Jornada

Jornada conceitual, reconstruída a partir do escopo do PRD:

1. A empresa cliente inicia a conversa no WhatsApp.
2. O agente identifica a empresa e a solicitação.
3. O agente coleta os documentos necessários.
4. A camada de automação consulta ou envia dados às integrações.
5. As regras de negócio definem se a rotina segue automática ou vai para validação humana.
6. A equipe contábil acompanha e, quando necessário, finaliza pelo painel.
7. A empresa recebe o retorno no WhatsApp.

## 08. Solução proposta

- **Agente de IA no WhatsApp** como interface única com a empresa cliente.
- **Camada de automação** que orquestra as rotinas e as integrações.
- **Integrações** com serviços governamentais, dados públicos, Open Finance e o sistema contábil do escritório.
- **Painel de atendimento** para a equipe contábil.

## 09. Arquitetura conceitual

Diagrama e explicação de entrada, processamento, integrações, regras, saída e pontos de falha: [arquitetura-conceitual.md](arquitetura-conceitual.md).

## 10. Integrações

| Integração | Papel no produto |
|---|---|
| WhatsApp (Meta), via Twilio | Canal de conversa com a empresa cliente |
| SERPRO Integra Contador | Serviços fiscais federais para rotinas contábeis |
| BrasilAPI | Consulta a dados públicos, como cadastro de empresas |
| Infosimples | Consultas a fontes públicas |
| Pluggy | Open Finance: dados bancários para conciliação |
| Alterdata | Sistema contábil do escritório |
| eSocial e FGTS | Obrigações trabalhistas ligadas a folha, admissão e rescisão |
| Google Drive | Armazenamento de documentos |

A coluna "papel no produto" descreve o uso pretendido no escopo. Contratos de API, autenticação e volumes: **[NÃO DOCUMENTADO neste portfólio]**.

## 11. Regras de negócio

Regras documentadas:

- **Perfil do MVP:** MEI, com tributação fixa e no máximo um funcionário.
- **Abertura de CNPJ:** a etapa final é sempre humana.

Demais regras do PRD (por rotina e por regime tributário): **[NÃO DOCUMENTADO neste portfólio]**.

## 12. Exceções e cenários de erro

Exceções especificadas no PRD original: **[NÃO DOCUMENTADO neste portfólio]**.

Cenários que a arquitetura obriga a cobrir, como análise de produto:

- API governamental indisponível ou lenta durante uma rotina.
- Documento enviado ilegível, incompleto ou do tipo errado.
- Empresa fora do perfil do MVP (não MEI): encaminhar para atendimento humano.
- Conversa retomada após a janela de 24 horas do WhatsApp, que exige mensagem de modelo aprovada pela Meta.
- Divergência entre dado consultado em fonte pública e dado informado pela empresa.

## 13. MVP

**Decisão:** propor um MVP focado em MEI em vez de defender o escopo integral.

**Por quê:** o MEI combina público amplo com tributação fixa e no máximo um funcionário. Menos variação de regra significa um fluxo completo entregável em menos tempo.

**Trade-off explícito:** o cliente apontou que as integrações centrais continuariam necessárias no MVP. O recorte reduz regras e rotinas, mas não elimina as dependências mais pesadas. Esse ponto ficou registrado como risco, não escondido.

## 14. Priorização

- Roadmap precificado em **4 marcos**, montado para um segundo prospect com prazo curto.
- Conciliação bancária via Open Finance incluída no roadmap desse prospect.

Critérios de ordenação dos marcos: **[NÃO DOCUMENTADO neste portfólio]**.

## 15. Épicos

| Versão do PRD | Estrutura |
|---|---|
| v0.8 | 13 épicos, 43 histórias |
| PRD completo | 16 épicos, com 743 h estimadas para os épicos 1 a 13 |
| PRD Genérico v1.0 a v1.2 | Versão reaproveitável como SaaS, sem dependência do cliente original |

Épico documentado neste portfólio: **Épico 12, painel de atendimento**, com protótipo.

Lista completa dos épicos: **[NÃO DOCUMENTADO neste portfólio]**.

## 16. User stories

As histórias originais pertencem ao PRD do cliente. O exemplo abaixo mostra o formato que uso, aplicado a uma regra documentada do escopo.

**[ILUSTRATIVO]** US-XX: Encaminhar abertura de CNPJ para finalização humana

**Como** contador do escritório,
**quero** receber no painel os pedidos de abertura de CNPJ com os documentos já coletados,
**para** finalizar a abertura sem precisar pedir os documentos de novo à empresa.

## 17. Critérios de aceite

**[ILUSTRATIVO]** para a história acima:

| # | Critério |
|---|---|
| CA-01 | Quando a empresa conclui o envio dos documentos de abertura de CNPJ, o pedido aparece no painel com status "Aguardando finalização humana". |
| CA-02 | O pedido no painel exibe todos os documentos recebidos, cada um com link de abertura. |
| CA-03 | **Dado** um pedido de abertura de CNPJ, **quando** o agente responde à empresa, **então** a mensagem informa que a finalização será feita por um contador. |

## 18. Riscos

| Risco | Origem |
|---|---|
| Prazo do escopo completo (6 a 12 meses) alto para o investimento do cliente | Documentado no discovery |
| MVP ainda depende das integrações centrais | Levantado pelo cliente |
| Alta complexidade regulatória das rotinas fiscais e trabalhistas | Documentado |
| Dependência de disponibilidade e regras de APIs de terceiros e do governo | Análise de produto |

## 19. Dependências

- Acesso às APIs listadas em [Integrações](#10-integrações), com as autorizações exigidas por cada uma. Requisitos específicos de autorização: **[A VALIDAR]**.
- Conta do WhatsApp Business e modelos de mensagem aprovados pela Meta.
- Acesso ao sistema contábil do escritório.

## 20. Estimativa

- **743 horas** estimadas para os épicos 1 a 13.
- Prazo do escopo completo: **6 a 12 meses**.
- Estimativa dos épicos 14 a 16: **[NÃO DOCUMENTADO]**.

## 21. Resultado

**Resultado documentado:** escopo estruturado em 16 épicos, com 743 horas estimadas para os épicos 1 a 13; PRD convertido em versão genérica (v1.0 a v1.2), reaproveitável como SaaS; roadmap em 4 marcos usado em uma nova oportunidade comercial.

**Resultado pós-implantação:** não existe. A contratação pelo cliente original não se concretizou, e o produto não foi implantado. Receita gerada pela versão genérica: **[NÃO DOCUMENTADO]**.

## 22. Aprendizados

- Dimensionar um produto de alta complexidade regulatória exige separar, desde o início, o que é regra fixa do que varia por perfil de empresa.
- Um MVP defensável é aquele cujo trade-off está escrito, inclusive o que ele não resolve.
- Trabalho de produto pode virar ativo: quando a venda não fecha, um PRD bem estruturado pode ser generalizado e reaproveitado.

## 23. O que eu faria diferente hoje

**[A VALIDAR pelo autor]** Pontos em revisão:

- Apresentar o recorte de MVP antes de detalhar o escopo completo, para testar a disposição de investimento do cliente mais cedo.
- Validar com o cliente, antes do PRD integral, o prazo e o investimento aceitáveis.
