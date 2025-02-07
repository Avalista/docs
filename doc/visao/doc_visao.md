# Documento de Visão

## Histórico de Revisões

| Data       | Versão | Descrição      | Autores                                         |
| ---------- | ------ | -------------- | ----------------------------------------------- |
| 02/12/2024 | 1.0    | Versão Inicial | Radmila Gama |
| 19/12/2024 | 1.1    | Revisão do Escopo e dos Usuários | Radmila Gama |
| 01/02/2025 | 1.2    | Correções do texto com os comentários da orientadora.  | Radmila Gama |

---

## Objetivo

O principal objetivo da aplicação é fornecer uma plataforma onde alunos possam avaliar interfaces gráficas com base nas diretrizes de design, utilizando como base a Lista Eureca, criada e documentada por Silvia Matos, Marília Aranha, Isis Duarte e Ramon Vieira. A aplicação permitirá a criação e o gerenciamento de projetos com foco na avaliação das interfaces gráficas, incentivando a melhoria contínua delas e promovendo a qualidade e sistematização na hora de identificar problemas. Além de ser uma ferramenta para apoio computacional a identificação de problemas, é também idealizada para permitir o registro da proposta de solução para as diretrizes que foram feridas de acordo com a avaliação, além de relatar a gravidade do problema detectado e o esforço para que o mesmo seja resolvido. Com esses dados, a aplicação irá gerar relatório final da avaliação com uso de gráficos e métricas para o avaliador.
---

## Descrição do Problema

**O problema de:**
Falta de uma plataforma específica para avaliar interfaces gráficas com base em heurísticas de usabilidade.

**Afetando:**
Alunos de TADS que precisam identificar e corrigir problemas de design de forma sistemática.

**Cujo impacto é:**
Dificuldade em documentar violações de heurísticas, propor melhorias e priorizar correções de maneira organizada.

**Uma boa solução seria:**
Uma aplicação web que permita a avaliação de projetos, incluindo upload de imagens, classificação de problemas, descrição de melhorias e análise da gravidade e esforço necessário para resolvê-los.

---

## Descrição dos Usuários

| Nome          | Descrição                                                     | Responsabilidade                                                             |
| ------------- | ------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Avaliador     | Especialista ou membro da equipe                              | Avaliar os projetos com base nas heurísticas, fornecer feedback e sugestões. |
| Cliente       | Usuário que vai receber a avaliação e o feedback do avaliador | Criar conta; Acessar relatórios;                                             |
| Administrador | Gestor do sistema                                             | Gerenciar usuários, projetos e configurações do sistema.                     |

---

## Descrição do Ambiente dos Usuários

Os usuários poderão acessar a aplicação por meio de qualquer dispositivo com acesso à internet e um navegador atualizado. O sistema será com foco no desktop, mas terá uma versãon responsiva para celular, na qual mostrará apenas os relatórios dos projetos.

---

## Principais Necessidades dos Usuários

1. **Avaliadores:** Precisam de uma ferramenta que permita identificar e documentar violações de heurísticas com facilidade, incluindo o upload de imagens e a descrição de melhorias.
2. **Cliente:** Precisam acessar relatórios claros sobre a análise de usabilidade, incluindo detalhes de violações e propostas de melhorias.
3. **Administradores:** Necessitam gerenciar usuários, projetos e manter a integridade das informações cadastradas.

---

## Alternativas Concorrentes


1. Lyssna
2. Heurix | A free heuristic evaluation tool
Trata-se de uma ferramenta utilizada para avaliar telas por meio de questionários. A avaliação começa imediatamente após o login, quando o usuário é solicitado a criar um projeto. Em seguida, as perguntas são iniciadas, organizadas em diferentes categorias: Primeiras Impressões (First Impressions), Navegação do Site (Site Navigation), Informações (Information), Confiança e Persuasão (Trust and Persuasion), Interação (Interaction), Formulários (Forms) e Pesquisa (Search).


## Visão Geral do Produto

A aplicação será uma ferramenta web para avaliação de usabilidade com foco em heurísticas. Permitíra aos usuários:

- Criar e gerenciar projetos, incluindo nome, descrição e logotipo.
- Adicionar casos de uso ao projeto e selecionar imagens para avaliação.
- Identificar violações de princípios, identificar a heuristica ferida, selecionar o esforço e propor melhorias.
- Gerar relatórios detalhados com base nas análises realizadas.

---

## Requisitos Funcionais

| Código | Nome                          | Descrição                                                                                  | Prioridade |
| ------ | ----------------------------- | ------------------------------------------------------------------------------------------ | ---------- |
| F01    | Cadastro de Projetos          | Criar, editar e excluir projetos com nome, descrição e logotipo e se tiver, o nome do cliente.                           | Essencial  |
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

