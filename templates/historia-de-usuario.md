# Template de História de Usuário

## US-XX: [Título curto e descritivo]

**Como** [persona],
**quero** [ação],
**para** [benefício de negócio].

### Contexto

Por que essa história existe e qual dor ela resolve.

### Critérios de aceite

Regras para todo critério de aceite:

- **Observável:** alguém consegue ver o resultado acontecer.
- **Binário:** passou ou não passou. Sem "parcialmente".
- **Sem interpretação:** duas pessoas testando chegam à mesma conclusão.

O formato Dado/Quando/Então é opcional. Use quando ajudar a clareza.

| # | Critério |
|---|---|
| CA-01 | [Ex.: Ao receber uma mensagem fora do horário comercial, o agente responde com o texto de ausência configurado em até 10 segundos.] |
| CA-02 | **Dado** [condição], **quando** [ação], **então** [resultado verificável]. |

### O que não é critério de aceite

Investigação, causa-raiz e evidências de QA **não** entram aqui. Vão para uma tarefa ou para a Definition of Done.

### Fora do escopo desta história

- [Item]

### Dependências

- [História, integração ou acesso necessário]

---

## Exemplo: ruim x bom

| Ruim | Por quê | Bom |
|---|---|---|
| O agente deve responder de forma natural. | "Natural" depende de interpretação. | O agente responde usando apenas as frases aprovadas no roteiro anexo. |
| O sistema deve ser rápido. | Não é mensurável. | A resposta aparece em até 3 segundos após o envio. |
| Investigar por que a tabulação falha. | É tarefa, não critério. | Toda chamada encerrada recebe uma das tabulações da lista oficial. |
