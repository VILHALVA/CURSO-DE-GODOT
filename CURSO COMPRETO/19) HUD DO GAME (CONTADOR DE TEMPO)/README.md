# HUD DO GAME (CONTADOR DE TEMPO) 
Para criar uma HUD (Heads-Up Display) que exibe um contador de tempo em um jogo de plataforma 2D na Godot 4.0, você pode seguir estes passos:

**1. Preparação de Recursos:**

Certifique-se de ter os recursos gráficos necessários para a HUD, incluindo sprites para elementos visuais como o contador de tempo, fontes para exibir os números e qualquer arte adicional que você deseja incluir na HUD.

**2. Criando o Nó da HUD:**

- No Godot, crie um nó para representar a HUD. Você pode usar um nó "CanvasLayer" para garantir que a HUD esteja sempre na parte superior da cena.

- Adicione elementos visuais, como sprites e labels, para representar o contador de tempo.

**3. Configurando o Script da HUD:**

- Adicione um script ao nó da HUD para controlar a lógica da exibição do contador de tempo.

- No script, você pode criar variáveis para controlar o tempo restante e atualizar a exibição da HUD:

```gdscript
extends CanvasLayer

var time_remaining = 60  # Tempo inicial em segundos
var label_time

func _ready():
    label_time = $LabelTime  # Substitua "LabelTime" pelo nome do nó que representa o contador de tempo

func update_time(new_time):
    time_remaining = new_time
    label_time.text = str(time_remaining)
```

**4. Atualizando a HUD com o Contador de Tempo:**

- No seu jogo, a cada quadro, atualize a contagem regressiva do tempo e chame a função `update_time()` do script da HUD para atualizar o contador de tempo:

```gdscript
onready var hud = $HUD  # Substitua "$HUD" pelo caminho correto para o nó da HUD

func _process(delta):
    if game_is_running:
        time_remaining -= delta
        if time_remaining < 0:
            time_remaining = 0  # Certifique-se de que o tempo não seja negativo
            game_over()  # Implemente a lógica de fim de jogo quando o tempo acabar
        hud.update_time(time_remaining)  # Atualize a HUD com o tempo restante
```

- O código acima presume que o jogo está rodando e que você tem uma função `game_over()` para tratar do fim do jogo quando o tempo acaba.

**5. Testando e Ajustando:**

- Execute o jogo e teste a HUD para garantir que o contador de tempo seja atualizado corretamente.

- Ajuste a aparência e a posição da HUD de acordo com as necessidades do seu jogo.

**6. Exportação:**

Certifique-se de que a HUD e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

A criação de uma HUD com um contador de tempo é fundamental para muitos tipos de jogos, especialmente aqueles com limites de tempo ou desafios temporizados. Prática e experimentação ajudarão a aprimorar suas habilidades na criação de HUDs no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre a criação de interfaces de usuário e elementos HUD nesta versão.