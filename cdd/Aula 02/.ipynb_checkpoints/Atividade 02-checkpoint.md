### Atividade 02
#### Resolução de problema com pseudocódigo

Problema:
A rede social quer criar uma funcionalidade para identificar usuários que não usam a plataforma há um tempo e enviar uma mensagem para incentivá-los a voltar.

Sugestão de solução:
- Encontrar usuários inativos: Precisamos encontrar os usuários que não fizeram login nos últimos 30 dias.
- Enviar uma mensagem personalizada: Precisamos enviar uma mensagem para esses usuários, convidando-os a voltar a usar a rede social.

#### O Pseudocódigo:

1. Para encontrar usuários inativos:
    - Buscar o registro de usuários na rede
    - Realizar uma varredura: verificar o ultimo acesso de todos os usuários registrados no sistema
    - Se o ultimo acesso tiver ocorrido a mais de 30 dias:
       - marcar o usuário como inativo
    - Caso não, se o ultimo acesso tiver ocorrido a menos de 30 dias:
       - não alterar nada e buscar o próximo usuário

2. Enviar uma mensagem para os usuários inativos:
    - Para cada usuário inativo:
        - Criar uma mensagem personalizada usando o nome de usuário
        - Enviar a mensagem para o usuário usando o e-mail registrado

3. Quando um usuário marcado como inativo realiza login:
    - O sistema o remove do grupo de inativos
  
#### Explicação:
Uma maneira simples de resolver o problema, o pseudocódigo sugere a varredura dentro de uma base de usuários que busca, em meio às suas chaves, a data de seus últimos acessos.
Sob determinadas circunstâncias (último login > 30 dias), o código registra o usuário em um grupo específico - o de inativos - de forma a remover a necessidade de futuras varreduras dentro deste grupo específico, aumentando a eficiência da função ao longo do tempo.
Quando um usuário marcado como inativo loga no sistema ele é, imediatamente, removido do grupo de inativos, entrando, novamente, nas varreduras.