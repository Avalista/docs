# Caso de Uso: Avaliação de Heurísticas no Sistema

## Nome:
SEM NOME

## Pré-condição:
- O usuário deve estar autenticado no sistema.
- O ponto de avaliação deve estar previamente cadastrado.

## Pós-condição em caso de sucesso:
- A avaliação é registrada no banco de dados.
- O feedback do usuário é exibido como mensagem de sucesso.
- O resultado é atualizado no dashboard de métricas em tempo real.

## Pós-condição em caso de falha:
- O sistema exibe uma mensagem de erro explicativa.
- Nenhuma alteração é feita no banco de dados.

## Ator principal:
- Usuário Avaliador

## Outros atores:
- Administrador do sistema (para monitorar avaliações).

## Evento disparador:
- O usuário seleciona o botão "Avaliar" no ponto de interesse desejado.

## Fluxo normal:
1. O usuário acessa o painel de avaliação.
2. O sistema exibe os critérios e as opções de avaliação disponíveis.
3. O usuário seleciona o número de estrelas e insere um comentário (opcional).
4. O usuário clica no botão "Enviar Avaliação".
5. O sistema valida os dados inseridos.
6. O sistema registra a avaliação no banco de dados.
7. O sistema exibe uma mensagem de sucesso para o usuário.
8. O sistema atualiza o dashboard de métricas.

## Fluxos alternativos e de exceção:
- **Passo 5:** Caso os dados inseridos sejam inválidos (exemplo: comentário excedendo limite de caracteres), o sistema exibe uma mensagem de erro e solicita correção.
- **Passo 6:** Se houver falha na conexão com o banco de dados, o sistema salva a avaliação localmente em cache para envio posterior.
- **Passo 7:** Se o envio da avaliação falhar, o sistema exibe uma mensagem informando o problema e orienta o usuário a tentar novamente.

## Extensões:
- **Avaliação detalhada por categoria:** Após o passo 2, o usuário pode acessar critérios específicos como "Usabilidade", "Acessibilidade", "Estética" para avaliações mais detalhadas.
- **Compartilhamento de avaliações:** Após o passo 8, o usuário pode compartilhar a avaliação via redes sociais.

## Informações relacionadas:
- **Frequência:** Estima-se que os usuários realizem avaliações ao término de cada interação principal.
- **Desempenho:** Tempo de resposta esperado de menos de 2 segundos entre o envio da avaliação e a confirmação do registro.
- **Relação com outros casos de uso:** Está diretamente relacionado ao caso de uso de Gerenciamento de Pontos de Interesse e Dashboard de Métricas.
