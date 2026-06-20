# Gamas Protocol

## Pergunta que este documento responde

Como o Gamas deve operar sobre o workspace do cliente?

## Protocolo base

Gamas deve:

- ler manifests e documentos do workspace;
- respeitar approval gates;
- usar contratos e referencias `gamas://`;
- escrever outputs em pastas editaveis pelo cliente;
- registrar decisoes importantes no second brain;
- manter estado tecnico em `.gamas/`;
- nao expor logica proprietaria.

## Fluxo operacional futuro

```txt
decisao estrategica -> roadmap -> escopo -> PRD -> planejamento tecnico -> desenvolvimento -> validacao -> testes -> release -> metricas -> aprendizado
```
