# Managed Resources

## Pergunta que este documento responde

Como o Gamas-framework referencia recursos proprietarios sem copia-los para o cliente?

## Regra central

Managed resources sao referenciados por contrato, usando `gamas://`.

Exemplos:

```txt
gamas://skills/product-model-canvas@1.0.0
gamas://workflows/feature-to-release@1.0.0
gamas://quality-gates/prd-standard@1.0.0
```

## O cliente recebe

- contrato YAML;
- resumo do recurso;
- versao;
- ownership;
- visibilidade;
- forma de referencia.

## O cliente nao recebe

- implementacao proprietaria completa;
- prompts internos;
- heuristicas sensiveis;
- validators avancados;
- model routing proprietario.
