# Documento de Visão

## Histórico de Revisões

| Data       | Versão | Descrição      | Autores                                         |
| ---------- | ------ | -------------- | ----------------------------------------------- |
| 02/12/2024 | 1.0    | Versão Inicial | Alessandro Souza, Ariane Silveira, Cibele Diniz |

---

## Objetivo

O principal objetivo da aplicação é fornecer uma plataforma onde usuários possam avaliar projetos de software e interfaces gráficas com base nas heurísticas de usabilidade. A aplicação permitirá a criação e o gerenciamento de projetos com foco na análise de usabilidade, incentivando a melhoria contínua de interfaces digitais e promovendo uma abordagem colaborativa para identificar problemas e propor melhorias.

---

## Descrição do Problema

**O problema de:**
Falta de uma plataforma específica para avaliar interfaces gráficas com base em heurísticas de usabilidade.

**Afetando:**
Equipes de desenvolvimento e designers que precisam identificar e corrigir problemas de usabilidade de forma sistemática.

**Cujo impacto é:**
Dificuldade em documentar violações de heurísticas, propor melhorias e priorizar correções de maneira organizada.

**Uma boa solução seria:**
Uma aplicação web que permita a avaliação de projetos, incluindo upload de imagens, classificação de problemas, descrição de melhorias e análise da gravidade e esforço necessário para resolvê-los.

---

## Descrição dos Usuários

| Nome          | Descrição                                                     | Responsabilidade                                                             |
| ------------- | ------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Avaliador     | Especialista ou membro da equipe                              | Avaliar os projetos com base nas heurísticas, fornecer feedback e sugestões. |
| Administrador | Gestor do sistema                                             | Gerenciar usuários, projetos e configurações do sistema.                     |
| Cliente       | Usuário que vai receber a avaliação e o feedback do avaliador | Criar conta; Acessar relatórios;                                             |

---

## Descrição do Ambiente dos Usuários

Os usuários poderão acessar a aplicação por meio de qualquer dispositivo com acesso à internet e um navegador atualizado. O sistema será responsivo, suportando acesso em dispositivos móveis e desktops.

---

## Principais Necessidades dos Usuários

1. **Avaliadores:** Precisam de uma ferramenta que permita identificar e documentar violações de heurísticas com facilidade, incluindo o upload de imagens e a descrição de melhorias.
2. **Administradores:** Necessitam gerenciar usuários, projetos e manter a integridade das informações cadastradas.
3. **Cliente:** Precisam acessar relatórios claros sobre a análise de usabilidade, incluindo detalhes de violações e propostas de melhorias.

---

## Alternativas Concorrentes

1. **Heuristic Evaluation Tool (HET):**

   - Pontos positivos: Interface intuitiva, suporte para classificação de gravidade.
   - Pontos negativos: Limitações na personalização de projetos e ausência de recursos para upload de imagens.

2. **Usability Hub:**

   - Pontos positivos: Ferramentas para teste de usabilidade, ampla base de usuários.
   - Pontos negativos: Foco em testes gerais, não específico para heurísticas.

---

## Visão Geral do Produto

A aplicação será uma ferramenta web para avaliação de usabilidade com foco em heurísticas. Permitíra aos usuários:

- Criar e gerenciar projetos, incluindo nome, descrição e logotipo.
- Adicionar casos de uso e selecionar imagens para avaliação.
- Identificar violações de princípios, classificá-las e propor melhorias.
- Gerar relatórios detalhados com base nas análises realizadas.

---

## Requisitos Funcionais

| Código | Nome                          | Descrição                                                                                  | Prioridade |
| ------ | ----------------------------- | ------------------------------------------------------------------------------------------ | ---------- |
| F01    | Cadastro de Projetos          | Criar, editar e excluir projetos com nome, descrição e logotipo.                           | Essencial  |
| F02    | Gerenciamento de Casos de Uso | Adicionar e gerenciar casos de uso associados a projetos.                                  | Essencial  |
| F03    | Upload de Imagens             | Fazer upload de imagens para cada caso de uso.                                             | Essencial  |
| F04    | Classificação de Heurísticas  | Associar violações de heurísticas a imagens, com descrição e proposta de melhoria.         | Essencial  |
| F05    | Avaliação de Gravidade        | Classificar a gravidade do problema identificado.                                          | Importante |
| F06    | Avaliação de Esforço          | Estimar o esforço necessário para corrigir o problema.                                     | Importante |
| F07    | Relatórios                    | Gerar relatórios detalhados por projeto, caso de uso e imagem.                             | Desejável  |
| F08    | Autenticação                  | Efetuar login e cadastro de usuários com diferentes permissões (Administrador, Avaliador). | Essencial  |

---

## Requisitos Não-Funcionais

| Código | Nome                      | Descrição                                                                          | Categoria       | Classificação |   |
| ------ | ------------------------- | ---------------------------------------------------------------------------------- | --------------- | ------------- | - |
| NF01   | Segurança dos Dados       | As informações armazenadas devem ser protegidas com autenticação e criptografia.   | Segurança       | Obrigatório   |   |
| NF02   | Tempo de Resposta         | O sistema deve carregar os projetos e as demais  em menos de 1 minuto.             | Desempenho      | Desejável     |   |
| NF03   | Ambiente de funcionamento | O sistema deve funcionar nos navegadores mais usados, como Chrome, Firefox e Edge. | Desenvolvimento | Essencial     |   |
|        |                           |                                                                                    |                 |               |   |

