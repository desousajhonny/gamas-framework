# Architecture

## Pergunta que este documento responde

Como o Gamas-framework se separa entre produto comercial, agente local, workspace do cliente, runtime e logica proprietaria?

## Principio central

O Gamas-framework deve separar claramente:

- arquivos da empresa do cliente;
- estado interno e runtime do Gamas;
- logica proprietaria do framework.

O cliente deve possuir e editar os arquivos da propria empresa. O cliente nao deve receber, dentro do workspace local, toda a logica proprietaria do Gamas-framework.

## Componentes macro

### Camadas do repositorio

O repositorio deve refletir a separacao comercial do produto:

- `packages/`: CLI, runtime, schemas, validators, registry client e VS Code Agent;
- `framework/`: contratos publicos, standards e templates distribuiveis;
- `internal/`: area internal-only para managed core e recursos proprietarios;
- `examples/`: exemplos seguros de uso, sem logica proprietaria completa;
- `docs/`: especificacoes canonicas.

Essa divisao evita que o Gamas-framework evolua como apenas um template de pastas.

### Gamas CLI

Instala e cria o workspace inicial da empresa.

Responsabilidades:

- criar a estrutura inicial;
- registrar empresa e produto ativo ou planejado;
- criar manifests iniciais;
- preparar o workspace para o VS Code;
- orientar o usuario a usar o Gamas.

O CLI faz onboarding estrutural. Ele nao deve executar diagnostico profundo nem carregar toda a logica proprietaria.

### Gamas VS Code Agent

Interface local do usuario dentro do VS Code.

Responsabilidades:

- operar comandos como `/setup`, `/status`, `/run workflow` e `/validate`;
- ler o workspace do cliente;
- conduzir configuracoes e rotinas;
- ajudar a escrever e refinar documentos da empresa;
- atuar como copiloto operacional do founder.

Gamas e o agente/orquestrador local. Ele nao e o nome do framework inteiro.

### Client Workspace

Workspace local, editavel e versionavel em GitHub pelo cliente.

Pode conter:

- estrutura da empresa;
- produtos;
- manifests;
- documentos estrategicos;
- agentes configuraveis;
- workflows customizaveis;
- second brain;
- metricas;
- logs;
- contratos e referencias de skills e workflows.

Esse workspace pertence ao cliente.

### Gamas Runtime

Camada local responsavel por executar comandos, ler manifests, manter estado interno, aplicar validacoes e orquestrar interacoes locais.

O runtime pode manter estado proprio separado dos documentos editaveis do cliente.

### Gamas Registry

Catalogo de skills, workflows, templates e capabilities disponiveis.

O cliente pode receber contratos, referencias e configuracoes, mas nao necessariamente a implementacao completa de todos os recursos proprietarios.

### Gamas Cloud / Managed Core

Camada futura para recursos comerciais e logica sensivel.

Pode controlar:

- implementacao real de skills proprietarias;
- workflows-base avancados;
- prompts internos;
- quality gates avancados;
- validators avancados;
- heuristicas de setup;
- model routing proprietario;
- standards operacionais;
- logica sensivel de orquestracao.

Essa camada nao precisa existir completa na v1, mas a arquitetura deve reservar sua fronteira desde o inicio.

## Fronteira de propriedade

O cliente recebe:

- CLI;
- VS Code Agent Gamas;
- workspace local da empresa;
- estrutura organizada;
- manifests;
- documentos estrategicos;
- agentes configuraveis;
- workflows customizaveis;
- second brain;
- metricas;
- logs;
- contratos e referencias de skills e workflows.

O Gamas-framework controla:

- implementacao real de skills proprietarias;
- workflows-base avancados;
- prompts internos;
- quality gates avancados;
- validators avancados;
- heuristicas de setup;
- model routing proprietario;
- standards operacionais;
- logica sensivel de orquestracao.

## Regras arquiteturais obrigatorias

1. O workspace do cliente nunca deve conter implementacoes completas de managed skills, managed workflows ou managed quality gates.
2. Recursos proprietarios devem ser referenciados por contrato, nao copiados como Markdown, prompts ou scripts abertos.
3. O runtime local pode executar comandos e validacoes basicas, mas deve resolver recursos gerenciados via registry/runtime apropriado.
4. O cliente pode criar overrides locais, mas nao deve sobrescrever diretamente a implementacao base de recursos `gamas://`.
5. Manifests YAML devem guardar estado estruturado.
6. Markdown deve guardar conhecimento humano e contexto legivel por LLM.
7. A pasta `.gamas/` e system-managed e nao deve ser tratada como area principal de edicao do usuario.
8. Toda decisao importante gerada por workflow deve poder ser registrada no second brain.
9. Qualquer acao critica deve respeitar approval gates configuraveis.
10. O framework nao deve hardcodar um unico modelo de IA como obrigatorio.

## Managed resources e namespace `gamas://`

`gamas://` e o namespace interno usado para referenciar recursos gerenciados pelo Gamas-framework.

Exemplos:

```txt
gamas://skills/product-model-canvas
gamas://workflows/feature-to-release
gamas://quality-gates/prd-standard
```

Esses identificadores apontam para recursos controlados pelo framework, registry, runtime ou managed core.

O workspace do cliente pode declarar que usa um recurso `gamas://`, mas nao deve conter a implementacao proprietaria completa desse recurso.

## Contratos, overrides e customizacao

O cliente pode customizar a operacao por meio de:

- manifests;
- configuracoes locais;
- documentos Markdown;
- overrides declarativos;
- workflows customizados;
- agentes configuraveis;
- regras especificas da empresa.

Essas customizacoes devem estender ou configurar recursos do Gamas-framework, nao sobrescrever diretamente a implementacao base proprietaria.

## Uso de YAML e Markdown

YAML deve ser usado para estado estruturado, manifests, configuracoes, referencias e relacoes entre recursos.

Markdown deve ser usado para conhecimento humano, contexto legivel por LLM, decisoes, estrategia, playbooks editaveis e second brain.

Essa separacao evita que documentos humanos virem banco de dados improvisado e evita que manifests virem textos longos demais para manutencao.

## Pasta `.gamas/`

`.gamas/` e uma pasta gerenciada pelo sistema.

Ela pode conter estado local, cache, locks, referencias resolvidas, logs tecnicos e metadados do runtime.

O usuario nao deve tratar `.gamas/` como area principal de edicao. Conteudo de negocio, estrategia, memoria e workflows editaveis devem viver fora dela.

## Approval gates

Acoes criticas devem respeitar approval gates configuraveis.

Exemplos de acoes criticas:

- alterar arquivos importantes do Company OS;
- executar workflow que modifica muitos arquivos;
- aplicar validacoes que bloqueiam release;
- chamar recursos gerenciados pagos;
- executar comandos com impacto em repositorios, deploy ou dados sensiveis.

O Gamas deve favorecer confirmacao explicita quando houver risco operacional, financeiro, tecnico ou de privacidade.

## Modelos de IA

O Gamas-framework deve ser model-agnostic.

Ele pode recomendar modelos por papel, mas nao deve hardcodar um unico fornecedor ou modelo como obrigatorio.

Papeis possiveis:

- orquestrador;
- estrategista;
- implementador;
- revisor;
- analista;
- suporte;
- comercial.

## Decisao de arquitetura

A v1 pode ser local-first, mas nao deve ser arquitetada como um simples template de pastas.

O produto deve nascer com fronteiras claras entre o que o cliente edita, o que o runtime opera, o que referencia recursos gerenciados e o que pertence ao valor proprietario do Gamas-framework.
