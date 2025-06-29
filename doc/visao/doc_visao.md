# Documento de Visão - Avalista

---

## Histórico de Revisões

| Data       | Versão | Descrição                          | Autores                     |
| :--------- | :----- | :--------------------------------- | :-------------------------- |
| 02/12/2024 | 1.0    | Versão Inicial                     | Radmila Gama                |
| 19/12/2024 | 1.1    | Revisão do Escopo e dos Usuários   | Radmila Gama                |
| 01/02/2025 | 2.0    | Alteração no escopo e na ideia     | Radmila Gama                |
| 28/04/2025 | 2.1    | Adição do método Eureca            | Radmila Gama e Ramon Vieira |
| 29/06/2025 | 3.0    | Versão final alinhada ao TCC       | Radmila Gama e Ramon Vieira |

---

## Objetivo
O objetivo do projeto Avalista é desenvolver uma plataforma web que transforme a prática da avaliação de interfaces por inspeção em uma experiência engajadora, sistemática e pedagógica. Utilizando como base a Lista Eureca 2024, a ferramenta visa combater a resistência e a baixa motivação dos estudantes de tecnologia em relação à avaliação heurística. A plataforma foi idealizada para não apenas organizar o processo de identificação de problemas, mas também para incorporar elementos de gamificação e uma identidade visual forte, criando um ambiente que incentiva a aprendizagem e a aplicação de boas práticas de design de forma dinâmica e eficiente.

---

## Descrição do Problema

**O problema de:**
O processo de avaliação de interfaces por inspeção, embora crucial, é frequentemente percebido por estudantes de tecnologia como uma atividade tediosa, subjetiva e desmotivadora.

**Afetando:**
Estudantes do curso de Análise e Desenvolvimento de Sistemas (TADS) e áreas afins, que precisam desenvolver um olhar crítico e sistemático sobre design de interfaces.

**Cujo impacto é:**
A baixa adesão às atividades de avaliação, a dificuldade em aplicar as diretrizes heurísticas de forma consistente e a perda de uma valiosa oportunidade de aprendizado prático, resultando em projetos com menor qualidade de usabilidade.

**Uma boa solução seria:**
Uma plataforma web gamificada, o Avalista, que organiza e automatiza o processo com base na Lista Eureca, transformando uma tarefa repetitiva em uma experiência de aprendizagem dinâmica e estruturada, com geração de relatórios e métricas para apoiar a análise.

---

## Descrição dos Usuários

| Nome        | Descrição                       | Responsabilidade                                                     |
| :---------- | :------------------------------ | :------------------------------------------------------------------- |
| Avaliador   | Alunos desenvolvedores e designers. | Avaliar os projetos com base nas heurísticas, fornecer feedback e sugestões. |
| Administrador| Gestor do sistema                 | Gerenciar usuários, projetos e configurações do sistema.           |

---

## Descrição do Ambiente dos Usuários
Os usuários poderão acessar a aplicação por meio de qualquer dispositivo com acesso à internet e um navegador atualizado. O sistema será com foco no desktop, mas, para planos futuros, terá uma versão mobile apenas com as métricas dos projetos.

---

## Principais Necessidades dos Usuários
**Avaliadores:** Precisam de uma ferramenta que permita identificar e documentar violações de heurísticas com facilidade, incluindo o upload de imagens e a descrição de melhorias. Além disso, terão acesso a métricas detalhadas sobre as violações registradas, permitindo uma análise mais precisa e facilitando a priorização e resolução dos problemas identificados.

**Administradores:** Necessitam gerenciar usuários, projetos e manter a integridade das informações cadastradas.

---

## Alternativas Concorrentes
Existem ferramentas que auxiliam na avaliação de interfaces, servindo como referência para o Avalista:

- **Heurix:** Uma ferramenta web que guia o avaliador por meio de um questionário. Embora seja funcional para gerar relatórios, sua principal limitação é a ausência de um foco pedagógico e de elementos de engajamento, além da rigidez por não permitir o uso de listas de heurísticas personalizadas como a Lista Eureca.

- **Extensão UX Check:** Uma extensão de navegador (atualmente descontinuada) que permitia analisar qualquer website, associando problemas às 10 heurísticas de Nielsen. Sua principal inspiração para o Avalista foi a interação de selecionar uma parte da tela, anotar o problema e gerar um relatório, mostrando a viabilidade de uma avaliação contextual e direta na interface.

Ambas as ferramentas validam a necessidade de soluções na área, mas nenhuma atende à necessidade específica de um ambiente de aprendizagem gamificado e adaptado a um contexto acadêmico específico como o do IFRN.

---

## Visão Geral do Produto
O Avalista é uma plataforma web projetada para ser a ferramenta padrão de apoio ao ensino e à prática da avaliação heurística de interfaces no IFRN e, futuramente, para um público mais amplo. A visão do produto é criar um ecossistema onde a avaliação deixa de ser uma obrigação e se torna uma atividade de aprendizado interativa.

A plataforma permitirá que usuários (avaliadores) criem e gerenciem seus projetos de avaliação, cadastrem as telas a serem analisadas e, no ciclo completo, registrem as violações das diretrizes da Lista Eureca de forma estruturada. A ferramenta fornecerá feedback visual e, através de mecânicas de gamificação como emblemas e estatísticas, buscará engajar e motivar o usuário a aprimorar suas habilidades de avaliação. Para os administradores, a plataforma oferecerá controle sobre as diretrizes e categorias, garantindo a integridade e a evolução do conteúdo. O resultado final para o avaliador será um relatório claro e objetivo, que não apenas documenta os problemas, mas também facilita a tomada de decisão para as melhorias.

---

## Requisitos Funcionais

**Prioridade (Metodologia MoSCoW):**
1.  **Essencial** (Must Have)
2.  **Importante** (Should Have)
3.  **Desejável** (Could Have)
4.  **Opcional** (Won't Have)

| Código | Nome                            | Descrição                                                                                                                                     | Prioridade  |
| :----- | :------------------------------ | :---------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| F01    | Autenticação                    | O sistema deve permitir efetuar login e cadastro de usuários com diferentes permissões (Administrador, Avaliador).                               | Essencial   |
| F02    | Adicionar Projetos              | O sistema deve permitir criar, editar e excluir projetos, contendo nome, descrição e marca gráfica.                                           | Essencial   |
| F03    | Adicionar Casos de Uso          | O sistema deve permitir criar, editar e excluir casos de uso, com nome, descrição e fotos que compõem aquele fluxo.                               | Essencial   |
| F04    | Upload de Imagens               | O sistema deve permitir o upload de imagens para cada caso de uso.                                                                              | Essencial   |
| F05    | Categorizar Violações           | O sistema deve permitir que o avaliador associe violações encontradas às diretrizes da lista de Matos e Freire.                                   | Essencial   |
| F06    | Estimar o Tempo de Resolução    | O sistema deve permitir que o avaliador estime, em horas e minutos, o tempo necessário para corrigir cada problema.                               | Essencial   |
| F07    | Avaliação de Esforço            | O sistema deve permitir que o avaliador estime o esforço necessário para corrigir cada problema.                                                | Essencial   |
| F08    | Proposta de Melhoria            | O sistema deve permitir que o avaliador descreva sugestões de melhorias para resolver os problemas identificados.                                | Essencial   |
| F09    | Avaliação por Múltiplos Avaliadores | O sistema deve permitir que de 3 a 5 avaliadores avaliem o mesmo projeto de forma independente.                                                 | Essencial   |
| F10    | Consolidação de Avaliações      | O sistema deve permitir que os avaliadores, após suas avaliações individuais, consolidem os resultados em uma única avaliação final.             | Essencial   |
| F11    | Identificação de Erros Comuns   | O sistema deve permitir a identificação dos erros que foram encontrados por mais de um avaliador.                                               | Essencial   |
| F12    | Resumo da Avaliação Consolidada | O sistema deve gerar um resumo da avaliação final, indicando os erros consensuais, erros únicos e soluções propostas.                           | Essencial   |
| F13    | Controle de Status da Avaliação | O sistema deve permitir que um projeto tenha status como: "Em Avaliação Individual", "Em Consolidação" e "Avaliação Consolidada".                 | Essencial   |
| F14    | Coleta de Métricas do Projeto   | O sistema deveria coletar métricas detalhadas por projeto (ex: diretrizes mais violadas, tempo/esforço total).                                  | Importante  |
| F15    | Coleta de Métricas do Avaliador | O sistema deveria coletar métricas detalhadas do avaliador (ex: projetos com maior tempo de resolução, categoria mais comum).                     | Importante  |
| F16    | Visualização de Métricas        | O sistema deveria permitir que o avaliador visualize as métricas coletadas em gráficos e classificações.                                        | Importante  |
| F17    | Resolver a Diretriz             | O sistema poderia permitir que o avaliador marque uma diretriz como resolvida e faça upload de uma foto mostrando a resolução.                    | Desejável   |
| F18    | Seção Educacional               | O sistema deveria oferecer uma seção educativa com materiais sobre princípios de design de interfaces.                                          | Opcional    |

---

## Requisitos Não-Funcionais

| Código | Nome                      | Descrição                                                                            | Categoria                | Classificação |
| :----- | :------------------------ | :----------------------------------------------------------------------------------- | :----------------------- | :------------ |
| NF01   | Segurança dos Dados       | As informações armazenadas devem ser protegidas com autenticação e criptografia.       | Segurança                | Obrigatório   |
| NF02   | Tempo de Resposta         | O sistema deve carregar os projetos em menos de 5 segundos.                            | Eficiência e Performance | Desejável     |
| NF03   | Ambiente de funcionamento | O sistema deve funcionar nos navegadores mais usados, como Chrome, Firefox e Edge.     | Compatibilidade          | Essencial     |
