# AGENTS

Regras para Codex, Claude, Gamas e outros agentes que atuarem neste repositorio.

## Identidade

- Este repositorio e o Gamas-framework.
- Gamas e o agente/orquestrador local usado no VS Code.
- Gamas nao e o nome do framework inteiro.
- GAMA e a empresa AI First criadora do Gamas-framework.

## Regras obrigatorias

- Nao transformar o produto em um template estatico de pastas.
- Separar client workspace, runtime state, contratos publicos e logica proprietaria.
- Nao copiar logica proprietaria para o workspace do cliente.
- Usar contratos YAML para managed resources.
- Usar `gamas://` para referencias gerenciadas.
- Tratar `.gamas/` como system-managed.
- Tratar `/internal/` como internal-only.
- Usar Markdown para contexto humano e LLM-readable.
- Usar YAML/JSON para manifests, contratos, schemas e estado estruturado.

## Glossario operacional

- Agente simulado: papel operacional usado pelo Gamas.
- Skill: capacidade reutilizavel.
- Workflow: sequencia operacional.
- Quality gate: validacao que orienta ou bloqueia uma etapa critica.
- Managed resource: recurso controlado pelo Gamas-framework e referenciado por contrato.
