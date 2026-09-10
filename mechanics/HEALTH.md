# Health

A nave do jogador possui um sistema de vida que determina quanto dano ela pode receber antes de ser destruída.

## Funcionamento

* A nave possui uma quantidade máxima de vida.
* Colisões com inimigos, projéteis e obstáculos causam dano.
* A vida atual é reduzida conforme o dano recebido.
* Quando a vida chega a zero, a nave é destruída.
* A destruição da nave encerra a tentativa atual e leva à tela de Game Over.

## Dano

As principais fontes de dano são:

* Projéteis inimigos
* Asteroides
* Sucata espacial
* Criaturas orgânicas

Cada fonte pode causar uma quantidade diferente de dano.

## Invulnerabilidade

Após sofrer dano, a nave recebe um curto período de invulnerabilidade.

Durante esse período:

* Novos danos são ignorados.
* A nave pode apresentar um efeito visual para indicar a invulnerabilidade.

Isso evita que uma única colisão resulte em vários danos consecutivos.

## HUD

A vida atual deve ser exibida na HUD por meio de uma barra ou indicador visual.

Exemplo:

```text
Vida
[████████████████░░░░]
```

A barra diminui imediatamente após a nave receber dano.

## Recuperação

A vida não é recuperada automaticamente.

Itens de recuperação podem ser adicionados posteriormente, caso sejam necessários para o balanceamento.

## Condição de derrota

Quando:

```text
Vida <= 0
```

a nave é destruída e a partida termina.

## Balanceamento

O sistema deve permitir que o jogador sobreviva a alguns erros sem tornar o dano irrelevante.

A quantidade máxima de vida e o dano causado por cada ameaça devem ser ajustados junto com a dificuldade dos padrões de inimigos.
