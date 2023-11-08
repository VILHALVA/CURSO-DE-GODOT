# PARALLAX LAYERS
O uso de camadas de parallax é uma técnica comum para adicionar profundidade visual a jogos de plataforma 2D, criando a ilusão de que os elementos de fundo se movem a diferentes velocidades em relação ao jogador. Aqui está como você pode configurar camadas de parallax em seu jogo de plataforma 2D no Godot 4.0:

**1. Preparação de Recursos:**

Antes de começar, você deve ter os recursos gráficos para suas camadas de parallax, como imagens ou texturas de fundo.

**2. Configurando Camadas de Parallax:**

- No Godot, selecione a cena do seu jogo de plataforma no Scene Tree.
- Adicione um nó "ParallaxBackground" como um nó filho da cena principal.
- Adicione um ou mais nós "ParallaxLayer" como filhos do "ParallaxBackground" para cada camada de parallax que você deseja criar.

**3. Configurando Camadas de Parallax:**

- Selecione cada nó "ParallaxLayer" e defina sua textura (ou sprite) no Inspector.
- Ajuste a "scroll_offset" e a "scroll_scale" para controlar o movimento da camada em relação à câmera e ao jogador.
  - "scroll_offset": Isso define a posição inicial da camada em relação à câmera.
  - "scroll_scale": Isso define a velocidade de movimento da camada. Um valor menor tornará a camada mais lenta em relação à câmera, criando a ilusão de profundidade.

**4. Câmera e Jogador:**

Certifique-se de que a câmera esteja configurada para seguir o jogador corretamente. Você pode usar um nó "Camera2D" e configurá-lo para seguir o personagem principal.

**5. Testando e Ajustando:**

Execute o jogo e ajuste as configurações das camadas de parallax até obter o efeito desejado. Você pode experimentar com diferentes texturas e velocidades de deslocamento para criar a sensação de profundidade desejada.

**6. Exportação:**

Certifique-se de que suas camadas de parallax estejam configuradas corretamente no exportador para que elas sejam incluídas quando você exportar o jogo para a plataforma desejada.

As camadas de parallax podem adicionar uma dimensão visual interessante ao seu jogo de plataforma 2D, tornando-o mais envolvente para os jogadores. Lembre-se de que a prática e a experimentação ajudarão a aprimorar suas habilidades na criação de camadas de parallax para seu jogo no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre o uso de camadas de parallax nesta versão.