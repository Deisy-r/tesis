---
layout: post
title:  "Polinomio Interpolante de Lagrange"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---

*Polinomio Interpolante de Lagrange*
En análisis numérico el polinomio de Lagrange, interpola un conjunto de puntos dados en forma de Lagrange.

La reformulación del polinomio de Newton que evita el calculo por diferencias divididas es la siguiente: 
$f_n(x)=\sum^n_{i=0}L_i(x)f(x_i)$ donde $L_i(x)=\pi^n_{i=0,j\neq i}\frac{x-x_j}{x_i-x_j}$.

**Teorema**
Si $x_0,x_1,...,x_n$ son distintos en el intervalo $[a,b]$ y si  $f\in C^{n+1}[a,b]$ entonces para cada $x\in[a,b]$ existe un número $\xi(x)$ en $(a,b)$ tal que $f(x)=p(x)+\frac{f^{n+1}(\xi(x))}{(n+1)!}(x-x_0)(x-x_1)...(x-x_n)$

Donde $P$ es el polinomio interpolante dado el siguiente: 

$p(x)=f(x_0)L_{n,0}(x)+...+f(x_n)L_{n,n}(x)=$

$\sum^n_{k=0}f(x_k)L_{n,k(x)}$
