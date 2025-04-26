**Definicion** SEa $S$ y $T$ conjuntos finitos y sea $d$ un entero positivo. Decimos queuna funcions $f: T \to S$ es una $d$-funcion si para cada $s \in S$ el conjunto $f^{-1}(s)$ tiene exactamente $d$ elementos distintos.

**Teorema**: Sea $f$ una funcion de $T$ en $S$ tal que $f$ es una $d - 1$ , entonces $|S| = \frac{|T|}{d}$

**Definicion**: Dos permutaciones $\Pi = a_1 a_2 \cdots a_n$ y $\Pi' = b_1 b_2 \cdots b_n$ estan relacionadas si existe unentero $k$ en $0\leq k < n$ tal que $b_i = a_{i + k \mod n}$ para $i = 1,2,\cdots,n$. Se denota como $\Pi \sim \Pi'$.

$\sim$ defina una relacion de equivalencia sobre el conjunto de permutaciones de $[n]$. 

**Definicion**: Una permutacion circular de $[n]$ es una clase de equivalencia que se obtiene de la relacion $\sim$.

Por ejemplo: $1234 \sim 2413$ 

**Teorema**: El numero de permutaciones circulares de $n$ elementos es $(n-1)!$

**Demostracion** definamos $f: T \to S$ con $S$ el cojunto de permutaciones circulares de tamanio n, $T$ el numero de permuaticon de $[n]$. Definimos $f(x_1, \dots,x_n) = f[x_1,\dots,x_n]$ luego $f$ es $n$ a $1$. ASei por el P.D se tiene que:

$$
\begin{align*}
|S| = \frac{|T|}{n} = \frac{n!}{n} = (n-1)!
\end{align*}
$$

### R-permutaciones circulares.

Sea $P(n,r)/r$ es el numero de permutaciones circulares, donde $P(n,r) = \frac{n!}{(n-r)!}$


De cuantasformas se pueden 5 hombres y tres mujeres sentarse alrededor de una mesa redonda si:

1. No hay restricciones.
2. El hombre $H$ t la mujer $M$ no pueden ir juntos
3. ninguna mujer adyancente,

1.El primero es 7!
2. Considerar el complemento, es decir cuando $M$ y $H$ estan juntos, asi considerar las permutaciones circulares de $7$ elementos, los cual es 2(7!/7), el 2 es debido a que podemos permutar el hombre y la mujer, luego entonces, la solucion al problema original es: $7! - 2(6!)

**Teorema**:Los numeros de Stirling de segunda clase estan dados por:

$$
\begin{align*}
S(n,k) 
= \frac{n!}{k!}\sum_{j_1 + j_2 +\dots + j_k = n} \frac{1}{j_1! j_2! \cdots j_k!} 
\end{align*}
$$

Donde la suma toma sobre todas las $k$ tuplas de enteros positivos $j_1, j_2, \cdots, j_k$ tales que $j_1 + j_2 + \cdots + j_k = n$.

Dado $S(n,k)$ es el numero de particiones de $n$ elementos en $k$ subconjuntos no vacios. Asi definimos los bloques $B_1, B_2, \cdots, B_k$ . Supongamos que:


$$
\begin{align*}
|B_i| = j_i \text{ para } i = 1,2,\cdots,k
\end{align*}
$$

para estos $j_1 + j_2 + \cdots + j_k = n$. 

Por otro lados en la parte $n!$ me cuenta todas las permutaciones de $n$, $\Pi_1, \Pi_2, \cdots, \Pi_n$ y dividimso por las permutaciones de los bloques $k!$ debido a que no importa el orden de los bloques. Y igualmente como elorden dentro de los bloques no importa, tenemos que dividir por $j_1! j_2! \cdots j_k!$, y la suma me cuenta la forma de escoger los tamanios de los bloques. Los $j_i$  suman n dado que los elemntos de $n$ se van agotando,]


### Numeros de Strirling de primera clase.

Una permutacion de $S$ con $S =n$, se puede definir tambien como una funcion biyectiva de $\pi: S \to S$. La permutaciones como por ejemplo:

$$
\begin{align*}
\pi = \begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9\\
5 & 2 & 7 & 9 & 3 & 4 & 1 & 8 & 6
\end{pmatrix}
\end{align*}
$$

se representa en terminos de permutaciones circulares como:

$$
\begin{align*}
\pi = (1,5,3,7)(2)(4,9,6,8)
\end{align*}
$$

**Definicion**:  Ek byneri de permutaciones de $[n]$ en $k$ ciclos se denota como $\begin{bmatrix}
n\\k
\end{bmatrix}$. Estos son los numero de Stirling de primera clase. Y se define como:


$$
\begin{align*}
\begin{bmatrix}
0\\0
\end{bmatrix} = 1
\end{align*}
$$

$$
\begin{align*}
\begin{bmatrix}
n\\0
\end{bmatrix} = 0 \text{ para } n > 0
\end{align*}
$$

$$
\begin{align*}
\begin{bmatrix}
n\\k
\end{bmatrix} = 0 \text{ para } k > n
\end{align*}
$$


Veaamos que 

$$
\begin{align*}
\begin{bmatrix}
3\\
0    
\end{bmatrix} = 0
\end{align*}
$$


$$
\begin{align*}
\begin{bmatrix}
3\\
1
\end{bmatrix} = |\{(123), (132)\}| =2
\end{align*}
$$

$$
\begin{align*}
\begin{bmatrix}
3\\
2
\end{bmatrix} = |\{(12)(3), (13)(2), (23)(1)\}| = 3
\end{align*}
$$

$$
\begin{align*}
\begin{bmatrix}
3\\
3
\end{bmatrix} = |\{(1)(2)(3)\}| = 1
\end{align*}
$$




**Teorema**: SEan $n,k$ enteros positivos con &1\leq k \leq n$ entonces:

$$
\begin{align*}
\begin{bmatrix}
n\\k
\end{bmatrix} = (n-1)\begin{bmatrix}
n-1\\k
\end{bmatrix} + \begin{bmatrix}
n-1\\k-1
\end{bmatrix}
\end{align*}
$$

Con los valores iniciales:

$$
\begin{align*}
\begin{bmatrix}
0\\0
\end{bmatrix} = 1
\end{align*}
$$

$$
\begin{align*}
\begin{bmatrix}
n
\\k
\end{bmatrix} = 0 \text{ para } n < k
\end{align*}
$$

$$
\begin{align*}
\begin{bmatrix}
n\\0
\end{bmatrix} = 0 \text{ para } n > 0
\end{align*}
$$

**Demosntracion**

1. Sea $n$ fijo $(n)$ 

$$
\begin{align*}
\begin{bmatrix}
n - 1\\
k - 1
\end{bmatrix} = \text{ el numero de permutaciones de } n-1 \text{ elementos en } k-1 \text{ ciclos}
\end{align*}
$$

2. No es punto fijo:

$$
\begin{align*}
(n-1)\begin{bmatrix}
n - 1\\
k
\end{bmatrix} = \text{ el numero de permutaciones de } n-1 \text{ elementos en } k \text{ ciclos}
\end{align*}








