---
layout: post
title: 1. Programación en python
description: Actividad de evaluación continua 1
comments: true
mathjax: true
---


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


