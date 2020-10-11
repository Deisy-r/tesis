---
layout: post
title:  "Interpolación y Diferencias Divididas"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---
*DIFERENCIAS DIVIDIDAS*
Supongamos que $P_n$ es un polinomio de lagrange de grado $n$ que coincide con la función $f$ con los números distintos $x_0,x_1,x_2,...,x_n$. Se pueden derivar que $p_n$ tiene la siguiente representación: 
$P_n(x)=a_0+a_1(x-x_0)+a_2(x-x_0)(x-x_1)+...+a_n(x-x_0)(x-x_1)...(x-x_{n-1})$
Simultáneamente cuando $P_n$ se evalúa en $x_1$ los únicos términos distintos de cero en la evaluación $P_n(x_1)$  
$f(x_0)+a_2(x_1-x_0)\equiv P_n(x_1)=f(x_1)$
Así despejando las constantes
$a_1(x_1-x_0)=f(x_1)-f(x_0)$
$a_1=\frac {f(x_1)-f(x_0)}{x_1-x_0}$
Así que introducimos lo que se conoce como *notación de diferencias divididas*
La diferencia dividida $0$ (cero) de la función $f$ con respecto a $x_1$ se denota $f[x_1]$, es simplemente la evaluación de $f$ en $x_1$.

Las diferencias divididas restantes se definen inductivamente, la primera diferencia dividida de $f$ con respecto a $x_i$ y $x_{i+1}$, se denota $f[x_i,x_{i+1}]$y esta definida por:
$\frac{f[x_{i+1}]-f[x_i]}{x_{i+1}-x_i}$
