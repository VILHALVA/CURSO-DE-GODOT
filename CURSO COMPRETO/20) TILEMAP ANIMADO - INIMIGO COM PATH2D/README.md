# TILEMAP ANIMADO - INIMIGO COM PATH2D
A criação de um tilemap animado com inimigos que seguem um caminho (utilizando o Path2D) em um jogo de plataforma 2D na Godot 4.0 é um processo envolvente que adiciona dinamismo ao seu jogo. Aqui estão os passos para realizar essa tarefa:

**1. Tilemap Animado:**

Primeiro, você pode criar um tilemap animado para criar um ambiente mais vivo e dinâmico:

- Crie um nó "TileMap" na sua cena para representar o tilemap.

- Adicione os sprites animados (tiles) que deseja usar no tilemap. Certifique-se de que esses sprites tenham animações definidas no Godot.

- No "TileMap," selecione os tiles animados e desenhe o mapa do seu nível. Você pode usar diferentes tiles para criar uma variedade de efeitos animados, como a água, nuvens, chamas, etc.

**2. Criando um Inimigo com Path2D:**

Agora, vamos criar um inimigo que segue um caminho usando o Path2D:

- Crie um nó "KinematicBody2D" ou "RigidBody2D" para representar o inimigo na cena.

- Adicione um sprite ao inimigo para a sua aparência visual.

- Crie um nó "Path2D" na cena e desenhe um caminho para o inimigo seguir. Certifique-se de ajustar os pontos do caminho conforme necessário.

- No nó do inimigo, adicione um "PathFollow2D" como um nó filho e conecte-o ao caminho que você desenhou. Isso fará com que o inimigo siga o caminho automaticamente.

- No script do inimigo, você pode adicionar a lógica para atualizar a posição do inimigo de acordo com o "PathFollow2D" para que ele siga o caminho. Você pode usar a função `set_offset()` para mover o inimigo ao longo do caminho.

```gdscript
extends KinematicBody2D

var path_follow
var speed = 100  # Velocidade do inimigo

func _ready():
    path_follow = $PathFollow2D
    path_follow.set_offset(randf())  # Comece em um ponto aleatório no caminho

func _process(delta):
    # Mova o inimigo ao longo do caminho
    path_follow.offset += speed * delta
```

**3. Testando e Ajustando:**

- Execute o jogo e teste o inimigo seguindo o caminho animado no tilemap.

- Ajuste a velocidade do inimigo e a configuração do caminho conforme necessário para criar o comportamento desejado.

**4. Exportação:**

Certifique-se de que os elementos do tilemap animado e do inimigo estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

A combinação de um tilemap animado com inimigos que seguem um caminho adiciona uma camada de complexidade e vida ao seu jogo de plataforma 2D. Prática e experimentação são essenciais para aprimorar suas habilidades na criação de níveis e mecânicas de jogo no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre o uso de tilemaps e Path2D nesta versão.