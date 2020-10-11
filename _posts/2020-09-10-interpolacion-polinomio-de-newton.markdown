---
layout: post
title:  "Polinomio Interpolante de Newton"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---

*Polinomio Interpolante de Newton*
Este método es algorítmico y resulta sumamente como en determinados casos, sobre todo cuando se requiere calcular un polinomio interpolador de grado elevado.
Para un polinomio de *n-esimo* orden se requiere de $(x_0,f(x_0)), (x_1,f(x_1)), ..., (x_n,f(x_n))$. Con la Siguiente formula: 

$P_n(x)=b_0+b_1(x-x_0)+b_2(x-x_0)(x-x_1)+b_n(x-x_0)(x-x_1)...(x-x_{n-1})$
$P_n(x)=b_0+\sum^n_{i=1}b_i(\pi^{i=1}_{j-1}(x-x_j))$

Estos coeficientes se calculan mediante diferencias divididas cuya expresión general esta dada por:

$f[x_i,...,x_i+j+1]=\frac {f[x_{i+1},...,x_i+j+1]-f[x_i,...,x_i+j]}{x_i+j+1-x_i}$

Como se ve en la formula, la diferencia dividida se calcula de modo recursivo usando coeficientes anteriores. Una vez se halla realizado cada uno de los cálculos, notara que hay muchas mas diferencias divididas que coeficientes $b_i$. 

El cálculo de todos los términos intermedios debe realizarse simplemente porque son necesarios para poder formar todos los términos finales. 

La construcción del polinomio interpolador son aquellos que involucren a $x_0$. 
$b_0=f[x_0], b_1=f[x_0,x_1],...,b_i=f[x_0,x_1,...,x_i]$

Con esta notación podemos expresar el polinomio $p_n(x)$ con:
$p_n(x)=[x_0]+f[x_0,x_1](x-x_0)+f[x_0,x_1,...,x_n](x-x_0)(x-x_1)...(x-x_{n-1})$

A esta ecuación se conoce con el nombre de *Formula de diferencias Divididas Interpolantes de Newton* 
___
*Ejemplo:* Determine el polinomio Interpolante de Newton que contiene los puntos $(-3,9),(5,2),(7,-1)$ y $(8,0)$.

*Solución:*
| $x_i$  | $y_i$   | $b_1$  | $b_2$   |$b_3$   |
|--|--|--|--|--|
| -3 | 9 | $\frac{-7}{8}$ |$\frac{-1}{16}$  | $\frac{-43}{528}$   
| 5 | 2 |$\frac{-3}{2}$| $\frac{5}{6}$
| 7 |-1  |1
| 8 | 0 |

Para entender el algoritmo del polinomio interpolante de newton mediante las diferencias divididas, hagamos la construcción por niveles o columnas.

Nivel $b_1=\frac{2-9}{5-(-3)}=\frac{-7}{8}$, $\frac{(-1)-2}{7-5}=\frac{-3}{2}$,  $\frac{0-(-1)}{8-7}=\frac{1}{1}=1$

Nivel $b_2=\frac{\frac{-3}{2}-\frac{-7}{8}}{7-(-3)}
=\frac{\frac{-5}{8}}{10}=\frac{-1}{16}$,  $\frac{1-\frac{-3}{2}}{8-5}=\frac{\frac{5}{2}}{3}=\frac{5}{6}$

Nivel $b_3=\frac{\frac{-1}{16}-\frac{5}{6}}{8-(-3)}
=\frac{\frac{-43}{48}}{11}=\frac{-43}{528}$
