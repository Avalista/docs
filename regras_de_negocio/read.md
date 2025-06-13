# 📘 Regras de Negócio

Este documento lista todas as regras de negócio utilizadas no Avalista. Elas podem ser referenciadas nas histórias de usuário usando seus identificadores.

---

## 🟦 RN001 - E-mail único por conta

Nenhum usuário pode se registrar com um e-mail já existente no sistema.

---

## 🟦 RN002 - Campos obrigatórios para cadastro de **projeto**

Para cadastrar um projeto, os seguintes campos são obrigatórios:

- Título (mínimo de 2 caracteres e máximo de 40 caracteres)
- Descrição (mínimo de 10 caracteres e máximo de 90 caracteres)

---

## 🟦 RN003 - Um usuário avalista so pode visualizar projetos dos quais participa

Usuários autenticados só têm acesso à visualização dos projetos nos quais estão vinculados como avaliadores ou responsáveis.

---

## 🟦 RN004 - Campos obrigatórios para cadastro de **tela**

Para cadastrar uma tela, os seguintes campos são obrigatórios:

- Título (mínimo de 2 caracteres e máximo de 40 caracteres)
- Descrição (mínimo de 10 caracteres e máximo de 90 caracteres)
- Screenshot (imagem obrigatória)

---

## 🟦 RN005 - Níveis de **gravidade do problema**

Todo problema registrado em uma avaliação individual ou final deve conter um nível de gravidade, que deve ser obrigatoriamente selecionado entre as seguintes opções:

- **Baixa**: impacto menor, não impede o uso, mas prejudica a experiência.
- **Média**: impacto moderado, dificulta o uso.
- **Alta**: impacto severo, impede ou bloqueia.

Esses níveis são utilizados para priorizar correções e gerar estatísticas.

---

## 🟦 RN006 - Níveis de **esforço da alteração**

Todo problema registrado deve conter uma estimativa de esforço para correção, selecionada entre os seguintes níveis:

- **Leve**: a correção pode ser feita rapidamente, com pouca ou nenhuma reestruturação de código ou design.
- **Moderada**: exige ajustes intermediários, podendo envolver alterações em componentes ou lógica da interface.
- **Alta**: demanda mudanças significativas no projeto, layout ou fluxo do sistema.

Essa estimativa auxilia na priorização e no planejamento das correções junto à equipe de desenvolvimento e a gerar estatísticas.

---

## 🟦 RN007 - Finalização da avaliação individual

Uma avaliação individual só pode ser finalizada se todas as interações com telas estiverem encerradas (ou seja, marcadas como finalizadas em todas as diretrizes de todas as categorias).

---

## 🟦 RN008 - Prioridade do problema

Todo problema registrado em uma avaliação individual deve conter um atributo de **prioridade**, que indica se o problema é considerado mais relevante ou urgente para análise posterior.  
Esse atributo deve ser representado como um **valor booleano** (verdadeiro ou falso), onde:

- `true` (verdadeiro) indica que o problema possui prioridade.
- `false` (falso) indica que o problema não possui prioridade especial.

---

## 🟦 RN009 - Itens de avaliação ao iniciar avaliação

Quando uma avaliação é iniciada, todos os itens(telas, categorias, diretrizes) recebem o status **NOT_REVIEWED**

- `NOT_REVIEWED` Ainda não foi revisada pela avaliador.

---

## 🟦 RN010 - Problema adicionado para um item(tela, categoria, diretriz)

Quando um problema é adicionado para um item(tela, categoria, diretriz), o item recebe o status **REVIEWED_ISSUE**, marcando que ja foi avaliado nessas circunstancias, mas ainda é possíveis adicionar mais problemas para o mesmo item.

- `REVIEWED_ISSUE` Revisado com pelo menos um problema adicionado.

---

## 🟦 RN011 - Item(tela, categoria, diretriz) foi avaliado, porém nao encontrou nenhum problema.

Quando um item(tela, categoria, diretriz) é avaliado, mas não é encontrado nenhuma problema para ele, pode ser marcado como "revisado", recebendo o status **REVIEWED_OK**

- `REVIEWED_ISSUE` Revisado, mas sem problemas encontrados.

---
