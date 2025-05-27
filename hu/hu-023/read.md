### HU023 - Editar categoria

---

**Como** usuário adminstrador do sistema autenticado

**Eu quero** editar os dados de uma categoria existente

**Para que** eu possa corrigir informações incorretas ou atualizar detalhes de uma categoria

---

### Critérios de Aceitação

- O sistema deve fornecer uma forma para o administrador selecione ou identifique uma categoria existente que deseja editar
- Ao iniciar a edição de uma categoria, o formulário de edição deve ser pré-preenchido com os dados atuais da categoria selecionada: **nome** e **cor**.
- O campo nome da categoria deve ser editável.
- Ao salvar as alterações, o campo **nome** não pode estar vazio ou conter apenas espaços em branco.
- O campo cor da categoria deve ser editável.
- Ao salvar as alterações, o campo **cor** não pode estar vazio ou conter apenas espaços em branco.
- O campo **cor** deve ter uma validação de formato #RRGGBB.
- Ao salvar as alterações com sucesso, o sistema deve exibir uma mensagem de confirmação (por exemplo, "Categoria atualizada com sucesso!").
