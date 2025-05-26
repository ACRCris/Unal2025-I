**Teorema**

Para todo $m,n \geq 2$ tenemos que:

$$
\begin{align*}
R(n,m) \leq \binom{n+m-2}{m-1}
\end{align*}
$$

Luego 

$$
\begin{align*}
R(n,n) \leq \binom{2n-2}{n-1} \leq 4^{n-1}
\end{align*}
$$

Realizando induccion sobre $p=m+n$

$$
\begin{align*}
    R(n,m) &\leq R(n-1,m) + R(n,m-1)\leq 
    \binom{n-1+m-2}{n-2} + \binom{n+m-1-2}{n-2}\\
     &=\binom{n+n+3}{n-2}+\binom{n+n+3}{n-2} = \binom{n+n-2}{n-1}
\end{align*}
$$

# Identidades combianotrias: Caminos en el plano - Numero de catalan

Existen otras formas de pensar en coeficiente binomial como por ejemplo en terminos de caminos. De un vertice a otro cuales el menor camino que puedo tomar? cuantas caminos hay>


Si notamos $H(m,n)$ es el numero de caminos reticulares que inician en $(0,0)$ y terminan en $(m,n)$, y utilizan unicamente pasos $(1,0)$(ir hacia derecha) y $(0,1)$(ir hacia arriba). Por ejemplo 

$$
\begin{align*}
H(1,2)=3\\
H(2,1)=3\\
\end{align*}
$$

**Proposicion**

Para todo $m,k \geq 0$ se cumple que:

$$
H(m,n) = \binom{m+n}{m} = \binom{m+n}{n}
$$

A cada camino se le puede asociar una secuencia de letras $x$ y $y$ donde $x$ representa un paso hacia la derecha y $y$ un paso hacia arriba. Asi contar todos los caminos equivale a contar palabras sobre  $\{x,y\}^*$ de longitud $m+n$ que tales que hay $n$ letras $x$ y $m$ letras $y$. Por

Puedo intepretar la los coeficiente de la expacion binomial $\binom{n}{k} x^n y^{n-k}$ como el numero de caminos al punto $(n+k,k)$.

**Teorema (identidad del palo de Hockey)**

Para todo $n,m \geq 0$ se cumple que:

$$
\begin{align*}
\sum_{k=0}^{n} \binom{k}{m} = \binom{n+1}{m+1}
\end{align*}
$$

**Demostracion**

$$
\begin{align*}
\binom{n+1}{m+1} 
\end{align*}
$$

Es el numero de caminos reticualares que inician en $(0,0)$ y terminan en $(n-m,m+1)$, ahora sea $P_c=(j,m+1)$ donde $0\leq j \leq (n-m)$  el primer cpunto del camino de altura $m+1$. Sea $P_c'$ el punto que esta por debajo de de $P_c$ (distancia 1), asi todo camino $C$ de $(0,0)$ u termina en $(n-m,m+1)$, esta dividido en dos tramos.

1. (0,0) a $P_c= (j,m)$, para llegar a este punto hay $\binom{j+m}{m}$  caminos
2. $P_c \to P_c' \to \dots \to (n-m,m+1)$

Sumando sobre $j$ tenemos que 
$$
\begin{align*}
\sum_{j=0}^{n-m} \binom{j+m}{m} = \sum_{j=m}^{n} \binom{j}{m} = \binom{n+1}{m+1}
\end{align*}
$$

**Teorema**

Para todo $n \geq 0$ se cumple que:
DE
$$
\begin{align*}
\sum_{k=0}^{n} \binom{n}{k}^2 = \binom{2n}{n}
\end{align*}
$$

**Demostracion**

$$
\begin{align*}
\binom{2n}{n} 
\end{align*}
$$

Cuenta caminos reticulares que inician en $(0,0)$ y terminan en $(n,n)$, cualquiera de los caminos  corta exactamente un punto en la recta $y=n-x$.

Sea $P_c = (k,n-k)$ este punto, $0\leq k \leq n$, Debemos contar cominos de $(0,0)$ a $P_c$ y de $P_c$ a $(n,n)$. Asi

1)
$$
\begin{align*}
\binom{n}{m-k} = \binom{n}{k}
\end{align*}
$$

2)
$$
\begin{align*}
\binom{n-k+k}{k} = \binom{n}{k}
\end{align*}
$$

PM y PA,

$$
\begin{align*}
\sum_{k=0} \binom{n}{k}^2 = \binom{2n}{n}
\end{align*}
$$

## Demostracion de aperi

$$
\begin{align*}
\sum_{n}\binom{n}{i} = 2^n
\end{align*}
$$

$$
\begin{align*}
\sum_{i=0}^{n} \binom{n}{i}^3 = ?
\end{align*}
$$

$$
\sum_{i,j,k} x_{ij}= *
$$
es cerrada cuando $*$ es un termino hipergeometrico.

Existe un algoritmo que demuestra que $A=B$. Wilp - Zelbergar.

(Experimental mathematics zelbergar),para entrar al zoom en vivo es un numero de catalan.


Para cada camino le pueda asociar un peso relacionado con el area debajo de la curva, la version discreta del calculo integral.

## Numeros de catalan

**Definicion**

Un camino de Dyck es un camino retucular que inicia en $(0,0)$ y termina en el punto $(n,n)$ tal que nunca pasa por encima de la recta $y=x$ 


$D_n$ denota el numero de caminos de Dyck de longitud $n$. $C_n = |D_n|$ es el $n$-esimo numero de catalan.

Se puede utilizar en votaciones para determinar las formas en la que las votaciones pueden no pasar cierto umbral. El problema del votante es variar la recta.

**Teorema**

Para todo $n \geq 0$ se cumple que:

$$
\begin{align*}
C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i}
\end{align*}
$$


Con el valor inicial $C_0=1$.

**Demostracion**

Cualquier camino de Dyck arranca con un camino horizontal y termina con un camino vertical. Asi asumo primero un camino de Dyck que no toca la recta, la cantidad de esos caminos es $C_{n}$ que conecta (1,0) y (n+1,n). Ahora si toca la recta, y consideramos el ultimo punto de coordenadas $(k,k)$, donde $0\leq k \leq n$, el numero de caminos a este punto es $C_k$ y hay $C_{n-k}$ caminos de Dyck que van de $(k,k)$ a $(n+1,n)$. Por lo tanto tenemos $C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i}$ caminos de Dyck de longitud $n+1$. cuando sumo por todos los $k's$