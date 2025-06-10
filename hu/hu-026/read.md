### HU026 - Cadastrar categoria

---

**Como** usuário adminstrador do sistema autenticado

**Eu quero** cadastrar uma categoria

**Para que** as heurísticas possam ser agrupadas e organizadas facilmente

---

### Critérios de Aceitação

- O formulário de cadastro de categoria deve conter os campos: **nome** (obrigatório) e **cor** (obrigatório).
- O campo **nome** da categoria deve ser único no sistema.
- O campo **cor** deve ter uma validação de formato #RRGGBB.
- Se o **nome** informado já estiver cadastrado para outra categoria, o sistema deve exibir uma mensagem de erro, como "Nome de categoria já existente.", e não permitir o cadastro.
- Ao cadastrar a categoria com sucesso, o sistema deve exibir uma mensagem de confirmação, como "Categoria cadastrada com sucesso!".
