# HUD DO GAME (CONTADOR DE MOEDAS-PONTOS)
Para criar uma HUD (Heads-Up Display) em um jogo de plataforma 2D na Godot 4.0, que inclui um contador de moedas ou pontos, você pode seguir estes passos:

**1. Preparação de Recursos:**

Certifique-se de ter os recursos gráficos necessários para a HUD, incluindo sprites para elementos visuais como o contador de moedas/pontos, fontes para exibir os números e qualquer arte adicional que você deseja incluir na HUD.

**2. Criando o Nó da HUD:**

- No Godot, crie um nó para representar a HUD. Você pode usar um nó "CanvasLayer" para garantir que a HUD esteja sempre na parte superior da cena.

- Adicione elementos visuais, como sprites e labels, para representar o contador de moedas ou pontos.

**3. Configurando o Script da HUD:**

- Adicione um script ao nó da HUD para controlar a lógica da exibição dos valores do contador.

- No script, você pode criar variáveis para controlar a pontuação do jogador e atualizar a exibição da HUD:

```gdscript
extends CanvasLayer

var score = 0
var label_score

func _ready():
    label_score = $LabelScore  # Substitua "LabelScore" pelo nome do nó que representa o contador

func update_score(new_score):
    score = new_score
    label_score.text = str(score)
```

**4. Atualizando a HUD:**

- No seu jogo, a cada vez que o jogador coletar uma moeda ou ganhar pontos, chame a função `update_score()` do script da HUD para atualizar o contador:

```gdscript
onready var hud = $HUD  # Substitua "$HUD" pelo caminho correto para o nó da HUD

func _on_Coin_collected():
    player_score += 1  # Aumente a pontuação do jogador
    hud.update_score(player_score)  # Atualize a HUD com a nova pontuação
```

**5. Testando e Ajustando:**

- Execute o jogo e teste a HUD para garantir que o contador de moedas ou pontos seja atualizado corretamente.

- Ajuste a aparência e a posição da HUD de acordo com as necessidades do seu jogo.

**6. Exportação:**

Certifique-se de que a HUD e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

A criação de uma HUD com um contador de moedas ou pontos é essencial para fornecer feedback visual ao jogador sobre seu progresso no jogo. Prática e experimentação ajudarão a aprimorar suas habilidades na criação de HUDs no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre a criação de interfaces de usuário e elementos HUD nesta versão.