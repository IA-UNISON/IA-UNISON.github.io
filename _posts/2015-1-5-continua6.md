---
layout: post
title: 8. Jugando al BlackJack
description: Actividad de evaluación continua 8
comments: true
mathjax: true
---


## Simulación de Blackjack para Aprendizaje por Refuerzo

### Descripción del Entorno

El objetivo es modelar el juego de Blackjack simplificado (siguiendo las reglas estándar de los casinos pero sin opciones complejas como *split* o *double down* inicialmente) como un **Proceso de Decisión de Markov (MDP)** pero para ser simulado, lo que lo hace más simple.

**Reglas Base:**

* **Baraja:** Infinita (con reemplazo) para simplificar las probabilidades.
* **Valores:** Las figuras (J, Q, K) valen 10. El As vale 1 u 11 (es "usable" si puede valer 11 sin que el jugador se pase de 21).
* **El Crupier (Dealer):** Sigue una política fija: pide carta (*hit*) si su suma es menor a 17 y se planta (*stand*) si es 17 o más.


### Definición de los Componentes del MDP

#### Espacio de Estados ($S$)

Para que el agente tome decisiones óptimas, no necesita conocer toda la historia, solo la información crítica actual. El estado se define como una tupla:

$$s = (\text{Suma Jugador}, \text{Carta Visible Crupier}, \text{As Usable})$$

* **Suma del Jugador:** Entero entre 12 y 21. (Si es $< 12$, el jugador siempre debería pedir carta, por lo que se suele simplificar el aprendizaje a este rango).
* **Carta Visible del Crupier:** Entero del 1 al 10 (donde 1 representa al As).
* **As Usable:** Booleano (Verdadero/Falso).

¿Cual es la cardinalidad del espacio de estado?

#### Espacio de Acciones ($A$)

En cada estado, el agente puede elegir entre dos acciones discretas:

1. **Plantarse (0 - Stand):** El jugador termina su turno y se compara su suma con la del crupier.
2. **Pedir (1 - Hit):** El jugador recibe una carta adicional.

¿Como se puede encontrar las acciones legales en cada estado?

#### Dinámica y Estados Terminales

El juego termina (estado terminal `True`) cuando:

1. El jugador elige **Plantarse**.
2. El jugador elige **Pedir** y su suma supera 21 (derrota inmediata).
3. Se alcanza un Blackjack natural.


#### Función de Recompensa ($R$)

La recompensa en cada estado no terminal es 0.

Se otorga únicamente al final del episodio (estado terminal) un valor como sigue:

* **+1:** El jugador gana.
* **0:** Empate (*Push*).
* **-1:** El jugador pierde o se pasa (*Bust*).
* **+1.5:** Victoria por Blackjack natural (21 con las dos primeras cartas).

### A desarrollar

Propon como hacer los siguientes métodos:

1. **`estado_inicial(self)`**:
* Reinicia el mazo y reparte dos cartas al jugador y dos al crupier (una oculta).
* Calcula el estado inicial $s_0$.
* Verifica si hay Blackjack natural inmediato.

2. **`acciones_legales(self, s)`**:

3. **`sucesor(self, s, a)`**:
* Recibe la acción del agente $$a$$.
* Si es **Hit**: Reparte carta, actualiza la suma y verifica si se pasó de 21.
* Si es **Stand**: Ejecuta el turno del crupier (pedir hasta llegar a $\geq 17$) y determina quién ganó.
* Retorna el siguiente estado $s'$, la recompensa.

4. **`recompensa(self, s, a, s_p)`**:
* Recibe la acción del agente $$a$$.
* Si es **Hit**: Verifica si se pasó de 21 y si devuelve 0 o -1 segun el caso.
* Si es **Stand**: Ejecuta el turno del crupier (pedir hasta llegar a $\geq 17$) y determina quién ganó.

5. **`reparte_carta()`**:
* Función auxiliar que devuelve un valor aleatorio entre 1 y 10 (con probabilidad $4/13$ para el valor 10).


### La Lógica del As Usable

Este es el punto donde los estudiantes suelen fallar. Es fundamental implementar una función que:

* Contabilice el As como 11 si no excede 21.
* Si la suma excede 21 y se tiene un As de valor 11, lo transforme automáticamente a valor 1 y cambie el estado a `As Usable = False`.
