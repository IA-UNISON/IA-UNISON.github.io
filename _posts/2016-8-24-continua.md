---
layout: post
title: Evaluación continua
description: Actividades de evaluación continua
image: assets/images/larga1.jpg
---

Como estrategia de evaluación continua, vamos a hacer una serie de actividades de evaluación rápidas todas (o casi todas) las semanas. Algunas de estas actividades serán colaborativas y otras serán para desarrollarlas de forma individual.

Conforme vaya avanzando el semestre vamos a ir colocando las actividades que estamos realizando.

### Actividad 1: Programación en python

Durante el curso vamos a hacer varios programas, todos en *python* por lo que es necesario conocer los
aspectos básicos de programación en python (en la versión 3.X).

Descargue el [siguiente archivo con ejercicios en python](https://github.com/IA-UNISON/material/raw/master/examenes-rapidos/examen%20rápido%201/examen-rapido-01.pdf) y resuelve todos los ejercicios (se entregó una copia física en clase). Fecha límite de entrega *24 de agosto de 2018*. Este ejercicio es el mismo desde hace un año, procura no copiarlo, ya que van a ser muy importante las habilidades de programación en python en el resto del curso.


Algunas consideraciones visto su trabajo (en forma genérica):

1. Por convención las variables y funciones se acostumbra escribirlas en minúsculas y con el estilo de guión bajo (`una_variable`), mientras que para las clases se utiliza la notación tipo camello (`UnaClase`). No parece gran cosa pero mejora mucho la legibilidad del código si nos atenemos a los estándares.

2. En lugar de mandar mensajes, cuando ha ocurrido un error es mejor lanzar una excepción. Por ejemplo:

```python
if self.ren != otro.col:
	print("No se pueden multiplicar las matrices")
```

es mejor poner

```python
if self.ren != otro.col:
	raise ValueError("No se pueden multiplicar las matrices")
```

3. es importante procurar cargar todas las librerías que se van a utilizar al inicio del módulo, no es mandatorio pero mejora mucho la legibilidad y posterior corrección.

4. Sólamente se debe poner un constructor (método `__init__`) por clase.

5. Los diccionaros son tablas hash, por lo que es importante aprovechar sus ventajas y no hacer una

6. Todo se debe de programar a través de una función y/o clase. El uso de `input` debe evitarse al máximo, y pasar todos los datos como parámetros de una función.

Los resultados son los siguientes:

| Sección | Castro | Encinas | Espinoza | Noriega | Paredes |
|---------|--------|---------|----------|---------|---------|
| 1.1     | bien   | bien    | bien     | bien    | bien    |
| 1.2     | bien   | bien    | bien     | bien    | bien    |
| 2.1     | bien   | bien    | bien     | bien    | bien    |
| 2.2     | mal    | bien    | mal      | bien    | bien    |
| 2.3     | maso   | bien    | maso     | bien    | bien    |
| 3.1     | bien   | bien    | bien     | bien    | mal     |
| 3.2     | bien   | bien    | bien     | bien    | faltó   |
| 3.3     | faltó  | faltó   | maso+    | maso    | maso+   |



### Actividad 2: Crucigrama de conceptos

Con el fin de revisar los conceptos teóricos sobre IA y agentes racionales, se realizó una dinámica grupal,
donde el grupo se dividió en dos y cada equipo desarrolló un crucigrama con conceptos base de IA,
y posteriormente se lo intercambiaron con el otro equipo. Los crucigramas desarrollados fueron los siguientes

**Crucigrama 1**

![](/assets/images/continua/cru1.jpg)

**Crucigrama 2**

![](/assets/images/continua/cru2.jpg)


Los dos equipos hicieron muy buen trabajo (todo se realizó en menos de una hora que dura el curso los viernes). ¡Felicidades!


### Actividad 2: Inventando un algoritmo metaheurístico

Con el fin de evaluar si se comprendió correctamente la mecánica detrás de los algoritmos metaheurísticos de búsquedas locales,
se dividió el grupo en dos equipos y cada una va a desarrollar (de manera muy breve) una propuesta de algoritmo metaheurístico,
no importa si es factible, eficiente o funcional (o si ya existe).

Cada equipo entregará un reporte en $\LaTeX$ lo más concreto posible el cuál deberá contener lo siguiente:

- ¿Cuál es la metaheurística de donde se inspira?

- ¿Porqué podría pensarse que el algoritmo converge asintóticamente a un mínimo global?

- El pseudocódigo en muy grandes rasgos, sin detalles de implementación

A continuación se agregarán los links de ambas propuestas.
