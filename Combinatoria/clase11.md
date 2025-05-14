# Por que hay tantos calvos?

Por las personas tienen a los muchos 150 mil cabellos.

**Teorema**

Sean $m,n,r$ enteros positivos,  tales que $n>rm$. supongamos que se colocan n bolas identicas en $m$ cajas identicas. Entonces al menos una de la cajas tiene $r+1$ bolas. 

$$
\begin{align*}
r+1 = \text{parte entera techo de } n/m \quad \text{parte techo de $n/m$}
\end{align*}
$$

**Teorema**

Suponga que $n^2+1$ personas se ubican en una fila. Entonces siempre es posible encontrar $n+1$ personas (siguiendo el orden de la fila ) talque de la iquierda a derecha sus alturas son crecientes.

Afiram que dada una sucesion $a_1,a_2,\ldots,a_{n^2+1}$ entonces es posible encontrar una subsecuencia $a_{i_1}, a_{i_2}, \ldots, a_{i_{n+1}}$ talque $a_{i_1} \leq a_{i_2} \leq \ldots \leq a_{i_{n+1}}$ o es decreciente. con $1 \leq i_1 < i_2 < \ldots < i_{n+1} \leq n^2+1$.


**Demostracion:**

Sean $a_1,a_2,\ldots,a_{n^2+1}$ numeros reales. Y supongamos que esta sucesion no contiene una subsucesion creciente de longitud $n+1$. Sea $m_k$ la longitud de la subsucesion creciente mas larga que inicia en el termino $a_k$. Ej:

$$
\begin{align*}
(4,7,1,2,8,5,10,3,9,6)\\
(a_1,a_2,a_3,a_4,a_5,a_6,a_7,a_8,a_9,a_{10})\\
\end{align*}
$$

entonces $m_4 = 3$.

De la definición $k$ tiene cumple que:

$$
\begin{align*}
m_k \leq n \quad \text{por la hipotesis de que no se tiene una subsucesion creciente de longitud $n+1$}\\
\end{align*}
$$

Esto significa que los $n^2+1$ valores $m_k$ estan en $[n]=\{1,2,3\dots,n\}$. Entonces por el principio del palomar generalizado existen indicies $k_1,k_2,\ldots,k_{n+1}$ tales que $1\leq k_1 \leq k_2 \leq \ldots \leq k_{n+1} \leq n^2+1$ para los cuales se cumple que:

$$
\begin{align*}
m_{k_1} = m_{k_2} = \ldots = m_{k_{n+1}}
\end{align*}
$$

Considere entonces la siguiente susecion :

$$
\begin{align*}
a_{k_1}, a_{k_2}, \ldots, a_{k_{n+1}} \\
\end{align*}
$$

Veamos que es decreciente, ya que si no fuera asi, existiría algun indice tal que $a_{k_i} < a_{k_{i+1}}$, como $k_i < k_{i+1}$, podemos considerar subsucecion creciente mas larga que inicia en $a_{k_{i+1}}$ (de tamanio $m_{k_{i+1}}$), le agregamos al incio el termino $a_{k_i}$, luego obtenemos una subsucesion creciente de tamanio $m_{k_{i+1}}+1$ que inicia en $a_{k_i}$, lo cual contradice que $m_{k_i} = m_{k_{i+1}}$. 

Es $n+1$ el valor optimo? si es optimo. Esto es general la teoria de Ramsey.

## Numeros de Ramsey

Un problema prototipico e n la teoria de Ramsey, consiste en determinar las condiciones bajo las cuales un conjunto suficientemente grande necesariamente contiene un cierto tipo de estructura ordenada. En otras palabras, se busca saber cuantos elementos debe tener un conjunto para que cierta propiedad combinatoria este garantizada.

**Ejemplo:**

En un conjunto de $6$ o mas personas siempre hay 3 personas que se conocen entre si o hay 3 personas que no se conocen entre si.

Existen $2^{\binom{6}{2}} = 2^{15} = 32768$ total de coloraciones con dos colores de los vertices.


**Definicion:**

$K_n$ denota al grafo completo de $n$ vertices. Observe que $K_n$ tiene $\binom{n}{2}$ aristas.

$$
\begin{align*}
K_p \to (K_n,K_m) 
\end{align*}
$$


Denotamos por $K_p \to (K_n,K_m)$ si para cualquier $2$-coloracion de las aristas de $k_p$ (rojo y azul) existe $n$ subgrafo $k_n$ cuyas aristas, son todas rojas o bien existe $m$ subgrafo $k_m$  de color azul.

**Ejemplo:**

$K_6 \to (K_3,K_3)$

$K_8 \to (K_3,K_3)$

$K_5 \to (K_3,K_3)$ Falso.

**Definicion:**

El numero de Ramsey $R(n,m)$ es el menor entero positivo $p$ talque 

$$
\begin{align*}
K_p \to (K_n,K_m)
\end{align*}
$$

**Ejemplo:** 
$$
\begin{align*}
R(3,3) = 6
\end{align*}
$$

**Teorema:**

Para todo $n,m \in \mathbb Z^+$ se tene que 

$$
\begin{align*}
R(n,m) = R(m,n)
\end{align*}
$$ 

$$
\begin{align*}
R(n,1) = 1
\end{align*}
$$

$$
\begin{align*}
R(n,2) = n
\end{align*}
$$

$$
K_n \to (K_n,K_2)
$$

**Teorema:(Erdos-Szekeres)**


PAra todo $n,m$ enteros mayores iguales que 1 el numero de Ramsey $R(n,m)$ existe. Ademas para todos los enteros $n,m\geq 2$ se cumple que:

$$
\begin{align*}
R(n,m)  \leq R(n-1,m) + R(n,m-1)
\end{align*}
$$

**Demostracion:**


Si $n=1$ o $m=1$, $R(n,1) = 1= R(1,m)$.

El argumento es por induccion en $p=n+m$, con $n,m\geq 2$. $p=4$ ,5

$(2,2)$, $(2,3)$, $(3,2)$

$$
\begin{align*}
R(2,2) = 2\\
R(2,3) = 3 = R(3,2)\\
\end{align*}
$$

Ademas si se reemplaza en la desigualdad se obtiene que es verdadera.

Supongamos quese tiene para toda parja de enteros $n,m$ tal que $n+m < p+1$. Debemos mostrar que se tiene para $n+m = p+1$. Sea 

$$
\begin{align*}  
h = R(n,m-1) + R(n-1,m)
\end{align*}
$$ 
El cual esta bien definido ya que por hipotesis de induccion $R(n,m-1)$ y $R(n-1,m)$ existen.

Vamos a demostrar que cualquier $2$-coloracion de $K_h$ siempre contiene a $K_m$ azul o a $K_n$ rojo. Sea $X$ un vertice cualquiera del grafo $K_h$. Definimos:

$$
\begin{align*}
R_x = \text{todos los vertices que son adyacentes con $X$ cuyas aristas son de color rojo}

A_x=\text{todos los vertices que son adyacentes con $X$ cuyas aristas son de color azul}
\end{align*}
$$

El calor que: $|R_x| + |A_x| = h-1$.

Ademas se tiene una de las siguientes desigualdades:

$$
\begin{align*}
|R_x| \geq R(n-1,m) \quad \text{o} \quad |A_x| \geq R(n,m-1)
\end{align*}
$$

De no ser asi:

$$
\begin{align*}
|R_x| + |A_x| < R(n-1,m) + R(n,m-1) = h
\end{align*}
$$

(Paila)

Probando solo la desigualdad:

$$
\begin{align*}
    K_h \to (K_n,K_m)\\
\end{align*}
$$

$R(n,m)\leq h$ 

SEa $x \in V(K_h)$, y definimos:

$$
\begin{align*}
R_x = \{
    z \in V(K_h) : (x,z) \text{ es rojo}
\}
\end{align*}
$$

Y $A_x$  de forma analoga

entonces $|R_x| + |A_x| = h-1$. Afirmo que:

$$
\begin{align*}
|R_x| \geq R(n-1,m) 1\\
|A_x| \geq R(n,m-1)
\end{align*}
$$
si no fuera asi $|R_x| \leq R(n-1,m) - 1$ y $|A_x| \leq R(n,m-1) - 1$ entonces:

$$
\begin{align*}
h-1=|R_x| + |A_x| \leq R(n-1,m) + R(n,m-1) - 2 = h-2
\end{align*}
$$

lo cual contradice la hipotesis de que $h$ es el menor entero tal que $K_h \to (K_n,K_m)$.

Supongamos que se tiene que :

$$
\begin{align*}
|R_x| \geq R(n-1,m)
\end{align*}
$$

Considere el grafo $K_{q}$ donde $q = |R_x|$, y es el grafo generado por todos los vertices de $R_x$. Por la definicion de $K_q$ contiene $K_{n-1}$ rojo. o $K_{m}$ azul. Si se da el segundo caso $K_{m} \subseteq K_q \subseteq K_h$. 

Si $K_{n-1}$ rojo, entonces agregamos el vertice $x$ y obtenemos un subgrafo $K_n$ rojo. cuadradito.