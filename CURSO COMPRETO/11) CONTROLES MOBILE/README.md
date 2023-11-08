# CONTROLES MOBILE
Adicionar controles para dispositivos móveis em um jogo de plataforma 2D no Godot 4.0 é fundamental para criar uma experiência de jogo acessível em smartphones e tablets. Aqui estão os passos para implementar controles móveis:

**1. Configurando os Controles de Toque:**

- No Godot, crie um nó "CanvasLayer" para seus controles de toque. Este nó deve conter os elementos de interface do usuário (UI) que os jogadores tocarão, como botões virtuais de direção, botões de salto, ataque, etc.

- Adicione nós filhos ao nó "CanvasLayer" para representar os botões e elementos de UI desejados, como "Button" ou "TextureButton" para criar botões clicáveis.

- Configure a posição, tamanho e aparência dos elementos de UI de acordo com o design do seu jogo.

**2. Configurando o InputMap:**

- No Godot, vá para "Project" > "Project Settings".
- Na guia "Input Map," configure os mapeamentos de input para as ações que deseja controlar por meio de toques na tela. Por exemplo, você pode criar ações como "move_left," "move_right," "jump," "attack," etc.

**3. Scripting dos Controles de Toque:**

- Adicione um script ao nó "CanvasLayer" para controlar a lógica dos controles de toque.

- No script, você pode usar as funções `Input.is_action_just_pressed()` e `Input.is_action_just_released()` para detectar quando os botões virtuais são tocados e liberados.

- Você também pode usar as funções de toque do Godot, como `Input.is_action_pressed("touchscreen_pressed")`, para detectar toques na tela e responder a eles.

- Implemente a lógica para traduzir os toques na tela em ações no jogo, como movimento do personagem, pulo, ataque, etc.

**4. Adicionando Feedback Visual:**

- Para uma melhor experiência do jogador, adicione feedback visual aos controles de toque. Isso pode incluir animações ou alterações visuais nos botões quando são pressionados.

**5. Testando em Dispositivos Móveis:**

- Para testar os controles de toque, você pode usar o simulador de dispositivo móvel no Godot ou compilar e implantar o jogo em um dispositivo físico.

- Certifique-se de testar em vários dispositivos com diferentes tamanhos de tela e proporções para garantir que os controles funcionem bem em todos eles.

**6. Exportação:**

- Certifique-se de configurar corretamente as configurações de exportação para dispositivos móveis no Godot para que seu jogo seja executado corretamente em smartphones e tablets.

**7. Ajustando para Diferentes Plataformas:**

- Lembre-se de que as interfaces de toque variam entre as diferentes plataformas móveis (Android, iOS). Certifique-se de ajustar os controles de toque para atender aos requisitos de cada plataforma.

Implementar controles móveis bem projetados é essencial para a acessibilidade e a jogabilidade em dispositivos móveis. A prática e a iteração são fundamentais para criar uma experiência de jogo eficaz em plataformas móveis. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre a implementação de controles móveis nesta versão.