# Correccion quices

# Productos infinitos

Supongamos que tenemos una famillia contable de espacios topologicos $\{(X_i, \tau_i)\}_{i \in \mathbb N}$ y

$$
\begin{align*}
X = \prod_{i \in \mathbb N} X_i = \{ (x_1,x_2,  \dots, x_n): x_i \in X_i\}
\end{align*}
$$

Que topologia podemos darle a $X$

- Con franjas.
- Productos de abiertos.


Dado \( j \in \mathbb{Z}^+ \),

$$
\prod_{i=1}^{\infty} X_i \xrightarrow{\pi_j} X_j
$$

$$
(x_i)_{i=1}^{\infty} \mapsto x_j
$$


Sea:

$$
\begin{align*}
\mathcal P= \{
    \Pi_j^{-1}(U_j): j \in \mathbb{Z}^+, U\subseteq^{ab} X_j
\}
\end{align*}
$$


$\mathcal P$ es una subbase para alguna topologia:
**Topologia producto**

$$
\begin{align*}
\mathcal B = \{\prod_{i=1}^\infty : \forall i \in \mathbb{Z}^+, U_i \subseteq^{ab} X_i \text{ y } U_i = X_i \text{ para casi todo } i\}
\end{align*}
$$

**Topologia de los gatos**

$$
\begin{align*}
\mathcal B' = \{
    \prod_{i=1}^\infty U_i : U_i \subseteq^{ab} X
\}
\end{align*}
$$

Por que la topologia de gatos  es mala? por que tiene demasiados abiertos. Sea

$$
\begin{align*}
f: \mathbb R &\to \prod_{i=1}^\infty\\
x&\to (x,x,x, \dots)
\end{align*}
$$

$f$ no es continua.


Sea $U = (-1,1)\times (-1/2,1/2) \times \dots$. U es abierto en la topologia de cajas,. (Pero no en la topologia producto.)

$$
\begin{align*}
f^{-1}(U) =\{x \in \mathbb R: f(x) = (x,x,x, \dots) \in U\} 
\end{align*}
$$
lo cual implica que $x\in (-1/n, 1/n)$ para todo $n$. Por lo tanto $x \in \bigcap_{n=1}^\infty (-1/n, 1/n) = \{0\}$, lo cual es cerrado, asi $f$ no es continua.

**Lema**

Sean $X_1, X_2, \dots$ y $Y$ espacios topologicos y 

$$
\begin{align*}
f_i: X_i \to Y
\end{align*}
$$

entonces:

$$
\begin{align*}
f: Y &\to \prod_{i=1}^\infty X_i\\
y &\to  (f_1(y), f_2(y), \dots)
\end{align*}
$$

Es continua sii $f_i$ es continua para todo $i \in \mathbb{Z}^+$. Donde $\Prod_{i=1}^\infty X_i$ es la topologia producto.


**Demostracion**

$\implies$ $f_i= \pi_i \circ f$ es continua luego $f_i$ es continua.

$\impliedby$ Basta ver que $f^{-1}(\Pi^{-1}_j (U_j)) \subseteq^{ab} Y$ , para todo $j \in \mathbb{Z}^+$ y $U_j \subseteq^{ab} X_j$ abierto.  Con $\Pi_j^\circ f^{-1}(U_j) = f^{-1}((U_j))\subseteq^{ab} Y$.


**Teorema(Tychonoff-contable)**

Si cada $X_i$,$i\in \mathbb Z^+$ es compacto, entonces el producto $X = \prod_{i=1}^\infty X_i$ es compacto.

**Demostracion**

Supongamos que existe un cubrimiento $\mathcal U$ de $\prod_{i=1}^\infty X_i$ tal que no tiene un subcubrimiento finito, veamos que. 

(1) $\exist x_1 \in X_1$ tq no hay un asico de la forma 

$$
\begin{align*}
U_1 \times X_2 \times X_3 \times \dots
\end{align*}
$$

tq $x_1 \in U_1$. y es cubierto por finitos elemento en $U$.

----

Si no fuese cierto lo anterior $x_1 \in U_1 \times X_2 \times X_3 \times \dots$  esta contenido en la union de finitos elementos de $U$. Consideremos la familia:


$$
\begin{align*}
\{
U_1: U_1 \times X_2 \dots \quad \text{esta continido en la union de finitos elementos de $U$}
\}
\end{align*}
$$

en esta familia si dejamos variar $x_1$ cubre a $x_1$, como $X_1$ es compacto, existen finitos $U_1^{(1)}, \dots, U_1^{(l)}$ que crubren a $X_1$.


$$
\begin{align*}
U_1^{(1)} \times X_2 \dots, U_1^{(2)} \times X_2 \dots, \dots, U_1^{(l)} \times X_2 \dots
\end{align*}
$$

Cada uno de estos es contenidos en finitos elementos de $U$. cubre a 

$$
\begin{align*}
\prod_{i=1}^\infty X_i
\end{align*}
$$

Esto implica que que $\prod_{i=1}^\infty X_i$ esta cubierto por finitos elementos de $U$. contradiccion Luego (1) es verdadera. $\exist x_1$ tq no existe $U_1 \subseteq^{ab} X_1$ tal que $x_1 \in U_1 \times X_2 \times \dots$ y $U_1 \times X_2 \times \dots$ no esta contenido en una union finita de elementos de $U$, veamos que:


(2) $\exist x_2 \in X_2$ no hay un elemento basico $U_1\times U_2 \times X_3 \times \dots$ con $(x_1, x_2) \in U_1 \times U_2$ tq $U_1 \times U_2 \times X_3 \times \dots$ tq $U_1 \times U_2 \times X_3 \times \dots$ no esta contenido en una union finita de elementos de $U$.


Si no es cierto la afirmacion (2):

$\forall x_2 \exist U_1 \subseteq^{ab} U_1, U_2 \subseteq^{ab} X_2$ tal que $x_2 \in U_2$ y $U_1 \times U_2 \times X_3 \times \dots$ esta contenido en una union finita de elementos de $U$. Consideremos la familia:

$$
\begin{align*}
\{
U_1 \times U_2: U_1 \times U_2 \times X_3 \times \dots \text{ esta contenido en una union finita de elementos de $U$}
\}
\end{align*}
$$

Es un cubrimiento de $X_1 \times X_2$, como $X_1 \times X_2$ es compacto existen finitos $U_1^{(1)} \times U_2^{(1)}, \dots, U_1^{(l)} \times U_2^{(l)}$ elemento de la familia que cubren a $X_1 \times X_2$.

$$
\begin{align*}
\{
    U_1^{(i)} \times U_2^{(i)} \times X_3 \times \dots: i = 1, \dots, l
\}
\end{align*}
$$

Esta familia cubre a $\prod_{i=1}^\infty X_i$. Esto implica que hay finitos elementos de $U$ que cubren a $\prod_{i=1}^\infty X_i$. Contradiccion. 

($\frac{n(n+1)}2 = 1+ \dots + n$).

$\exists x_i \in X_i$ $(i=1\dots,n)$ tq no existe un abierto $U_i$ de $X_i$ tq $x_i \in U_i$ y 

$$
\begin{align*}
U_1 \times U_2 \times \dots \times U_n \times X_{n+1} \times \dots
\end{align*}
$$
esta cubierto por initamente elementos de $U$.

Notese que:

$$
\begin{align*}
(x_1, x_2, \dots, x_n) 
\end{align*}
$$

debe pertenecer a un elemento de $U$ de $\mathcal U$ luego existen un abierto basico

$$
\begin{align*}
U_1 \times U_2 \times \dots \times U_n \times X_{n+1} \times \dots
\end{align*}
$$
tq $(x_1, x_2, \dots) \in V \subseteq^{ab} U$ si y solo si $x_i \in U_i$ para $i=1, \dots, n$ 

Esto contradice la afirmacion anteriormente probada contradiccion, entonces:

$$
\begin{align*}
\prod_{i=1}^\infty X_i \text{ es compacto}
\end{align*}
$$

Cuando se toma una familia arbitraria eso es equivalente al axioma de eleccion.


