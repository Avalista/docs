### 📄 Contrato (Request Body) – POST `/evaluations/initialize`

**Content-Type:** `application/json`

| Campo       | Tipo     | Obrigatório | Descrição                                                       |
| ----------- | -------- | ----------- | --------------------------------------------------------------- |
| `projectId` | `string` | Sim         | ID do projeto a ser avaliado. Deve ser um uuid, deve ser string |

#### 🔴 Exemplo de resposta de sucesso

```json
{
  "project": {
    "id": "cd90d1cf-a817-4bc1-b36c-a1293cc5275b",
    "name": "string",
    "description": "string"
  },
  "evaluator": {
    "id": "594295ae-f2c0-4fff-9d93-b80679518ef5",
    "name": "Ramon",
    "email": "Ramon@email.com"
  },
  "evaluationSession": {
    "id": "335e2de8-d1b2-4f07-8603-ede06b160913",
    "startedAt": "2025-07-03T04:21:03.466Z",
    "finishedAt": null,
    "status": "IN_PROGRESS",
    "evaluationItems": [
      {
        "id": "91a64dcd-874c-4481-925e-06a4787e2d17",
        "status": "NOT_REVIEWED",
        "reviewedAt": null,
        "screen": {
          "id": "cf0782ba-1966-4571-8c8e-365a1c4b378e",
          "title": "Tela de Cadastro",
          "description": "Esta tela é responsável por cadastrar novos pets",
          "screenshot": "https://lupapet.com.br/AppPets/img/how_work1.png",
          "category": {
            "id": "b4a6b998-29c3-4913-ab67-38595200e54e",
            "name": "ASPECTOS FUNCIONAIS (AF)",
            "color": "#ccc",
            "heuristic": {
              "id": "2b39797c-3304-4117-8fce-26952821cef1",
              "name": "Funcionalidade",
              "code": "AF1",
              "problems": []
            }
          }
        }
      },
      {
        "id": "bec48ad7-0197-4758-8adf-dfc214a55559",
        "status": "NOT_REVIEWED",
        "reviewedAt": null,
        "screen": {
          "id": "7a2173b1-7021-4517-934a-aed23273d9bc",
          "title": "Tela de Login",
          "description": "Esta tela é responsável pela autenticação na plataforma de dogs",
          "screenshot": "https://img.freepik.com/vetores-gratis/modelo-de-pagina-de-aterrissagem-de-login-de-espaco_23-2148260289.jpg?semt=ais_hybrid&w=740",
          "category": {
            "id": "b4a6b998-29c3-4913-ab67-38595200e54e",
            "name": "ASPECTOS FUNCIONAIS (AF)",
            "color": "#ccc",
            "heuristic": {
              "id": "2b39797c-3304-4117-8fce-26952821cef1",
              "name": "Funcionalidade",
              "code": "AF1",
              "problems": []
            }
          }
        }
      }
    ]
  }
}
```

#### 1. 🔴 Ausência do campo `projectId`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": [
    "projectId must be a UUID",
    "projectId should not be empty",
    "projectId must be a string"
  ],
  "error": "Bad Request"
}
```

#### 2. 🔴 Projeto não encontrado

Caso o projectId não exista

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["Projeto não encontrado"],
  "error": "Bad Request"
}
```

#### 3. 🔴 Ausência de telas para o projeto

Caso o projeto não tenha telas cadastradas:

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["Não há telas cadastradas para esse projeto."],
  "error": "Bad Request"
}
```

#### 4. 🔴 Ausência de heurísticas

Caso não existam heurísticas para o projeto:

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["Não há heurísticas."],
  "error": "Bad Request"
}
```

#### 4. 🔴 Ja tem avaliação individual

**Resposta:**

```json
{
  "message": "Já existe uma sessão de avaliação para este usuário neste projeto.",
  "error": "Bad Request",
  "statusCode": 400
}
```
