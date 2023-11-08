# CRIANDO ITENS COLETÁVEIS
Criar itens coletáveis em um jogo de plataforma 2D no Godot 4.0 é uma maneira de adicionar elementos de desafio e recompensa aos seus níveis. Aqui estão os passos para criar itens coletáveis:

**1. Preparação de Recursos:**

Antes de começar, você deve criar os recursos gráficos para seus itens coletáveis, como sprites para moedas, power-ups, ou qualquer item que os jogadores possam coletar.

**2. Criando o Nó do Item Coletável:**

- No Godot, crie um nó na sua cena que represente o item coletável (por exemplo, um nó "Area2D").
- Adicione um sprite ao nó para a aparência do item.

**3. Adicionando Lógica de Coleta:**

- Adicione um "CollisionShape2D" ao nó do item para detecção de colisões com o jogador.
- Certifique-se de que o jogador tenha uma máscara de colisão que permita a interação com os itens coletáveis.

**4. Script para Coleta:**

- Adicione um script ao nó do item coletável para lidar com a lógica de coleta.
- Use a função `_on_<collision_signal_name>` para detectar a colisão com o jogador. Por exemplo:

```gdscript
func _on_Area2D_body_entered(body):
    if body.is_in_group("player"):
        # O jogador colidiu com o item coletável
        # Execute aqui a lógica de coleta
        queue_free()  # Destrua o item coletável
```

- Na lógica de coleta, você pode atualizar a pontuação do jogador, aplicar efeitos, ou fazer qualquer ação desejada.

**5. Testando e Ajustando:**

- Execute o jogo e teste a coleta de itens para garantir que ela funcione conforme o esperado.
- Ajuste o valor dos itens coletáveis e outras propriedades conforme necessário.

**6. Adicionando Mais Itens:**

Repita os passos anteriores para criar diferentes tipos de itens coletáveis, se desejar. Você pode criar diferentes classes de itens coletáveis e definir propriedades únicas para cada um.

**7. Exportação:**

Certifique-se de que os itens coletáveis e seus recursos estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

Itens coletáveis são uma maneira eficaz de criar um objetivo no jogo, como coletar moedas ou power-ups, e proporcionar aos jogadores uma sensação de progresso e recompensa. A prática e a experimentação são importantes para aprimorar suas habilidades na criação de itens coletáveis no Godot 4.0. Consulte a documentação oficial do Godot para obter mais detalhes sobre o uso de itens coletáveis nesta versão.