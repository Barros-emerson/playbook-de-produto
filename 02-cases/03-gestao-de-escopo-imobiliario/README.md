# Case 03: Gestão de escopo no setor imobiliário

**Setor:** imobiliário | **Papel:** Product Owner | **Período:** jun. a set. de 2026 | **Status:** desenvolvimento pausado pelo cliente em set. de 2026

> **Resumo.** Uma imobiliária contratou uma suíte de agentes de IA comerciais: pré-venda (BDR), qualificação e reativação de leads, integrada ao CRM. Durante o projeto, um épico se mostrou inviável no cronograma, e a Meta anunciou cobrança por todas as mensagens enviadas no WhatsApp, o que ameaçava a viabilidade da prospecção ativa. Analisei impacto, esforço, risco e valor, renegociei o escopo e retirei do MVP a entrega de menor valor relativo, inviável no cronograma, para preservar a previsibilidade do restante.

Este case mostra o raciocínio de decisão. Não é uma história de sucesso: o projeto foi pausado pelo cliente depois de mudanças sucessivas de prioridade.

## Contexto

- Suíte de agentes de IA para pré-venda, qualificação e reativação de leads, integrada ao CRM da imobiliária.
- **Dor de origem:** segundo o levantamento do discovery, cerca de metade dos leads se perdia no WhatsApp pessoal dos corretores.
- **Ferramentas do projeto:** CRM da imobiliária, WhatsApp (Z-API), Twilio Voice e ElevenLabs.
- **Meu papel:** PO da suíte. PRD (até a v5), épicos, redesenho do BDR para dois canais, análise de impacto dos preços do WhatsApp, negociação de escopo com o cliente e testes de aceite.

## Problema

Três mudanças pressionaram o escopo ao mesmo tempo:

1. **Épico inviável no cronograma:** uma integração planejada não cabia no prazo, e uma parte do escopo dependia de julgamento humano.
2. **Mudança de custo da plataforma:** a Meta anunciou cobrança por todas as mensagens enviadas no WhatsApp, a partir de outubro. A prospecção ativa, base do BDR, ficava mais cara por mensagem.
3. **Mudança de sistema pelo cliente:** a imobiliária trocou de CRM durante o projeto.

## Divergência

| Lado | Posição |
|---|---|
| Cliente | Queria manter o escopo original e, em um momento, propôs trocar o BDR, já em fase final, por outra funcionalidade |
| Tecnologia | Apontava o épico como inviável no cronograma |
| Produto | Precisava preservar o valor contratado sem comprometer a previsibilidade das entregas |

## Opções

**Para o épico inviável:**

| Opção | Resultado |
|---|---|
| Manter o épico original | Descartada: inviável no cronograma |
| Substituir por captura dos leads perdidos no WhatsApp para o CRM | Escolhida e acordada com o cliente |
| Outras três opções avaliadas | Detalhes: **[NÃO DOCUMENTADO neste portfólio]** |

**Para o custo por mensagem:**

| Opção | Resultado |
|---|---|
| Usar API não oficial de WhatsApp para fugir do custo | Não recomendada: risco de banimento do número |
| Medir o impacto com simulador e decidir com números | Escolhida: decisão do BDR adiada até a definição dos novos preços |

## Critérios de decisão

| Critério | Como pesou |
|---|---|
| **Valor** | Reinvestir onde já havia retorno: os épicos de pré-venda estavam gerando valor |
| **Esforço** | O épico inviável consumiria esforço sem entrega dentro do prazo |
| **Risco** | API não oficial reduziria custo, mas colocaria o número do cliente em risco |
| **Previsibilidade** | Retirar a entrega de menor valor protegia o prazo das demais |

## Decisão

1. **Cancelar o épico original** e reinvestir o esforço em enriquecimentos dos épicos que já geravam valor: sequência de aquecimento, pontuação de leads (lead scoring) e integração do WhatsApp com o CRM.
2. **Não recomendar API não oficial**, mesmo com o aumento de custo.
3. **Análise de custo com simulador interativo**, comunicada ao cliente, para que a decisão sobre o volume de mensagens fosse dele, com números.
4. **BDR em dois canais:** WhatsApp e ligação por voz com IA (Twilio e ElevenLabs), com canal escolhido lead a lead pela própria operação, em planilha, sem depender do time técnico.
5. **Cadência de reativação** em 30, 60 e 90 dias, com horários fixos de disparo.
6. **Script do agente** substituído pelo script de SDR do próprio cliente, focado em qualificação.

## Requisitos

A decisão virou escopo verificável:

- Novo escopo acordado com o cliente e registrado no PRD.
- Épico do BDR em dois canais especificado até a versão final.
- Teste de aceite com o time encontrou bugs críticos antes da entrega: ordem das mensagens e ausência de tags. Os dois foram registrados para correção.

## MVP

O recorte foi a própria decisão de escopo: o épico inviável saiu, e o esforço foi para o fluxo principal de pré-venda, que precisava atravessar a jornada do lead de ponta a ponta.

## Riscos

| Risco | Tratamento |
|---|---|
| Custo por mensagem inviabilizar a prospecção ativa | Simulador de custo e decisão do cliente com números |
| Banimento do número por uso de API não oficial | Não recomendada |
| Troca de CRM pelo cliente durante o projeto | Tratada como mudança de escopo |

## Impacto

| Item | Situação |
|---|---|
| Novo escopo | Acordado com o cliente |
| Fluxo principal do BDR (entrada de leads e relatórios) | Funcionando no teste de aceite |
| Hipótese de valor | A sequência de nutrição buscava elevar o comparecimento a visitas de 45% a 60% para 65% a 70%. **Estimativa do discovery, não resultado medido** |
| Resultado em produção | **[NÃO DOCUMENTADO]** |

## O que não deu certo

Mudanças sucessivas de prioridade e a troca de CRM pelo cliente consumiram esforço já investido, e o desenvolvimento foi pausado. Casos como este levaram à política de tratar migração de sistema do cliente como mudança formal de escopo.

## Aprendizado

- Cancelar um épico não é fracasso, é disciplina. Reforçar o que já gerava valor era a aposta de maior retorno esperado; o retorno real não chegou a ser medido.
- Mudança de custo da plataforma é decisão de produto, não só nota técnica: o cliente precisa decidir com números.
- Dar controle operacional ao cliente, como a planilha de canais, reduz a dependência do time e acelera ajustes.
