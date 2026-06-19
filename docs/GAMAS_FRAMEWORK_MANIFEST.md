# Gamas-Framework Manifest

## Status

Este documento define a visao inicial do Gamas-Framework e deve ser tratado como a fonte canonica do produto enquanto a arquitetura, o wizard, os workflows e o modelo de negocio evoluem.

## Contexto

Gamas-Framework e um produto da GAMA, uma empresa AI First. A propria GAMA sera o primeiro ambiente de teste do framework, usando a estrutura para organizar sua operacao, desenvolver seus produtos e validar o modelo antes de disponibiliza-lo para clientes.

O objetivo do Gamas-Framework e permitir que uma empresa, especialmente uma startup operada por uma pessoa so, crie um sistema operacional AI First para gerir estrategia, organizacao, execucao, produto, codigo, qualidade, metricas e aprendizado continuo com apoio de IA.

## Definicao do Produto

Gamas-Framework e o framework instalavel que clientes poderao ativar em suas empresas para estruturar uma operacao AI First.

Ele devera ser disponibilizado por uma CLI, por exemplo `npx gamas-framework`, que guia o usuario por um wizard e cria a estrutura necessaria para a empresa operar com clareza organizacional e disciplina operacional.

O framework nao e apenas um gerador de arquivos. Ele e uma metodologia operacional empacotada em software, templates, playbooks, regras, workflows, contratos de agentes e memoria estruturada.

## GAMA

GAMA e a empresa criadora do Gamas-Framework.

Ela tambem sera o primeiro caso de uso do proprio produto. Isso significa que as decisoes, fluxos, processos e aprendizados da GAMA devem ser usados para validar, melhorar e refinar o framework.

O Gamas-Framework deve ser pensado como um produto comercial da GAMA, com potencial de evoluir para um ecossistema composto por CLI, templates, extensoes, agentes, integracoes, conteudo premium e suporte especializado.

## Gamas Agent

Gamas e o agente interno do ecossistema Gamas-Framework.

Ele atua como copiloto operacional do CEO solo, ajudando a gerenciar tarefas, demandas internas, decisoes, produto, codigo, qualidade, metricas, memoria e rotinas da empresa.

Gamas nao e a empresa e nao substitui o Gamas-Framework. Gamas e a interface/agente que opera sobre a estrutura criada pelo Gamas-Framework.

Em versoes futuras, Gamas podera existir como extensao do VS Code, interface local, agente conectado a modelos de IA ou camada de orquestracao de comandos e workflows.

## Camadas Principais

O Gamas-Framework possui duas camadas principais: Organizacional e Operacional.

### 1. Camada Organizacional

A Camada Organizacional define como a empresa e estruturada.

Ela descreve as areas, funcoes, responsabilidades, agentes simulados, memoria institucional, estrategia, posicionamento, produtos, governanca e divisao de trabalho da empresa.

Essa camada responde perguntas como:

- O que e a empresa?
- Qual problema ela resolve?
- Como ela se posiciona?
- Quais produtos ela desenvolve?
- Como ela se divide internamente?
- Quais areas existem?
- Quem ou qual agente e responsavel por cada tipo de decisao?
- Como a empresa preserva memoria, contexto e aprendizado?

### 2. Camada Operacional

A Camada Operacional define como a empresa executa o trabalho no dia a dia.

Ela nao existe apenas para desenvolvimento de software. Ela cobre a operacao completa da empresa: produto, engenharia, comercial, suporte, financeiro, metricas, qualidade, decisoes, aprendizado e gestao interna.

Dentro dela ficam os workflows, playbooks, regras, skills, gates de qualidade, handoffs, processos de decisao e rotinas que permitem que modelos como Claude, Codex, Gemini, DeepSeek ou outros atuem com contexto e responsabilidade.

A programacao do produto e apenas um dos fluxos operacionais, junto com suporte, vendas, discovery, roadmap, QA, metricas e melhoria continua.

Essa camada responde perguntas como:

- Como uma demanda nasce?
- Como uma decisao e tomada?
- Como uma feature vira escopo?
- Como uma tarefa e priorizada?
- Como o codigo e implementado, revisado, testado e entregue?
- Como suporte, comercial, produto, engenharia e financeiro se comunicam?
- Como metricas geram aprendizado?
- Como aprendizados viram memoria ou melhoria de workflows?

## Relacao com Repositorios de Produto

O Gamas-Framework deve suportar empresas que ja possuem um produto em desenvolvimento e empresas que ainda nao possuem produto criado.

Quando o cliente ja tiver um produto, o wizard devera conectar esse repositorio ao sistema operacional da empresa, sem assumir automaticamente controle sobre o codigo.

Quando o cliente ainda nao tiver produto, o wizard devera ajudar a estruturar a empresa, definir estrategia, produto planejado, MVP e roadmap antes de conectar ou criar um repositorio de produto.

A memoria canonica da empresa deve ficar no ambiente do Gamas Company OS, enquanto os repositorios de produto continuam sendo fontes de codigo, testes, infraestrutura e implementacao.

## Memoria da Empresa

A memoria da empresa deve ser centralizada no Gamas Company OS.

Essa memoria deve incluir decisoes, estrategia, posicionamento, aprendizados, areas, processos, playbooks, metricas, historico operacional e contexto especifico de produtos.

Quando a empresa possuir mais de um produto, a memoria global da empresa deve permanecer compartilhada, enquanto memorias especificas de produto devem ser separadas por produto.

## Modelos de IA

O Gamas-Framework nao deve depender de um unico modelo de IA.

Ele deve ser compativel com diferentes modelos e superficies, como Claude, Codex, Gemini, DeepSeek ou outros. Cada modelo pode assumir papeis diferentes conforme capacidade, custo, preferencia e contexto.

O framework deve definir papeis e responsabilidades antes de definir fornecedores de modelo. Exemplos de papeis:

- orquestrador;
- estrategista;
- implementador;
- revisor;
- analista de metricas;
- suporte;
- comercial;
- pesquisador.

## Principios Iniciais

- Local-first por padrao.
- Memoria da empresa separada do codigo do produto.
- Organizacao visivel para humanos e modelos.
- Workflows claros, com inicio, fim, entradas e saidas.
- Decisoes importantes registradas e rastreaveis.
- Operacao completa da empresa, nao apenas desenvolvimento.
- Compatibilidade com multiplos modelos de IA.
- Protecao de propriedade intelectual por produto, marca, atualizacoes, experiencia e extensoes, nao por esconder arquivos locais.

## Modelo de Negocio Inicial

O Gamas-Framework deve nascer como produto da GAMA e pode evoluir em camadas comerciais.

Possiveis frentes:

- CLI e estrutura base;
- templates premium;
- extensao Gamas para VS Code;
- pacotes de workflows por tipo de empresa;
- agentes especializados;
- suporte e consultoria de implantacao;
- conteudo educacional;
- integracoes com ferramentas externas;
- recursos cloud ou API para diagnosticos, recomendacoes e upgrades.

## Direcao de Produto

O primeiro objetivo e criar uma base clara, instalavel e util para a propria GAMA.

Depois, o framework deve ser testado em cenarios reais:

- empresa com produto existente;
- empresa sem produto ainda;
- empresa com multiplos produtos;
- founder solo usando IA como equipe ampliada;
- operacao com agentes simulados e modelos especializados.

O sucesso inicial do Gamas-Framework sera medido pela capacidade de ajudar uma empresa pequena a tomar decisoes melhores, executar com mais clareza, preservar memoria e transformar IA em uma estrutura operacional pratica.
