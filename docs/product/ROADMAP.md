# Roadmap

## Objetivo

Organizar as etapas para transformar o Gamas-framework em uma v1 publicavel sem construir interfaces antes do produto core estar claro.

## Principio

Produto primeiro, interfaces depois.

O Gamas-framework precisa definir bem o que gera, como organiza uma empresa AI First e como sera usado pela propria GAMA antes de implementar landing page, wizard CLI ou Gamas no VS Code.

## Fase 0: Fundacao Lean

Status: em andamento.

Objetivo: criar a base minima para qualquer humano ou IA entender o Gamas-framework e tomar boas decisoes sobre o produto sem inventar contexto.

### 0.1 Identidade do produto

- [x] Definir o que e a GAMA.
- [x] Definir o que e o Gamas-framework.
- [x] Definir o que e o Gamas Agent.
- [x] Definir a categoria: Company OS para founders solo AI First.
- [x] Definir que Gamas-framework e o produto e Gamas e o agente local.
- [ ] Remover termos redundantes ou confusos dos docs.

### 0.2 Cliente e dor

- [x] Definir cliente principal: founder solo de SaaS/AI app.
- [x] Definir dor central: IA sem sistema operacional.
- [x] Definir alternativas atuais: docs soltas, prompts, GitHub, Notion, IDEs, consultoria.
- [ ] Validar se a dor esta escrita de forma simples o bastante para um cliente reconhecer.

### 0.3 Proposta e transformacao

- [x] Definir one-liner.
- [x] Definir proposta de valor.
- [x] Definir transformacao antes/depois.
- [x] Definir fluxo norte: demanda -> decisao -> escopo -> implementacao -> testes -> review -> release -> aprendizado.
- [ ] Garantir que a proposta nao parece apenas "mais documentacao".

### 0.4 Limite da v1

- [ ] Definir claramente o que a v1 gera.
- [ ] Definir o que fica fora da v1.
- [ ] Definir que produto core vem antes de landing, wizard CLI e VS Code.
- [ ] Definir que a v1 foca em um produto ativo ou planejado.

### 0.5 Documentos canonicos

- [x] Criar `docs/GAMA.md`.
- [x] Criar `docs/product/PRODUCT_MODEL_CANVAS.md`.
- [x] Criar `docs/product/VALUE_PROPOSITION.md`.
- [x] Criar `docs/ARCHITECTURE.md`.
- [x] Criar `docs/product/ROADMAP.md`.
- [x] Criar `docs/product/CLI_WIZARD.md`.
- [ ] Garantir que Claude entende o produto lendo apenas esses arquivos.
- [ ] Garantir que nao ha docs redundantes competindo entre si.

### 0.6 Saida da fase

- [ ] A Fase 1 esta clara: definir o Produto Core.
- [ ] O proximo trabalho nao e interface, landing ou CLI.
- [ ] O proximo trabalho e definir a estrutura real que o Gamas-framework gera para uma empresa cliente.

Criterio de pronto:

- Claude consegue explicar o Gamas-framework sem contexto adicional;
- um founder entende rapidamente o problema e a promessa;
- o roadmap deixa claro que Produto Core vem antes das interfaces;
- nao existem documentos redundantes atrapalhando a leitura;
- a proxima fase tem uma pergunta objetiva: "o que o Company OS gerado precisa conter?".

## Fase 1: Produto Core

Objetivo: definir o que o Gamas-framework realmente gera para uma empresa cliente.

Checklist:

- [x] Definir estrutura do Company OS gerado.
- [x] Definir camada organizacional minima.
- [x] Definir camada operacional minima.
- [x] Definir arquivos obrigatorios do cliente.
- [x] Definir memoria, decisoes, workflows e produto ativo.
- [x] Definir catalogo v1 de areas/agentes.
- [x] Definir nucleo obrigatorio de areas.
- [x] Definir o que fica visivel e oculto na instalacao.
- [ ] Definir como a GAMA usara isso no dogfood.
- [x] Definir fronteira entre Client Workspace, Gamas Runtime, Registry e Managed Core.
- [x] Definir quais arquivos o cliente possui.
- [x] Definir quais recursos sao apenas referencias ou contratos.
- [x] Definir o que nao deve ser entregue no workspace local.
- [x] Definir manifests iniciais.
- [x] Definir estrategia inicial de protecao de IP.
- [x] Criar scaffold arquitetural em `packages/`, `framework/`, `internal/` e `examples/`.
- [x] Criar specs operacionais em `docs/`.

Criterio de pronto:

- qualquer implementador entende qual estrutura o produto deve gerar antes de pensar nas interfaces.

## Fase 2: Setup Conversacional

Objetivo: detalhar o `/setup` antes de qualquer implementacao de interface.

Checklist:

- [ ] Definir modulos do `/setup`.
- [ ] Definir empresa nova vs empresa existente.
- [ ] Definir perguntas minimas por modulo.
- [ ] Definir saidas geradas pelo setup.
- [ ] Definir pausa, retomada e refinamento.
- [ ] Definir como o `/setup` alimenta estrategia fina.

Criterio de pronto:

- o Gamas consegue guiar um founder ate uma primeira versao coerente da empresa, produto e estrategia.

## Fase 3: Interfaces do Produto

Objetivo: preparar as interfaces do Gamas-framework depois que o produto core estiver definido.

### 3.1 Landing Page

Interface de venda.

Checklist:

- [ ] Definir promessa de venda.
- [ ] Definir secoes da pagina.
- [ ] Definir CTA inicial.
- [ ] Definir prova de valor com dogfood da GAMA.

Criterio de pronto:

- a landing explica o problema, a promessa e o caminho para experimentar o Gamas-framework.

### 3.2 Wizard CLI Terminal

Interface de onboarding e instalacao.

Checklist:

- [x] Definir especificacao do wizard em `docs/product/CLI_WIZARD.md`.
- [ ] Criar package Node/TypeScript.
- [ ] Configurar bin `gamas-framework`.
- [ ] Criar banner GAMAS premium tech.
- [ ] Adicionar cores, spinners e checkpoints.
- [ ] Implementar perguntas rapidas.
- [ ] Diferenciar empresa nova vs existente.
- [ ] Diferenciar produto existente vs produto planejado.
- [ ] Capturar nome do produto e descricao curta.
- [ ] Capturar estagio atual do produto.
- [ ] Registrar produto ativo ou planejado.
- [ ] Implementar catalogo completo v1 de areas/agentes.
- [ ] Manter nucleo obrigatorio sempre ativo.
- [ ] Pre-selecionar Engenharia, Design/UX, Metricas/Analytics e Growth/Marketing para SaaS/AI apps.
- [ ] Gerar estrutura leve para areas ativas.
- [ ] Gerar apenas manifests, READMEs curtos e referencias `gamas://` por area.
- [ ] Mostrar preview da estrutura.
- [ ] Gerar Company OS inicial.
- [ ] Criar `START_HERE.md`.
- [ ] Gerar manifest da empresa.
- [ ] Gerar manifest do produto.
- [ ] Gerar manifest de areas/agentes ativos.
- [ ] Salvar config local.
- [ ] Evitar overwrite sem confirmacao.
- [ ] Finalizar orientando abrir VS Code e rodar `/setup`.

Criterio de pronto:

- um usuario instala, responde ao wizard em menos de 5 minutos e entende claramente o proximo passo.

### 3.3 Gamas no VS Code

Interface operacional do founder.

Checklist:

- [ ] Definir experiencia inicial do agente.
- [ ] Definir comandos como `/setup`.
- [ ] Definir como le o Company OS.
- [ ] Definir como escreve e refina documentos.
- [ ] Definir limites da v1 sem runtime autonomo.

Criterio de pronto:

- o founder consegue usar o Gamas como copiloto operacional sobre o Company OS.

## Fase 4: Fluxo Operacional Minimo

Objetivo: validar o fluxo de demanda ate aprendizado.

Checklist:

- [ ] Demanda.
- [ ] Decisao.
- [ ] Escopo.
- [ ] Implementacao.
- [ ] Testes/review.
- [ ] Release.
- [ ] Aprendizado.

Criterio de pronto:

- uma demanda real percorre o fluxo completo:

```txt
demanda -> decisao -> escopo -> implementacao -> testes -> review -> release -> aprendizado
```

## Fase 5: Dogfood da GAMA

Objetivo: usar a propria GAMA como primeiro caso real.

Checklist:

- [ ] Criar Company OS da GAMA.
- [ ] Conectar Gamas-framework como produto.
- [ ] Usar `/setup` na propria GAMA.
- [ ] Registrar decisoes reais.
- [ ] Registrar aprendizados.
- [ ] Ajustar framework com base no uso real.

Criterio de pronto:

- a GAMA consegue operar o desenvolvimento do proprio produto com a estrutura gerada.

## Fase 6: Publicacao V1

Objetivo: preparar publicacao externa.

Checklist:

- [ ] Pacote npm.
- [ ] README publico.
- [ ] Guia de instalacao.
- [ ] Exemplo de uso.
- [ ] Templates base.
- [ ] Licenca.
- [ ] Primeira versao publicavel.

Criterio de pronto:

- um founder externo consegue rodar `npx gamas-framework`, criar seu Company OS e entender o proximo passo sem ajuda direta.
