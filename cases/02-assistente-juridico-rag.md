# Caso 02: Assistente jurídico com RAG

**Setor:** advocacia | **Papel:** Product Owner

## Contexto

Escritório de advocacia com assistente de IA baseado em RAG (busca em base de conhecimento jurídica) dividido em agentes especializados por área do direito.

## Problema

Além de correções de bugs e desempenho, havia uma divergência entre o escopo **percebido** e o escopo **real**: a documentação de arquitetura indicava muito mais agentes do que de fato estavam em produção. E o modelo de custo de infraestrutura precisava ser redefinido.

## Decisões de produto

- Revisão da documentação de arquitetura com base no que estava efetivamente em produção. O número real de agentes era cerca de um terço do documentado.
- Estruturação de alternativas de modelo de custo para o cliente, com recomendação clara: a empresa mantém a infraestrutura e repassa o custo como mensalidade de serviço.
- Correções e melhorias organizadas em histórias com critérios de aceite verificáveis.

## Aprendizado

Documento desatualizado é dívida de produto. Quando o cliente acredita ter mais do que tem, qualquer conversa comercial começa torta. Corrigir a fonte da verdade veio antes de qualquer nova funcionalidade.
