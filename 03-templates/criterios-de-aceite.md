# Critérios de aceite

Critério de aceite diz **o que** a entrega faz. Se o time não consegue testar, o critério não está pronto, e a história não avança.

## Regras

- **Observável:** alguém consegue ver o resultado acontecer.
- **Binário:** passou ou não passou. Sem "parcialmente".
- **Sem interpretação:** duas pessoas testando chegam à mesma conclusão.

O formato Dado/Quando/Então é opcional. Use quando ajudar a clareza.

## Formatos

| Formato | Exemplo |
|---|---|
| Direto | Ao receber uma mensagem fora do horário comercial, o agente responde com o texto de ausência configurado em até 10 segundos. |
| Dado/Quando/Então | **Dado** um lead sem resposta há 30 dias, **quando** o horário de disparo chega, **então** o lead recebe a mensagem de reativação da cadência de 30 dias. |

## O que não é critério de aceite

Investigação, causa-raiz e evidências de QA **não** entram aqui. Vão para uma tarefa ou para a Definition of Done.

## Ruim x bom

| Ruim | Por quê | Bom |
|---|---|---|
| O agente deve responder de forma natural. | "Natural" depende de interpretação. | O agente responde usando apenas as frases aprovadas no roteiro anexo. |
| O sistema deve ser rápido. | Não é mensurável. | A resposta aparece em até 3 segundos após o envio. |
| Investigar por que a tabulação falha. | É tarefa, não critério. | Toda chamada encerrada recebe uma das tabulações da lista oficial. |
| Responder bem o cliente. | Não há como testar "bem". | Para cada pergunta da lista de testes, o agente responde com a informação da base de conhecimento indicada no gabarito. |

## Checklist de revisão

- [ ] Cada critério tem um resultado que se vê acontecer
- [ ] Nenhum critério usa adjetivo sem medida (rápido, natural, adequado, bom)
- [ ] Limites de sistemas de terceiros estão no critério (latência, formato, volume)
- [ ] Nenhum critério é investigação ou evidência de QA
- [ ] Duas pessoas testando chegariam à mesma conclusão
