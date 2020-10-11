---
layout: post
title:  "Método de Taylor"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---

**Teorema de Taylor**
Supongamos que $f\in C^n[a,b]$ y $f^{n+1}$ existe en $[a,b]$. Sea $x_o\in[a,b]$ para todo $x\in[a,b]$, existe $\xi(x)$ entre $x_0^x$

$f(x)=P_n(x)+R_n(x)$
Donde
$P_n(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)+...+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n=$
$R_n(x)=\frac{f^{(n+1)}(\xi(x))}{n+1!}(x-x_0)^{n+1}$
$=\sum^n_{k=0} \frac{f^{(k)}(x_0)}{k!}(x-x_0)^k$
________
Suponga que la función $f$ es continuamente diferenciable dos veces en el intervalo cerrado $[a,b]$, es decir, $f\in C^2[a,b]$, sea $x̄\in[a,b]$, una aproximación a $P$, tal que $f'(x̄)\neq0$ y $|x̄-p|$ es "pequeño". 
$f(x)=f(x̄)+(x-x̄)f'(x̄)+\frac{(x-x̄)^2}{2}f'(\xi(x))$, $x<\xi(x)<x̄$
como $f(p)=0$
$0=f(x̄)+(p-x̄)f'(x)+\frac{(p-)^2}{2}f'(\xi(x))$, 
$f(x̄)+(p-x̄)f'(x̄) \approx0$
$f(x̄)+pf'(x̄)-x̄f'(x̄) \approx0$
$pf'(x̄)\approx x̄f'(x̄)-f(x̄)$
$p\approx \frac{x̄f'(x̄)-f(x̄)}{f'(x̄)}$
$p\approx \frac{x̄f'(x̄)}{f'(x̄)}-\frac{f(x̄)}{f'(x̄)}$ $\approx x̄-\frac{f(x̄)}{f'(x̄)}$
Una sucesión ${p_n}$ definida por:
$p_n=p_{n-1}\frac{f(p_{n-1})}{f'(p_{n-1)}}$ donde $n>1$

**Teorema**
Sea $f\in C^2[a,b]$. Si $p\in[a,b]$, es tal que $f(p)=0$ y $f(p)\neq0$, entonces existe $\delta>0$ tal que el *Método de Newton* genrea una sucesión $(p)^\infty n=1$ que converge a $p$ para cualquier aproximación inicial $p_0 \in[p-\delta_1p+\delta]$
