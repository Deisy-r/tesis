---
layout: post
title:  "Representación Entera"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---
**REPRESENTACION ENTERA**
Los enteros o números en punto fijo son números que no tienen punto decimal. Un entero **J** se representa en la memoria de un computador por medio de su forma binaria si son positivos y por medio de su complemento a **2** de su valor absoluto. 
*Ejemplo:*
$4  2  3 = 1 1 0 1 0 0 1 1 1$

0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 1 |

 El computador almacena $-423$ en una localización de memoria, tomando el complemento a $1$ de la anterior representación $423$ y sumándole un $1$ el computador puede saber si un entero **J** en la memoria es positivo o negativo minando el primer digito. 
Si $J=0\rightarrow+$

Si $J=1\rightarrow-$

