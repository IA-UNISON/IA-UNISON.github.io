---
layout: post
title: 7. El problema del inventario
description: Actividad de evaluación continua 7
comments: false
mathjax: true
---

## Un problema de inventario

### Contexto del Problema

La empresa *Necroelectronica* distribuye un componente electrónico especializado. Debido a la naturaleza del producto, el gerente de inventario debe decidir cada tarde cuántas unidades pedir al proveedor para maximizar el beneficio a largo plazo.

### Dinámica de Operación

El ciclo de operación sigue una secuencia estrictamente temporal:

1. **Mañana:** Se reciben las unidades que fueron pedidas la tarde anterior (el tiempo de entrega es de 1 día). Estas se incorporan inmediatamente al inventario disponible.
2. **Durante el día:** Ocurre la demanda de los clientes.
3. **Tarde:** Se contabiliza el inventario final, se pagan los costos de almacenamiento o penalizaciones, y se decide la cantidad a pedir para recibir el día siguiente.

### Parámetros y Valores Realistas

Para el modelado, considera los siguientes datos:

* **Capacidad de Almacén:** El estante tiene una capacidad máxima de **20 unidades**. No se pueden almacenar más unidades.
* **Comportamiento de la Demanda ($D$):** La demanda diaria sigue una **Distribución de Poisson** con una media de $\lambda = 4$ unidades/día.
* **Estructura de Costos y Ganancias:**
  * **Precio de Venta:** $150.00 por unidad vendida.
  * **Costo de Compra:** $80.00 por unidad pedida al proveedor.
  * **Costo Fijo de Pedido:** $40.00 por cada pedido realizado (independientemente de la cantidad, siempre que sea $> 0$).
  * **Costo de Almacenamiento:** $5.00 por cada unidad que se quede en el estante al final del día.
  * **Costo de Backlogging (Inventario Negativo):** Si la demanda supera las existencias, los clientes aceptan esperar, pero la empresa incurre en un costo de "buena voluntad" y logística de **$15.00 por unidad faltante** al final del día.
  * **Pérdida por Demanda no Satisfecha:** Además del costo de backlogging, cada unidad demandada que no puede entregarse en el momento representa una pérdida de oportunidad (margen no ganado).

### ¿Qué hacer?

A partir del escenario anterior, define formalmente los elementos del MDP:

1. **Espacio de Estados ($S$):** Define el rango de valores posibles para el inventario al final del día. Considera si el estado puede ser negativo (backlogging).
2. **Espacio de Acciones ($A$):** Define qué decisiones puede tomar el gerente por la tarde y qué restricciones existen respecto a la capacidad del almacén.
3. **Probabilidades de Transición ($T$):** Escribe la expresión para calcular \(T(s, a, s') = \Pr[s' | s, a] \) utilizando la función de probabilidad de Poisson:

$$ f(k; \lambda) = \frac{e^{-\lambda} \lambda^k}{k!} $$



4. **Función de Recompensa ($R$):** Construye la ecuación de recompensa inmediata $R(s, a)$ que incluya los ingresos por ventas, los costos de pedido (fijos y variables), los costos de mantenimiento y las penalizaciones por faltantes.


### Notas para la resolución

* Recuerda que el inventario disponible para satisfacer la demanda del día $t$ es la suma del inventario que quedó al final del día $t-1$ más el pedido realizado esa misma tarde.

* Para efectos de cómputo, puedes truncar la distribución de Poisson en un valor donde la probabilidad acumulada sea cercana a 1.
