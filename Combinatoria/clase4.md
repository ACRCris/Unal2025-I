## Las torres de Hanoi

En el problema de las torres, la recursion no esta bien

## Teseleaciones 

Para un la teselacion de tamanio $n\times 1$ se tiene que:

$$
\begin{align*}
t_n = F_{n+1}
\end{align*}
$$

Cual es el numero de formas de teselar una cinta de tamano $n\times 1$ con cuadrados $1\times 1$ y rectangulos $2\times 1$? 

![alt text](image-3.png)


$t_n{n-1} t_{m-1}$ reperesenta el caso den donde el domino que entre la cinta de 1xn y la cinta de 1xm,

$t_n t_{m}$ reperesenta el caso en el que no hay domino que entre la cinta de 1xn y la cinta de 1xm,


Claramente estos casos son distyuntos, por lo que se debe aplicar el principio de la suma,

-------

**Ejemplo**(Numero de divisores)


Sea $n$ un entero positivo. La funcion $\tau(n)$, se define como la cantidad de divisiores de $n$


$$
\tau(2021) = 4
$$

$$
\begin{align*}
\tau(p) = 2
\end{align*}
$$

si $p$ es primo.


Si $n\geq 2$, se tiene que:

$$
\begin{align*}
n =\begin{cases}
\text{primo} \\
p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k} & \text{si } n \text{ es compuesto}
\end{cases}
\end{align*}
$$

si $n$ es compuesto, aplicamos el principio de la multiplicacion, y tenemos que:

$$
\begin{align*}
\tau(n) = (a_1+1)(a_2+1)\cdots (a_k+1)
\end{align*}
$$

Revisar las notas de sistemas numericos en las que desarrolle el ejercio.

## Bumero de funciones 

Cuantas funciones se pueden definir de $A$ en $B$ si $|A|=m$ y $|B|=n$? son $n^m$ y se resuelve por el principio de la multiplicacion:

$a_1$ tiene $n$ posibilidades, $a_2$ tiene $n$ posibilidades, $a_3$ tiene $n$ posibilidades, y asi sucesivamente hasta $a_m$, por lo que se tiene que:

![alt text](image-4.png)

$$
\begin{align*}
n^m = n \cdot n \cdots n = n^m
\end{align*}
$$

----- 

Ahora cual es el numero de funciones inyectivas:

Si $m>n$, no hay funciones inyectivas, por lo que se tiene que son $0$ funciones inyectivas.

Si $m\leq n$, se tiene que:

$$
\begin{align*}
|A :=\{\text{numero de funciones inyectivas}\}| = (n)_m = \frac{n!}{(n-m)!}
\end{align*}
$$

donde 

$$
\begin{align*}
(n)_m = \begin{cases}
1 & \text{si } m=0\\
n(n-1) & \text{si } m=1\\
$$

Se conoce como factorial de creciente 

----- 
Ahora cuantas funciones sobreyectivas hay:
Si $n<m$, no hay funciones sobreyectivas, por lo que se tiene que son $0$ funciones sobreyectivas.

Si $n\geq m$, se tiene que ver cuantas forma puedo particionar un conjunto de $n$ elementos en $m$ bloques, son los numeros de stirling de segunda clase.

Asi el numero de funciones sobreyectivas es:

![alt text](image-5.png)
$$\begin{align*}
\left\{n \atop m\right\} n!
\end{align*}$$

---

## Numero de stirling

Def:

Sea $n$ y $k$ enteros con $0\geq k\geq n$. Denotamos 

$$
\begin{align*}
\left\{n \atop k\right\} 
\end{align*}
$$

por el numero de particionaes del conjunto $[n] = \{1,2,\cdots,n\}$ en exactamente $k$ bloques o subconjuntos disjuntos no vacios. Estos coeficientes se denomianan numero de Stirling de la segunda clase. Definimos 

$$
\begin{align*}
\left\{0 \atop 0\right\} = 0 \quad \text{si } n>0
\end{align*}
$$
**Teorema**

Para $n$, $k$ enteros positivos con $1\leq k\leq n$, se tiene que:

$$
\begin{align*}
\left\{n \atop k\right\} = \left\{n-1 \atop k-1\right\} +  k \left\{n-1 \atop k\right\} 
\end{align*}
$$

Con los valores iniciales $\left\{0 \atop 0\right\} = 1$ y $\left\{n \atop 0\right\} = 0$ para $n>0$, y $\left\{n \atop k\right\} = 0$ para $k>n$.

La parte derecha representa la formas de particiona un conjunto de $n -1$ elementos en $k -1$  mas la forma de particionar un conjunto de $n -1$ elementos en $k$ bloques por $k$.


el primer termino de la derecha representa fijar un bloque unitario y entonces yo calculo el numero de stirling para $n-1$ y $k-1$.


Probar( Formula de Striling)

PAra todo $n\geq 1$ se tiene que:

$$
x^n =\sum_{k=0}^n \left\{n \atop k\right\} (x)_k
$$

Si cambiar de base, los coeficientes son los numero de stirlign, $x\geq$ es equivalente a a contar fuciones de $[n]$ en $[x]$ y $k$ es el numero de bloques. Ahora partimos el domingo en $k$ bloques,  ahora contar la formas de asignar un bloque a un elemento de $[x]$. 

$k$ es el numero de imagenes distintas de la funcion $f: [n] \to [x]$ 

Asi la parte de la derecha considera los casos excluyentes en los una funcion tiene $k$ imagenes distintas.