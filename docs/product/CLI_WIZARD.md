# CLI Wizard v0.1

## Pergunta que este documento responde

Como o wizard terminal do Gamas-framework deve instalar e organizar o workspace inicial de uma empresa AI First sem virar um diagnostico profundo?

## Principio

O CLI instala e organiza. O Gamas, dentro do VS Code, entende e preenche.

O wizard deve capturar apenas o contexto minimo para criar um Company OS inicial e preparar o usuario para rodar `/setup`.

Ele nao deve:

- executar Product Model Canvas completo;
- aprofundar estrategia;
- criar areas customizadas;
- copiar managed skills, managed workflows ou managed quality gates para o workspace do cliente;
- transformar o terminal em um questionario longo.

## Fluxo do wizard

1. Boas-vindas com identidade GAMAS.
2. Nome da empresa.
3. Empresa nova ou existente.
4. Produto existente ou produto planejado.
5. Nome do produto.
6. O que o produto faz, em uma frase curta.
7. Estagio atual: ideia, MVP, em desenvolvimento ou com usuarios.
8. Caminho local ou URL do repo, se existir.
9. Catalogo de areas/agentes.
10. Modelos/ferramentas pretendidos: Claude, Codex, Gemini, DeepSeek, outros.
11. Idioma principal dos documentos.
12. Criar workspace VS Code.
13. Preview da estrutura.
14. Confirmacao e geracao.
15. Mensagem final: abrir VS Code e rodar `/setup`.

## Catalogo de areas/agentes

O wizard deve mostrar um catalogo completo da v1, com nucleo obrigatorio e areas opcionais.

### Nucleo obrigatorio

Estas areas ficam sempre ativas:

- CEO & Estrategia;
- Produto;
- Operacoes;
- Memoria & Decisoes;
- Qualidade.

O usuario nao deve conseguir desativar o nucleo obrigatorio.

### Areas opcionais

O usuario pode ativar ou desativar:

- Engenharia;
- Design/UX;
- Growth/Marketing;
- Comercial/Vendas;
- Suporte/Customer Success;
- Metricas/Analytics;
- Financeiro;
- Legal/Compliance;
- Infraestrutura/Security;
- Data/AI Ops.

Para SaaS/AI apps, o wizard deve sugerir Engenharia, Design/UX, Metricas/Analytics e Growth/Marketing como pre-selecionadas, mas editaveis.

## Saida gerada por area ativa

Cada area ativa deve gerar apenas estrutura leve:

- manifest YAML da area;
- README curto explicando o papel da area;
- referencias `gamas://` para skills, workflows e quality gates aplicaveis.

Exemplos de referencias:

```txt
gamas://skills/product-model-canvas
gamas://workflows/feature-to-release
gamas://quality-gates/prd-standard
```

O workspace do cliente pode declarar que usa esses recursos, mas nao deve conter a implementacao proprietaria completa.

## Saida geral do wizard

O workspace inicial deve conter:

- `START_HERE.md`;
- manifest da empresa;
- manifest do produto ativo ou planejado;
- manifest de areas/agentes ativos;
- config local do Gamas-framework;
- instrucoes para abrir o VS Code e rodar `/setup`.

## Preview antes de gerar

Antes de escrever arquivos, o CLI deve mostrar um resumo com:

- empresa;
- empresa nova ou existente;
- produto;
- produto existente ou planejado;
- estagio;
- repo ou caminho local, quando existir;
- areas obrigatorias;
- areas opcionais ativadas;
- modelos/ferramentas escolhidos;
- idioma dos documentos;
- workspace VS Code: sim ou nao.

## Regras de seguranca e IP

- O CLI nao deve sobrescrever arquivos existentes sem confirmacao.
- O CLI nao deve copiar prompts proprietarios para o workspace.
- O CLI nao deve copiar workflows-base avancados como Markdown aberto.
- O CLI nao deve copiar managed quality gates completos.
- Recursos proprietarios devem ser referenciados por contrato via `gamas://`.
- A pasta `.gamas/` e system-managed e nao deve ser usada como area principal de edicao do usuario.

## Criterio de pronto

O wizard v0.1 esta pronto quando:

- pode ser respondido em menos de 5 minutos;
- diferencia empresa nova de empresa existente;
- diferencia produto existente de produto planejado;
- cria estrutura leve para areas ativas;
- nao cria estrutura principal para areas nao ativadas;
- preserva a fronteira de IP do Gamas-framework;
- termina com o proximo passo claro: abrir VS Code e rodar `/setup`.
