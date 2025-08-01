### HU001 - Criar conta

---

**Como** usuário não autenticado

**Eu quero** criar minha conta

**Para que** eu possa me autenticar na plataforma

---

### Critérios de Aceitação

- O formulário de cadastro deve conter **nome**, **e‑mail**, **senha** e **confirmar senha** como campos obrigatórios.
- O campo **e‑mail** deve aceitar apenas endereços em formato válido (por exemplo, `usuario@exemplo.com`).
- O campo **e‑mail** deve ser único, não podendo utilizar um email já cadastrado, conforme [RN001](../../regras_de_negocio/read.md#-rn001---e-mail-único-por-conta).
- Se o **e‑mail** já estiver cadastrado, deve ser exibida uma mensagem informando "E‑mail já em uso" e o cadastro não deve ser concluído.
- O campo **senha** deve ter no mínimo 8 caracteres e incluir pelo menos uma letra maiúscula, uma letra minúscula e pelo menos um número.
- Os campos **senha** e **confirmar senha** devem coincidir.
- Ao submeter o formulário com dados inválidos, devem ser exibidas mensagens de erro.
- O sistema deve redirecionar para a tela de login.
