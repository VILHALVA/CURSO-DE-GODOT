# CRIANDO INIMIGO TIPO PATRULHA
A criação de inimigos do tipo patrulha em um jogo de plataforma 2D no Godot 4.0 é uma maneira eficaz de adicionar desafios aos níveis do jogo. Esses inimigos se movem em um padrão de patrulha predefinido e podem atacar o jogador quando se aproximam. Aqui estão os passos para criar um inimigo tipo patrulha:

**1. Preparação de Recursos:**

Antes de começar, você deve criar os recursos gráficos para o inimigo, como sprites para a aparência do inimigo, sprites para animações de movimento e ataque, etc.

**2. Criando o Nó do Inimigo:**

- No Godot, crie um nó na sua cena que represente o inimigo (por exemplo, um nó "KinematicBody2D").
- Adicione um sprite ao nó para a aparência do inimigo.
- Adicione um "CollisionShape2D" ao nó para detecção de colisões com o jogador.

**3. Adicionando Lógica de Patrulha:**

- Adicione um script ao nó do inimigo para controlar seu movimento.
- Crie variáveis para a posição inicial e final da patrulha do inimigo.

```gdscript
extends KinematicBody2D

var start_position: Vector2
var end_position: Vector2
var velocity: Vector2 = Vector2(100, 0)
var direction: int = 1
```

- No `_process`, você pode implementar a lógica de movimento de patrulha.

```gdscript
func _process(delta):
    move_and_collide(velocity * delta * direction)
    
    if position.x < start_position.x or position.x > end_position.x:
        direction = -direction
        $Sprite.scale.x = direction  # Inverte a direção visual do inimigo
```

- Isso fará com que o inimigo se mova para a direita até atingir a posição final e depois se mova para a esquerda até atingir a posição inicial, invertendo sua direção quando necessário.

**4. Implementando a Lógica de Ataque:**

- Para adicionar lógica de ataque ao inimigo, você pode criar uma função que verifica a proximidade do jogador e dispara ataques quando ele está dentro de um alcance específico.

```gdscript
func attack():
    # Lógica de ataque ao jogador
```

- Chame esta função no `_process` ou em resposta a eventos específicos.

**5. Testando e Ajustando:**

- Execute o jogo e teste o movimento da patrulha do inimigo e sua lógica de ataque.
- Ajuste a velocidade de patrulha, alcance de detecção do jogador e outras propriedades conforme necessário.

**6. Exportação:**

Certifique-se de que o inimigo e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

Criar inimigos tipo patrulha adiciona um elemento desafiador ao seu jogo de plataforma 2D. A prática e a experimentação são fundamentais para aprimorar suas habilidades na criação de inimigos do tipo patrulha no Godot 4.0. Consulte a documentação oficial do Godot para obter mais detalhes sobre como criar inimigos nesta versão.