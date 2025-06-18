### 📄 Contrato (Request Body) – POST `/evaluators`

**Content-Type:** `multipart/form-data`

| Campo              | Tipo         | Obrigatório | Descrição                          |
| ------------------ | ------------ | ----------- | ---------------------------------- |
| `name`             | `string`     | Sim         | Nome completo do avaliador         |
| `email`            | `string`     | Sim         | Email válido                       |
| `password`         | `string`     | Sim         | Senha para acesso                  |
| `confirmPassoword` | `string`     | Sim         | Para acesso confirmar a senha      |
| `avatar`           | `file` (img) | Não         | Imagem de avatar (JPEG, PNG, etc.) |

#### 1. 🔴 Ausência do campo `name`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["name é obrigatório"],
  "error": "Bad Request"
}
```

#### 2. 🔴 Ausência do campo `email`

```json
{
  "statusCode": 400,
  "message": ["email é obrigatório"],
  "error": "Bad Request"
}
```

#### 3. 🔴 Ausência do campo `password`

```json
{
  "statusCode": 400,
  "message": ["password é obrigatório"],
  "error": "Bad Request"
}
```

#### 4. 🔴 Ausência do campo `confirmPassword`

```json
{
  "statusCode": 400,
  "message": ["confirmPassword é obrigatório"],
  "error": "Bad Request"
}
```

#### 5. 🔴 formato inválido para `email`

```json
{
  "statusCode": 400,
  "message": ["email deve ser um endereço de e-mail válido"],
  "error": "Bad Request"
}
```
