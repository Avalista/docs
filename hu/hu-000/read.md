### HU000 - Criar projeto

---

**Como** usuário autenticado

**Eu quero** criar um novo projeto

**Para que** eu possa organizar e visualizar as avaliações

---

#### Critérios de Aceitação

- **Dado que** estou logado no sistema  
  **Quando** eu clicar no botão "Novo Projeto" na dashboard  
  **Então** o sistema deve exibir o formulário de criação de projeto
- **Dado que** preenchi os campos "Nome do Projeto" e “Descrição”  
  **Quando** eu clicar em "Salvar"  
  **Então** o projeto deve ser criado, salvo no banco de dados e exibido na lista de projetos
- **Dado que** o nome do projeto já exista  
  **Quando** eu tentar salvar  
  **Então** o sistema deve impedir a criação e mostrar mensagem de erro "Nome já em uso"
- **Dado que** eu não preencher o campo obrigatório "Nome do Projeto"  
  **Quando** eu clicar em "Salvar"  
  **Então** deve aparecer validação inline "Este campo é obrigatório"
