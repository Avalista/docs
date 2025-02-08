# Documento de Visão

## Histórico de Revisões

| Data       | Versão | Descrição      | Autores                                         |
| ---------- | ------ | -------------- | ----------------------------------------------- |
| 02/12/2024 | 1.0    | Versão Inicial | Radmila Gama |
| 19/12/2024 | 1.1    | Revisão do Escopo e dos Usuários | Radmila Gama |
| 01/02/2025 | 2.0    | Alteração no escopo e na ideia do projeto  | Radmila Gama |

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
| Avaliador     | Alunos desenvolvedores e designers.                           | Avaliar os projetos com base nas heurísticas, fornecer feedback e sugestões. |
| Administrador | Gestor do sistema                                             | Gerenciar usuários, projetos e configurações do sistema.                     |

---

## Descrição do Ambiente dos Usuários

Os usuários poderão acessar a aplicação por meio de qualquer dispositivo com acesso à internet e um navegador atualizado. O sistema será com foco no desktop, mas terá uma versãon responsiva para celular, na qual mostrará apenas os relatórios dos projetos.

---

## Principais Necessidades dos Usuários

1. **Avaliadores:** Precisam de uma ferramenta que permita identificar e documentar violações de heurísticas com facilidade, incluindo o upload de imagens e a descrição de melhorias. Além disso, terão acesso a métricas detalhadas sobre as violações registradas, permitindo uma análise mais precisa e facilitando a priorização e resolução dos problemas identificados. Essas métricas ajudarão a compreender a recorrência das falhas e a eficiência das soluções aplicadas ao longo do tempo.
2. **Administradores:** Necessitam gerenciar usuários, projetos e manter a integridade das informações cadastradas.

---

## Alternativas Concorrentes

1. [Heurix | A free heuristic evaluation tool]([url](https://www.heurix.io))
Trata-se de uma ferramenta utilizada para avaliar telas por meio de questionários. A avaliação começa imediatamente após o login, quando o usuário é solicitado a criar um projeto. Em seguida, as perguntas são iniciadas, organizadas em diferentes categorias: Primeiras Impressões (First Impressions), Navegação do Site (Site Navigation), Informações (Information), Confiança e Persuasão (Trust and Persuasion), Interação (Interaction), Formulários (Forms) e Pesquisa (Search).

<img src="heurix-home.png">

Essa aplicação não segue nenhuma lista de diretrizes ou heurísticas de usabilidade como referência, baseando-se apenas em perguntas objetivas com respostas limitadas a "Yes" (Sim), "Room to Improve" (Tem como melhorar), "No" (Não) e "Not Applicable" (Não se aplica). Isso significa que não há um conjunto estruturado de princípios reconhecidos, como as heurísticas de Nielsen ou as diretrizes da ISO, para fundamentar a avaliação.


A ausência de um referencial teórico claro pode comprometer a profundidade da análise, tornando-a subjetiva e inconsistente. Sem diretrizes bem estabelecidas, os avaliadores podem interpretar os critérios de diferentes formas, levando a conclusões variadas e menos confiáveis. Além disso, uma lista de heurísticas ajudaria a garantir que aspectos essenciais da usabilidade sejam cobertos de maneira sistemática, enquanto um modelo de perguntas objetivas pode deixar lacunas importantes na avaliação. Isso pode resultar em diagnósticos superficiais e recomendações imprecisas para melhorias, reduzindo a eficácia do processo de avaliação.


Outra limitação da aplicação é que o questionário é aplicado ao sistema como um todo, em vez de ser direcionado a casos de uso específicos. Isso significa que as perguntas são formuladas de maneira genérica, avaliando o sistema de forma global, sem considerar fluxos específicos de interação. Como consequência, uma determinada funcionalidade, como a tela inicial, pode atender corretamente aos critérios avaliados, enquanto uma página interna pode apresentar problemas que passam despercebidos. Essa abordagem ampla e pouco detalhada torna a ferramenta ineficiente para a avaliação de interfaces, pois não identifica com precisão os pontos críticos de usabilidade em diferentes partes do sistema.


Apesar dos problemas anteriormente citados, o Heurix permite que o usuário adicione uma imagem e uma nota por cada pergunta. A inserção desses dados contribui para os resultados obtidos pelo avaliador, o que, consequentemente, colabora para a resolução do problema encontrado na interface. Outro ponto positivo encontrado na aplicação é mostrado quando o avaliador termina de responder todas as perguntas e a interface mostra um quadro com a pontuação sobre as perguntas respondidas. 

2. Extensão UX Check

A extensão não funciona mais, porém a página de detalhes dela apresenta fotos e uma descrição de como ela funciona. A extensão possui uma ferramenta para o usuário selecionar a parte da tela que possui erros, a aplicação dá a entender que essa extensão funciona para qualquer website e que essa ferramenta tira um print da tela completa exibida para o usuário quando ele seleciona a parte que possui erros. 

A UX Check utiliza a lista de diretrizes de Nielsen e quando o usuário seleciona a parte com erros, uma janela aparece para que ele selecione qual heurística representa aquele erro. Para complementar a avaliação, o usuário também precisa informar a gravidade do problema, ele pode deixar notas e comentários de recomendações para que o problema seja resolvido.

Por fim, após a avaliação, é possível que o usuário baixe a avaliação como um arquivo do tipo docs.

<img src=”uxcheck.jpg”>

## Visão Geral do Produto

A aplicação será uma ferramenta web para avaliação de usabilidade com foco em heurísticas. Permitíra aos usuários:

- Criar e gerenciar projetos, incluindo nome, descrição e logotipo.
- Adicionar casos de uso ao projeto e selecionar imagens desses casos de uso para avaliação.
- Identificar violações de princípios, identificar a heuristica ferida, selecionar o esforço e propor melhorias.
- Gerar métricas relatórios detalhados com base nas análises realizadas.

---

## Requisitos Funcionais

| Código | Nome                          | Descrição                                                                                         | Prioridade |
| ------ | ----------------------------- | ------------------------------------------------------------------------------------------------- | ---------- |
| F08    | Autenticação                  | Efetuar login e cadastro de usuários com diferentes permissões (Administrador, Avaliador).        | Essencial  |
| F02    | Cadastro de Projetos          | Criar, editar e excluir projetos com nome, descrição e logotipo e se tiver, o nome do cliente.    | Essencial  |
| F03    | Gerenciamento de Casos de Uso | Adicionar e gerenciar casos de uso associados a projetos.                                         | Essencial  |
| F04    | Upload de Imagens             | Fazer upload de imagens para cada caso de uso.                                                    | Essencial  |
| F05    | Classificação de Heurísticas  | Associar violações encontradas nas imagens com as diretrizes da lista de Matos e Freire           | Essencial  |
| F06    | Avaliação de Gravidade        | Classificar a gravidade do problema identificado.                                                 | Essencial  |
| F07    | Avaliação de Esforço          | Estimar o esforço necessário para corrigir o problema.                                            | Essencial  |
| F08    | Proposta de Melhoria          | O avaliador precisa descrever como resolver aquele problema.                                      | Essencial  |
| F09    | Relatórios                    | Gerar relatórios detalhados por projeto, caso de uso e imagem.                                    | Desejável  |

---

## Requisitos Não-Funcionais

| Código | Nome                      | Descrição                                                                          | Categoria       | Classificação |   |
| ------ | ------------------------- | ---------------------------------------------------------------------------------- | --------------- | ------------- | - |
| NF01   | Segurança dos Dados       | As informações armazenadas devem ser protegidas com autenticação e criptografia.   | Segurança       | Obrigatório   |   |
| NF02   | Tempo de Resposta         | O sistema deve carregar os projetos e as demais  em menos de 1 minuto.             | Desempenho      | Desejável     |   |
| NF03   | Ambiente de funcionamento | O sistema deve funcionar nos navegadores mais usados, como Chrome, Firefox e Edge. | Desenvolvimento | Essencial     |   |
