# CAUSANDO E SOFRENDO DANOS (HITBOX E HURTBOX)
Causar e sofrer danos em um jogo de plataforma 2D no Godot 4.0 envolve o uso de hitboxes (causadores de dano) e hurtboxes (recebedores de dano) para detectar colisões entre personagens, inimigos e outros objetos. Aqui estão os passos para implementar causar e sofrer danos com hitboxes e hurtboxes:

**1. Preparação de Recursos:**

Antes de começar, você deve criar os recursos gráficos para seus personagens, inimigos e quaisquer objetos relacionados a dano, como armas ou projéteis.

**2. Criando Hitboxes e Hurtboxes:**

- No Godot, crie um nó na sua cena que represente o personagem ou inimigo.
- Adicione um "CollisionShape2D" ao nó para definir a hitbox, que é a área que causa dano.
- Crie outro nó para representar a hitbox (por exemplo, um nó "Area2D").
- Adicione um "CollisionShape2D" a este nó para definir a hurtbox, que é a área que recebe dano.

**3. Implementando a Lógica de Causar e Sofrer Danos:**

- Adicione um script ao nó do personagem ou inimigo para controlar a lógica de causar e sofrer danos.
- Use as funções `_on_<collision_signal_name>` para detectar colisões entre a hitbox e a hurtbox.

```gdscript
func _on_Hitbox_body_entered(body):
    if body.is_in_group("enemy"):
        # A hitbox colidiu com um inimigo, aplique dano ao inimigo
        body.apply_damage(damage_value)
    elif body.is_in_group("player"):
        # A hitbox colidiu com o jogador, aplique dano ao jogador
        body.apply_damage(damage_value)

func _on_Hurtbox_body_entered(body):
    if body.is_in_group("enemy"):
        # A hurtbox colidiu com um inimigo, aplique dano ao jogador
        apply_damage(damage_value)
    elif body.is_in_group("player"):
        # A hurtbox colidiu com o jogador, aplique dano ao inimigo
        apply_damage(damage_value)
```

- Implemente a lógica de aplicação de dano nos objetos relevantes. Isso pode incluir a redução da saúde ou a execução de ações específicas, como morte ou efeitos de status.

**4. Testando e Ajustando:**

- Execute o jogo e teste a lógica de causar e sofrer danos.
- Ajuste os valores de dano, alcances de colisão e outras propriedades conforme necessário.

**5. Exportação:**

Certifique-se de que os personagens, inimigos e objetos relacionados a dano estejam configurados corretamente no exportador para que eles sejam incluídos quando você exportar o jogo para a plataforma desejada.

Implementar causar e sofrer danos com hitboxes e hurtboxes é uma parte importante da criação de jogos de plataforma 2D envolventes e desafiadores. A prática e a experimentação ajudarão a aprimorar suas habilidades na criação de mecânicas de dano no Godot 4.0. Certifique-se de consultar a documentação oficial do Godot para obter mais detalhes sobre como lidar com colisões e danos nesta versão.