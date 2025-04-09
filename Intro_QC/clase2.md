Ejemplo continuacion.


$$ Tr(A) = Tr(\ket{\psi}\bra{\psi}) = \sum_i \braket{e_i|\psi}\braket{\psi|e_i} \dots
$$

$$
\ket{\psi} = \alpha \ket{0} + \beta \ket{1}
$$

entonces:

$$
\ket{\psi}\bra{\psi} = \begin{pmatrix}
\alpha \alpha^* & \alpha \beta^* \\
\beta \alpha^* & \beta \beta^*
\end{pmatrix}
$$

Luego 

$$
\ket{\psi}\bra{\psi} = \alpha \alpha^* P_1 + \alpha \beta^* P_2 + \beta \alpha^* P_3 + \beta \beta^* P_4
$$ 

y

$$
Tr(\ket{\psi}\bra{\psi}) = \alpha \alpha^*  + \beta \beta^* $$


calculando $\braket{e_i|\psi} \braket{\psi|e_i}$: con $e_1 = \ket{0}$ y $e_2 = \ket{1}$, realizando el producto:


$$
i=0: \braket{e_1|\psi} \braket{\psi|e_1} = \bra{0}(\alpha\alpha^* \ket{0} \bra{0}+ \alpha \beta^* \ket{0} \bra{1} + \beta \alpha^* \ket{1} \bra{0} + \beta \beta^* \ket{1} \bra{1})
$$

observe que $\braket{e_i|e_j}= \delta_{ij}$, Aasi

$$
i=0: \braket{e_0|\psi} \braket{\psi|e_i} = \alpha \alpha^* $$

y tambien para $i=1$:

$$
\braket{e_1|\psi} \braket{\psi|e_1} = \beta \beta^* $$

$Tr(\ket{\psi}\bra{\psi}) =\sum_i^{1} \braket{e_i|\psi} \braket{\psi|e_i}$


Nota:

$$
\begin{align*}
\sum_{j=1}^m \mathbb P(j) &= \sum_{j=1}^m tr(P_j \ket{\psi}\bra{\psi}) = Tr((\sum_{j=1}^m P_j )\ket{\psi}\bra{\psi}) \\
\end{align*}
$$

Demo: ejercicio

Tambien en vez ONB $\ket{0},\dots,\ket{N-1}$, se puede considerar otras ONBm, $\ket{\psi_0},\dots,\ket{\psi_{N-1}}$ y la proyeccion (se mantiene via el operador de densidad) $P_j = \ket{\psi_j}\bra{\psi_j}$.

Ejemplo( Una medicion que se distribuye sobre j):

Consideremos :

$$
\begin{align*}
P_1 = \sum_{j<\frac{N}{2}} \ket{j}\bra{j} \\
P_2 = \sum_{j\geq \frac{N}{2}} \ket{j}\bra{j} \\
\end{align*}
$$

y sea el estado $\ket{\psi} = \frac{1}{\sqrt{3}}(\ket{1}) + \frac{2}{\sqrt{3}}(\ket{N})$


(i) La medicion puede colapsa al estado $\ket{1}$ con probabilidad:

$$
\begin{align*}
P(1) = ||P_1 \ket{\psi}||^2 = \braket{\psi|P_1 \ket{\psi}} =  \braket{\psi|1} \braket{1|\psi} = \braket{\psi|1} \braket{\psi|1}^* = |\braket{\psi|1}|^2 = \frac{1}{3}
\end{align*}
$$

ii) Ejercicio Ver que $P(N) = \frac{2}{3}$


Observables:

Una medida proyectiva con proyectores $P_1,\dots, P_M$ y distintas salidas asociadas $\lambda_1,\dots, \lambda_M$ con $\lambda_i \in \mathbb R$, se puede escribir como uan matrix $M$

$$
M = \sum_{i=1}^M \lambda_i P_i$$


a esta matrix se le conoce como matriz observable. El valor esperado de la salida puede calcularse directamente. 

Si medidos $\ket{\psi}$ entonces las partes de la salida $\lambda_i$ asociada a $||P_i \ket{\psi}||^2$, por lo tanto el valor esperado:

$$
\begin{align*}
\sum_{i=1}^m \lambda_i Tr(P_i \ket{\psi}\bra{\psi}) = Tr(\sum_{i=1}^m \lambda_i P_i \ket{\psi}\bra{\psi})  = Tr(M \ket{\psi}\bra{\psi}) \\
\end{align*}
$$

Nota: Ina matrix M es hermitiana si $M = M^*$ (transpuesta conjugada). La matriz observable M es hermitiana,  y en efecto tendra su propia descomposicion espectral.


Ejemplo (Observable de 2-dimensiones):


Matices de Pauli:

$$
\begin{align*}
X = \begin{pmatrix}
0 & 1 \\ 1 & 0 \end{pmatrix} \\
Y = \begin{pmatrix}
0 & -i \\ i & 0 \end{pmatrix} \\
Z = \begin{pmatrix}
1 & 0 \\ 0 & -1 \end{pmatrix} \\
I = \begin{pmatrix}
1 & 0 \\ 0 & 1 \end{pmatrix} \\
\end{align*}
$$

Estas matrices son unitarias (e.d su inversa es igual a su transpuesta conjugada).

Para la matrices de pauli, $X,Y,Z$ los valores propios son $\pm 1$.


-----

Sean $\ket{\psi} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11})$ estado de Bell,.


Vamos a medir al operador de Pauli en ambos qubits:

Si consideramos 

$$
\begin{align*}
Z\ket{0} =  \begin{pmatrix}
1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \ket{0} \\
Z\ket{1} =  \begin{pmatrix}
0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ -1 \end{pmatrix} = -\ket{1} \\
\end{align*}
$$

Este es un ejemplo de una medicion separada donde cada qubit se mide de manera independiente.

Por otro lado, la medicion conjunta considera el producto tensorial:

$$
\begin{align*}
Z \otimes Z&= \begin{pmatrix}
1 & 0 \\ 0 & -1 \end{pmatrix} \otimes \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \\
&= \begin{pmatrix}
z\cdot 1 & z\cdot 0 \\ z \cdot 1 & z\cdot 0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 \\
\end{pmatrix} \\
\end{align*}
$$

Se puede observar que:

$$
\begin{align*}
Z \otimes Z \ket{\psi} &= +1 \ket{\psi} \\
\end{align*}
$$

Verificar.

Nota si se mide directamente de forma independiente el estado se altera, pero si se mide de forma conjunta el estado no se altera.


## Modelo generalizado de medición en mecanica cuantica:

### Positive- operator -value - measure (POVM):


Este metodo esta especificado por $m$ matrices semidefinidas positivas p.s.d (Hermitianas, simetrica, $\lambda>0$). 

La medicion del estado $\ket{\psi} \to P(i) = tr(E_i \ket{\psi}\bra{\psi})$.

**Observacion:** Una medida proyectiva $P_i$ es un caso especial de POVM donde los $E_i$ son proyectores.

Ejemplo: Sea $\ket{\psi} = \alpha \ket{0} + \beta \ket{1}$,  queremos hacer la medicion proyectiva sobre las bases computacionales :

$$
\begin{align*}
P_0 &= \ket{0}\bra{0} \\
P_1 &= \ket{1}\bra{1} \\
\end{align*}
$$

Facilmente se observa que $P_0 + P_1 = I$ y la probabilidad de colapso es:


$$
\begin{align*}
P(0) &= ||P_0 \ket{\psi}||^2 = |\alpha|^2 \\
P(1) &= ||P_1 \ket{\psi}||^2 = |\beta|^2 \\
\end{align*}
$$

Considere ahora, los siguientes operadores:

$$
\begin{align*}
E_0 &= \frac{2}{3} \ket{0}\bra{0} 
; \quad E_1 = \frac{2}{3} \ket{1}\bra{1} ; \quad E_2 = \frac{1}{3} I \\
\end{align*}
$$

Por una lado, es facil ver que $E_0 + E_1 + E_2 = I$(Ejercicio) y las probabilidades:

$$
\begin{align*}
P(0) = \braket{\psi|E_0|\psi} = \frac{2}{3} |\alpha|^2 \\
P(1) = \braket{\psi|E_1|\psi} = \frac{2}{3} |\beta|^2 \\    
P(2) = \braket{\psi|E_2|\psi} = \frac{1}{3} \braket{\psi||\psi} = \frac{1}{3} 
\end{align*}
$$

**Observacion:** En la medicion proyectiva el estado colapsa (ex: $\ket{0}$, $\ket{1}$) con probabilidad $|\alpha|^2$ y $|\beta|^2$. 
