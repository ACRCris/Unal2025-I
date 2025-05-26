### Espacios metricos normales

Metricos implica normales, y normales implica hausdorff.

**Teorema**

todo espacio metrico es normal.


**Demostracion**

Necesitamos un lemma $\epsilon = d(A,B)$ . Dado $(X,d)$ un espacio metrico y $A\subseteq X$ existe por que 0 es cota infrerior del conjunto 

$$
\begin{align*}
d(x, A)= \inf_{a\in A} d(x,a)
\end{align*}
$$

Distancia de $A$ a $x$. 

Esto definie 

$$
\begin{align*}
d(-,A) : X &\mapsto A \to \mathbb{R}\\
x&\mapsto d(x,A)
\end{align*}
$$

**Lema**

$d(-,A)$ es continua.

**Demostracion**

Sea $\epsilon > 0$ y $x\in X$. Talque la $d(x,y)<\epsilon/2$ existe $a \in A$ tq:

$$
\begin{align*}
d(x,a) < d(x,A) + \delta
\end{align*}
$$


$$
\begin{align*}
d(y,A) \leq d(y,a) \leq d(x,y) + d(x,a) < \epsilon/2 + d(x,A) + \delta
\end{align*}
$$


Se tiene para todo $\delta > 0$.

Esto implica que 

$$
\begin{align*}
d(y,A) < d(x,A) + \epsilon/2
\end{align*}
$$

luego 

$$
\begin{align*}
d(y,A) - d(x,A) \leq \epsilon/2
\end{align*}
$$
por simetria 

$$
\begin{align*}
d(x,A) - d(y,A) \leq \epsilon/2
\end{align*}
$$

Luego:


$$
\begin{align*}
|d(x,A) - d(y,A)| \leq \epsilon/2
\end{align*}
$$

Esto prueba que $d(-,A)$ es continua.

**Nota**: $f:(
    X,d
) \to (Y,p)$ es continua si para todo $x \in X$, para todo  $\epsilon > 0$ existe $\delta > 0$ tal que para todo $x' \in X$, $d(x,x') < \delta$ implica $p(f(x),f(x')) < \epsilon$.


Sean $A,B \subseteq^{\text{cerr}} X$, $A \cap B \neq \emptyset$. Sea $U = \{
    x \in X : d(x,A) < d(x,B)\}$ y $V = \{
    x \in X : d(x,B) < d(x,A)\}$.

Veamos que:

- $U,V \subseteq^{\text{abierto}} X$.
- $U \cap V = \emptyset$. (es facil)
- $A \subseteq U$ y $B \subseteq V$.   
  
  SEa $A \in A$, $d(a,A) = 0$ 

  $\a \in U $? , 
  s.c $d(a,B) = 0$ 

Sea $n\in \mathbb{N}/\{0\}$, $\frac {1}{n}$, es cota inferior de $\{d(a,b): b \in B\}$. Existe $b_n \in B$ tq $d(a,b_n) < \frac{1}{n}$. $\{b_n\}$ es una sucesion de elementos en $B$ converge a $a$ (**Ejercicio**).

Como $B$ es cerrado, entonces $a \in B$. contradiccion.

Luego $d(a,B) > 0$. y entonces $a \in U$. ($d(a,A) = 0<d(a,B)$).

Analogamente $B \subseteq V$.

$$
\begin{align*}
  U = \{
    x \in X : d(x,A) - d(x,B)<0
  \} = f^{-1}((-\infty,0))
\end{align*}
$$
donde $f(x) = d(x,A) - d(x,B)$. es continua, como $(-\infty,0) \subseteq^{\text{abierto}} \mathbb{R}$, donde $U \subseteq^{\text{abierto}} X$. y $V$ es abierto de $X$.


## numeros de lebesgue

Sea $(X,d)$ un espacio metrico y sea $\{
    u_i : u_i \in I\}$ un cubrimiento abierto de $X$.

Existe un $\epsilon > 0$  tq si para todo $A\subseteq X$, $diam(A) < \epsilon$  entonces $A\subseteq^{\text{abierto}} U_i$, para algun $i$. Solo se puede garantizar si $X$ es compacto. $\epsilon$ se llama un numero de $lebesgue$,  del cubrimiento.
 
Consideremos por ejemplo $\{n-1,n+1: m \in \mathbb{Z}\}$, $\epsilon = 2$ no sirve.

Si $\epsilon = 1$ para todo $x \in \mathbb{R}$,

$$
\begin{align*}
  \{x - 1/2, x + 1/2\} \subseteq ([[x]], [[x]]+2)
\end{align*}
$$

o

$$
\begin{align*}
  \{x - 1/2, x + 1/2\} \subseteq ([[x]]-1, [[x]]+1)
\end{align*}
$$

**Ejercicio**
 
Encontrar un cubrimiento de $\mathbb{R}$ (si existe) no que tenga numero de $lebesgue$.

**Teorema** Tdoo cubrimiento de un espacio metrico compacto $X$ tiene un numero de lebesgue.

**Demostracion**

Como $X$ es comapcto todo cubrimiento tiene un subcubririmiento finito. Podemos suponer que el cubrimmiento es finito, digamos 
$$
\begin{align*}
  \{U_i \}_{i=1}^n
\end{align*}
$$

Si  $diam(A) = \sup\{d(x,y) x,y\in A\} < \epsilon$. entonces 

$$
\begin{align*}
  A \subseteq B_{2\epsilon}(x_0)
\end{align*}
$$

para algun $x_0 \in A$. $x \in A$

$$
\begin{align*}
  d(x,x_0) \leq diam(A) < \epsilon
\end{align*}
$$

entonces 

$$
\begin{align*}
  x\in B_{\epsilon}(x_0) 
\end{align*}
$$

Basta con demostrar la condicion de lebesgue para 

$$
\begin{align*}
A= B_{\epsilon}(x_0)
\end{align*}
$$

$B_{\epsilon}(x_0) \subseteq U_i$ sii $d(xm X- U_i) \geq \epsilon$. 



Basta con encontrar un $\epsilon>0$ tal que existe un $i =1,\ldots,n$ tal que $d(x,X-U_i) \geq \epsilon$. sii $\max\{
    d(x,X-U_i): i=1,\ldots,n
\} \geq \epsilon$.


Cada $d(-,X-U_i)$ es continua, $f$ es continua. donde 
$$
\begin{align*}
  f: X &\to \mathbb{R}\\
  x&\mapsto \max\{
    d(x,X-U_i): i=1,\ldots,n
    \}
\end{align*}
$$

Como $X - U_i$ es cerrado, si $x\in U_i$

$$
\begin{align*}
  d(x,X-U_i) >0
\end{align*}
$$

Si no existiría una sucesión $\{y_i\}\subseteq X - U_i$ como $X-U_i$ es cerrado, $x \in X - U_i$. Contradiccion.

Ahora sea $x \in X$ como $\{U_1,\dots ,U_n\}$ es un cubrimiento entonces existe $i \in \{1,\ldots,n\}$ tal que $x \in U_i$.luego $d(x_i,X-U_i) >0$. es decir $f(x) > 0$.

Como $X$ es compacto, $f$ es continua y $f(X)$ es compacto de $\mathbb R$ luego $f(X)$ es cerrado y acotado. Pero $|f(x)| >0$, luego 



$$
\begin{align*}
  \inf_{x\in X} f(x) = \epsilon >0
\end{align*}
$$

Luego para todo $x \in X$, $f(x) \geq 0$. Esto demuestra lo que queríamos.


**Colorario** $f:(X,d)\to (Y,p)$ es continua con $X$ espacion metrico compacto y $Y$ espacio metrico, entonces $f$ es uniforme continua.

Para todo $\epsilon > 0$ existe un $\delta > 0$ tal que para todo $x,y \in X$, $d(x,y) < \delta$ implica $p(f(x),f(y)) < \epsilon$.


**Demostracion**
Sea $\epsilon > 0$ cubrimos $X$ con los abiertos $\{
    f^{-1}(B_{\epsilon/2}(y)): y \in Y\}$. Sea $\gamma >0$ el numero de lebesgue asociado al cubrimiento y sea $\gamma = \delta/2$

$$
d(x,y) < \gamma/2
$$

SI Y SOLO SI 

$$
x \in B_{\gamma/2}(y)  
$$

entonces existe un $y \in Y$ tal que $B_{\gamma/2}(x) \subseteq f^{-1}(B_{\epsilon/2}(y))$. 

Ahora sean $x \in B_{\gamma/2}(x)$ y $x'$ en $B_{\gamma/2}(x)$, entonces $f(x) \in B_{\epsilon/2}(y)$ y $f(x') \in B_{\epsilon/2}(y)$, luego 


$$
\begin{align*}
  p(f(x),f(x')) \leq p(f(x),y) + p(f(x'),y) < \epsilon
  \end{align*}
  $$


**Ejercicios**

Hatcher pg 38, 39: 15-16
Viro - ivanov : pg 85 12.33 12.34 pg 88
./