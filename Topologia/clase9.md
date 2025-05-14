# Espacios compactos

**Def**: $X$ es compacto si todo cubrimiento por abiertos de $X$ tiene un subcubrimiento finito.


**Ej**: $\mathbb R$ es compacto, sea:

$$
\begin{align*}
U = \{(n-1,n+1)\}_{n \in \mathbb Z}
\end{align*}
$$

es un cubrimiento de $\mathbb R$ 


$U$ no tiene subcubrimiento finitos, de hecho $U$ no tiene subcubrimiento propios., muncho menos finitos.


- b) Si $X$  es un conjunto infinito.
$(X,\mathcal T_{discreto})$ no es compacto,

$$
X = \bigcup_{x \in X} \{x\}
$$


$\{\{x\}, x\in X\}$ es un cubrimiento que no tiene subcubrimiento propios,

-c) $(0,1)$ no es compacto,


$$
\begin{align*}
\bigcup_{(0,1-\frac 1 n): n \in \mathbb N}
\end{align*}
$$

$U$es un vubriemiento abierto de $(0,1)$.  Sean $\{(0,1-\frac 1 {n_1}), (0,1-\frac 1 {n_2}), \ldots, (0,1-\frac 1 {n_k})\}$ un subfamilia finita.


$$
\begin{align*}
\bigcup_{i=1}^k (0,1-\frac 1 {n_i}) = (0,1-\frac 1 {max\{n_1,n_2,\ldots,n_k\}}) \neq (0,1)
\end{align*}
$$

luego $(0,1)$ no es compacto.

## compactos

- a) $(X,\mathcal T$ es compacto , $X$ es finito. 
- b) $(X,\mathcal T_{\trivial})$ es compacto, $X$ es infinito.

$(X,\mathcal T)$ $\mathcal T$ finita,  es compacto.


**Teorema** Heine-Borel: 
$[0,1]$ es compacto.

**Dem**: SEa

$$
\begin{align*}
U = \{U_\alpha: \alpha\in I\}
\end{align*}
$$ 

un cubrimiento abierto de $[0,1]$.


existe $\alpha_0 \in I$ talque $0\in U_{\alpha_0},


Existe $c_0=\epsilon/2>0$ tq $[0,c_0]\subset U_{\alpha_0}$, luego $[0,c_0]$ esta contenido en la union finita de finitos elemento de $U$.


SEa 
$$
\begin{align*}
L = \sup\{c \in [0,1]: [0,c] \quad \text{esta contenido en la union de finitos elementos de $U$}\}
\end{align*}
$$


$L$ esta bien definido $L>0$ por que $1\geq L\geq C_0 > 0$ 

$
L \in [0,1]$ luego existe $\beta \in I$ talque 

$$
\begin{align*}
L \in U_\beta
\end{align*}
$$

Existe $\epsilon>0$ tq $[L-\epsilon,L] \subseteq U_\beta$. Ahora $L-\epsilon$ no es una cota superor de del conjunto por el cual se conturye $L$ , luego existe $c$ en ese conjunto tq $L-\epsilon < c$. es decir $[0,C]$ esta contenido en la union de finitos elementos de $U$ $U_{\alpha_1},\ldots,U_{\alpha_l}$, Esot es

$$
\begin{align*}
[0,C] \subseteq U_{\alpha_0} \cup U_{\alpha_1} \cup \ldots \cup U_{\alpha_l}
\end{align*}
$$

Luego 

$$
\begin{align*}
[0,L] \subseteq U_{\alpha_0} \cup U_{\alpha_1} \cup \ldots \cup U_{\alpha_l} \cup U_\beta
\end{align*}
$$

Esto muestra que $L$ es en conjunto sobre el se define $L$. Ademas si suponemos que $L<1$ entonces el mismo argumento demuestra que 
$$
\begin{align*}
[0,L+\epsilon] \subseteq  U_\beta
\end{align*}
$$
y por lo tanto $:

$$
\begin{align*}
[0,L+\epsilon]\subseteq \bigcup_{i=1}^l U_{\alpha_i} \cup U_\beta
\end{align*}
$$

entonces $L+\epsilon$ esta en ese conjunto. Lo cual es una contradiccion. Por lo tanto $L=1$  y $1$ esta en ese conjunto. 

$[0,1]$ es contenido en la union de finitos elementos de $U$.


**Prop** $X$ compacto y $A$ subconjunto de $X$ cerrado. Entonces $A$ es compacto.

**Dem**

Sea $U$ un cubrimiento abierto de $A$. 

$$
\begin{align*}
U = \{U_i \cap A: i \in I \land U_i \subseteq^{ab}  X\}
\end{align*}
$$

$X-A \subseteq^{ab}  X$ es abierto. 

Consideremao la familia.

$$
\begin{align*}
U' = \{U_i: i \in I\} \cup \{X-A\}
\end{align*}
$$

$U_i$ es un cubrimiento abierto de $X$.


$$
\begin{align*}
\bigcup_{i \in I} U_i \cup A = A
\end{align*}
$$
entonces
$$
\begin{align*}
\bigcup_{i \in I} U_i  \supseteq A
\end{align*}
$$

$$
\begin{align*}
X-A \supseteq X-A_i
\end{align*}
$$

entonces

$$
\begin{align*}
\bigcup U' = X
\end{align*}
$$

Como $X$ es compacto existen $U_1, \ldots, U_n, X-A$ tal que 


$$
\begin{align*}
\left(
    \bigcup_{i=1}^n U_i 
\right) U (X-A) = X
\end{align*}
$$


entonces intersectando con $A$  tenemos que


$$
\begin{align*}
\bigcup_{i=1}^n U_i \cap A = A
\end{align*}
$$

con $U_1\cap A, \ldots, U_n \cap A$ es una familia finita y por lo tanto $A$ es compacto.


**Ejemplos**
- a) $\mathcal C \subseteq^{\text{cerr}} [0,1]$ luego es compacto.
- $\{\frac 1 n: n \in \mathbb Z^+\}$ no  es compacto con la topologia de subespacio.
-  $\{\frac 1 n: n \in \mathbb Z^+\} \cup \{0\}$  es compacto con la topologia de subespacio.

**Prop**

Si $f:X \to Y$ es continua, y $X$ es compacto, entonces $f(X)$ es compacto.

**Dem** Sea $U$ un cubrimiento de $f(x)$ por abiertos,asi sea:

$$
\begin{align*}
f^-1(U) = \{f^{-1}(U_i): i \in I\}
\end{align*}
$$

$f^{-1}(U)$ es un cubrimiento abierto de $X$, como $X$ es compacto, existen $U_1,\ldots,U_n$, tal que:

$$
\begin{align*}
X = \bigcup_{i=1}^n f^{-1}(U_i)
\end{align*}
$$

entonces
$$
\begin{align*}
f(X) = \bigcup_{i=1}^n U_i
\end{align*}
$$

Luego $f(X)$ es compacto.

**Obs** $[a,b]$ es compacto.


**Prop** $A\subseteq \mathbb R$ cerrado y acotado es compato

**Dem**

Como $A$ es acotado, entonces existen $a,b \in \mathbb R$ tq:

$$
\begin{align*}
A\subseteq [a,b]
\end{align*}
$$

Pero $A \subseteq^{cerr} \mathbb R$ entonces $A \cap [a,b] \subseteq^{cerr} [a,b]$ con $A = A \cap [a,b]$. 

Por la prop anterior (2 veces) $A$ es compacto.

**Teorema** Si $X$ y $Y$ son compactos, entonces $X \times Y$ es compacto.


**Dem**


Sea $\{U_\alpha: \alpha \in I\}$ un cubrimiento abierto de $X \times Y$.


Si $(x,y) \in X \times Y$ entonces existe $\alpha$ tal que $(x,y) \in U_\alpha$. Ademas existen $U_{(x,y)} \subseteq^{ab}  X$ y $V_{(x,y)} \subseteq^{ab} Y$, $(x,y) \in U_{(x,y)} \times V_{(x,y)}\subseteq U_\alpha$.

Ahora fijemos $x$ y dejemos variando $y$ 

$$
\begin{align*}
\{U_{(x,y)} \times V_{(x,y)}: y \in Y\} \end{align*}
$$

un cubrimiento de $\{x\} \times Y$ quees comapcto, luego existen $y_1,\ldots,y_{n_x}$ tal que:


$$
\begin{align*}
\{x\} \times Y = \left(\bigcup_{i=1}^{n_x} U_{(x,y_i)} \times V_{(x,y_i)}\right) \cap (\{x\} \times Y)
\end{align*} 
$$

entonces:

$$
\begin{align*}
\{x\} \times Y \subseteq \bigcup_{i=1}^{n_x} U_{(x,y_i)} \times V_{(x,y_i)}
\end{align*}
$$

Sea 
$$
\begin{align*}
x \in U_x = \bigcap_{i=1}^{n_x} U_{(x,y_i)} \subseteq^{ab}  X
\end{align*}
$$

Se tiene que 
$$
\begin{align*}
\{x\} \times Y \subseteq U_x \times V_{(x,y_i)} \subseteq \bigcup_{i=1}^{n_x} U_{(x,y_i)} \times V_{(x,y_i)} \subseteq U_\alpha
\end{align*}
$$ 

Notese que $\{U_x, x\in X\}$ es un cubrimiento $X$, como es $X$ es compacto, existen $x_1,\ldots,x_{m}$ tal que:


$$
\begin{align*}
X = \bigcup_{i=1}^m U_{x_i}
\end{align*}
$$

Luego:


$$
\begin{align*}
X \times Y = \bigcup_{i=1}^m U_{x_i} \times Y = \bigcup_{i=1}^m \bigcup_{j=1}^{n_{x_j}} U_{(x_i,y_j)} \times V_{(x_i,y_j)}
\end{align*}
$$

Es decir $X \times Y$ esta contiendoa en uan union finita de $U_{\alpha}$'s, 


Entonces $X \times Y$ esta contiednos en uan subfamilia finita de $\{U_\alpha\}_{\alpha \in I}$, luego $X \times Y$ es compacto.


**Teorema** $X \subseteq^{ab}  \mathbb R^n$ es compacto sii $X$ es cerrado y acotado.


**Dem** ($\impliedby$) E.P.L


($\implies$) Veamosque $X$ es acotado. Sea 

$$
\begin{align*}
U = \{B_n(0): n \in \mathbb N\}
\end{align*}
$$

es un cubrimiento de $\mathbb R^n$ Como $X$ es compacto, existen $B_{n_1}(0),\ldots,B_{n_k}(0)$ tal que:

$$
\begin{align*}
X = \bigcup_{i=1}^k B_{n_i}(0)
\end{align*}
$$

Asi $X$ es acotado.


Falta ver que $X$ es cerrado. Sea $x$ un punto limite de $X$. Suponga que $x \notin X$. Entonce para todo $r>0$ 

$$
\begin{align*}
\overline{B_r(x)} \cap X \neq\emptyset
\end{align*}
$$
Sea 

$$
\begin{align*}
U = \{\mathbb R^n - \overline{B_r(x)}: r>0\}
\end{align*}
$$

donde $\mathbb R^n - \overline{B_r(x)} \subseteq^{ab}  \mathbb R^n$:

- $U$ cubre a $X$.

$$
\begin{align*}
\bigcup U \supseteq X
\end{align*}
$$


existen $r_1,\ldots,r_l$ tal que:


$$
\begin{align*}
X \subseteq \bigcup_{i=1}^l 
\mathbb R^n - \overline{B_{r_i}(x)} = \mathbb R^n -  \overline{B_{\min{r_1,\ldots,r_l}}(x)}
\end{align*}
$$

Luego $B_{\min{r_1,\ldots,r_l}}(x)$ es una vecindad de $x$ que no contien puntos de $X$. Es no es posible por que $x$ es un punto limite de $X$. Por lo tanto $X$ es cerrado.