# Definição de MVP

MVP não é a versão barata do escopo completo. É o menor recorte que entrega valor real e testa a hipótese principal do produto.

## Como recorto

1. **Recorte por público, não por funcionalidade solta.** Escolher um segmento em que as regras variam menos permite entregar o fluxo completo para alguém, em vez de um fluxo pela metade para todos.
2. **Preservar o fluxo principal.** O MVP precisa atravessar a jornada de ponta a ponta, ainda que para um caso simples.
3. **Retirar o que tem menor valor em relação ao esforço e ao risco.** Uma entrega pode sair do MVP mesmo já planejada, se mantê-la ameaça a previsibilidade do restante.
4. **Separar o que é núcleo do que é extensão.** Integrações sem as quais o produto não funciona ficam no MVP. Integrações que ampliam alcance vão para marcos seguintes.

## Pergunta de controle

> O recorte reduz de fato o esforço, ou as integrações centrais continuam necessárias?

Essa pergunta foi feita por um cliente durante a apresentação de um MVP, e é a pergunta certa. Um MVP que mantém todas as dependências pesadas reduz escopo funcional, mas não reduz risco. O recorte precisa responder às duas coisas, e o trade-off precisa ser explícito.

## Exemplos reais

| Situação | Recorte | Racional |
|---|---|---|
| Produto de automação contábil com escopo completo estimado em 6 a 12 meses | MVP focado em MEI | Público amplo, tributação fixa e no máximo um funcionário: menos variação de regra. [Case 01](../02-cases/01-automacao-contabil-whatsapp/) |
| Suíte de agentes comerciais com um épico inviável no cronograma | Cancelar o épico e reforçar os que já geravam valor | O épico consumiria esforço sem entrega no prazo; o esforço foi para o que já gerava valor. [Case 03](../02-cases/03-gestao-de-escopo-imobiliario/) |

## Checklist do MVP

- [ ] A hipótese principal está escrita em uma frase
- [ ] O público do MVP está definido
- [ ] O fluxo principal atravessa a jornada de ponta a ponta
- [ ] O que ficou fora está listado no PRD como "fora do escopo"
- [ ] As dependências que continuam necessárias estão explícitas
- [ ] O trade-off está escrito: o que o recorte reduz e o que não reduz
- [ ] A métrica que valida o MVP está definida
