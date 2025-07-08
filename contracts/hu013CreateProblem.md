### 📄 Contrato (Request Body) – POST `/evaluations/initialize`

**Content-Type:** `application/json`

| Campo                    | Tipo               | Obrigatório | Descrição                                                                       |
| ------------------------ | ------------------ | ----------- | ------------------------------------------------------------------------------- |
| `screenId`               | `string`           | Sim         | ID da tela onde o problema foi identificado. Deve ser um uuid e do tipo string. |
| `heuristicId`            | `string`           | Sim         | ID da heurística aplicada. Deve ser um uuid e do tipo string.                   |
| `description`            | `string`           | Sim         | Descrição do problema identificado na tela.                                     |
| `screenshots`            | `array de strings` | Sim         | Lista de URLs das capturas de tela que ilustram o problema identificado.        |
| `improvementSuggestions` | `string`           | Sim         | Sugestões de melhorias para o problema identificado.                            |
| `severity`               | `string`           | Sim         | Severidade do problema. Pode ser LOW, MEDIUM, ou HIGH.                          |
| `effort`                 | `string`           | Sim         | Esforço necessário para resolver o problema. Pode ser LIGHT, MEDIUM, ou HIGH    |
| `priority`               | `boolean`          | Sim         | Indica se o problema deve ser tratado com alta prioridade.                      |

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
              "problems": [
                {
                  "id": "e6974e3e-81a7-4932-a2f6-9a0788b8d5b1",
                  "description": "dificuldade e entender e ler o texto",
                  "screenshot": ["print"],
                  "improvementSuggestions": "Diminuir o brilho e melhorar tudo",
                  "severity": "HIGH",
                  "effort": "HIGH",
                  "resolvedAt": null,
                  "priority": false
                },
                {
                  "id": "22eeda7b-654d-44c1-bbad-9ae99ede8c99",
                  "description": "dificuldade e entender e ler o texto",
                  "screenshot": ["print"],
                  "improvementSuggestions": "Diminuir o brilho e melhorar tudo",
                  "severity": "HIGH",
                  "effort": "HIGH",
                  "resolvedAt": null,
                  "priority": false
                }
              ]
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

#### 1. 🔴 Ausência do campo `screenId`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": [
    "screenId must be a UUID",
    "screenId should not be empty",
    "screenId must be a string"
  ],
  "error": "Bad Request"
}
```

#### 2. 🔴 Ausência do campo `heuristicId`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": [
    "heuristicId must be a UUID",
    "heuristicId should not be empty",
    "heuristicId must be a string"
  ],
  "error": "Bad Request"
}
```

#### 3. 🔴 Ausência do campo `description`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["description should not be empty"],
  "error": "Bad Request"
}
```

#### 4. 🔴 Ausência do campo `screenshots`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["screenshots must be an array of valid URLs"],
  "error": "Bad Request"
}
```

#### 5. 🔴 Ausência do campo `severity`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": [
    "severity must be one of the following values: LOW, MEDIUM, HIGH"
  ],
  "error": "Bad Request"
}
```

#### 6. 🔴 Ausência do campo `effort`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": [
    "effort must be one of the following values: LIGHT, MEDIUM, HEAVY"
  ],
  "error": "Bad Request"
}
```

#### 7. 🔴 Ausência do campo `priority`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["priority must be a boolean"],
  "error": "Bad Request"
}
```

#### 8. 🔴 Ausência do campo `improvementSuggestions`

**Resposta:**

```json
{
  "statusCode": 400,
  "message": ["improvementSuggestions should not be empty"],
  "error": "Bad Request"
}
```
