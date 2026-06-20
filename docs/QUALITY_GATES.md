# Quality Gates

## Pergunta que este documento responde

Como quality gates devem funcionar no Gamas-framework?

## Conceito

Quality gate e uma validacao que orienta ou bloqueia uma etapa critica.

## Regras

- gates basicos podem rodar localmente;
- gates avancados devem ser managed resources;
- acoes criticas devem respeitar approval gates;
- contratos ficam em `framework/contracts/quality-gates`;
- implementacoes proprietarias nao devem ser copiadas para o workspace.
