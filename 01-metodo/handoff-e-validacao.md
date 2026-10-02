# Handoff, desenvolvimento e validação

O que acontece depois que o PRD é congelado, até o aceite e o aprendizado.

## Handoff para o desenvolvimento

A história só entra no desenvolvimento com a **Definition of Ready** completa. Os itens que mais derrubam sprints, na minha experiência, são acessos e dependências externas.

- PRD congelado e aceito pelo cliente
- Critérios de aceite testáveis
- Dependências mapeadas, com responsável
- Acessos, tokens e credenciais de teste disponíveis
- Dúvidas abertas resolvidas ou registradas como questão (Q-xx)

Checklist completo: [03-templates/dor-dod.md](../03-templates/dor-dod.md).

## Durante o desenvolvimento

- **O PO mantém a bola.** O acompanhamento ativo é responsabilidade do PO: bloqueio sem dono não fica esperando.
- **Atualização específica e rastreável.** Status diz qual item, com quem foi falado e quando. "Estamos aguardando o cliente" não é status.
- **Mudança de escopo é formal.** Pedido novo do cliente durante o desenvolvimento passa por avaliação de valor, esforço, risco e impacto no prazo antes de entrar.

## Validação e aceite

1. **Roteiro de testes** derivado dos critérios de aceite, executado com o time antes da demonstração.
2. **Teste no ambiente do cliente**, não só em ambiente simulado.
3. **Demonstração ao cliente**, com o roteiro em mãos.
4. **Aceite registrado.** Entregue não é aceito; aceito é quando o critério passou.

## Auditoria pós-entrega

Depois da entrega, reviso o que foi entregue contra a Definition of Done. Lacunas encontradas viram um **épico de correções** com histórias próprias e critérios reescritos para serem binários, em vez de bugs avulsos.

A auditoria encontra o que o QA funcional não pega quando os critérios originais permitiam interpretação ([case 04](../02-cases/04-agente-de-voz-call-center/)).

## Melhoria contínua

- Cada falha relevante vira regra de processo escrita. A regra de critério de aceite testável e os quatro portões do [método](README.md) nasceram assim.
- Começo pela regra mais objetiva e de efeito mais rápido, e só depois proponho as demais.
- Meta de melhoria precisa de linha de base medida. Sem linha de base, a meta não se sustenta como resultado.
