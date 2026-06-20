# Workspace Spec

## Pergunta que este documento responde

Como deve ser o workspace local gerado para uma empresa cliente?

## Regra central

O workspace pertence ao cliente, e deve ser editavel, legivel por humanos, versionavel em GitHub e seguro para modelos de IA.

## Estrutura base

O template canonico vive em `framework/templates/client-workspace`.

Ele contem:

- manifests YAML da empresa, produto, operacao e configuracao do Gamas;
- `company-os/` para conexao entre estrategia e operacao;
- `strategy/`, `business/`, `product/`, `departments/`, `agents/`;
- `skills/open/` para skills do cliente;
- `skills/managed/` para referencias gerenciadas;
- `workflows/custom/`, `workflows/overrides/`, `workflows/managed/`;
- `second-brain/` para decisoes e aprendizados;
- `metrics/` para sinais operacionais;
- `.gamas/` para estado tecnico system-managed.

## Proibido no workspace

- implementacoes completas de managed skills;
- workflows managed completos;
- managed quality gates completos;
- prompts proprietarios;
- heuristicas internas;
- logica sensivel de orquestracao.
