# Producto de operadores:


$$
Tr(\lambda_1 A +\lambda_2 B) = \lambda_1 Tr(A) + \lambda_2 Tr(B)
$$

Este  operador traza define junto con los operadores un espacio de hilbert. Que debe satisfacer:

1. $(A,B) = Tr(A^\dag B)= Tr(A,B)^*\geq= 0$, donde $A^\dag$ es el adjunto de $A$, con las matrices $A$, $B$ son semidefinida positica


Op autoadjuntos  = op Hermiticos. losoperadores autoadjuntos son aquellos que:

$$
A^\dag = A$$

por lo que se satisface:

$$
\braket{\psi|A|\phi} =\braket{\phi|A|\psi}
$$

$$
M \to M_{ij} = \braket{u_i|M|u_j}$$

$$
(M_{ij}) = M_{ij} = M_{ij}^* =M_{ij}$$


Notemos que:

$$
\sigma_y = \begin{pmatrix}
0 & -i\\
i & 0
\end{pmatrix}
$$
 
$$
\sigma_y \sigma_y = \begin{pmatrix}
0 & -i\\
i & 0
\end{pmatrix} \begin{pmatrix}
0 & -i\\
i & 0
\end{pmatrix} = 1
$$

## $T_1$ Identificando matrices hermiticas

$$
\braket{\psi|X|\psi} = \braket{\psi|X|\psi}^*
$$

entonces


$$
\braket{\phi_1|X|\phi_2} = \braket{\phi_2|X|\phi_1}^*
$$


Se tiene que $X = X^{\dagger}$

### Valores propios

$$
X\ket{x_1} = x_i \ket{x_i}
$$

y tambien:

$$
\bra{x_i}X^\dagger = x_i^* \bra{x_i}
$$

con $x_i = e^{i\theta}$

### Base computacional 

$$
\ket{0} = \begin{pmatrix}
1\\
0
\end{pmatrix} \quad \ket{1} = \begin{pmatrix}
0\\
1
\end{pmatrix}$$


si operamos $\sigma_z$ entonces $\sigma_z \ket{0} = 1\ket{1}$ y $\sigma_x \ket{1} = -1\ket{1}$


## $T_2$ Valores propios de operadores hermiticos son reales


$$
X = X^{\dagger}
$$ 

tenemos 

$$
X\ket{x_i}= x_i\ket{x_i}
$$

Multiplicando con el bra

$$
\braket{x_i |X|x_i} = x_i^*\braket{x_i|x_i}= x_i\braket{x_i |x_i} = x_i^*\braket{x_i|x_i}
$$

Asi $x_i = x_i^*$

## Teorema 3: Vectores propios correspondientes a vectores propios distintos son ortogonales


$$
X\ket{x_i} = x_i\ket{x_i} \quad X\ket{x_j} = x_j\ket{x_j}
$$

con $x_i \neq x_j$


Luego multiplicando la anteriores ecuaciones:

$$
\bra{x_j}X\ket{x_i} = x_i\bra{x_j}\ket{x_i} \quad \bra{x_i}X\ket{x_j} = x_j\bra{x_i}\ket{x_j}
$$

Asi 

$$
(x_i -  x_j) \braket{x_i|x_j} = 0
$$
luego 
$$
\braket{x_i|x_j} =0 
$$
-----
### Definiciones

**Espectro** $X$ es $\{x_1,\dots,x_n\}$ conjunto de autovalres

**Degeneramiento**: $x_1$  es n degenerado entonces existen $n$ vectores propios diferentes con valor propio $x_1$ (puede ser indicio de una simetria)

**Proyectores** Un operador $\mathbb P$ talque $\mathbb P^2 = P$ y $P^{\dagger} = P$, como por ejemplo:

$$
P = \ket{x_i} \bra{x_i}$$
Si $i$ es degenerado 

$$
\mathbb P_i=\sum_{l=1}^n \ket{x_i^{(l)}}\bra{x_i^{(l)}}
$$

Si $i$ tienen degeneracion n.

Descomposicion espectral. Sea $X\ket{x_i}  = x_i \ket{x_i}$ Estos vectores los propios los usamos para una base, y en esta base el operado $X$ es diagonal, y la matriz de $X$ es diagonal.
$$
X = \sum_{i=1}^n x_i \mathbb P_i$$


Nos sirve para definir funciones de operadores. Para demostrar que una serie de funciones converge se debe hacer descomposicion espectral.

$$
f(x) \equiv = \sum_{i=1}^n f(x_i) \mathbb P_i$$


**Ejemplo**: Sea $e^{iHt}\equiv \sum_{i=1}^n e^{iE_it} \mathbb P_i$


### From EPRto Bell's inequalities  EPR

En el paper original trabajan sobre el espacio de los momentos.

Vamos a considerar dos qubits y consideramso el siguiente estado:

$$
\psi = \frac{1}{\sqrt{2}}(\ket{01} - \ket{10}) \text{(estado de Bell, es el estado con mas entrelazammiento, depronto lo escogen por que tiene spin 0)}
$$


$q_1 \to \mathcal H_1$, $q_2 \to \mathcal H_2$, y entonces consideramos:

$$
\mathcal H = \mathcal H_1 \otimes \mathcal H_2$$

Base $\mathcal H_1$ es $\{\ket{0}, \ket{1}\} = \mathcal H_2$ , base $\mathcal H_T = \{
\ket{00}, \ket{01},\ket{10}, \ket{11}\}$

Consideremos entonces el siguiente observable: $\mathbf v\cdot \sigma$ en el qubit 1 actua como 
$$
\mathbf v\cdot \sigma \otimes \mathbb I$$

y sobre el qubit 2 actua como $\mathbb I \otimes \mathbf v\cdot \sigma$

Luego 

$$
\mathbf v \cdot \otimes I \ket{\psi \phi}  =\mathbf v \cdot \otimes I \ket{\psi \phi}  = \mathbf v\cdot \vec \sigma \ket{\psi} \otimes \ket{\phi}$$

y ademas 

$$\mathbf v \cdot \sigma  \ket{a} = \ket{a}$$

$$\mathbf v \cdot \sigma  \ket{b} = -1\ket{b}$$

Por lo que si expresamos 

$$
\ket{0} = \alpha\ket{a} + \beta \ket{b}
$$

$$
\ket{1} = \gamma \ket{a} + \delta \ket{b}$$

con $|\alpha|^2 + |\beta|^2=1$ y ademas $|\gamma|^2 + |\delta|^2$ 

**Transformacion unitaria **

$$
\begin{pmatrix}
\alpha & \beta \\
\gamma & \delta
\end{pmatrix}
$$

Asi


$$
\begin{align*}
\bra{\psi} &= \frac{1}{\sqrt{2}}(\alpha \ket{a} + \beta \ket{b})\otimes(\gamma \ket{a} + \delta \ket{b}) -  
 \frac{1}{\sqrt{2}}(\gamma \ket{b} + \delta \ket{a}) \otimes(\alpha \ket{b} + \beta \ket{a})\\
 &= \frac{1}{\sqrt{2}}(\alpha \delta - \beta \gamma) (
    \ket{ab} - \ket{ba}) 

\end{align*}
$$

Este estado sigue estando completamente entrelazado.

**Alice** Realice mediciones proyectivas con el operador $\mathbb P_{+1} = \ket{a}\bra{a}$ y $P_{-1} = \ket{b} \bra{b}$  asi:

$$
p(+1) = \bra{\psi} \mathbb P_{+1}^2|\ket{\psi} = \braket{\psi|a} \braket{a|\psi} =\frac12
$$
Del mismo modo

$$
p(-1) = \frac{1}2
$$


Supongamos que Alice midio y obtuvo $+1$ luego:

$$
\frac{\mathbb P_{+1} \ket{\psi}}{\sqrt{p(+1)}} = \ket{ab}
$$

y tambien 


$$
\frac{\mathbb P_{-1} \ket{\psi}}{\sqrt{p(+1)}} = \ket{ba}
$$


Alice sabe con absoluta certeza que Bob tendra lo opuesto a lo que mide si miden en misma base.

Einstein dice que la mecanica cuantica es imcopleta pues una teoria debe cumplir el realismo, es decir que se debe poder predecir con anterioridad los que se va a medir , pues si no es asi, hasta que alice no mide bob puede obterner ambos resultados y si alice mide bob solo puede tener un resulado, luego se daria segun "transmitira informacion mas rapido que la luz" lo cual es falso.

Como puedo determinar si la naturaleza tiene ese elemento de realismo?

Definimos C:camiseta clara y $\bar C$ camiseta oscura$, $P$ patalon claro, y $\bar P$ pantalon oscuro, y $B$ es de bogota y $\bar B$ no es de bogota.



$$
N(C,\bar P) + N(P, \bar B) \geq N(C,B)$$
$$
2 + 1\geq 3$$




$$
N(C,\bar P) = N(C,\bar P ,B)  + N(C,\bar P ,\bar B) 
$$



$$
N(P,\bar B) = N(C, P ,B)  + N(\bar C, P ,\bar B) 
$$

$$
N(C,\bar B) = N(C, P ,\bar B)  + N( C, \bar P ,\bar B) 
$$


Asi sumando:


$$
N(C,\bar P, B) + N(\bar C, P, \bar B) + N(C, \bar P , \bar B) = 
N(C,\bar P, B) + N(\bar C, P, \bar B) \geq 0$$







