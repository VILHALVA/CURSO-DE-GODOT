# GERENCIAR OS STATES ANIMATIONS
Gerenciar estados de animação em um jogo de plataforma 2D no Godot 4.0 é uma parte crucial para criar personagens e inimigos com animações dinâmicas. Isso permite que os personagens mudem de animação com base em diferentes estados do jogo, como andar, pular, atacar e muito mais. Aqui estão os passos para gerenciar estados de animação:

**1. Preparação de Recursos:**

Antes de começar, você deve ter as animações criadas e os sprites correspondentes para os diferentes estados do personagem ou inimigo.

**2. Organizando as Animações:**

- No Godot, crie um nó "AnimationTree" ou "AnimationPlayer" no nó do seu personagem ou inimigo para gerenciar as animações.

- Adicione as diferentes animações (como andar, pular, atacar, etc.) ao "AnimationPlayer" como "AnimationPlayerAnimations". Você pode criar animações no Godot ou importá-las.

**3. Criando Estados de Animação:**

- Use o "AnimationTree" para criar estados de animação, que são representações visuais dos diferentes estados do personagem ou inimigo.

- Crie um nó "StateMachine" no "AnimationTree" e adicione estados de animação, como "Idle," "Walking," "Jumping," "Attacking," etc.

**4. Configurando Transições:**

- Configure as transições entre os estados de animação no "AnimationTree". Isso define como as animações mudam quando o personagem ou inimigo muda de estado.

- Você pode adicionar condições para as transições, como a detecção de eventos do jogo ou a lógica do script. Por exemplo, você pode configurar uma transição para "Walking" quando o personagem pressiona a tecla de movimento.

**5. Controlando as Animações por Script:**

- No script do seu personagem ou inimigo, você pode controlar as transições de animação programaticamente com funções como `play`, `playback_speed`, `queue` e `crossfade`.

- Use as funções do "AnimationPlayer" para controlar a reprodução da animação, pausar, retroceder, etc.

```gdscript
# Mudar para a animação "Walking"
$AnimationPlayer.play("Walking")
```

**6. Testando e Ajustando:**

- Execute o jogo e teste as animações com base nos estados do personagem ou inimigo.

- Ajuste as transições e os tempos de animação conforme necessário para garantir uma jogabilidade suave.

**7. Exportação:**

Certifique-se de que as animações e o sistema de gerenciamento de estados estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

Gerenciar estados de animação é essencial para criar personagens e inimigos realistas e dinâmicos em um jogo de plataforma 2D. Prática e iteração ajudarão a aprimorar suas habilidades na criação de animações baseadas em estados no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre como criar e gerenciar animações nesta versão.