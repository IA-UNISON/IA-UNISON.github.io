---
layout: post
title: 3. El autobús mágico
description: Actividad de evaluación continua 3
comments: false
mathjax: true
---


Vamos a plantear un problema para resolver con búsquedas:

Supongamos que quiero trasladarme desde la posición discreta $1$ hasta la posición discreta $N$ en una vía
recta. Puedo trasladarme de dos maneras:

1. A pie, desde el punto $x$ hasta el punto $x + 1$ en un tiempo de 1 minuto.
2. Usando un camión mágico, desde el punto $x$ hasta el punto $2x$ con un tiempo de 2 minutos.

Mi problema es establecer un plan para ir desde el punto $1$ hasta el punto $N$ en el menor tiempo posible.

Desarrolla en un archivo `camion-magico.py` lo siguiente:

1. ¿Cual es el modelo discreto determinista del proceso? Desarróllalo.
2. ¿Cual es el problema de búsqueda a resolver? Desarrolla el problema
3. ¿Cuantos nodos revisa si se utiliza una búsqueda con costo uniforme para encontrar la solución para ir a la posición 31,459.
4. Propón una heurística para usar en una búsqueda tipo $A^*$ en este problema.
5. Demuestra (en el mismo archivo, como comentario o como `string`) que la heurística que propones es admisible.
6. Trata de mostrar si podría (o no) la heurística ser consistente.
7. ¿Cuantos nodos se exploran usando el algoritmo $A^*$ y la heurística que propones.
