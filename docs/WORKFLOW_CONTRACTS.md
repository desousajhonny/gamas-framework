# Workflow Contracts

## Pergunta que este documento responde

Como um workflow gerenciado deve ser declarado?

## Conceito

Workflow e uma sequencia operacional. Ele pode usar agentes simulados, skills, documentos, approvals e quality gates.

## Formato minimo

```yaml
id: feature-to-release
type: managed
source: gamas://workflows/feature-to-release@1.0.0
visibility: contract
owner: gamas-framework
implementation: managed
```

Contratos ficam em `framework/contracts/workflows`.
