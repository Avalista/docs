### 📄 Contrato (Request Body) – POST `/screens`

**Content-Type:** `application/json`

| Campo         | Tipo     | Obrigatório | Descrição             |
| ------------- | -------- | ----------- | --------------------- |
| `title`       | `string` | Sim         | Título da tela        |
| `description` | `string` | Sim         | Descrição da tela     |
| `screenshot`  | `string` | Sim         | URL da imagem da tela |
| `projectId`   | `string` | Sim         | ID do projeto (UUID)  |

#### Validações

- `title`, `description` e `screenshot` devem ser strings não vazias.
- `projectId` deve ser um UUID válido.

---

### 📄 Contrato (Response Body) – POST `/screens`

**Content-Type:** `application/json`

#### 🔁 Resposta: `201 Created`

```json
{
  "id": "string", // ID gerado da tela (UUID ou string)
  "title": "string", // Título da tela
  "description": "string", // Descrição da tela
  "screenshot": "string", // URL da imagem da tela
  "projectId": "string" // ID do projeto relacionado (UUID)
}
```

#### 1. 🔴 Ausência do campo `title`

```json
{
  "statusCode": 400,
  "message": ["title é obrigatório"],
  "error": "Bad Request"
}
```

#### 2. 🔴 Ausência do campo `description `

```json
{
  "statusCode": 400,
  "message": ["description  é obrigatório"],
  "error": "Bad Request"
}
```

#### 3. 🔴 Ausência do campo `screenshot `

```json
{
  "statusCode": 400,
  "message": ["screenshot  é obrigatório"],
  "error": "Bad Request"
}
```

#### 4. 🔴 Ausência do campo `projectId `

```json
{
  "statusCode": 400,
  "message": ["projectId  é obrigatório"],
  "error": "Bad Request"
}
```
