---
layout: post
title: Evaluación continua
description: Actividades de evaluación continua
mathjax: true
image: assets/images/larga1.jpg
---

Como estrategia de evaluación continua, vamos a hacer una serie de actividades
de evaluación rápidas todas (o casi todas) las semanas. Algunas de estas
actividades serán colaborativas y otras serán para desarrollarlas de forma
individual.

Conforme vaya avanzando el semestre vamos a ir colocando las actividades que
estamos realizando. En esta página vamos a mantener una *bitácora* con las
actividades realizadas y las evaluaciones que vamos realizando.

Las actividades de evaluación continua son trabajos que se espera se realicen en
equipos, o de forma individual con mucha comunicación entre los estudiantes y
con el profesor (e incluso comentando y asesorándose con otros profesores).
Estas actividades tienen como objetivo el poder medir (tanto para los
estudiantes como para el profesor) la comprensión de los temas tratados hasta el
momento. Algunas serán actividades a realizar en la hora de curso, otras serán
actividades para realizar en horas extra clase. La discusión de lo que se ha
hecho en éstas actividades es muy importante para completar la comprensión de
los temas vistos.

### Actividad 1: Programación en python

Durante el curso vamos a hacer varios programas, todos en *python* por lo que es
necesario conocer los aspectos básicos de programación en python (en la versión
3.X).

Descargue el [siguiente archivo con ejercicios en
python](https://github.com/IA-UNISON/material/raw/master/examenes-rapidos/examen%20rápido%201/examen-rapido-01.pdf)
y resuelve todos los ejercicios. Fecha límite de entrega *21 de enero de 2019*.
Este ejercicio es el mismo desde hace varios semestres, procura no copiarlo, ya
que van a ser muy importante las habilidades de programación en python en el
resto del curso.

Los trabajos hay que guardarlos en un archivo con el nombre
`continua1_apellido.py` donde obviamente `apellido` se sustituye por su primer
apellido. Ese archivo me lo deben de enviar a mi correo electrónico
(juliowaissman@unison.mx) con el asunto *Actividad continua 1*.


Algunas consideraciones (en forma genérica):

1. Por convención las variables y funciones se acostumbra escribirlas en
   minúsculas y con el estilo de guión bajo (`una_variable`), mientras que para
   las clases se utiliza la notación tipo camello (`UnaClase`). No parece gran
   cosa pero mejora mucho la legibilidad del código si nos atenemos a los
   estándares.

2. En lugar de mandar mensajes, cuando ha ocurrido un error es mejor lanzar una
   excepción. Por ejemplo:

```python
if self.ren != otro.col:
	print("No se pueden multiplicar las matrices")
```

es mejor poner

```python
if self.ren != otro.col:
	raise ValueError("No se pueden multiplicar las matrices")
```

3. Es importante procurar cargar todas las librerías que se van a utilizar al
   inicio del módulo, no es mandatorio pero mejora mucho la legibilidad y
   posterior corrección.

4. Solamente se debe poner un constructor (método `__init__`) por clase.


### Actividad 2: Crucigrama de conceptos

Con el fin de revisar los conceptos teóricos sobre la definición e historia de la IA, así como de los agentes racionales, vamos a realizar una dinámica grupal/individual el viernes 25 de enero.

La dinámica es la siguiente:

1. Cada estudiante va a elaborar, en media hora, un pequeño test con 10 enunciados los cuales puedan ser falsos o verdaderos. Los enunciados pueden ser sobre:

   1. Definición de IA y/o agentes racionales
   2. Historia de la IA
   3. Entornos, definición PEAS y/o caracteríaticas de los entornos
   4. Agentes racionales, definición y/o tipos de agentes racionales
   5. Ejemplos de aplicaciones de la IA
   
2. Los estudiantes se van a intercambiar en forma aleatoria los examenes realizados, cada uno tendrá 15 minutos para reponderlo.

3. Los examenes se devuelven a quien los elaboró y los evalúa en 5 min.

4. Tienen 5 min. para explicar (y discutir) en grupos de 6 estudiantes, cuales estuvieron mal contestadas y porqué.

Los exámenes al final deben de llevar el nombre **unicamente** de quien lo elaboró. Como profesor, voy a evaluar lo interesante de los enunciados y el hecho que se encuentren bien evaluados. El estudiante que elaboré el mejor de los examenes a juicio (subjetivo) del profesor, recibirá un estimulo, ya sea como puntos extra en otras actividades de evaluación continua, ya sea como puntos extra en el primer examen parcial, dependiendo de la calidad del trabajo.
 



<!--

### Actividad 2: Crucigrama de conceptos

Con el fin de revisar los conceptos teóricos sobre IA y agentes racionales, se realizó una dinámica grupal,
donde el grupo se dividió en dos y cada equipo desarrolló un crucigrama con conceptos base de IA,
y posteriormente se lo intercambiaron con el otro equipo. Los crucigramas desarrollados fueron los siguientes

**Crucigrama 1**

![](/assets/images/continua/cru1.jpg)

**Crucigrama 2**

![](/assets/images/continua/cru2.jpg)


Los dos equipos hicieron muy buen trabajo (todo se realizó en menos de una hora
que dura el curso los viernes). ¡Felicidades!


### Actividad 3: Inventando un algoritmo metaheurístico

Con el fin de evaluar si se comprendió correctamente la mecánica detrás de los
algoritmos metaheurísticos de búsquedas locales, se dividió el grupo en dos
equipos y cada una va a desarrollar (de manera muy breve) una propuesta de
algoritmo metaheurístico, no importa si es factible, eficiente o funcional (o si
ya existe).

Cada equipo entregará un reporte en $\LaTeX$ lo más concreto posible el cuál
deberá contener lo siguiente:

- ¿Cuál es la metaheurística de donde se inspira?

- ¿Porqué podría pensarse que el algoritmo converge asintóticamente a un mínimo
  global?

- El pseudocódigo en muy grandes rasgos, sin detalles de implementación

A continuación se agregarán los links de ambas propuestas.

- [Algoritmo homo-inspirado](/assets/docs/metaheuristica1.pdf) propuesto por
  Víctor Noriega, Fabián Encinas y Mario Castro

- [Algoritmo de drones](/assets/docs/metaheuristica2.pdf) propuesto por Gilberto
  Espinoza y Jorge Xavier Paredes


| Característica                                                                        | Homo-inspirado | Drones |
|---------------------------------------------------------------------------------------|----------------|--------|
| ¿Explica la inspiración a un proceso de optimización?                                 | si             | si     |
| ¿Explica brevemente porqué piensan que el algoritmo podría tender a un mínimo global? | si             | no     |
| ¿Presenta un pseudocódigo a grandes rasgos del algoritmo?                             | si             | no     |                                                                                      |


Cada actualización de los documentos, implica un cambio en la tabla de
evaluación.


### Actividad 4: Planteando un problema de CSP

Para esta actividad hay que plantear (no resolver) un problema de CSP
particular: La generación de crucigramas.

Tenemos una lista de palabras horizontales $\{w^h_1, \ldots, w^h_n\}$ y una
lista de palabras verticales $\{w^v_1, \ldots, w^v_m\}$, las cuales se van a
colocar en un espacio cuadriculado con $n_max$ columnas y $m_max$ renglones.
Cada palabra está compuesta por una cadena de caractéres, $w = (c_1, \ldots,
c_{len(w)})$.

Para hacer un crucigrama hay que cumplir con las siguientes restricciones:

1. No se pueden traslapar dos palabras horizontales o verticales, ni pueden
   estar en columnas adyacentes si se traslapan.
2. Si se cruzan una palabra vertical con una horizontal, el espacio donde se
   cruzan debe de compartir la misma letra
3. Todas las palabras deben de estar conectadas entre si, con al menos un cruce.

Lo que se pide es proponer un modelo de CSP basado en gráficas de restricciones
respondiendo los siguientes incisos:

1. ¿Cuál es el espacio de estado $X$?
2. ¿Cuál es el dominio de cada una de las variables?
3. ¿Cuales son los vecinos de cada variables?
4. Expresa en forma general cuales son las restricciones binarias?
5. ¿Existen restricciones globales? y de ser el caso ¿Cuáles?

Los documentos con los modelos son los siguientes:

1. [Modelo 1](/assets/docs/cruci1.pdf)
2. [Modelo 2](/assets/docs/cruci2.pdf)

y la evaluación es la siguiente:

| Característica           | Modelo 1 | Modelo 2 |
|--------------------------|----------|----------|
| ¿Espaco de estado?       | si       | si       |
| ¿Dominios?               | si       | si       |
| ¿Vecindades?             | si       | si       |
| ¿Restricciones binarias  | si       | si       |
| ¿Restricciones globales? | si       | si       |



### Actividad 5: Desarrollando heurísticas admisibles

Desarrolla los ejercicios que se encuentran en el documento de [evaluación
contínua 5](/assets/docs/continua_5.pdf), desarrolla tus respuestas en un
documento en $\LaTeX$. Las respuestas pueden ser realizadas en forma individual
o por equipos. Una vez que todos hayan mandado sus respuestas, vamos a discutir
las heurísticas propuestas en clase.

Las respuestas por equipos se pueden consultar en [este
documento](/assets/docs/busqueda1.pdf) y en [este otro
documento](/assets/docs/busqueda2.pdf).


| Problema 1                       | Equipo 1 | Equipo 2 | Problema 2               | Equipo 1 | Equipo 2 |
|----------------------------------|----------|----------|--------------------------|----------|----------|
| Factor de ramificación           |    si    |   si     | Espacio de estado        |   si     |   si     |
| Estados a profundidad k          |    si    |   si     | Acciones legales         |   si     |   si     |
| Nodos expandidos BFS árboles     |    si    |   si     | Estado sucesor           |   si     |   si     |
| Nodos expandidos BFS grafos      |    si    |   si     | Costo local              |   si     |   si     |
| Nodos expandidos DFS árboles     |    si    |   si     | Cardinalidad de S        |   si     |   si     |
| Nodos expandidos DFS grafos      |    si    |   si     | ¿Heurísticas admisibles? |   si     |   si     |
| Heurística admisibles            |    si    |   si     | Dos heurísticas          |   si     |   si     |
| Nodos expandidos A*              |    si    |   si     | ¿Admisibles?             |   no     |   no     |
| Admisible primer cambio entorno  |    si    |   si     | ¿Dominancia?             |   no     |   si     |
| Admisible segundo cambio entorno |    si    |   si     | ¿Gráfos o árboles?       |   no     |   no     |


## Actividad 6: Busquedas con adversarios: Minimax y poda $\alpha$--$\beta$

Desarrolla los ejercicios que se encuentran en el documento de [evaluación
contínua 6](/assets/docs/continua_6.pdf), desarrolla tus respuestas en un
documento en $\LaTeX$. Las respuestas pueden ser realizadas en forma individual
o por equipos. Una vez que todos hayan mandado sus respuestas, vamos a discutir
los resultados en clase.

## Actividad 7: Modelos gráficos probabilistas

Desarrolla los ejercicios que se encuentran en el documento de [evaluación
contínua 7](/assets/docs/continua_7.pdf), desarrolla tus respuestas en un
documento en $\LaTeX$. Las respuestas pueden ser realizadas en forma individual
o por equipos. Una vez que todos hayan mandado sus respuestas, vamos a discutir
los resultados en clase.

## Actividad 8: Introducción a `numpy` y `matlotlib`

Para poder aplicar las bibliotecas de aprendizaje automático en *python* es necesario
cnocer y dominar 3 tecnologías: *jupyter* como un medio de programación literal en python, 
`numpy` como biblioteca matemática básica en el *stack* científico de *python* y `matplotlib`
como la biblioteca de base para graficación. 

Como actividad continua se deja la solución de una *libreta-tutorial* que desarrollé, para la cual hay
que instalar algunos modulos especializados (si instalaste la versión de *Anaconda* de *python* ya viene todo lo que necesitas). La libreta se puede descargar [aqui](https://nbviewer.jupyter.org/github/IA-UNISON/IA-UNISON.github.io/blob/master/assets/docs/intro_numpy.ipynb).

Si requieres información sobre *jupyter* [aqui te dejo la liga a un tutorial que hice hace algo de tiempo](https://juliowaissman.github.io/jupyter-intro).

## Actividad 8: Introducción a `pandas`

Para manipular datos en python, la mejor (y la más popular) de las bibliotecas que existen es `pandas`. En `pandas` se dedinen objetos tipi `DataFrame` y `Series` que permiten manejar los datos en forma sencilla, y como ambas clases heredan de `numpy.ndarray`, mantienen compatibilidad para ser usadas dentro de `scikit-learn` y otras bibliotecas de aprendizaje automático.  

Como actividad continua se deja la solución de una *libreta-tutorial* que desarrollé, para la cual hay
que instalar algunos modulos especializados (si instalaste la versión de *Anaconda* de *python* ya viene todo lo que necesitas). La libreta se puede descargar [aqui](/assets/docs/intro_pandas.ipynb). Para desarrollar la libreta es necesario descargar una tabla de datos en formato csv sobre [transito de bicicletas](/assets/docs/bikes.csv).

-->
