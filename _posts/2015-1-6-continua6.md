---
layout: post
title: 6. Diversión con CSPs
description: Actividad de evaluación continua 6
comments: true
mathjax: true
---

## En *Esperanza*

En *Esperanza* viven 4 familias: los Sosa, los Waissman, los Yeomans y los Gutú, en casa próximas, numeradas 101, 102, 103 y 104. 

Los Gutú viven en una casa con menor número que los Waissman. Los Waissman viven próximos a los Sosa en una casa con un número mayor. Hay al menos una casa entre los Waissman y los Yeomans. Los Gutú no viven en una casa cuyo número termina en 2. Los Yeomans no viven en una casa cuyo número termina en 4.

Vamos a resolver este problema como si fuera dificil, usando una representación como *CSP*.

1. Define cuales son las variables, y el dominio de cada una de las variables, una vez reducido por las restricciones unarias y los vecinos de cada variable.

2. Escribe en una función en *pseudopython* cuales son las restricciones binarias (todas)

3. Si utilizamos el grado heurístico como método para seleccionar la primera variable ¿Cuál sería la variable?

4. Si utilizamos la variable mas restringida como heurística para las siguientes variables ¿Cuál sería la siguiente variable a seleccionar si se utiliza el método de 1 consistencia? 

5. Si se utiliza el método de 1-consistencia, la selección de variables ya especificada y el ordenamiento de valores por el valor menos restrictivo, ¿Cuántos *backtrackings* se realizan para tener la asignación completa? 

## Un cuadrado mágico

Un cuadrado mágico es una matriz de $n \times n$ de números enteros positivos, todos diferentes, tal que la suma de cada uno de sus renglones, cada una de sus columnas y las dos diagonales principales sumen el mismo número. Vamos a plantear el problema como un CSP binario.

1. Define las variables ($X$), el dominio de cada variables ($D$) y los vecinos de cada variable ($N$) para un problema genérico de un cuadrado mágico de $n \times n$.

2. Basado en tu definición, y haciendo uso de las heurísticas vistas en clase. Decide si vas a utilizar *1-consistencia* o *2-consistencia* y representa gráficamente el árbol primero en profundidad que se genera para resolver un cuadrado mágico de $3 \times 3$. La originalidad y claridad para presentar el proceso es muy importante.


<!-- 
## 1. Algoritmos metaheurísticos

Los [algortimos metaheurísticos de acuerdo a wikipedia]() son *métodos de búsquedas locales para resolver un tipo de problema general, usando los parámetros dados por el usuario sobre unos procedimientos genéricos y abstractos de una manera que se espera eficiente.*  

Las metaheurísticas generalmente se aplican a problemas que, por su naturaleza, no tienen un algoritmo específico que dé una solución satisfactorio. Las metaheurísticas no son la panacea y suelen ser menos eficientes que los algoritmos de optimización para usos específico, por lo que solo es eficiente usarlos en problemas realmente dificiles.

En [éste arttículo de Blum y Roli del 2003](https://www.iiia.csic.es/~christian.blum/downloads/blum_roli_2003.pdf) los autores presentan un marco general de los algoritmos metaheurísticos y algunos de los pseudocódigos de las metaheurísticas más populares. Por supuesto, además de estas heurísticas hay algunas bastante sorprendentes, como algunas de las listadas en [ésta página de wikipedia](https://en.wikipedia.org/wiki/List_of_metaphor-based_metaheuristics), o como el algoritmo [*Anarchic Society Optimization (ASO) Algorithm*](https://link.springer.com/chapter/10.1007/978-981-10-5221-7_4), o (en una posición completamente opuesta) el [*Imperialist Competitive Algorithm*](https://www.sciencedirect.com/science/article/pii/S1568494614003895?via%3Dihub). Estos dos artículos sólo los vas a poder consultar dentro de la UNISON gracias a las bases de datos que tiene a nuestra disposición la Universidad.


En la siguiente imagen de wikipedia se puede observar una clasificación general de estos algoritmos:

![](https://upload.wikimedia.org/wikipedia/commons/2/26/Metaheur%C3%ADsticas_clasificación.png)


## 2. Planteamiento del problema

Una vez que se realizó una revisión rápida de algunos algoritmos o su inspiración, por equipos (o individualmente) se deberá proponer un algoritmo basado en una metaheurística inventada (utilizando alguna metáfora aunque sea muy forzada). Lo importante aqui es tener en cuenta dos detalles: la aleatoreidad en la búsqueda y guardar siempre el mejor mínimo encontrado hasta el momento. 

Sean creativos, no es importante su funcionalidad, solo reforzar los principios básicos en los que se basan las búsquedas locales con metaheurísticas.

Se debe de presentar: 

1. Una descripción, un pseudocódigo o un diagrama de flujo que muestre en términos generales como funcionaría el algoritmo. 

2. Cuales son los parámetros que puede modificar el usuario.

3. Las razones por las que piensas que la probabilidad que el algoritmo encuentre un mínimo global tiende a 1 conforme se realizan iteraciones, si los parámetros de ajusta están bien seleccionados. 

Por supuesto, el reporte debe de ser enviado en $\LaTeX$.

Compartan información e ideas. Utilicen por favor el foro de este post para compartir ideas de posbles metaheurísticas y dudas.
 -->
