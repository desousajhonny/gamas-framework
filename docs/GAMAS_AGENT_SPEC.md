# Gamas Agent Spec

## Pergunta que este documento responde

Qual e o papel do Gamas Agent no VS Code?

## Papel

Gamas e o agente local/orquestrador. Ele opera sobre o workspace do cliente.

Ele deve:

- ler contexto;
- conduzir comandos como `/setup`, `/status`, `/validate` e `/run-workflow`;
- respeitar approval gates;
- usar `gamas://`;
- escrever outputs no workspace;
- registrar decisoes no second brain;
- proteger logica proprietaria.

Scaffold documental: `packages/vscode-agent`.
