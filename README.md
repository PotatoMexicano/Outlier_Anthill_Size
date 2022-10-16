# Outlier anthill detection

**Objetivo**: Detectar ninhos de formigueiros que estão com tamanho (largura x comprimento) incorretos.

Foram utilizados parametros para realizar a classificação dos formigueiros, tais como:

|Situação|Código|
|:-:|:-:|
|Ativo|1|
|Amuado|2|
|Morto|3|

|Grupo|Código|
|:-:|:-:|
|Sauva|1|
|Quenquém|2|
|Olheiro|3|

Para determinar a incoerência na coleta das informações foi considerado a escala 1:1 de tamanho e largura, ou seja:

|Comprimento x Largura|Débito|
|:-:|:-:|
|2x2|0|
|9x3|6|
|30x3|27|

Considerando que o ninho normalmente cresce proporcional, a subtração da largura pelo comprimento em numero absoluto retorna a imprecisão da coleta.

Para levar em consideração o fator organico adotado por alguns formigueiros para adaptar-se ao ambiente, considerei apenas incorretos as coletas onde o débito foi superior a 10 unidades.

![Alt text](/images/sauva_01.jpg "Erro #1")

Como podemos observar o ponto mais inferior destacado em roxo, remete a um ninho 30x3, que apresenta erro de coleta. Por estar muito acima em débito que os demais, apenas ele fica mais destacado, porém após sua correção, este é o resultado obtido.

![Alt text](/images/sauva_02.jpg "Erro #2")