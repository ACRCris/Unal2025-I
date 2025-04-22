### Enunciado 1
- I would suggest him to verify right now that the interior of $B$ is the union of all open sets contained in $B$, and that the closure of $B$ is the intersection of all closed sets containing $B$.

### Solution

#### Lemmita 

If $A \subseteq^{ab} B$, $A \subseteq \mathring{B}$.

By contradiction, suppose $x\in A$ and $x \in \partial B$, then for all neighborhood $U_x$ of $x$, $U_x \cap B \neq \emptyset$ and $U_x \cap (X/B) \neq \emptyset$. So how $A \subseteq B$ then $X/B \subseteq X/A$ and $U_x \cap (X/A) \neq \emptyset$.Therefore for that $x$ there is no $U_x$ such that $U_x \subseteq A$ but $A$ is open, there is a neighborhood $U_x$ of $x$ such that $U_x \subseteq A$. Then we have a contradiction. So $x \in \mathring{B}$.



#### Interior of $B$
Let $B\neq \emptyset$ and $\{A_{i}\}_{i\in I}$ the family of all open subsets of $B$ then:

$$
\bigcup_{i\in I} A_{i} = \mathring{B}
$$

**Case** $\subseteq$:

Let $x\in \bigcup_{i\in B} A_{i}$ then $x\in A_{i}$ for some $i\in I$ then $x \in B \supseteq A_{i}$ so from the before lemma $x \in \mathring{B}$. 

**Case** $\supseteq$:

Let $x\in \mathring{B}$ then there is a neighborhood $U_x$ of $x$ such that $U_x \subseteq B$. So there is an $i \in I$ such that $x \in A_{i} \subseteq U_x \subseteq B$. So $x \in \bigcup_{i\in I} A_{i}$.


So we have that $\mathring{B} = \bigcup_{i\in I} A_{i}$.

#### Closure of $B$
Let:

$$
\begin{aligned}
\mathcal F = \{F \subseteq X \mid F \text{ closed and } B \subseteq F\}
\end{aligned}
$$

then:

$$
\begin{aligned}
\bigcap_{F \in \mathcal F} F = \overline B
\end{aligned}
$$

**Case** $\subseteq$:

The closure $\overline B$ is itself closed and contains $B$ so $\overline B \in \mathcal F$. and therefore:

$$
\begin{aligned}
F^* = \bigcap _{F \in \mathcal F} F \subseteq \overline B
\end{aligned}
$$

**Case** $\supseteq$:

That is: if $x \in \overline B$ then $x \in F^*$ or equivalently, for all $x\notin F^*$ then $x \notin B$

So let $x \notin F^*$ then theris and $F_0 \in \mathcal F$ such that $x \notin F_0$. So $F_0$ is closed and $X/F_0$ is open. Now $B \subseteq F_0$ so $X/F_0 \subseteq X/B$ and $x \in X/B$, that is $x \notin B$. Therefore there is a neighborhood $U_x$ of $x$ such that $U_x \cap B = \emptyset$. So $x \notin \overline B$ and we have that if $x \in \overline B$ then $x \in F^*$. 
