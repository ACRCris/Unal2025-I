# Logica proposicional clasical.

**Idea**: Construir una estructura indcutiva donde los bloques sean las proposiciones mas simples (Sin conectivos) y los operadores de la estructura sean considerandos usando los conectivos clasicos.


Bloques:

$$ 
B_{\text{prop(A)}} := \{p_n: n<\omega\} \cup \{T,\perp\}
$$

$[p_n: \text{Letras proposicionales atomos propocionales}]$

Operadores:

$$
\begin{align*}
\Sigma := (B_{\text{prop(A)}} \cup \{ \land, \lor, \neg\})^{<\omega} \\
\end{align*}
$$

Es muy necesaria la unicidad de lectura. Notacion Polac? los conectivos vas al inicio como si fuera una funcion. sigma es nuestro conjunto de 

$$
\begin{align*}
    K_{props(A)}: F_{\neg}: \Sigma &\to \Sigma\\
                            x \to \neg x
\end{align*}
$$

$$
\begin{align*}
    K_{props(A)}: F_{\land}: \Sigma \times \Sigma &\to \Sigma\\
                            (p,q) \to  \land pq
\end{align*}
$$

$$
\begin{align*}
    K_{props(A)}: F_{\lor}: \Sigma \times \Sigma &\to \Sigma\\
                            (p,q) \to  \lor pq
\end{align*}
$$




Definicion $Prop(A): = C(B_{props(A)}, K_{props(A)})$

Observacion: En general, los elementos de $A =\{p_n: n<\omega\}$ se denotan con letras latinos minusculos $p,q,r,s \dots$.

**Ejemplos:**

(1) $p,q,r \in Prop(A) (\text{por que estan en A})$ 

(2) $F_{\neg}(p) = \neg p$

(3) $F_{\lor}(\neq p, q) = \lor \neg p\,q [:= (\neg p)\lor q] \in Prop(A)$ 

(4) $F_{\land}(\lor \neg pq,r) = \land \lor \neg pqr [:= ((\neg p) \lor q) \land r] \in Prop(A)$ 


Teorema $Prop(A)$ satisface unicidad de lectura

Demostracion:

* Sea $\alpha$ atomo (proposicional T o $\perp$), proposiciones de la forma $F_{\neg}(\gamma)$, $F_{\delta}(\gamma,\delta)$, con $\delta \in \{\land,\lor \}$ tienen longitud mayor igual que 2, luego $\alpha$ No puede ser de la forma.
* 
* Si $\alpha$ no es atomo (Bloque), por construccion de $Prop(A)$, existe una proposicion $\beta$ tal que $\alpha = \neg \beta$  o existen proposciones $\gamma, \delta$ tales que $\alpha = \land \gamma \delta$ o $\alpha = \lor \gamma \delta$. No se da el caso de que $\neg \beta = \Delta \gamma \delta$ (El primer simbolo es diferente). Tampoco se da el caso de que $\alpha = \land \gamma \delta = \lor \gamma \delta$ (mismo motivo)

(1) Si $\alpha = \neg \beta = \neg \beta'$,  $\beta = \alpha|dom(\alpha)\{0\} = \beta'$, como funciones $\neq \neg p$ es diferente de p aunque sean equivalentes.

(2) si $\alpha  = \Delta \beta \gamma = \Delta \beta' \gamma'$, note que $\beta \gamma = \alpha | \, dom(\alpha)\{0\} = \beta' \gamma'$

A probar: $\beta = \beta'$ y $\gamma = \gamma'$ (por unicidad de lectura).

Definicion: Sea $\braket{} \neq \alpha \in \Sigma$. Decimos que $\braket{} \neq \alpha$  es segmento terminal (propio) de $\alpha$  sii existe (propio) otra palabra $\gamma \in \Sigma$ tal que $\alpha = \gamma \cdot \beta$ (concatenacion de palabras).

Ejemplo: 

$\alpha := \neg pq \lor \land r$ con $\beta = \lor \land r$ y $\gamma = \neg pq$ luego $\gamma \cdot \beta = \neg pq \cdots \lor \land r= \neg rq\lor \land r = \alpha$ por lo tanto, $\beta$ es un segmento terminal (propio) de $\alpha$.

Lema Dada $\alpha$ proposicion, todo segemento terminal de $\alpha$ es concatenacion de propocisiones. (Un segemento terminal es eliminar el inicio y me quedo con el final).

Demostracion: Por induccion en $Prop(A)$. Sea $\alpha$ propsicion. 

(1) Caso Base: Si $\alpha$ es atomo (Letra proposicional, T o $\perp$), el unico semenento terminal de $\alpha$ es $\alpha$ mismo, que es una proposcion.

(2) Sea $\alpha = \neg \beta$ con $\beta$ proposicion que satisface el lema (hipostesis de induccion). Sea $\gamma$ segmento termminal de $\alpha = \neg \beta$.
* Si $\gamma = \neg \beta$, $\gamma$ es una proposicion.
* Si $\gamma$ es segmento terminal propio de $\alpha$, o bien $\gamma = \beta$ (seria proposicion) o es segmento terminal propio de $\beta$  por lo que por hipotesis de induccion es concatenacion de proposiciones.

(3) Sea $\alpha = \Delta \beta \gamma$ con $\beta, \gamma$ proposiciones que satisfacen el lema (hipotesis de induccion). Sea $\delta$ segmento terminal de $\alpha$. 
* Si $\delta = \Delta \beta \gamma$, $\delta$ es una proposicion.
* Si $\delta = \beta \gamma$, $\delta$ es una concatenacion de las proposiciones $\beta$ y $\gamma$.
* Si $\delta$ es un segmento terminal propio de $\beta \gamma$:
* 
  (a) Si $\delta = \beta' \gamma'$, con $\beta'$ segmento terminal propio de $\beta$, por hipostesis de induccion $\beta'$ eses concatenacion de proposiciones $\beta_1, \dots, \beta_n$. (Es concatenacion de propociones).

  (b) Si $\delta = \gamma$, $\delta$ es uan proposicion.

  (c) Si $\delta$ es un segmento terminal propio de $\gamma$, por hipotesis de induccion es concatenacion de proposiciones.

Por el principio de induccion generalizado en $Prop(A)$, la afirmacion VALe pra todo $\alpha \in Prop(A)$.

Definicion: Sean $\alpha = s_0 \cdot \dots \cdot s_n \in \Sigma$ y $\beta = t_0 \cdot \dots \cdot t_k \in \Sigma$ :

$$
\alpha \beta = s_0 \cdots s_n \cdot t_0 \cdots t_k
$$

Defincion: Sea $\braket{} \neq \alpha \in \Sigma$. Decimos que $(\braket{}) \neq \alpha \in \Sigma$ es un segmento inicial (propio) de $\alpha$ sii existe $(\braket{}) \neq \gamma \in \Sigma$ tal que $\alpha = \gamma \beta$ (concatenacion de palabras).

Lema: Sea $\alpha \in Prop(A)$ y $\beta \neg \braket{} \es segemento inicial propio de $\alpha$. Entonces $\beta \neq Prop(A)$.

Definicion $W(\neg):= 0$ 
$W(\alpha) 1 (\text{ $\alpha$ ;etra proposicional T o $\perp$})$

$W(V) = W(\land) = -1\dots

Dada $\alpha = s_0 \cdots s_n \in \Sigma$ y, $W(\alpha) = W(s_0) + \dots + W(s_n)$

(2) Si $\alpha = \neg \lor \land$, 
$W(\alpha) = W(\neg) + W(\lor) + W(\land) + W(p) =0 + -1 + - 1+ 1 = -1$


Afirmacion: Para todo $\alpha \in Prop(A)$, $W(\alpha) =1$.


Demostracion: por induccion en $Prop(A)$:

(1) Caso base: Por definicion para los atomos tienen peso 1.
(2) Caso $neg$ suponga que $\alpha \in Prop(A)$  satisface que $W(\alpha) = 1$. (hipotesis de induccion).

$W(\neg \alpha) = W(\neg) + W(\alpha) = 0 + 1 = 1$

(3) Caso $\Delta$ suponga que $\alpha, \beta \in Prop(A)$   satisface que $W(\alpha) = 1$ y $W(\beta) = 1$ (hipotesis de induccion).

$$
W(\Delta \alpha \beta) = W(\Delta) + W(\alpha) + W(\beta) = -1 + 1 + 1 = 1$$

Por lo tanto, por el principio de induccion generalizada en $Prop(A)$, para toda $\alpha \in Prop(A)$, se tiene que $W(\alpha) = 1$.


Observacion: Ell reciproco no es cierto, 

$W(p\neg \neg ) = 1$ pero $p \neg \neg$ no es una proposicion. y $\alpha \notin Prop(A)$, ? (? es completar detalles.)  