**Teorema** $A \subseteq \mathbb R^n$ es compacto sii es cerrado y acotado.

## Axiomas de separacion

**Def** $X$ un espacio topologico, $X$ es un espacio de Hausdorff sii para cualesquiera $x,y \in X$ distintos existen abiertos $U,V$ tales que $x \in U$, $y \in V$ y $U \cap V = \emptyset$.

![alt text](image-6.png)

**Ejemplo** 

-1. Sea $(X,d)$ un espacio metrico, sean $x,y \in X$ distintos. 

Sea $\epsilon = d(x,y)>0$. Entonces:

$$
\begin{align*}
U_x = B_{\frac{\epsilon}{2}}(x) \\
U_y = B_{\frac{\epsilon}{2}}(y)
\end{align*}
$$
![alt text](image-7.png)
son vecindades abiertas  de $x$ y $y$ respectivamente. Luego si por contradiccion:

$$
\begin{align*}
U_x \cap U_y \neq \emptyset
\end{align*}
$$

Sea $z \in U_x \cap U_y$, entonces:

$$
\begin{align*}
d(x,y) \leq d(x,z) + d(z,y) < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon
\end{align*}
$$
lo cual es una contradiccion. Por lo tanto $U_x \cap U_y = \emptyset$.

Esto muestra que todas las topologias inducidas por metricas son Hausdorff.

-2 Sea $(X,\mathcal T_{\text{trivial}})$ si $|X|>1$, sean $x,y \in X$ distintos. La unicas vecindades de $x$ y $y$ son $U_x = X$ y $U_y = X$. Luego $U_x \cap U_y = X \neq \emptyset$. Por lo tanto no es Hausdorff. Esto muestra que la topologia trivial no viene de una metrica. 

-3 Dado $X$ infinito, $A\subseteq X$, $A$ es cerrado si y solo si $A$ finito o $A = X$ en $(X,\mathcal T_{\text{Zariski}})$. (Ejercico ver que en efecto Zariski es una topología).

$X$ no es Hausdorff. Sean $x,y \in X$ distintos. Sean $U_x$ y $U_y$ vecindades de $x$ y $y$ respectivamente.

$$
\begin{align*}
U_x \cap U_y = \emptyset ?
\end{align*}
$$

$x \in U_x$, $X-U_x$ es finito.
$y \in U_y$, $X-U_y$ es finito.

Si $U_x \cap U_y = \emptyset$, entonces

$$
\begin{align*}
X - (U_x \cap U_y) &= X\\
(X - U_x) \cup (X - U_y) &= X\\
\end{align*}
$$

con $X - U_x$ y $X - U_y$ finitos. Luego $X$ es finito. Contradiccion.

### Propiedades de los espacios Hausdorff

a) Si $X$ es Hausdorff entonces para todo $x \in X$, $\{x\}\subseteq^{\text{cerr}} X$.

b) Si $X$ es Hausdorff y $Y \subseteq X$, entonces $Y$ es Hausdorff.

c) Si $X$ y $Y$ son Hausdorff, entonces $X \times Y$ es Hausdorff.

**Demostracion**:

a) Sea $y \notin \{x\}$. $y \in X-\{x\}$, entonces $U_x$ y $U_y$ vecindades abiertas de $x$ y $y$ respectivamente talque $U_x \cap U_y = \emptyset$. entonces $x \notin U_y$. entonces $U_y \subseteq X - \{x\}$, entonces $X - \{x\}$ es abierto de $X$. 

**Ejericicio**: Ver si el reciproco es cierto ek de $a)$.


b) E.F

c) Sean $(x_1,y_1)$, $(x_2,y_2) \in X \times Y$ distintos. Entonces $x_1 \neq x_2$ o $y_1 \neq y_2$. Si $x_1 \neq x_2$, entonces existen abiertos $U_{x_1}$ y $U_{x_2}$ vecindades abiertas de $x_1$ y $x_2$ respectivamente tales que $U_{x_1} \cap U_{x_2} = \emptyset$. Asi:

$$
\begin{align*}
U_{x_1} \times Y \quad \text{es vecindad abierta de } (x_1,y_1)\\

U_{x_2} \times Y \quad \text{es vecindad abierta de } (x_2,y_2)\\

\end{align*}
$$

Asi:

$$
\begin{align*}
(U_{x_1} \times Y) \cap (U_{x_2} \times Y) = (U_{x_1} \cap U_{x_2}) \times Y = \emptyset
\end{align*}
$$

![alt text](image-8.png)


-----

**Prop** $A \subseteq X$, compacto y $X$ es Hausdorff, entonces $A$ es cerrado en $X$. Esta propiedad nos sirve para ver si funciones son cerradas

**Nota**: Dada un funcion $f:X \to Y$, Tome $A$ un cerrado de $X$ compacto y entonces $A$ es compacto. $f(A)$ es compacto de $Y$ entonces $f(A)$ es cerrado en $Y$. por la proposicion anterior (Muy util para el parcial.)

**Dem**: Veamos que para todo $x \in X - A$ existen un abiertos $U,V \subseteq X$ tales que $x \in U$, y $A \subseteq V$, $U \cap V = \emptyset$.

![alt text](<WhatsApp Image 2025-05-14 at 09.49.21_b1197898.jpg>)

Tome se un elemento arbitrario $a \in A$ luego $a \neq x$.

Como $X$ es Hausdorff, existen abiertos $U_{x,a},V_{x,a}$ de $x$ y $a$ respectivamente tales que $U_{x,a} \cap V_{x,a} = \emptyset$. Notemos que:

$$
\begin{align*}
\{V_{x,a}: a \in A\} \text{Es un cubrimiento de $A$ } 
\end{align*}
$$

Como $A$ es compacto, existe $V_{x,a_1},\ldots,V_{x,a_n}$ tal que:

$$
\begin{align*}
A \subseteq V_{x,a_1} \cup \ldots \cup V_{x,a_n} = V
\end{align*}
$$

![alt text](image-9.png)


Sea $U = \bigcap_{i=1}^n U_{x,a_i} \subseteq^{ab} X$, entonces $U$, donde $U_{x,a_i}$ son abiertos de $U$ y por lo tanto $U$ es abierto.

- $U \cap V = \emptyset$ 
- $A \subseteq V$, $x \in U$ 

Asi $x$ es punto interior de $X-A$ es decir $X-A$ es abierto. Por lo tanto $A$ es cerrado.

**Nota-Ejercicio** Ademas hemos demostrado que si $X$ es Hausdorff, $X$ separa conjuntos compactos.

**Colorario** $f:X \to Y$ continua, d$X$ es compacto y $Y$ es Hausdorff, entonces $f(X)$ es cerrado en $Y$.

**Dem**: Sea $A \subseteq^{cerr} X$, por la proposicion anterior $A$ es compacto. entonces $f(A)$ es compacto y como $Y$ es Hausdorff, $f(A)$ es cerrado en $Y$. Por lo tanto $f(X)$ es cerrado en $Y$.

**Colorario** $f:X \to Y$ continua y bijectiva, tq $X$ es compacto y $Y$ es Hausdorff, entonces $f$ es homeomorfismo.

**Ejemplo** $[0,1] \not \simeq [0,1]^2$

![alt text](image-10.png)

No ha una función $\phi: [0,1] \to [0,1]^2$ continua y biyectiva.

Existe $\phi [0,1] \to [0,1]^2$ continua y sobre?Si existe, se llama función de Peano. Es decir con una linea de grosor infinitesimal se pueda colocar un cuadrado.

![alt text](image-11.png)


**Def** un espacio $X$ Hausdorff es normal si separa conjuntos cerrados. E.d  para todo $A,B \subseteq^{cerr} X$, $A \cap B = \emptyset$, existen abiertos $U,V$ tales que $A \subseteq U$, $B \subseteq V$ y $U \cap V = \emptyset$.`

![alt text](image-12.png)

**prop** Un espacio compacto de Hausdorff $X$ es normal.
**Dem**: Sean $A,B \subseteq^{cerr} X$, $A,B$ son compactos, luego por el ejercicio se puede separar.

Tenemos hasta el momento las siguientes clases de espacios topologicos:

- Espacios Hausdorff
- Espacios normales
- Espacios 

Todo espacio metrico es Hausdorff.
Los espacios normales son Hausdorff.
Falta mostar que los espacios Hausdorff son normales.

Pero no es cierto que Hausdorff implique normal, y un normal no implica ser metrico.

![alt text](image-13.png)

**Lema**: Existe un espacio Hausdorff que no es normal.
$$e
\begin{align*}
X = \{(x,y) \in \mathbb R^2: y\geq 0\} 
\end{align*}
$$

Sea $X' = \{(x,y) \in \mathbb R^2: y > 0\}$.Definimos una topologia en $X$ mediante la siguiente base:

$$
\begin{align*}
\mathcal B = \{B_r(x,y) : B_r(x,y) \subseteq X', (x,y)\in X'\} \cup \{\{
    (x,0) 
\} \cup \{
    X' \cap B_r(x,0) : (x,0) \in X -X'
\}\}
\end{align*}
$$

![alt text](image-14.png)


Veamos que $\mathcal B$ es una base de la topologia de $X$. Por dibujo.

![alt text](image-16.png)

- $(X, \mathcal T_{\mathcal B})$ es Hausdorff (por dibujo).

Queremos ver que no es normal. Para todo $A \subseteq^{cerr} X-X'$, $A$ es cerrado


$$
\begin{align*}
X-A = \bigcup_{B \in \mathcal B} \{B_r(x,0) : r > 0 \land (x,0) \in A\}
\end{align*}
$$

La cual es una union infinita de abiertos. Por lo tanto $X-A \subseteq^{ab} X$, $A$ es cerrado.

Ahora sea $A= \mathbb Q \times \{0\}$; y $B = \mathbb I \times \{0\}$, entonces $A,B$ son cerrados de $X$ y $A \cap B = \emptyset$.

Si $U\subseteq^{ab} X$, $A \subseteq U$ y $V\subseteq^{ab} X$ tal que $B \subseteq V$. $(0,0)$ y existe $r>0$ tal que $\{(0,0)\} \subseteq B_r(0,0) \cap X'\subseteq U$. Existe $\theta <r$ tal que $\theta \notin \mathbb Q$. Luego existe $r'>0$ tal que $\{(\theta,0)\}\cup B_{r'}(0,0) \cap X' \subseteq V$. Pero


$$
\begin{align*}
\{(0,0)\} \cup B_{r}(0,0) \cap X' \subseteq U
\end{align*}
$$

Se interseta con $\{(\theta,0)\} \cup B_{r'}(0,0) \cap X' \subseteq V$. Esto implica que $U \cap V \neq \emptyset$. Por lo tanto no es normal.