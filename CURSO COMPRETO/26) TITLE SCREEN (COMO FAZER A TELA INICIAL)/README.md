# TITLE SCREEN (COMO FAZER A TELA INICIAL)
Criar uma tela inicial (title screen) em um jogo de plataforma 2D na Godot 4.0 é uma parte importante do desenvolvimento do jogo, pois é a primeira coisa que os jogadores veem ao iniciar o jogo. Aqui estão os passos para criar uma tela inicial:

**1. Criando a Cena da Tela Inicial:**

- Crie uma nova cena que representará a tela inicial do jogo. Geralmente, essa cena contém elementos como o título do jogo, opções de menu (como "Iniciar Jogo", "Opções", "Sair", etc.), e possivelmente uma imagem de fundo ou animação.

**2. Configurando o Nó CanvasLayer:**

- Para garantir que a tela inicial esteja sempre na parte superior, crie um nó "CanvasLayer" como nó raiz da cena da tela inicial.

**3. Adicionando Elementos à Tela Inicial:**

- Adicione os elementos visuais, como sprites para o título do jogo e botões do menu, ao nó "CanvasLayer."

- Configure os botões do menu para que eles emitam sinais quando pressionados.

**4. Criando Funções para os Botões do Menu:**

- No script da tela inicial, implemente funções para responder aos sinais emitidos pelos botões do menu. Por exemplo, você pode criar funções como "start_game()" para começar o jogo e "open_options()" para abrir a tela de opções.

**5. Mudando de Cena:**

- Para iniciar o jogo quando o jogador pressionar o botão "Iniciar Jogo", você pode usar a função `change_scene()` da árvore de cenas para carregar a cena da fase do jogo:

```gdscript
func start_game():
    var game_scene = preload("res://GameScene.tscn")  # Substitua pelo caminho da cena do jogo
    get_tree().change_scene(game_scene)
```

- Certifique-se de criar um botão "Sair" ou "Opções" que permita que os jogadores voltem para a tela inicial ou ajustem as configurações.

**6. Testando e Ajustando:**

- Execute o jogo e teste a tela inicial para garantir que os botões funcionem conforme o esperado.

- Certifique-se de que os elementos visuais, como o título e os botões, sejam configurados de acordo com o design desejado.

**7. Exportando o Jogo:**

Certifique-se de que a tela inicial e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

A criação de uma tela inicial é uma parte fundamental da experiência do jogador, pois é a primeira impressão que os jogadores têm do seu jogo. Prática e experimentação ajudarão a aprimorar suas habilidades na criação de telas iniciais no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre a criação de interfaces de usuário e menus nesta versão.