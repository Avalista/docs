### 📄 Contrato (Request Body) – POST `/auth/login`

**Content-Type:** `application/json`

| Campo      | Tipo     | Obrigatório | Descrição        |
| ---------- | -------- | ----------- | ---------------- |
| `email`    | `string` | Sim         | Email do usuário |
| `password` | `string` | Sim         | Senha do usuário |

#### 1. 🔴 Ausência do campo `email`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["email é obrigatório"],
  "error": "Bad Request"
}
```

#### 2. 🔴 Ausência do campo `password`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["password é obrigatório"],
  "error": "Bad Request"
}
```

#### 3. 🔴 Formato inválido para `email`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["email deve ser um endereço de e-mail válido"],
  "error": "Bad Request"
}
```
