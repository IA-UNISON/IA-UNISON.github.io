---
layout: post
title: 3. Un puzzle un poco diferente
description: Actividad de evaluación continua 3
comments: true
mathjax: true
---

El *rompecabezas deslizante* es una versión diferente del 15 puzzle, en la cual cada linea y cada columna se deslizan, como si se encontrara en una esfera (por supuesto que este tipo de rompecabezas no se puede hacer en madera, pero en la computadora es facilísimo). Un esquema del entorno es el siguiente:


|              | $\Uparrow$ | $\Uparrow$ | $\Uparrow$ | $\Uparrow$ |               |
| ------------ | ---------- | ---------- | ---------- | ---------- |               |
| $\Leftarrow$ |     1      |     2      |     3      |      4     | $\Rightarrow$ |
| $\Leftarrow$ |     5      |     6      |     7      |      8     | $\Rightarrow$ |
| $\Leftarrow$ |     9      |    10      |    11      |     12     | $\Rightarrow$ |
| $\Leftarrow$ |    13      |    14      |    15      |     16     | $\Rightarrow$ |
|              | $\Downarrow$ | $\Downarrow$ | $\Downarrow$ | $\Downarrow$ |       |


Las acciones que el agente puede realizar sobre el ambiente son: a) Girar por la derecha
el renglón $i$ ($i \in \{1,2,3,4\}$); b) Girar por la izquierda el renglón $i$ ($i \in
\{1,2,3,4\}$); c) Girar por arriba la columna $j$ ($j \in \{1,2,3,4\}$); y d) Girar por
abajo la columna $j$ ($j \in \{1,2,3,4\}$). Se asume que el ambiente es completamente
observable. El objetivo del agente es que, después de aplicar un cierto numero de movimientos aleatorios
y no observados. El agente pueda realizar las acciones necesarias para regresar el sistema
al estado mostrado en el esquema anterior, utilizando la menor cantidad de movimientos
posibles.

Conteste las siguientes preguntas (10 puntos por pregunta):


1. Establezca una manera de representar el estado del problema.
2. Establezca cuales serían las acciones legales en un estado dado.
3. Establezca el estado sucesor a un estado dado, si se selecciona una acción.
4. Establezca el costo local dependiendo del estado y la acción.
5. ¿Cual es la cardinalidad del espacio de estado?
6. ¿La distancia de Manhattan, o el número de piezas mal colocadas podrían ser heurísticas admisibles?
7. Desarrolle 2 heurísticas ($h_1(n)$ y $h_2(n)$) para resolver el problema por el método de búsqueda A*.
8. Demuestre (o haga un esbozo de demostración) que las heurísticas son admisibles.
9. Determine si una heurística es dominante respecto a la otra. Demuestre que lo son (o que no lo son, en su caso).
10. ¿La búsqueda en grafos ofrecería ventajas respecto a la búsqueda en árboles en este problema? Justifique su respuesta.



<!-- Vamos a plantear un problema para resolver con búsquedas:

Supongamos que quiero trasladarme desde la posición discreta $1$ hasta la posición discreta $N$ en una vía
recta. Puedo trasladarme de dos maneras:

1. A pie, desde el punto $x$ hasta el punto $x + 1$ en un tiempo de 1 minuto.
2. Usando un camión mágico, desde el punto $x$ hasta el punto $2x$ con un tiempo de 2 minutos.

Mi problema es establecer un plan para ir desde el punto $1$ hasta el punto $N$ en el menor tiempo posible.

Desarrolla en un archivo `camion-magico.py` lo siguiente:

1. ¿Cuál es el modelo discreto determinista del proceso? Desarróllalo.
2. ¿Cuál es el problema de búsqueda a resolver? Desarrolla el problema
3. ¿Cuántos nodos revisa si se utiliza una búsqueda con costo uniforme para encontrar la solución para ir a la posición 31,459.
4. Propón una heurística para usar en una búsqueda tipo $A^*$ en este problema.
5. Demuestra (en el mismo archivo, como comentario o como `string`) que la heurística que propones es admisible.
6. Trata de mostrar si podría (o no) la heurística ser consistente.
7. ¿Cuántos nodos se exploran usando el algoritmo $A^*$ y la heurística que propones.
 -->