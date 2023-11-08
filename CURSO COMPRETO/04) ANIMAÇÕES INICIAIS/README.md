# ANIMAÇÕES INICIAIS
Adicionar animações iniciais a um jogo de plataforma 2D no Godot 4.0 pode tornar o jogo mais dinâmico e atraente. Aqui estão os passos básicos para criar animações iniciais em seu jogo de plataforma 2D:

**1. Preparação:**

Antes de começar a criar animações, você deve ter os recursos gráficos necessários, como sprites para o personagem, inimigos, objetos e outros elementos do jogo.

**2. Criando Animações:**

A criação de animações no Godot 4.0 envolve o uso do Editor de Animações. Siga estas etapas:

- No Godot, selecione o nó do personagem ou objeto que você deseja animar no Scene Tree.
- No Inspector, vá para a aba "Animation" e clique no botão "AnimationPlayer" para adicionar um AnimationPlayer ao nó. Isso permite que você crie e gerencie animações para o objeto.
- No AnimationPlayer, clique no botão "Animation" para criar uma nova animação. Dê um nome para a animação.
- Com a animação selecionada, clique no botão "Record" para ativar o modo de gravação. Isso permite que você faça alterações no objeto e grave os quadros-chave da animação.

**3. Criando Quadros-chave (Keyframes):**

Agora, você pode criar quadros-chave para a animação. Isso envolve a definição de propriedades do objeto (posição, escala, rotação, etc.) em momentos específicos da animação. Por exemplo, para uma animação de salto de um personagem:

- Avance na linha do tempo para o momento em que o personagem começa a pular.
- Altere a posição Y do personagem para representar o salto.
- Adicione um quadro-chave para essa posição.
- Avance na linha do tempo para o momento em que o personagem retorna ao chão.
- Defina a posição Y de volta ao valor original e adicione outro quadro-chave.

**4. Reproduzindo e Testando a Animação:**

Você pode reproduzir e testar a animação no Godot para ver como ela fica. Certifique-se de ajustar a velocidade da animação, o número de repetições e outros parâmetros conforme necessário.

**5. Lógica do Jogo:**

Dependendo das interações do jogo, você pode usar scripts para controlar o início e a parada das animações. Por exemplo, o pulo do personagem pode ser acionado por um script quando o jogador pressiona a tecla de salto.

**6. Exportação:**

Certifique-se de que seus recursos gráficos e animações estão configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

Lembre-se de que a criação de animações é uma parte importante da criação de jogos 2D atraentes no Godot 4.0, e a prática e a experimentação ajudarão a aprimorar suas habilidades na criação de animações para seu jogo de plataforma. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre a criação de animações no Godot 4.0.