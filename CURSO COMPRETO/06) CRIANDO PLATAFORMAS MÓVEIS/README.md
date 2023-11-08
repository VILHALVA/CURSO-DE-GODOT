# CRIANDO PLATAFORMAS MÓVEIS
A criação de plataformas móveis é uma adição divertida e desafiadora para jogos de plataforma 2D no Godot 4.0. Plataformas móveis podem adicionar variedade e complexidade aos níveis do seu jogo. Aqui estão os passos para criar plataformas móveis:

**1. Configurando a Plataforma Móvel:**

- Crie um novo nó na sua cena (por exemplo, um nó "Area2D" para a plataforma móvel).
- Adicione um sprite para representar a aparência da plataforma.
- Adicione um "RigidBody2D" ou "KinematicBody2D" como um nó filho para controlar o movimento da plataforma.

**2. Configurando o Movimento:**

- No nó do "RigidBody2D" ou "KinematicBody2D" da plataforma móvel, adicione uma nova "AnimationPlayer" ou "Tween" para controlar o movimento da plataforma.
- Defina a trajetória da plataforma móvel. Isso pode ser feito usando quadros-chave no "AnimationPlayer" ou usando interpolações no "Tween".
- Configure a velocidade, duração e trajetória de movimento da plataforma.

**3. Lógica de Colisão:**

- Certifique-se de que a plataforma móvel tenha um "CollisionShape2D" configurado para detecção de colisões com o jogador e outros objetos do jogo.
- Implemente a lógica de colisão para garantir que o jogador possa ficar na plataforma móvel. Isso geralmente envolve a alteração da posição do jogador para que ele se mova junto com a plataforma.

**4. Adicionando Comportamentos Extras:**

- Se desejar, você pode adicionar comportamentos extras, como ativação de interruptores para controlar o movimento da plataforma móvel, ou adicionar obstáculos que bloqueiam o caminho da plataforma até que certas condições sejam atendidas.

**5. Testando e Ajustando:**

- Execute o jogo e teste o movimento da plataforma móvel para garantir que ele funcione como planejado.
- Ajuste a velocidade, a trajetória e outros parâmetros até obter o efeito desejado.

**6. Exportação:**

Certifique-se de que a plataforma móvel e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

Criar plataformas móveis adiciona dinamismo aos seus níveis e desafios para o jogador. A prática e a experimentação são fundamentais para aprimorar suas habilidades na criação de plataformas móveis no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre como criar objetos móveis nesta versão.