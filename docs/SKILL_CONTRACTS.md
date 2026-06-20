# Skill Contracts

## Pergunta que este documento responde

Como uma skill gerenciada deve ser declarada?

## Conceito

Skill e uma capacidade reutilizavel. Ela nao e um agente e nao e um workflow.

## Formato minimo

```yaml
id: prd-writer
type: managed
source: gamas://skills/prd-writer@1.0.0
visibility: contract
owner: gamas-framework
implementation: managed
```

Contratos ficam em `framework/contracts/skills`.
