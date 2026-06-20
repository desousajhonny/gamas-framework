# GAMA

## O que e a GAMA

GAMA e uma empresa AI First e a criadora do Gamas-framework.

A propria GAMA sera o primeiro caso real do produto: ela usara o Gamas-framework para organizar sua estrategia, operar seus produtos, registrar decisoes, melhorar workflows e validar a estrutura antes de disponibiliza-la para clientes.

## O que e o Gamas-framework

Gamas-framework e um produto comercial para founders solo criarem e operarem empresas AI First com mais clareza, processo, qualidade e memoria.

Ele nao e apenas documentacao, template de pastas ou agente de codigo. Ele combina CLI, workspace local, manifests, Gamas Agent, runtime, registry e uma camada futura de managed core para ajudar humanos e modelos de IA a trabalharem com contexto compartilhado.

## O que e o Gamas Agent

Gamas e o agente/orquestrador local do ecossistema Gamas-framework.

Ele opera dentro do VS Code como copiloto operacional do founder, ajudando a conduzir setup, decisoes, tarefas, produto, codigo, qualidade, metricas e memoria da empresa.

Gamas nao e o framework inteiro. Gamas e a interface/agente local que opera sobre o workspace criado pelo Gamas-framework.

Na v1, Gamas deve ser tratado como contrato, comandos e experiencia planejada. A extensao VS Code e o runtime completo de agente virao depois.

## Fronteiras do produto

O Gamas-framework deve separar:

- arquivos da empresa do cliente;
- estado interno e runtime do Gamas;
- logica proprietaria do framework.

O cliente possui e edita o workspace local da propria empresa. A logica proprietaria avancada do Gamas-framework nao deve ser entregue integralmente dentro desse workspace.

## Camadas do Gamas-framework

O Gamas-framework possui duas camadas principais.

### Camada Organizacional

Define como a empresa e estruturada:

- estrategia;
- areas;
- responsabilidades;
- agentes simulados;
- decisoes;
- memoria;
- produto ativo ou planejado.

### Camada Operacional

Define como a empresa trabalha no dia a dia:

- workflows;
- playbooks;
- skills;
- qualidade;
- handoffs;
- metricas;
- rotinas;
- aprendizado.

## Contexto para IA

Para entender o Gamas-framework, leia:

- `docs/product/PRODUCT_MODEL_CANVAS.md`;
- `docs/product/VALUE_PROPOSITION.md`;
- `docs/ARCHITECTURE.md`;
- `docs/product/ROADMAP.md`.
