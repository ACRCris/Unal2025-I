Mecanica cuantica (1900's) Planck, Schrodinger, Bohr, Einstein, Feynman, 
| Concepto               | Descripción                                                                      |
|------------------------|-----------------------------------------------------------------------------------|
| Computacion (1940's)   | Turing, Von Neumann, Feynman                                                      |
| Fisica                 | "Desafios de la construccion y materializacion de los computadores cuanticos"      |
| Matematica aplicada    | "que podemos hacer con dichos desarollos"                                         |

# Mecanica cuantica

Un estado cuantico es una superposicion de estados calsiscos descritos como un vector de amplitudes al cual podems aplicar bien sea una medida o una operacion (unitaria).

Un estado clasico, es un estado de un sistema cuantico que nos presenta ni superposición ni entrelazamiento.


|| estado clasico| estado cuantico|
|----|---------------|-----------------|
|Represeantacion|bits | determinista  
| Valor | qubits | probabilistico|
| Entrelazamiento|No tiene entrelazamiento| tiene entrelazamiento|



Un bit clasico se puede representar como un "0" o un "1", un qubit puede estar en superposicion:

$$
\alpha |0\rangle + \beta |1\rangle$$

**superposición**: Un estado fisico que puede estar en N diferentes estados al mismo mutuamente excluyentes $|0\rangle, |1\rangle, |2\rangle, ... |N\rangle$.  Asi, un estado clasico puro  se puede considerar como un estado que puede encontrarse si se observa un estado fisico.

Un estado cuántico puro es una superposición de estados clásicos:

$$
|\omicron\rangle = \alpha_1 |0\rangle + \alpha_2 |1\rangle + \alpha_3 |2\rangle + ... + \alpha_N |N\rangle$$

donde $\alpha_i$ es la amplitud de probabilidad del i-esimo ket. 

Nota: un sistema es un estado cuántico esta en todos los estados clásicos al mismo tiempo.


Los estados $|0\rangle$, $|1\rangle$, $|2\rangle$, ... $|N-1\rangle$ forma una base ortonormal en un espacio N-dimensional de Hilbert (Espacio vectorial dotado de un producto interno). 

El estado notado:

$$
|\psi\rangle = \begin{pmatrix}
\alpha_1 \\ \alpha_2 \\ \alpha_3 \\ ... \\ \alpha_N \end{pmatrix}$$

y el estado:

$$
\langle \psi | = \begin{pmatrix}
\alpha_1^* & \alpha_2^* & \alpha_3^* & ... & \alpha_N^* \end{pmatrix}$$

**Producto interno**

El producto interno $\langle \psi | \psi \rangle$ se denominara "bra-ket", y de forma similar se puede montar $|\psi \rangle \langle \psi |$ que se denomina "ket-bra".

------

Si $|0\rangle$, $|1\rangle$, $|2\rangle$, ... $|N-1\rangle$ es una base ortonormal de $\mathbb{H}_A$
y $|0\rangle$, $|1\rangle$, $|2\rangle$, ... $|M-1\rangle$ es una base ortonormal de $\mathbb{H}_B$ entonces:

El espacio producto tensioral:
$$
\mathbb{H} = \mathbb{H}_A \otimes \mathbb{H}_B$$

es un espacio vectorial de dimension $N\cdot M$, y estara generado por los estados:

$$
\{ |i\rangle \otimes |j\rangle \text{ con } i=0,1,...,N-1 \text{ y } j=0,1,...,M-1 \}$$

Por otro lado, un estado arbitrario de $\mathbb{H}$ se conoce como bipartito y se describe como:


$$
\sum_{i,j} \alpha_{ij} |i\rangle \otimes |j\rangle$$


**Nota** (Producto tensorial): Sean $v, w \in \mathbb{C}^2$ con:

$$
v = \begin{pmatrix} a \\ b \end{pmatrix}$$
$$

w = \begin{pmatrix} c \\ d \end{pmatrix}$$

entonces:

$$
v \otimes w = \begin{pmatrix} a \\ b \end{pmatrix} \otimes \begin{pmatrix} c \\ d \end{pmatrix} 
= \begin{pmatrix}
    a \begin{pmatrix} c \\ d \end{pmatrix} \\
    b \begin{pmatrix} c \\ d \end{pmatrix}
\end{pmatrix}
= \begin{pmatrix} ac \\ ad \\ bc \\ bd \end{pmatrix}$$


**Nota**:

$$
|0\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$$
$$
|1\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$$


Asi el producto tensorial de dos qubits es:

$$
|01\rangle = |0\rangle \otimes |1\rangle  = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \otimes \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \\ 0 \\ 0 \end{pmatrix}$$


y 

$$
|00\rangle = |0\rangle \otimes |0\rangle  = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \otimes \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}$$

$$
|10\rangle = |1\rangle \otimes |0\rangle  = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \otimes \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}$$


$$
|11\rangle = |1\rangle \otimes |1\rangle  = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \otimes \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \end{pmatrix}$$

### Ejemplo

Sea $\mathbb{H}_A = \{|0\rangle_A, |1\rangle_A\}$ y $\mathbb{H}_B = \{|0\rangle_B, |1\rangle_B\}$, el producto tensorial:

$$
\mathbb{H} = \mathbb{H}_A \otimes \mathbb{H}_B$$

y la base sera:

$$
\mathbb{H} \equiv^{b} \{|0\rangle_A\otimes |0\rangle_B, |0\rangle_A\otimes |1\rangle_B, |1\rangle_A\otimes |0\rangle_B, |1\rangle_A\otimes |1\rangle_B\} = \{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$$


El estado bipartito:

$$
|\psi\rangle =  \sum_{i,j=0}^{1} \beta_{ij} |i\rangle_A \otimes |j\rangle_B = \beta_{00} |00\rangle + \beta_{01} |01\rangle + \beta_{10} |10\rangle + \beta_{11} |11\rangle$$



------ 


los estados cuánticos pueden ser medibles o dejados evolucionar unitariamente sin medir.

**Mediciones**: Para el estado $\psi\rangle$ no es posible observar la superposición. Si sera posible observar alguno de sus estados Cual?

Regla de Born: Solo se observar el estado $|j\rangle$ con probabilidad $p_j = |\alpha_j|^2$.

Esto es, observar un estado cuantico induce una distribucion de  probabilidad sobre los estados clasico y estara dad por la nomra de loas amplitudes. Asi:

$$
\sum_{j=0}^{N-1} p_j = \sum_{j=0}^{N-1} |\alpha_j|^2 = 1$$

Si medimos el estado cuantico $|\psi\rangle$ entonces el estado desaparace y todo lo que quedara es un estado $|j\rangle$ con probabilidad $p_j = |\alpha_j|^2$.(Medir u observar colapsa la superposicion).

### Ejemplo

Las probabilidades de medir $|\psi\rangle$ y $e^{i\theta}|\psi\rangle$ son las mismas. Donde %$e^{i\theta}$ se conoce como fase global. 

Sean $|\psi\rangle = \alpha |0\rangle + \beta |1\rangle$ y $|\phi\rangle = e^{i\theta}|\psi\rangle = e^{i\theta}(\alpha |0\rangle + \beta |1\rangle)$, entonces:

$$
P(0) = |\alpha|^2 = |e^{i\theta}\alpha|^2 = |\alpha|^2$$

$$
P(1) = |\beta|^2 = |e^{i\theta}\beta|^2 = |\beta|^2$$


## Medición proyectiva (MP)

Una MP en algun espacion con m posibles salidas (estados)
es una coleccion de proyectores $P_j$ que actuan sobre el espacio y:


$$
\sum_{j=0}^{m-1} P_j = I$$


Aqui trataremos a los proyectores (via operador densidad $\rho$), como $P_j = |j\rangle\langle j|$. Tambien se necesita que los proyectores sean ortogonales, es decir:

$$
P_j P_k = \delta_{jk} $$

Para el proyector $P_j$ se tendra una proyeccion sobre el sub espacio $\mathbb{H}_j$ del espacio total de Hilbert $\mathbb{H}$, y cada estado $|j\rangle$ en $\mathbb{H}$ se puede escribir como:

$$
|\psi\rangle = \sum_{j=0}^{m-1} |\psi_j\rangle$$


donde $|\psi_j\rangle = P_j |\psi\rangle$ es el estado proyectado sobre el subespacio $\mathbb{H}_j$.

Ejemplo: $\mathbb{H} = C^2$ (un solo qubit) queremos proyectar un estado arbitrario sobr edos subespacios definidos sobre $|0\rangle$ y $|1\rangle$:

Sea $|\psi\rangle $ estado cuantico arbitrario:
$$
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle$$
$$
|\psi\rangle =|\psi_0\rangle + |\psi_1\rangle$$

con $\alpha, \beta \in \mathbb{C}$ y $|\alpha|^2 + |\beta|^2 = 1$.

El proyector $P_0$ sobre $\mathbb{H}_0  = gen(\{|0\rangle\})$ es $P_0 = |0\rangle\langle 0| = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$ y el proyector $P_1$ sobre $\mathbb{H}_1 = gen(\{|1\rangle\})$ es $P_1 = |1\rangle\langle 1| = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$. Entonces:
$$
|\psi_0\rangle = P_0 |\psi\rangle = |0\rangle\langle 0|(\alpha |0\rangle + \beta |1\rangle) = \alpha |0\rangle$$
$$
|\psi_1\rangle = P_1 |\psi\rangle = |1\rangle\langle 1|(\alpha |0\rangle + \beta |1\rangle) = \beta |1\rangle$$

Asi:

$$
|\psi\rangle = |\psi_0\rangle + |\psi_1\rangle = P_0 |\psi\rangle + P_1 |\psi\rangle$$

Note que:

$$
\sum_{j=0}^{1} P_j = P_0 + P_1 = |0\rangle\langle 0| + |1\rangle\langle 1| = I$$ 
y tambien 
$$P_0 P_1 = 0$$ 
$$P_1 P_0 = 0$$

**Medicion proyectiva MP

Podemos medir $|\psi\rangle$ para obtener la salida $j$-esima con probabilidad de obtener el estado $|j\rangle$ como:

$$
\mathbb P(j) = ||| \psi_j \rangle ||^2 = Tr(P_j |\psi\rangle\langle \psi|)= \langle \psi | P_j |\psi\rangle$$

Ejemplo, sea:

$$
|\psi\rangle = \frac 35 |0\rangle + \frac 45 |1\rangle$$

con O.N.B %$\{|0\rangle, |1\rangle\}$:

$$
\mathbb P(0) = \langle \psi | P_0 |\psi\rangle = \langle \psi | 0\rangle\langle 0| |\psi\rangle = \langle \psi | 0\rangle\langle 0| (\frac 35 |0\rangle + \frac 45 |1\rangle) = \frac 35$$
$$

\mathbb P(1) = \langle \psi | P_1 |\psi\rangle = \langle \psi | 1\rangle\langle 1| |\psi\rangle = \langle \psi | 1\rangle\langle 1| (\frac 35 |0\rangle + \frac 45 |1\rangle) = \frac 45$$

El estado despues de la medicion colapsara a:

$$
|\psi\rangle = \frac {|\psi_j\rangle}{|||\psi_j\rangle ||}= \frac {P_j |\psi\rangle}{||P_j |\psi\rangle ||}$$

Por ejemplo para el estado $|\psi\rangle = \frac 35 |0\rangle + \frac 45 |1\rangle$,con $\mathbb P(0) = \frac {9}{25}$ colapsa a:

$$
|\psi\rangle = \frac {P_0 |\psi\rangle}{||P_0 |\psi\rangle ||} = \frac {P_0 (\frac 35 |0\rangle + \frac 45 |1\rangle)}{||P_0 (\frac 35 |0\rangle + \frac 45 |1\rangle) ||} = \frac {\frac 35 |0\rangle}{\sqrt{\frac 9{25}}} = |0\rangle$$

Nota: $tr(A) = \sum_{i=0}^{N-1} \langle i | A | i \rangle$.

Ejemplo: Sea $|\psi\rangle = \alpha |0\rangle + \beta |1\rangle$ y $|\alpha|^2 + |\beta|^2 = 1$ y:

$$
|\psi\rangle\langle \psi| = \begin{pmatrix} \alpha \\ \beta \end{pmatrix} \begin{pmatrix} \alpha^* & \beta^* \end{pmatrix} = \begin{pmatrix} |\alpha|^2 & \alpha\beta^* \\ \alpha^*\beta & |\beta|^2 \end{pmatrix} = \alpha\alpha^* |0\rangle\langle 0| + \alpha\beta^* |0\rangle\langle 1| + \alpha^*\beta |1\rangle\langle 0| + \beta\beta^* |1\rangle\langle 1|$$
