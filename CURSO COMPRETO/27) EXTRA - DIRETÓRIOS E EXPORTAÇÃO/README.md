# EXTRA: DIRETÓRIOS E EXPORTAÇÃO
A estrutura das pastas do seu jogo na Godot e a exportação do jogo para diversas plataformas são etapas cruciais para garantir que seu jogo seja organizado e funcione em diferentes ambientes. Aqui está uma estrutura de pasta comum para o seu jogo e um guia sobre como exportá-lo para diferentes plataformas:

**Estrutura de Pastas do Jogo:**

Uma estrutura de pastas bem organizada pode facilitar o desenvolvimento, a manutenção e a exportação do jogo. Aqui está um exemplo de estrutura de pastas comuns para um jogo na Godot:

```
- game/
  - scenes/          # Pasta para as cenas do jogo
    - main_menu.tscn  # Cena da tela inicial
    - level_1.tscn    # Cena da primeira fase
    - level_2.tscn    # Cena da segunda fase
    - ...
  - scripts/         # Pasta para scripts do jogo
    - player.gd      # Script do jogador
    - enemy.gd       # Script do inimigo
    - ...
  - assets/          # Pasta para recursos do jogo
    - textures/      # Texturas e imagens
    - sounds/        # Áudios e efeitos sonoros
    - music/         # Músicas de fundo
    - fonts/         # Fontes
  - export/           # Pasta onde o jogo exportado será gerado
  - project.godot     # Arquivo do projeto Godot
```

Você pode adaptar essa estrutura às necessidades do seu jogo. Certifique-se de manter recursos, scripts e cenas bem organizados em pastas apropriadas.

**Exportando o Jogo para Diversas Plataformas:**

Para exportar seu jogo para diferentes plataformas na Godot, siga estas etapas:

1. **Configuração do Projeto:**
   - Abra seu projeto na Godot.
   - Vá para "Projeto" no canto superior esquerdo e selecione "Configurações do Projeto."

2. **Configuração das Plataformas:**
   - Na seção "Configurações de Exportação," você encontrará várias opções de plataformas suportadas. Selecione a plataforma para a qual deseja exportar (por exemplo, Windows, Linux, Android, iOS, etc.).

3. **Configurações de Exportação Específicas:**
   - Cada plataforma tem configurações específicas que você pode ajustar, como resolução, ícones, permissões, etc. Configure essas opções de acordo com as necessidades da plataforma.

4. **Exportação do Projeto:**
   - Após configurar as opções, clique em "Exportar Projeto" ou equivalente, dependendo da plataforma. Isso gerará um executável ou pacote do jogo específico para a plataforma selecionada.

5. **Teste o Jogo:**
   - Antes de lançar seu jogo, sempre teste-o na plataforma de destino para garantir que tudo funcione conforme o esperado.

6. **Distribuição:**
   - Dependendo da plataforma, você precisará seguir as diretrizes de distribuição apropriadas. Por exemplo, para Windows, você pode criar um instalador. Para Android, você precisará publicá-lo na Google Play Store, etc.

Lembre-se de que cada plataforma tem suas próprias exigências e diretrizes de exportação, portanto, é importante ler a documentação relevante e seguir as instruções apropriadas.

Com uma estrutura de pasta organizada e uma abordagem cuidadosa para exportação, você poderá criar e lançar seu jogo com sucesso em várias plataformas. Certifique-se de manter cópias de segurança de seu projeto e recursos antes de exportar, e teste seu jogo em cada plataforma para evitar problemas inesperados.