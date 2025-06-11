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
