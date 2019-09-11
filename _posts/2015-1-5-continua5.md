---
layout: post
title: 5. Haciendo crucigramas
description: Actividad de evaluación continua 5
comments: true
mathjax: true
---

## 1. ¿Qué hacer? ¿Qué entregar?

Plantear un problema de satisfacción de restricciones, de ser posible en forma de grafo de restricción.

Para esto, les pido, un documento en formato $\LaTeX$ (artículo) el cual venga lo siguiente:

1. Planteamiento del problema

2. Variables a utilizar (incluyendo variables auxiliares)

3. Dominio de cada variable (incluyendo las auxiliares)

4. Vecinos (relaciones binarias entre variables)

5. Restricciones unarias (para reducción de dominios)

6. Restricciones binarias

7. Restricciones globales (si no se pudo plantear en forma de restricciones binarias todo)

8. Referencias (si tomaste la idea de alguna página, artículo o libro, o combinación)


## 2. Planteamiento del problema

Se tienen $K$ palabras, las cuales son `strings` en `python` 
$$
w_1, w_2, \ldots, w_K
$$

y una cuadricula de dimensiones $N \times M$ donde la casilla $(1,1)$ es la casilla superior izquierda y la casilla $(N, M)$ 
es la casilla inferior derecha.

Se quiere encntrar un acomodo de las palabras en forma de crucigrama, dentro de las casillas (si es que es posible). Esto es:

1. Todas las palabras tienen una posicion inicial y una orientación (horizontales o verticales). 

2. Dos palabras con la misma orientación no se pueden translapar

3. Todas las palabras caben completas en la cuadricula (no se sale parte de la palabra de la cuadrícula).

4. Si dos palabras con orientación diferente se cruzan en algun punto, entonces en ese punto la letra debe de ser la misma.

5. Todas las palabras se cruzan al menos con otra palabra

6. Se puede ir, a través de los cruces, de cualquier palabra a cualquier otra



