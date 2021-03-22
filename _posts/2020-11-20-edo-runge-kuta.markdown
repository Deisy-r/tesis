---
layout: post
title:  "Métodos Númericos de Runge Kutta"
date:   2020-11-20 18:51:43 -0400
categories: edo
tag: 5
---

	El método de Runge- Kutta utiliza indirectamente el *algoritmo de Taylor*. En general, estos métodos evalúan {% katex %}f(x,y){% endkatex %} en más de un punto en la proximidad de {% katex %}(x_n,y_n){% endkatex %} en lugar de evaluar derivadas de {% katex %}f(x,y){% endkatex %}, las cuales se necesitarían para el uso directo del algoritmo por series de Taylor.


La derivación de estos métodos se acompaña de la suposición de un algoritmo particular con ciertos coeficientes indeterminados. Los valores de estos términos constantes se encuentran igualando la fórmula de Runge-Kutta de orden {% katex %}p{% endkatex %} al algoritmo de Taylor de orden {% katex %}p{% endkatex %}. La idea general es sustituir el problema de valor inicial: 

![runge kutta](/assets/images/runge kutta 1.png)

Por la ecuación integral equivalente:

![kutta](/assets/images/runge kutta 2.png)

Para proceder a aproximar esta última integral mediante un método numérico adecuado (recordemos que {% katex %}y(x){% endkatex %} es desconocida). Si nuevamente planteamos el problema “paso a paso” tendremos: 

{% katex display %}
	y_{n+1}=y_n+ \int ^{x_n+1} _{x_n}f(x,y(x))d_x
{% endkatex %}

**Método de Runge-Kutta de Cuarto Orden**

	Son muy utilizados porque son sencillos de programar y porque poseen una relación exactitud-coste óptima. El desarrollo de estas fórmulas se inició con el trabajo de *Carl Runge en 1895* y lo continuo *M. Kutta en 1901*. 
	Se deducen de una manera similar a la de tercer orden, con la diferencia que se introduce un nuevo paso intermedio en la evaluación de la derivada. El mas habitual es el determinado por las formulas siguientes: 


![4to](/assets/images/4to orden.png)


	Que al igual que el método de tercer orden está basado en el *método de interacción de Simpson*. Los errores local y global son en este caos proporcionales a {% katex %}h^5{% endkatex %}y  {% katex %}h^4{% endkatex %} respectivamente. 
