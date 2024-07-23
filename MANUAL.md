# MANUAL
## INSTALAÇÃO DO GODOT ENGINE:
1. **Baixar o Godot:**
   - Vá para o [site oficial do Godot](https://godotengine.org/download).
   - Selecione a versão apropriada para o seu sistema operacional (Windows, macOS, Linux) e baixe o arquivo.

2. **Instalar o Godot:**
   - **Windows:** Extraia o arquivo ZIP baixado e execute o arquivo `Godot_vX.Y.Z-stable_win64.exe` (ou similar).
   - **macOS:** Extraia o arquivo `.zip` e mova o `Godot_vX.Y.Z-stable_osx.64` para a pasta `Aplicações`.
   - **Linux:** Extraia o arquivo `.tar.xz` e execute o `Godot_vX.Y.Z-stable_x11.64` a partir do terminal.

3. **Iniciar o Godot:**
   - Execute o Godot Engine. A primeira vez que você iniciar o Godot, você verá a tela de inicialização com a opção de criar um novo projeto ou abrir um projeto existente.

## CONFIGURAÇÃO DO GODOT:
1. **Criar um Novo Projeto:**
   - Na tela inicial do Godot, clique em `New Project`.
   - Dê um nome ao seu projeto e escolha um diretório onde ele será salvo.
   - Selecione o diretório para o projeto e clique em `Create & Edit`.

2. **Configurar o Projeto:**
   - Com o projeto aberto, vá para `Project` > `Project Settings` para ajustar as configurações do projeto.
   - Na aba `General`, você pode definir várias configurações, como resolução da tela, modo de renderização, etc.
   - A configuração padrão deve funcionar para a maioria dos projetos iniciais.

3. **Configurar o Ambiente de Desenvolvimento:**
   - Você pode ajustar a interface do Godot conforme suas preferências, indo para `Editor` > `Editor Settings`.
   - Explore as opções para personalizar o layout, temas, atalhos e mais.

## CRIAR O PRIMEIRO JOGO:
1. **Criar uma Nova Cena:**
   - No Godot, uma "Cena" é o termo usado para uma tela ou um nível no jogo. Clique em `Scene` > `New Scene`.
   - Selecione um `Node` (nó) base para sua cena. Para um jogo 2D, escolha `2D Scene` (Node2D). Para um jogo 3D, escolha `3D Scene` (Node3D).

2. **Adicionar Objetos à Cena:**
   - Com a nova cena aberta, você pode adicionar diferentes tipos de nós. Para um jogo 2D básico, adicione um `Sprite`:
     - Clique com o botão direito na árvore de nós e selecione `Add Child Node`.
     - Escolha `Sprite` e clique em `Create`.
     - No painel de propriedades, você pode definir a textura do sprite (adicione uma imagem à sua pasta de projeto e selecione-a).

3. **Adicionar Código ao Jogo:**
   - Adicione um script ao seu objeto (por exemplo, ao Sprite):
     - Selecione o nó no painel de nós.
     - No painel de propriedades, clique em `Attach Script`.
     - Dê um nome ao script e clique em `Create`.
   - No editor de scripts, você pode escrever código para controlar o comportamento do objeto. Aqui está um exemplo básico de movimento para um sprite:

     ```gdscript
     extends Sprite

     var speed = 200

     func _process(delta):
         if Input.is_action_pressed("ui_right"):
             position.x += speed * delta
         if Input.is_action_pressed("ui_left"):
             position.x -= speed * delta
     ```

4. **Testar o Jogo:**
   - Para testar seu jogo, clique no botão `Play` (ícone de triângulo verde) na parte superior da interface.
   - Se for a primeira vez que você está executando o projeto, o Godot pedirá que você selecione uma cena principal. Selecione a cena que você criou e clique em `Play`.

5. **Salvar o Projeto e Cena:**
   - Para salvar o projeto, vá para `Scene` > `Save Scene` e dê um nome à cena.
   - Para salvar o projeto, vá para `Project` > `Save All`.

