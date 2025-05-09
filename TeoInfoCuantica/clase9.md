
Dado:

$$
\begin{align*}
\frac{d\rho}{dt} &= \Gamma\left(\sigma \rho \sigma_+ -\frac 12\{
    \sigma_+ \sigma_-,\rho
\} \right)
\end{align*}
$$


donde:

$$
\begin{align*}
    \sigma_+ &= \ket{1}\bra{0}\\
    \sigma_- &= \ket{0}\bra{1}
\end{align*}
$$

Este modelo funciona en banios de bosones. En un banio de bosones cual es la temperatura para que la probabilidad de decaimiento se igual a la probabilidad de aboserver un foton, es la temperatura infinita. En el universo primigenio podria existir esa temperautra infinita y que eso pueda conyevar a la asimetria materia antimateria o a otras cosas 

$\Gamma$ es el operador de desexitacion,

$$
\begin{align*}
L_- = \sqrt{P} \sigma_- 
\end{align*}
$$


Existe en un tiempo que es aleatorio.


----- 


Considere:


$$
\begin{align*}
\rho = \frac 12 \left(
    \mathbb 1+ \vec n(t) \vec n 
\right)
\end{align*}
$$



Como es una matriz el metica la ecuacion del inicion son realmente dos ecuaciones independientes.

Asi 

$$
\begin{align*}
\dot \rho &= \frac 12 \frac{d n}{dt} \cdot \vec \sigma\\
&= \frac{\Gamma}{2}(\ket 0\bra 0 - \ket 1\bra 1) + \frac{\Gamma}2 \left(
    -\frac {n_x} 2 \sigma_x - \frac{n_y}2 \sigma_y- n_z \sigma_Z
\right)
\end{align*}
$$

donde $\ket 0 \bra 0 - \ket 1 \bra 1$,

$$
\begin{align*}
\dot n_x &= -\frac {\Gamma}2 n_x\\
\dot n_y &= -\frac{\Gamma}2 n_y\\
\dot n_z &= -\frac{\Gamma}2\left(n_z -1\right) 
\end{align*}
$$

Integrando:

$$
\begin{align*}
n_x(t) = n_x (0)e^{\frac {-\Gamma}2t}\\
n_y(t) = n_y (0)e^{\frac {-\Gamma}2t}\\
n_z(t) = (n_z(0)-1)(0)e^{{-\Gamma}}+1
\end{align*}
$$

El canal de decaimiento contre la esfera en un punto.

Desde la ecuacion del inicio del archivo

$$
\begin{align*}
\frac{d\rho_{11}}{{dt}} =  -\Gamma \rho_{11}\\
\frac{d\rho_{01}}{dt} = -\frac 12\Gamma \rho_{01}\\
\end{align*}
$$

y por tanto:

$$
\begin{align*}
\rho(t)=\begin{pmatrix}
    1- \rho_{11}(0)e^{\Gamma t} & \rho_{01} (0) e^{-\frac \Gamma2t} \\
    \rho_{10}(0) e^{-\frac \Gamma 2t} & \rho_{11}e^{ -\Gamma t}
\end{pmatrix}
\end{align*}
$$

El cana de desfazamiento contra esfera.


### Sistemas compuesto

Son sistemas que se compoenen de dos partes que se pueden entender como un sistemas cada sistema.


El espacio de hilbert 3d es:

$$
\begin{align*}
H_x \otimes H_y\otimes H_z \otimes \mathcal H_2
\end{align*}
$$

dodne $H_x$ es el espacio de hilbert del momento angular. con $\mathcal H_2$

es el espacio de hilbert para el spin,


Dados dos sistemas $A$ y $B$ al sistema $A$ le asociamos el espacio de Hilbert $\mathcal H_A$ con base $\{\ket{a_n}\}$, al B le asociamos $\mathcal H_B$ con base $\{\ket{b_n}\}$. Y al sistema $AB$ le asociamos $\mathcal H_{AB}$ le asociamos la base $\{\ket{a_n} \otimes \ket{a_n b_n}\}$, luego:


$$
\ket{\psi} = \sum_{mn} \psi_{mn} \ket{a_n,b_m}
$$

con 
$$
\begin{align*}
\sum_{mn} |\psi_{mn}|^2 = 1
\end{align*}
$$

Normalizacion 


Para un sistema de dos niveles 

$$
\begin{align*}
\ket{\psi_A} = \alpha_A \ket{0} + \beta_A \ket1\\
\end{align*}
$$



$$
\begin{align*}
\ket{\psi_B} = \alpha_B \ket{0} + \beta_B \ket1\\
\end{align*}
$$


Asi el producto externo ya sabemos cual es.

Si definimos:

$$
\begin{align*}
\ket{\phi} = \sum_{nm} \phi_{nm} \ket{a_nb_m}
\end{align*}
$$

Por lo que:


$$
\begin{align*}
\braket{\psi|\phi} = \sum_{nm} \psi_{nm}^*\phi_{nm}
\end{align*}
$$

Producto interno. 

Forma de operar y propiedades del prudcuto tensorial. 

$$
O_A\otimes O_m\ket{a_nb_n} = O_A\ket{a_n}\otimes O_B \ket{b_n}
$$


Y en la descomposicion de operadores

$$
\begin{align*}
O_A \otimes O_B \to O_{nm,n'm'}
\end{align*}
$$

donde $n$y $n'$ asociado a $A$ y $m$,$m'$ asociados a $B$.

Y tambien 

$$
(trO)_{mm'}= \sum_{nm} O_{nm,nm}
$$
La traza parcial 
$$
(tr_A O)_{mm'} = \sum_{n} O_{nm,nm'}
$$

$$
tr_A O = \sum_{n} \braket{n|O|n}
$$

$$
tr_B O = \sum_{m} \braket{m|O|m}
$$