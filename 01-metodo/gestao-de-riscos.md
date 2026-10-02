# Gestão de riscos

Os riscos abaixo não são uma lista teórica. Cada um apareceu em projeto real e virou regra de trabalho.

## Riscos recorrentes em produtos de IA sob medida

| Risco | Como apareceu | Mitigação que adoto |
|---|---|---|
| **Expectativa formada na venda diferente do especificado** | O cliente esperava um agente adaptativo, como na demonstração comercial; o especificado era um roteiro mais rígido | Capturar a promessa comercial no portão de Entrada e escrevê-la no PRD |
| **Teste que não reproduz o ambiente real** | Teste de volume com 40 mil chamadas simuladas, sem o ambiente de produção do cliente | Teste de carga não substitui teste no ambiente do cliente; o roteiro de testes exige os dois |
| **Limite técnico de sistema de terceiro** | Latência de cerca de 6 s para responder, contra limite de 3 s da discadora, causando quedas | Levantar limites dos sistemas do cliente no discovery e transformar em critério de aceite |
| **Integração que o sistema do cliente não suporta** | A discadora recebia só o áudio e não processava dados de volta | Validar a viabilidade da integração antes de prometer a funcionalidade; ter plano alternativo |
| **Mudança de custo da plataforma** | A Meta anunciou cobrança por todas as mensagens enviadas no WhatsApp, ameaçando a prospecção ativa | Simulador de custo e decisão do cliente com números, antes de construir |
| **Atalho técnico com risco operacional** | API não oficial de WhatsApp como forma de fugir do custo | Não recomendar: risco de banimento do número |
| **Mudança de sistema pelo cliente durante o projeto** | Troca de CRM no meio do projeto tornou parte do trabalho obsoleta | Tratar mudança de sistema como mudança formal de escopo |
| **Documentação desatualizada** | Arquitetura documentada com 14 agentes; 5 em produção | Corrigir a fonte da verdade antes de qualquer nova funcionalidade ou conversa comercial |
| **Resposta de IA fora da base de conhecimento** | Assistentes com base documental podem responder além do que a base sustenta | Especificar o comportamento: sinalizar quando a resposta não vem da base |
| **Handoff incompleto** | Repasse ao desenvolvimento sem tokens e acessos | DoR exige acessos e credenciais de teste antes de a história entrar na sprint |

## Registro de riscos

Todo PRD tem uma tabela de riscos e premissas com impacto e mitigação. Risco sem dono e sem ação é só preocupação.

| Risco ou premissa | Impacto | Probabilidade | Mitigação | Responsável |
|---|---|---|---|---|
| [Descrição] | Alto / Médio / Baixo | Alta / Média / Baixa | [Ação] | [Quem] |
