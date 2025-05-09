Filbo de 8am hasta la 1 pm

Las transformaciones en el espacio de fase las realizan transformacioens unitarias. Si y el operador es unitario y el sistema es aislado, podemos construir un operador unitario que evolucione el sistema en el tiempo. El hamiltoniano puede no commutar con sigo mismo en tiempos diferentes. Throterizacion.  Basta tener mas de un grado de libertad y superposicion para tener entrelazamiento. 


## Qbit

Todas las transformaciones unitarias en esfera de bloch se corresponde con una rotacion. El hamiltoniano sismpre se puede escribir como:

$$
H = a\mathbb I + \vec h \cdot \vec \sigma = a\mathbb I + \omega \sigma_{\vec h}
$$

Asi el operador de evolucion es:

$$
\begin{align*}
    U_t = e^{-iHt} = e^{-ia\mathbb I t}e^{-i\vec h \cdot \vec \sigma t} = e^{-ia\mathbb I t}e^{-i\omega \sigma_{\vec h}t}
\end{align*}
$$

Podemos suprimir la fase $e^{-ia\mathbb I t}$, ya que no afecta a la evolucion del sistema. Entonces tenemos:

$$
\begin{align*}
    U_t = e^{-i\omega \sigma_{\vec h}t} = \cos(\omega t) \mathbb I - i \sin(\omega t) \sigma_{\vec h}
\end{align*}
$$

Representa una rotacion alrededor del eje $\vec h$ un angulo $\omega t$. Las trasnformaciones unitarias conservan la pureza de los sistemas. Asi definimos:

$$
\begin{align*}
    \rho(t) &= \frac 12 \left(\mathbb I + \vec n \cdot \vec \sigma\right) \\
    &= U_t p(0) U_t^\dagger
\end{align*}
$$

o equivalente:

$$
\begin{align*}
\dot \rho = -i [H, p(t) ] = \frac 1{2}\frac{d\vec n(t)}{dt}\cdot \vec \sigma
\end{align*}
$$

con $|\vec n| \leq 1$, $\vec \sigma = (\sigma_x, \sigma_y, \sigma_z)$ con 

$$
\begin{align*}
H\rho(t)&= (\omega\vec h \cdot \vec \sigma) \frac 12 (\mathbb I + \vec n(t) \cdot \vec\sigma)\\
&= \frac \omega 2 \left(\vec h  \cdot \vec \sigma + ((\vec h  \cdot \vec \sigma)(\vec n(t) \cdot \vec \sigma(t) ))\right)\\
\rho(t) &= \frac \omega 2 \left(\vec h  \cdot \vec \sigma +  (\vec n(t) \cdot \vec \sigma(t) (\vec h  \cdot \vec \sigma))\right) 
\end{align*}
$$

Asi:


$$
\begin{align*}
i[H,\rho(t)]&= i\frac \omega 2 \sum_{ij}h_i n_j(\sigma_i\sigma_j - \sigma_j \sigma_i)\\
&= -i\frac \omega 2 \sum_{ij} (h_i n_j 2x\epsilon_{ijk}) \sigma_k
\end{align*}
$$

Asi 

$$
\begin{align*}
-i[H,\rho(t)] = \omega (\vec h \times \vec n) \cdot \vec \sigma 
\end{align*}
$$

y 

$$
\begin{align*}
\frac{d n(t)}{dt} = 2\omega (\vec h \times \vec n)
\end{align*}
$$


Es decir el estado mas general de un qubit en la esfera de bloch es precesando. Un qubit se suele representar como 

$$
\begin{align*}
H = \frac{\Delta}2 \sigma_z + \frac \Omega{2} \cos (\omega t) \sigma_x
\end{align*}
$$

o tambien 


$$
\begin{align*}
H &= \frac{\Delta}2 \sigma_z + \frac \Omega{2} \left(\sigma_+ e^{i\phi} + \sigma_- e^{-i\phi}\right) \\
&= -\frac \Delta 2 \sigma_z  +\frac \Omega 2\left(
    \cos \phi \sigma_x - \sin \phi \sigma_y
\right)\\
&= \omega \sigma_{\vec h}
\end{align*}
$$


El menos es para hacer el cero el estado de minima energia. Aqui:

$$
\begin{align*}
\omega = \frac 12 \sqrt { \omega^2 +\Delta^2} 
\end{align*}
$$

y 

$$
\begin{align*}
\vec h = \frac 1{\sqrt{\Omega^2 \Delta^2}} \left(
    \Omega \cos\phi, \Omega \sin \phi, -\Delta
\right)
\end{align*}
$$

y 

$$
\begin{align*}
\sigma_{\vec h} = \frac 1{\sqrt{\Omega^2 + \Delta^2}} 
    \begin{pmatrix}
        -\Delta & \Omega e^{i \phi}\\
        \Omega e^{i\phi} & \Delta
    \end{pmatrix}
\end{align*}
$$


$$
U_t=\cos \omega t \mathbb I -\sin (\omega t)\vec \sigma_{\vec h}\\
$$

Para $\Delta =0$

$$
\begin{align}
U_t =\begin{pmatrix}
\cos \frac{\Omega }2t & -i \sin \frac{\Omega}2t \\
-i\sin\frac{\Omega}2 t & \cos \frac{\Omega}2 t
\end{pmatrix}
\end{align}
$$

Ahora si 

$$
\begin{align*}
\rho_0 = \ket 1\bra1
\end{align*}
$$
con $\ket{\psi_0} = \ket 1$

asi

$$
\begin{align*}
\rho_t(1) = |\braket{1|U_t|\psi_0}| = |\braket{1|U_t|1}| = \cos^2\omega tef
\end{align*}
$$

![alt text](<WhatsApp Image 2025-05-05 at 15.02.43_8c9b04c7.jpg>)


Operadores de saldo o de los canales cuentan los efectos del entorno en procesos markovianos

## Canal cuantico 

Un canal cuantico $\epsilon:\mathcal L(H) \to \mathcal L(H)$ tal que $p\to p' =\epsilon(p)$ con 

$$
\begin{align*}
\epsilon (p) = \sum_{i} p_i U_i p U_i^\dagger
\end{align*}
$$

si $p_1$ esta asociado a $U_1$ y $p_2$ esta asociado a $U_2$ entonces 

$$
\begin{align*}
\epsilon(p) = p_1 U_1 p U_1^{\dagger} + p_2 U_2 pU_2^\dagger
\end{align*}
$$

Representacion de Krauss:


$$
\begin{align*}
\epsilon (p) = \sum_i K_i p K_i
\end{align*}
$$

$\{K_i\}$ representacion de Krauss: $\sum_i K_i^\dagger K_i = \mathbb I$ todo canal cuantico tiene una de descomposicion de Krauss que no es unica, por ejemploL


$$
\begin{align*}
K_i = \sqrt p_i  U_i
\end{align*}
$$

Asi

$$
\begin{align*}
\sum_i K_i^\dagger K_i = \sum_i p_i U_i^\dagger U_i = \sum_{p_i} p_i \mathbb I = \mathbb I
\end{align*}
$$

Estos canales representas fuentes de ruido provimientes del entorno, como por ejemplo,Para un qubit
## El canal de depolarizacion:

$(1-p)$ no pasa nada
$p$ tomamos de forma aleatoria la direccion.

entonces 

$$
\begin{align*}
\epsilon(p) = (1-p) p + \frac p3 \sum_{\alpha} \sigma_\alpha p \sigma_\alpha
\end{align*}
$$

Asi sea 

$$
\begin{align*}
p &= \frac 12 \left(\mathbb I + \vec n \cdot \vec \sigma \right)\\
p' &= \epsilon (p) = \frac 12 \left(\mathbb I + \left(1 - \frac 43 p \right)\vec n\cdot \vec \sigma\right)
\end{align*}
$$


$$
\begin{align*}
    p= \frac 43 
\end{align*}
$$


El estado al pasar por el canal deja de ser puro. Asi podemos definir 

$$
\begin{align*}
K_0 &= \sqrt{1-p} \mathbb I\\
K_\alpha = \sqrt{\frac{p}3} \sigma_\alpha
\end{align*}
$$

$$
\begin{align*}
K_0^\dagger K_0 + \sum_{\alpha} K_\alpha^\dagger K_\alpha = (1-p)\mathbb I +\frac p3 \sum_\alpha \mathbb I = \mathbb I
\end{align*}
$$

## bit flip

$$
\begin{align*}
\epsilon(p) = (1-p)p + p\sigma_x p \sigma_x
\end{align*}
$$


## Canal de desfasamiento. (dephasing)

En los sistemas cuanticos la energia se mantiene constante pero pierde coherencia (no tiene analogo clasico )


$$
\begin{align*}
\epsilon(p) = (1-p) p + p \sigma_z p \sigma_z
\end{align*}
$$

Asi los operadores de Krauss son 

$$
\begin{align*}
K_0 = \sqrt{1-p} \mathbb I \\
K_1 =\sqrt p \sigma_z
\end{align*}
$$

Asi 
$$
\begin{align*}
p' = \epsilon(p) = \begin{pmatrix}
\rho_{00} & (1-2p) \rho_{01}\\
(1-2p) \rho_{01}& \rho_{11}\end{pmatrix}
\end{align*}
$$

Asi en la diagonal son las poblaciones y los otros son la coherencia, para $p=\frac{1}2$ la decoherencia desaparece.

$$
\begin{align*}
\braket{0|\epsilon(p)|1} = (1-p)\rho_{01} - p\rho_{01} = (1-2p) \rho_{01}
\end{align*}
$$


## Ecuacion maestra (esta relacionada con un semi grupo.)

Desde la ecuacion de Louvielle:


$$
\begin{align*}
\frac{dp}{dt} = -i[H,p] 
\end{align*}
$$

Le sumamos el termino $+ \sum_k \mathcal D(l_k) p$ es un termino de dispacion, donde $L_k$ es un opeardo de salto. Que satisfacen:

con

$$
\alpha p = -i[H,p] + + \sum_k \mathcal D(l_k) p$$

Es un invariante conocido como el lindbalndiano.


$$
\begin{align*}
\mathcal D(L_k) \rho &= L_k \rho L_k^\dagger - \frac 12 \{L_k^\dagger L_k,\rho\}\\
&= L_k \rho L_k^\dagger - \frac 12  L_k^\dagger L_k p - \frac 12 \rho L_k^\dagger L_k 
\end{align*}
$$

por ejemplo 

$$
L_z = \sqrt{\frac \gamma z} \sigma_z

