# INIMIGO DUPLO - CONCEITO BÁSICO DE CLASSE
Para criar inimigos duplicados com o conceito básico de classe na Godot 4.0 em um jogo de plataforma 2D, você pode seguir estes passos:

**1. Criando a Classe do Inimigo:**

- No Godot, crie uma nova cena chamada "Enemy" (Inimigo) para representar o inimigo. Você pode usar um nó "KinematicBody2D" ou "RigidBody2D" para o corpo do inimigo.

- Adicione um sprite ao inimigo para a sua aparência visual.

- Crie um script para o nó do inimigo. Este script conterá a lógica do inimigo.

- Dentro do script do inimigo, você pode definir variáveis para controlar seu comportamento, como velocidade, saúde, dano, etc.

```gdscript
extends KinematicBody2D

var speed = 100
var health = 100
var damage = 10
```

- Implemente a lógica do inimigo, como movimento, detecção de colisão com o jogador, causar dano, etc., dentro deste script.

**2. Criação de uma Instância do Inimigo na Cena:**

- Na cena principal do seu jogo, adicione um nó "Node2D" para representar o grupo de inimigos.

- No grupo de inimigos, você pode criar instâncias da cena "Enemy" que você criou anteriormente e configurar suas posições iniciais.

```gdscript
extends Node2D

func _ready():
    var enemy1 = preload("res://Enemy.tscn").instance()
    var enemy2 = preload("res://Enemy.tscn").instance()

    enemy1.position = Vector2(100, 100)
    enemy2.position = Vector2(300, 100)

    add_child(enemy1)
    add_child(enemy2)
```

Neste exemplo, criamos duas instâncias do inimigo e as posicionamos em locais diferentes na cena. Você pode ajustar as posições e a quantidade de inimigos conforme necessário.

**3. Testando e Ajustando:**

- Execute o jogo e teste a interação com os inimigos duplicados.

- Ajuste as propriedades dos inimigos e a lógica de acordo com as necessidades do seu jogo.

**4. Exportação:**

Certifique-se de que a cena do inimigo e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

A criação de inimigos duplicados usando o conceito de classe permite que você crie inimigos com comportamentos similares e reutilizáveis em seu jogo de plataforma 2D. Prática e experimentação são essenciais para aprimorar suas habilidades na criação de inimigos e classes no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre o uso de classes e instâncias nesta versão.