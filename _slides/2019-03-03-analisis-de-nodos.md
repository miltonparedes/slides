---
title: análisis de nodos
date: 2019-03-03
category: metodos-numericos
theme: iot
syntax_theme: atom-one-light
---

## Análisis de nodos en circuitos eléctricos

Métodos numéricos en ingeniería

---

### Método de tensiones nodales

Se configura y resuelve un sistema de ecuaciones en el que las incógnitas son los voltajes en los nodos principales del circuito.

Notes:
En este método, configuramos y resolvemos un sistema de ecuaciones en el que las incógnitas son los voltajes en los nodos principales del circuito. A partir de estos voltajes nodales, las corrientes en las diversas ramas del circuito se determinan fácilmente.

---

## Pasos para el análisis de nodos

---

1. Contar y numerar los nodos
2. Identificar los voltajes
3. Elegir un nodo y asignarle un voltaje $0​$

---

4.
Para cada nodo, excepto el nodo de referencia, anotar la **ley de corrientes de Kirchoff**.

$I_a + I_b + I_c = 0$

![Circuito 1](/assets/img/content/circuito.png) <!-- .element: style="padding: 2rem;" -->

Notes:
"La suma algebraica de las corrientes que fluyen desde un nodo es igual a cero"
Por suma algebraica queremos decir que una corriente que fluye en un nodo debe considerarse una corriente negativa que fluye fuera del nodo.

---

5.
Expresar la corriende de cada rama usando la **ley de Ohm**  ($I = \frac{V}{R}$)


### Por ejempo $\to$
<!-- .element: class="fragment" data-fragment-index="1" -->

---


La corriente descendente del nodo 1 depende de la diferencia de voltaje $V1-V2$ y la resistencia en la rama.

![Circuito 2](/assets/img/content/circuito1.png)
<!-- .element: style="padding: 2rem;" -->

---

En este caso, la diferencia de voltaje en la resistencia es $V1 - V2$ menos el voltaje en la fuente de alimentación.

![Circuito 3](/assets/img/content/circuito2.png)
<!-- .element: style="padding: 2rem;" -->

---

En este caso, la diferencia de voltaje a través de la resistencia debe ser 100 voltios mayor que la diferencia $V1 - V2$.

![Circuito 4](/assets/img/content/circuito3.png)
<!-- .element: style="padding: 2rem;" -->

---

6.
Formar, después de la simplificación, un sistema de $m$ ecuaciones lineales en $m$ voltajes nodales desconocidos (donde $m$ es uno menos que el número de nodos; $m = n - 1$).

### Resolver el sistema
<!-- .element: class="fragment" data-fragment-index="1" -->

---

### Ejercicio
![Circuito 5](/assets/img/content/circuito4.png)
<!-- .element: style="padding: 2rem;" -->

---

## Solución

---

Tener en cuenta que el "par de nodos" en la parte inferior es en realidad un nodo extendido.

![Circuito 6](/assets/img/content/circuito5.png)
<!-- .element: style="padding: 2rem;" width="60%" -->

---

$\frac{V_1}{30} + \frac{V_1-100}{5} + \frac{V_1 - V_3}{10} = 0$

$\frac{V_3-V_1}{10} + \frac{V_3}{10} + \frac{V_3}{20} = 0$

### =

$(\frac{1}{30}+\frac{1}{5}+\frac{1}{10})V_1 - (\frac{1}{10})V_3 = \frac{100}{5}$

$-(\frac{1}{10})V_1 + (\frac{1}{10}+\frac{1}{10}+\frac{1}{20})V_3 = 0$
