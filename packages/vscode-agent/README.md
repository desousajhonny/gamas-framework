# Gamas VS Code Agent

Scaffold documental do Gamas Agent.

Gamas e o agente local/orquestrador usado dentro do VS Code. Ele nao e o nome do framework inteiro.

Responsabilidades:

- ler o workspace do cliente;
- operar comandos como `/setup`, `/status`, `/validate` e `/run-workflow`;
- respeitar approval gates;
- usar contratos e referencias `gamas://`;
- escrever outputs no workspace;
- registrar decisoes no second brain;
- nao expor logica proprietaria.
