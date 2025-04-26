**Teorema**

$A \subseteq X$ convexo si $A\subseteq B \subseteq \overline{A}$, entonces $B$ es convexo


**Demostracion**: Supongamos que $B$ Se desompone en $B = C \cup D$, donde $C,D$ son abiertos disjuntos no vacios. Intersectando con $A$


Ahora 

$$
\begin{align*}
A\subseteq C \quad \lor \quad A \subseteq D
\end{align*}
$$

Ahora tenemos que 

$A = (C \cap A) \cup (D \cap A)$, como $A$ es convexo, y $A \cap C \neq \emptyset$ o $A \cap D \neq \emptyset$,por lo anterior.


Ahora suponga que $A\subseteq C$, tomando las clausuras 


$$
\begin{align*}
\overline A \subseteq \overline C
\end{align*}
$$

Sea $x\in \overline C \cap D$, dado $x \in D \subseteq^{ab} B y $D = U \cap B$, donde $U$ es abierto en $X$. U es vecindad de $x$:

$$
\begin{align*}
U \cap C \neq \emptyset
\end{align*}
$$

Tenemos que 


$$
\begin{align*}
\emptyset \neq B \cap (U\cap C) = U \cap (B \cap C) = U \cap C \neq \emptyset
\end{align*}
$$
pues $B \subseteq C$


Luego:


$$
\begin{align*}
B \cap (U \cap C) \neq \emptyset = (B\cap U)\cap C \neq \emptyset = D\cap C \neq \emptyset
\end{align*}
$$

entonces 

$$
\begin{align*}
\overline A \cap D \neq \emptyset
\end{align*}
$$

y como $B \cap D = \emptyset$,  entonces $D = \emptyset$ contradiccion.

Por que estabamos asumiendo que $D$ no es vacio.


**Teorema** Si $f: X \to Y$ es continua y $X$ es conexo, entonces $f(X)$ es conexo.

**Demostracion**: Supongamos que $f(X) = A \cup B$, donde $A,B$ son abiertos disjuntos no vacios. Entonces $f^{-1}(A) \cup f^{-1}(B)$ es una descomposicion de $X$ en abiertos disjuntos no vacios, lo cual contradice la hipotesis de que $X$ es conexo.

<!-- 
donde $C \cap A$ y $D \cap A$ son abiertos disjuntos de $A$, Entonces o bien $A\subseteq A$ o $A\subseteq D$. Por ejemplo si $A \subseteq C$ entonces $\overline A \subseteq \overline C$,  -->

**ejemplo**: $f: \mathbb R \to \mathbb R$ tal que $f(x) = x^2$ es continua, y $f^{-1}(\{1\}) = \{-1,1\}$, veamos que $f^{-1}(\{1\})$ no es conexo, pero $\{1\}$ es conexo.

Ahora si f es continua e inyecticva $A\subseteq Y$ conexo, entonces $f^{-1}(A)$ es conexo.? Falso.

Tenemos dificultades en el sentido de que si $f^(A)= A\cup B$, donde $A,B$ son abiertos disjuntos no vacios, no hay garantias de que $f$ mande abiertos en abiertos. $C= f^{-1}(A)$ y $D = f^{-1}(B)$ son abiertos disjuntos no vacios, pero no necesariamente $f(C) \cap f(D) = \emptyset$.pues no se puede garantizar que $f(C) \cap f(D)$ sean abiertos,


**ejemplo**: dada la metrica discreta $id: (X, \mathcal T_{discreta}) \to (X, \mathcal T_{trivial})$ es continua.

$(X, \mathcal T_{trivial})$ es conexo, pero $(X, \mathcal T_{discreta})$ no es conexo si $|X|>1$.


**Definicion** $f: X \to Y$ es abierta si envia abiertos en abiertos 

$f: X \to Y$ continua y abierta, $A\subseteq A$ conexo, entonces $f^{-1}(A)$ es conexo? y si es biyectiva? y si es homeomorfismo?

suponga que $f^{-1}(A) = C \cup D$, (una separacion).


**Teorema**: Si $X$ y $Y$ son conexos, entonces $X$ y $Y$ son conexos.


Demostracion: Necesitamos un lemma


**Lemma**: Si $\{A_i\}_{i \in I}$ es una coleccion de subespacion de $X$  y

$$
\begin{align*}
\bigcap_{i \in I} A_i \neq \emptyset
\end{align*}
$$

entonces $\bigcup_{i \in I} A_i$ es conexo.


**Demostracion**: Supongamos

$$
\begin{align*}
\bigcup_{i \in I} A_i = C \cup D
\end{align*}
$$
Separacion de la unitoria.

SEa $j \in I$ intersectando con $A_j$

$$
\begin{align*}
A_j = (C \cap A_j) \cup (D \cap A_j)
\end{align*}
$$

entonces $A_j \subseteq C$ o $A_j \subseteq D$

Como $\bigcap_{i \in I} A_i \neq \emptyset$, entonces

$$
\begin{align*}
\forall i \in I, A_i \cap C \quad \text{sii} \quad \bigcup_{i \in I} A_i \cap C \neq \emptyset \\

 \forall i \in I, A_i \cap D \quad \text{sii} \quad \bigcup_{i \in I} A_i \cap D \neq \emptyset
\end{align*}
$$

Luego $\bigcup_{i \in I} A_i$ es conexo.

**Demostracion** (teorema antes del lema):


a) $(X \times \{y_0\}) \cup (\{x_0\} \times Y)$ conexo, como $(X \times \{y_0\})$ es conexo al ser homeomorfo a $X$ y $(\{x_0\} \times Y)$ es conexo al ser homeomorfo a $Y$.Aplicando el lema tenemos que es conexo.

b) $X \times Y$ conexo sea $y_0$ fijo, 
$$
\begin{align*}
X \times Y = \bigcup_{x \in X}  (X \times \{y_0\}) \cup (\{x_0\} \times Y) 
\end{align*}
$$

 $(X \times \{y_0\}) \cup (\{x_0\} \times Y) $ es conexo por a)

 y 

$$
\begin{align*}
\bigcap_{x \in X} (X \times \{y_0\}) \cap (\{x_0\} \times Y) = (x_0,y_0) = X \times \{y_0\} 
\end{align*}
$$

Por el lema $X \times Y$ es conexo.

**Colorario** $\mathbb R^n$ es conexo.
$[a,b]$ es conexo.
$(a,b)$ es conexo.


$$ 
\begin{align*}
\bigcup_{a<c<\frac{a+b}{2}}[c,d] = (a,b) \quad text{conexo} \\
\end{align*}
$$

**Definicion** Un espacion topologico $X$ es arco conexo (conexo por caminos) si para cualesquiera $x,y \in X$ existe un camino continuo $\gamma: [0,1] \to X$ tal que $\gamma(0) = x$ y $\gamma(1) = y$.


Arco conexo implica conexo, pero no al reves.

**Teorema**
Si $X$ es arco conexo, entonces entonces conexo.

**Demostracion**: Necesitamos un lema.


**Lema**: Si $X$ es conexo sii los unicos subespacions de $X$ que son abiertos y cerrados son $X$ y $\emptyset$.

**Demostracion**: 
$\implies$ Si $A$ es abierto y cerrado no vacio y no todo $X$

$\impliedby$ sup. que $X$ no es conexo, entonces 

$$
\begin{align*}
    X = A \cup (X-A)
\end{align*}
$$

que es separacion de $X$ 

$$
\begin{align*}
X = A \sqcup B
\end{align*}
$$

y $A,B$ son abiertos de $X$ y $A,B \neq \emptyset$.

Entonces $A$ es abierto y cerrado, $A= \emptyset$ o $A = X$.

**Teorema**: $X$ arco conexo implica conexo.


Fijemos $x_0 \in X$, $\forall x \in X$ existe un camino conitnuo $\gamma_x:[0,1] \to X$  tq $\gamma_x(0) = x_0$ y $\gamma_x(1) = x$.

Notese que $\Im(\gamma_x)$ es conexo al ser imagen basjo una funcion continua de $[0,1]$ ahora:

$$
\begin{align*}
X = \bigcup_{x \in X} \Im(\gamma_x)
\end{align*}
$$

pero $x_0 \in \bigcap_{x \in X} \Im(\gamma_x) \neq \emptyset$

Luego por el lema (el que corresponda) $X$ es conexo.

**Ejercicio** mostrar $(0,\infty)$ es conexo.
La curva del topologo.

Sea $f(x) = \sin{\frac{1}{x}}$ para, una funcion de $(0,\infty)$ a $\mathbb R$. y consideremos $F(x) = (x,f(x))$.

Sea $C = \Gamma_F = \{(x,\sin{\frac{1}{x}}): x \in (0,\infty)\}$y 
-$C$ es conexo y 
- $C$ es arcoconexo. 
- $\overline C$ es conexo por un teorema anterior,
- $\overline C$ No es arcoconexo.

Como $\overline C = C \cup (\{0\}) \times [-1,1]$. $(0,1)$(ejercicio) no se conecta por un camino con $(\frac{2}\pi,1)$.

Si $\gamma: [0,1] \to \overline C$  es un camino. Con $\gamma(0) = (0,1)$, entonces $\Im(\gamma) \subseteq \{0\} \times [-1,1]$ 

Ahora sea $\gamma_\epsilon : = \gamma_{\gamma^{-1}(C_\epsilon)} : \gamma^{-1}(C_\epsilon) \to \overline C \cap B_{\epsilon}((0,1))$, con $C_\epsilon = \overline C \cap B_{\epsilon}((0,1))$. $\gamma_\epsilon$ es continua. 

$$
\begin{align*}
\Pi \circ \gamma_\epsilon :\gamma^{-1}(C_\epsilon) \to \mathbb R
\end{align*}
$$

Existe $c>0$ tq $[0,c] \subseteq \gamma^{-1}(C_\epsilon)$m entonces $\Pi \circ \gamma_\epsilon ([0,c]) =\{0\}$ es conexo.

Dado que 
$$
\begin{align*}
    \gamma(1) = \left(\frac{2}{\pi},1\right)
\end{align*}
$$

Sea $A = \Im (\gamma) \cap C$, A = \Im($\gamma$)?, $A\subseteq \Im(\gamma)$

- $A$ es abierto en $\Im(\gamma)$, 
- $A$ es cerrado en $\Im(\gamma)$,
- $A \neq \emptyset$.

entonces $A = \Im(\gamma)$.

Sea $(x,y) \in A$, $(x,y) = \gamma(t)$b , $t \in [0,1]$, $(x,y) \in C$,$(x,y) = (\ell.\sin{\frac{1}{\ell}})$, 

----

