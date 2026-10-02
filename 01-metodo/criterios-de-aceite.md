# Critérios de aceite

Regra de minha autoria, adotada como padrão no plano de redução de retrabalho: **toda história tem critério de aceite testável. Se o enunciado não fecha, a demanda não avança.**

## Por que a regra existe

| Problema | Causa | Decisão |
|---|---|---|
| Histórias aprovadas no QA funcional falhavam na auditoria pós-entrega | Critérios que permitiam interpretação, como "responder bem o cliente" | Começar pela regra mais objetiva e de efeito mais rápido: critério testável obrigatório |

## A regra

- **Observável:** alguém consegue ver o resultado acontecer.
- **Binário:** passou ou não passou.
- **Sem interpretação:** duas pessoas testando chegam à mesma conclusão.
- O formato Dado/Quando/Então é opcional. Uso quando ajuda a clareza.

## O que não é critério de aceite

- **Investigação e causa-raiz:** vão para tarefa ou para um item próprio do backlog. Exemplo real: "ouvir as gravações completas do lote de teste" entrou como história própria de investigação no épico de correções do [case 04](../02-cases/04-agente-de-voz-call-center/).
- **Evidência de QA:** vai para a Definition of Done.

## Limites técnicos viram critério

Quando um sistema de terceiro tem limite, o limite entra no critério. No [case 04](../02-cases/04-agente-de-voz-call-center/), a discadora derrubava chamadas com resposta acima de 3 segundos. Esse número deveria estar no critério desde a primeira versão.

Template com exemplos ruim x bom e checklist de revisão: [03-templates/criterios-de-aceite.md](../03-templates/criterios-de-aceite.md).
