# Definition of Ready e Definition of Done

Critério de aceite diz **o que** a entrega faz. A DoR diz **quando** a história pode começar. A DoD diz **como** ela foi entregue.

## Definition of Ready

Uma história só entra no desenvolvimento quando todos os itens abaixo estão marcados.

### Escopo

- [ ] PRD congelado e aceito pelo cliente
- [ ] História vinculada ao épico correspondente
- [ ] Critérios de aceite testáveis
- [ ] Regras de negócio e cenários de erro descritos

### Dependências

- [ ] Integrações mapeadas, com limites conhecidos
- [ ] Acessos, tokens e credenciais de teste disponíveis para o time
- [ ] Dependências de terceiros com responsável e prazo

### Entendimento

- [ ] Dúvidas abertas resolvidas ou registradas como questão (Q-xx)
- [ ] Time de desenvolvimento leu a história e não tem bloqueio

## Definition of Done

Uma história só está **pronta** quando todos os itens abaixo estão marcados.

### Desenvolvimento

- [ ] Código revisado e aprovado em pull request
- [ ] Pull request vinculado à história correspondente
- [ ] Sem erro conhecido pendente de registro

### Qualidade

- [ ] Todos os critérios de aceite testados e aprovados
- [ ] Evidências de teste anexadas à história (print, gravação ou log)
- [ ] Cenários de erro testados
- [ ] Teste realizado no ambiente do cliente, além do ambiente simulado

### Documentação

- [ ] Configurações e variáveis documentadas
- [ ] Mudanças de fluxo refletidas no PRD

### Aceite

- [ ] Validado pelo PO
- [ ] Demonstrado ao cliente
- [ ] Aceite do cliente registrado
