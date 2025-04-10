## CHSH

Charles prepara un estado $\ket{\psi}$ de dos qubits, y uno lo envia a Alice y el otro a Bob. 


### Alice 

Realiza observaciones en los observables $R = \pm 1$ y $Q = \pm 1$. 

### Bob 

Realiza observaciones con los observables $S = \pm 1$ y $T = \pm 1$.

---- 

Cada uno selecciona la base de forma aleatoria. Todas la medida estan casualmente disconectas, asi las mediciones de Alice y B ob son locales. Asi cuando calculamos 


$$
\begin{align*}
QS + RS + RT -QT = (Q+R)S + (R-Q)T = \pm 2
\end{align*}
$$

$p(q,r,s,t)$ prob de la medida. Luego 


$$
\begin{align*}
E(QS + RS +RT - QT) &= \sum_{rqst=\pm} (ps + rs +rt-qt)p(q,r,s,t)\\
&= 2 \sum_{rqst} p(q,r,s,t)
\end{align*}
$$

Asi:

$$
\begin{align*}
E(QS) + E(RS) + E(RT) - E(QT) \leq 2
\end{align*}
$$

$$
ket{\psi} = \frac{1}{\sqrt 2} (\ket{01}-\ket{10})
$$

y consideramos los siguientes operadores convenientes:

$$
\begin{align*}
Q = Z \quad  S = \frac 1{\sqrt 2} \left(-Z_2 - X_2\right)\\
R = X \quad  T = \frac 1{\sqrt 2} \left(Z_2 - X_2\right)
\end{align*}
$$

Luego:

$$
\begin{align*}
\braket{QS}&=\braket{\psi|QS|\psi} \\
&= \frac{1}{2\sqrt 2} \left(
    \braket{0|Z_1|0} \braket{1 |Z_2 - X_2| 1} - \braket{1|Z_1|0}\braket{ 0|Z_2 - X_2|1 } -  \braket{0|Z_1|1}\braket{ 1|Z_2 - X_2|0} + \braket{1|Z_1|1}\braket{ 0|Z_2 - X_2|0 }\\
\right)\\
&= \frac{1}{2\sqrt 2} \left(1 - 0 - 0 + 1\right) = \frac{2} {\sqrt 2}\\
&= \braket{RS} = \braket{RT} = \braket{QT}
\end{align*}
$$

Asi 

$$
\begin{align*}
\braket{QS} +\braket{RS} + \braket{RT} -\braket{QT} = 2\sqrt 2\geq 2 \quad \text{son con correlaciones}
 \end{align*}
$$

Este nos dice que tan no local es.  Correlaciones de dos variables, correlaciones en el tiempo, correlaciones de tres puntos. loguitud de correlacion si uno exita un material en un punto, a paritr de que distancia los atomos no son afectados por esta exitacion. Ademas existe un punto critico de correlacion en el que el sistema se comporta como un todo.


Dada una medicion de spin $Q = \vec q \cdot \vec \sigma$, $T = \vec E \cdot \vec \sigma$, ademas:

$$
\begin{align*}
\left(
    QS + RS + RT - QT
\right)^2 = QQ\otimes SS + QR \otimes SS + QR \otimes ST + QQ\otimes ST + .... = 4\mathbf I+[Q,R] \otimes [S,T] \leq 8 

Pues:

\end{align*}
$$

Se tiene que:

$$
\begin{align*}
Q^2 = \mathbf q^2 \mathbb I
\end{align*}
$$

Queremos maximar:

$$
\begin{align*}
\braket{[Q,R]} = ||\braket{QR- RQ}||\leq 2 ||\braket{QR}||= 2||\braket{Q}|||\cdot ||\braket R|| =2
\end{align*}
$$

Cota de Tsirelson

La norma se define como: $||Q|| = \max_{\psi} \{Q\ket{\psi}\}$

### Matrices 

Espacio  de matices $\mathbb M_{m \times n} (\mathbb C)$ y nos va interesar $\mathbb M_{n} (\mathbb C)$, ademas $(\mathbb I_n)_{ij} = \delta_{ij}$, 

Una matriz es normal si es cuadra y $[M, M^{\dagger}] = 0$, 

Veamos el siguiente proyector:

$$
\begin{align*}
\mathbb P = \frac{1}2\begin{pmatrix}1 & 1\\ 1 &1\end{pmatrix}
\end{align*}
$$

Dad la descomposicion espectral de M, para matrices normal siempre puede diagonalizarla:

$$
\begin{align*}
M = UDU^\dagger
\end{align*}
$$


Esta descomposion nos da la respuesta a varias preguntas.

### Matices semi-positiva

### MAtrix positiva


$X\geq Y$ si $X-Y \geq 0$

Los estados mezclados son matrices hermitcas y semidefinidas positivas , para una matrices semidefinidas positivas se tiene que los elementos de la diagonal son mayores que cero, y con traza 1.

En la matices de densidad las diagonales son probabilidad y las de afuera