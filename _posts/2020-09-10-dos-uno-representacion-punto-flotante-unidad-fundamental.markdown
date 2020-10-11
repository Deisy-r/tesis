---
layout: post
title:  "Unidad Fundamental"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---

*La unidad Fundamental*

Normalización de un numero: un número **“X”** está escrito en su forma normalizada si **“X”** está escrito en la siguiente forma: $$ x= \delta (u.d_1d_2d_3...d_p)_b. b^e$$

Donde  $\delta$ es el signo $(+1)$ si es positivo; $(-1)$ si es negativo, para $$0 \leq d_i \leq b - 1$$siendo $d_i \neq 0$ y $e$ es la característica. Por su puesto lo ubicado dentro del paréntesis es la mantisa.
La mantisa denota: $\frac{d_1}{b_1}$...$+\frac{d_p}{b_p}$ , es decir su parte fraccionaria. 
El entero $P$ denota la cantidad de dígitos de precisión y $e$ el entero tal que esta: $L\neq e \neq U$  siendo $L$ el exponente más pequeño que pueda tomar y $U$ el más grande.
Signo = 1 bit | Exponencial = 7 bits | Mantisa = 24 bits
---| ---|---|

Los números en punto flotante llamados también números reales, tienen decimales intercalados.
Tales números almacenan y procesan en sus formas exponenciales y binarios. 
La localización se memoria se divide comúnmente en 3 campos o bloques de bits. 
Un campo, el primer bit, se reserva para el primer número. Un segundo campo para el exponente del número y el ultimo campo para la mantisa. 
*Ejemplo:*
Representa el número -0,00523 en una palabra de 16 bits siendo b=10.
*Solución:* primero hay que normalizar el numero 
$$-0,00523 = (-1)(0,523)_10 10^2$$
1 | 1 | 2 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 5 | 2 | 3

 Se pone *“1”* porque el $\delta$ es negativo
Si fuese positivo se coloca *“0”*

