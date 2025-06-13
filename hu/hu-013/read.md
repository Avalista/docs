### HU013 - Adicionar problema à avaliação individual

---

**Como** avaliador autenticado

**Eu quero** adicionar um problema à avaliação individual

**Para que** eu possa registrar falhas encontradas em uma tela conforme a categoria e a diretriz selecionada

---

### Critérios de Aceitação

- O avaliador deve conseguir registrar um problema informando:
  1. Descrição clara do problema identificado (Obrigatório);
  2. A diretriz violada;
  3. A gravidade do problema, conforme [RN005](../../regras_de_negocio/read.md#-rn005---níveis-de-gravidade-do-problema)(Obrigatório);
  4. O esforço da alteração, conforme [RN006](../../regras_de_negocio/read.md#-rn006---níveis-de-esforço-da-alteração)(Obrigatório);
  5. O print da tela onde o problema ocorre (Obrigatório);
  6. Sugestão de melhoria (Obrigatório);
  7. Preencher se esse problema tem prioridade (Sendo um booleano, por padrão false).
- Ao submeter o formulário com dados inválidos, devem ser exibidas mensagens de erro.
- Ao submeter o formulário com dados válidos, deve ser exibida mensagem de sucesso "Problema cadastrado com sucesso."
- Ao adicionar o problema a um item(tela, categoria e diretriz) ela recebe REVIEWED_ISSUE para status, conforme [RN010](../../regras_de_negocio/read.md#-rn010---problema-adicionado-para-um-itemtela-categoria-diretriz).
- Após o cadastro bem-sucedido de um problema, o sistema deve limpar todos os campos do formulário e mantê-lo disponível para que o avaliador possa registrar um novo problema imediatamente.
