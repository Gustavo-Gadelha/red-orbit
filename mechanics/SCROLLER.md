# Scroller

O jogo utiliza um sistema de **auto-scroller vertical**, no qual o cenário se desloca continuamente enquanto a nave do jogador tenta escapar do planeta hostil.

## Funcionamento

* A câmera se move continuamente em uma única direção.
* O jogador não controla a velocidade do deslocamento do cenário.
* A nave pode se movimentar livremente dentro da área disponível da tela.
* Novos inimigos e obstáculos aparecem conforme o cenário avança.
* Elementos que ficam para trás deixam de fazer parte da área jogável.

## Direção

O deslocamento ocorre **de baixo para cima na tela**, representando a nave se afastando da superfície do planeta.

Visualmente:

```text
        ↑ Direção da fuga
        │
   [ Novos inimigos ]
        │
   [   Jogador     ]
        │
   [   Obstáculos  ]
        │
   [ Superfície do planeta ]
```

## Progressão

O avanço do cenário está diretamente relacionado à mecânica de altura.

* O início da fase representa uma região próxima à superfície.
* Conforme o cenário se desloca, a nave aumenta sua distância em relação ao planeta.
* A dificuldade pode aumentar durante o percurso.
* Ao atingir a distância necessária, a nave escapa do planeta.

## Spawn de elementos

Inimigos e obstáculos devem ser posicionados à frente da área atualmente visível.

Podem aparecer:

* Asteroides
* Sucata espacial
* Infested
* Wrecked
* Outros inimigos futuros

Os elementos devem ser removidos quando deixarem uma distância segura atrás da câmera, evitando o acúmulo desnecessário de objetos.

## Relação com a altura

O progresso do scroller determina o avanço da nave em relação à superfície.

Exemplo:

```text
Altura: 0%
[████░░░░░░░░░░░░░░░░]

Altura: 50%
[██████████░░░░░░░░░░]

Altura: 100%
[████████████████████]
           FUGA
```

A altura pode ser calculada com base na distância percorrida pela câmera ou pelo cenário.

## Objetivo

O scroller possui duas funções principais:

1. Manter o jogador em movimento constante.
2. Representar visualmente a fuga da nave para longe da superfície do planeta.

O sistema deve evitar que o jogador simplesmente permaneça parado, fazendo com que a sobrevivência dependa da reação aos inimigos e obstáculos que surgem durante o avanço.
