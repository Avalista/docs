### 📄 Contrato (Response Body) – GET `/projects`

**Content-Type:** `application/json`

**Descrição:** Retorna uma lista de projetos com suas respectivas informações, membros, telas, sessões e avaliação final (se existir).

#### 🔁 Resposta: `200 OK`

```json
[
  {
    "id": "string",                // ID do projeto (UUID ou string)
    "name": "string",              // Nome do projeto
    "description": "string",       // Descrição do projeto
    "memberships": [
      {
        "evaluatorId": "string",  // ID do avaliador (UUID ou string)
        "projectId": "string",    // ID do projeto (UUID ou string)
        "admin": true,            // Booleano que indica se o avaliador é admin do projeto
        "joinedAt": "string"      // Data ISO 8601 em que o avaliador entrou no projeto
      }
    ],
    "screens": [
      {
        "id": "string",           // ID da tela
        "title": "string",        // Título da tela
        "description": "string",  // Descrição da tela
        "screenshot": "string"    // URL da imagem da tela
      }
    ],
    "sessions": [
      {
        "id": "string",           // ID da sessão
        "startedAt": "string",    // Data ISO 8601 do início da sessão
        "finishedAt": "string",   // Data ISO 8601 do fim da sessão
        "status": "IN_PROGRESS" | "FINISHED"  // Status da sessão
      }
    ],
    "finalEvaluation": {
      "id": "string",             // ID da avaliação final
      "createdAt": "string"       // Data ISO 8601 da criação da avaliação final
    } | null                      // Pode ser nulo se não existir avaliação final
  }
]
```
