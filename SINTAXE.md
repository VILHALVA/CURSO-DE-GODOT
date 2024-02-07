# SINTAXE
No Godot Engine, os scripts são escritos usando sua própria linguagem de script chamada [GDScript](https://docs.godotengine.org/pt-br/4.x/tutorials/scripting/gdscript/index.html). Abaixo está um exemplo de como mover um objeto usando as teclas de seta no Godot:

```gdscript
# Criar um evento de pressionar tecla para mover o objeto
func _process(delta):
    # Verificar se a tecla de seta direita está sendo pressionada
    if Input.is_action_pressed("ui_right"):
        # Mover o objeto para a direita
        $Sprite.position.x += 5 * delta

    # Verificar se a tecla de seta esquerda está sendo pressionada
    elif Input.is_action_pressed("ui_left"):
        # Mover o objeto para a esquerda
        $Sprite.position.x -= 5 * delta

    # Verificar se a tecla de seta para baixo está sendo pressionada
    if Input.is_action_pressed("ui_down"):
        # Mover o objeto para baixo
        $Sprite.position.y += 5 * delta

    # Verificar se a tecla de seta para cima está sendo pressionada
    elif Input.is_action_pressed("ui_up"):
        # Mover o objeto para cima
        $Sprite.position.y -= 5 * delta
```

Aqui está uma explicação do código:

1. **Evento `_process`**:
   - O código está dentro do método `_process`, que é chamado a cada quadro.
   - Isso garante que o movimento do objeto seja atualizado constantemente enquanto as teclas estiverem pressionadas.

2. **Verificando Teclas Pressionadas**:
   - O método `Input.is_action_pressed(action)` é usado para verificar se uma determinada ação de entrada está sendo pressionada.
   - No exemplo, estamos verificando as ações de tecla de seta direita, esquerda, para baixo e para cima.

3. **Movendo o Objeto**:
   - Se uma tecla de seta correspondente estiver pressionada, o objeto é movido na direção apropriada.
   - Multiplicamos o movimento por `delta`, que representa a quantidade de tempo decorrido desde o último quadro. Isso garante que o movimento seja suave e independente da taxa de quadros.

Este é um exemplo simples de como mover um objeto usando as teclas de seta no Godot Engine. Com GDScript, você pode criar scripts para controlar todos os aspectos de seu jogo, desde movimento e física até lógica de jogo e interação com o jogador.