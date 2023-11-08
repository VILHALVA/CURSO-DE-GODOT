# COMO MUDAR DE CENA?
Para mudar de cena (passar de fase) em um jogo de plataforma 2D na Godot 4.0, você pode seguir os seguintes passos:

**1. Criando a Cena da Próxima Fase:**

- Crie uma nova cena que represente a próxima fase do jogo. Essa cena deve conter todos os elementos, como o mapa, personagens, inimigos, itens, etc., relacionados à próxima fase.

**2. Adicionando um Node de Área de Transição:**

- Na cena atual, crie um nó "Area2D" ou "KinematicBody2D" que servirá como área de transição que desencadeará a mudança de cena. Você pode colocar este nó em um local estratégico onde o jogador deve chegar para passar de fase, como uma porta ou portal.

- Adicione um sprite ao nó de área de transição para que ele seja visível.

**3. Configurando a Área de Transição:**

- No nó da área de transição, adicione um "CollisionShape2D" para detectar quando o jogador colide com a área de transição.

- No script do nó da área de transição, implemente a lógica para detectar a colisão do jogador e carregar a próxima cena:

```gdscript
extends Area2D

var next_scene_path = "res://NextScene.tscn"  # Substitua pelo caminho da próxima cena

func _on_Area2D_body_entered(body):
    if body.is_in_group("player"):
        change_scene(next_scene_path)
```

- Neste código, a função `_on_Area2D_body_entered()` detecta quando o jogador colide com a área de transição e chama a função `change_scene()` para carregar a próxima cena.

**4. Criando a Função de Mudança de Cena:**

- Fora do script da área de transição, crie uma função para carregar a próxima cena:

```gdscript
func change_scene(scene_path):
    var next_scene = load(scene_path)
    if next_scene:
        get_tree().change_scene(next_scene)
```

- Esta função carrega a próxima cena usando a função `change_scene()` do nó da árvore de cenas.

**5. Testando e Ajustando:**

- Execute o jogo e teste a área de transição para garantir que a mudança de cena ocorra corretamente quando o jogador colidir com ela.

- Verifique se a próxima cena é carregada com sucesso.

**6. Exportando o Jogo:**

Certifique-se de que todas as cenas e recursos da próxima fase estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

A mudança de cena é fundamental para criar uma progressão em um jogo de plataforma 2D. Prática e experimentação ajudarão a aprimorar suas habilidades na criação de transições de cena no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre como gerenciar cenas e transições nesta versão.