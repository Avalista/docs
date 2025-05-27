### HU025 - Detalhar categoria

---

**Como** avaliador autenticado

**Eu quero** visualizar todas as informações detalhadas de uma categoria específica, incluindo as heurísticas que estão associadas a ela

**Para que** eu possa compreender completamente o propósito e o contexto da categoria, verificar seus dados e suas relações no sistema.

---

### Critérios de Aceitação

- Na tela de detalhes da categoria, devem ser exibidas de forma clara todas as informações pertinentes à categoria:
  - **Nome** da categoria.
  - **Cor** da categoria.
- A tela de detalhes deve exibir uma seção listando todas as Heurísticas que estão atualmente associadas a esta categoria.
  - Para cada heurística listada, deve ser exibido, no mínimo, o seu **código**, **nome** e **descrição**.
- Se a categoria não possuir nenhuma heurística associada no momento, uma mensagem deve ser exibida na seção correspondente ("Nenhuma heurística está associada a esta categoria.").
- A tela de detalhes da categoria deve conter opções (como botões ou links) para as seguintes ações:
  - Voltar para a tela de listagem de categorias (HU024).
  - Editar categoria (Conforme HU023 - Editar categoria).
  - Deletar categoria (Conforme HU026 - Deletar categoria).