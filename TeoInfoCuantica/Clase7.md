$\rho$-qubit

$\{P_0,P_1, \sigma_+, \sigma_-\}$; $\{\sigma_0,\sigma_x, \sigma_y, \sigma_z\}$
Matrices de puaili.

Operadpr de Puali - $\mathbf n$

$\mathbf n \cdot \vec \sigma$; $\vec \sigma=(\sigma_x, \sigma_y,\sigma_z)=\sum_{\alpha} n_\alpha \sigma_\alpha$

$\rho^2 = \frac 14\left(\mathbb 1 + 2\mathbf n \cdot \vec \sigma + (\mathbf n \cdot \vec \sigma)(\mathbf n \cdot \vec \sigma)\right)$


## Oservables y medidas

Para cada observable le corresponde un operador hermitico en el espacio de estados del sistema.

Un observable $O = O^{\dagger}$ con 

$$
\begin{align*}
O= O_{00} P_0 + O_{11} P_1 + O_{01} \sigma_- + O_{10} \sigma_{+} &= \sum_{\alpha} O_\alpha \sigma_\alpha \\&=\begin{pmatrix}
O_{00} & O_{01}\\
O_{10} & O_{11}
\end{pmatrix}\\
\end{align*}
$$

donde
$$
\begin{align*}
O_\alpha = \frac 12 Tr (O \sigma_\alpha) \in\mathbb R
\end{align*}
$$

$$
O = \sum_{m} O_m P_m 
$$


$P_m$ proyecta sobre el subespacio de $O_m$, $O_m$ valores propios.

$$
\begin{align*}
P_n P_m = \delta_{mn} P_n \qquad \sum_{P_m} =1
\end{align*}
$$

Si todos los operadores proeyctivos sin degeneramiento se habla de medir en la base

## Postulado de la emdicion 

dados $\rho$ y $O$:

i) Posibles resultados son los elementos del espectro del $\{O_m\}$ con probabilidad $\rho(O_m) = \braket{\psi|P_m|\psi }$ con $\rho(O_m) = tr(\rho P_m)$



ii) Resultado $O_k$  con probabildad:

$$
\begin{align*}
\rho_k = \frac{P_k \rho P_k}{p (O_k)} \quad \text{$p(O_k)$ la probabilidad de obtener $O_k$} 
\end{align*}
$$

con $\rho = \ket{\psi}\bra{\psi}$  y $\frac{P_k \ket{\psi}}{\sqrt{\braket{\psi|P_k|\psi}}}$


**Nota** El tamaño de la norma nos habla de la pureza.

**Nota** Los qubits se prepeparan con probabilidad dada por medio de campos magneticos a traves de hamiltonianos como por ejemplo $H = \omega \sigma_x$


### Valor esperado 

$$
\begin{align*}
\braket{O} &= \sum_{m} O_m \rho(O_m)\\
&= \sum_{m} O_m p(O_m)\\
&= \lim_{N\to\infty} \frac{1}{N} \sum_{n=1}^{N} O_{m(i)}
\end{align*}
$$


Consideremos:

$$
\begin{align*}
\rho = \frac 14 \ket{0} \bra{0} + \frac 34 \ket{1} \bra{1} 
\end{align*}
$$

y 

$$
O = \frac 1{\sqrt{2}} (\sigma_x + \sigma_z)
$$

$$
\begin{align*}
\braket{O} = tr(\rho O) 
\end{align*}
$$

Primero calculemos:

$$
\begin{align*}
\rho O &= \frac 14 \ket{0} \bra{0} O + \frac 34 \ket{1} \bra{1} O\\
&= \frac 14 \ket{0} \bra{0} \frac 1{\sqrt{2}} (\sigma_x + \sigma_z ) + \frac 34 \ket{1} \bra{1} \frac 1{\sqrt{2}} (\sigma_x + \sigma_z )\\
&= \frac 14 \frac 1{\sqrt{2}} \left( \ket{0} \bra{0} \sigma_x + \ket{0} \bra{0} \sigma_z \right) + \frac 34 \frac 1{\sqrt{2}} \left( \ket{1} \bra{1} \sigma_x + \ket{1} \bra{1} \sigma_z \right)\\
&= \frac 14 \frac 1{\sqrt{2}} \left( \ket{0} \bra{0} \begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix} + \ket{0} \bra{0} \begin{pmatrix}
0 & -i\\
-i & 0
\end{pmatrix}\right) + \frac 34 \frac 1{\sqrt{2}} \left( \ket{1} \bra{1} \begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix} + \ket{1} \bra{1} \begin{pmatrix}
0 & -i\\
-i & 0
\end{pmatrix}\right)\\
\end{align*}
$$

Notemos que:


$$
\begin{align*}
\frac 1{\sqrt 2} tr(\rho O) &= \frac{1}{\sqrt{2}} tr(\rho \sigma_x) + \frac{1}{\sqrt{2}} tr(\rho \sigma_z)\\&= \frac 14 \braket{0|\sigma_x|0} + \frac 34 \braket{1|\sigma_x|1} + \frac 14 \braket{0|\sigma_z|0} + \frac 34 \braket{1|\sigma_z|1}\\
&= \frac 1{\sqrt 2}\left(\frac 14 \cdot 0 + \frac 34 \cdot 0 + \frac 14 \cdot 1 - \frac 34 \cdot 1\right)\\
&= -\frac 1{2\sqrt 2}
\end{align*}
$$


ahora la variancia:

$$
\begin{align*}
Var_p( O) = \braket{(O - \braket{O})^2} &= \braket{O^2} - \braket{O}^2\\
\end{align*}
$$

$$
\begin{align*}
\psi =\alpha \ket{0} + \beta \ket 1
\end{align*}
$$


dado 

$$
\begin{align*}
\rho &= \frac 12 \left(\mathbb 1 + \braket{\sigma_x } \sigma_x + \braket{\sigma_y } \sigma_y + \braket{\sigma_y} \sigma_y + \braket{\sigma_z} \sigma_z
 \right) \\
 &= \begin{pmatrix}
    \rho_{00} & \rho_{01}\\
    \rho_{10} & \rho_{11}
  \end{pmatrix}
\end{align*}
$$

Asi:

$$
\begin{align*}
\rho_\psi = \begin{pmatrix}
    |\alpha|^2 & \alpha^* \beta\\
    \beta \alpha & |\beta|^2
\end{pmatrix}
\end{align*}
$$

Para Qdits

$$
\begin{align*}
\rho = \sum_{mn}^{d} \rho_{mn} \ket n \bra m
\end{align*}
$$

con $\ket{n}\bra{m}$ No son observables, y

$$
\begin{align*}
 d + 2\frac{d(d-1)}{2} -1 = d^2 -1
\end{align*}
$$

el numero de parametros necesarios para determinar $\rho_{nm}$

Hacer tomografia es muy costos por que crece cuadraticamente con la dmiension del espacio.

$$
\begin{align*}
O_{mn} = O_{nm}^{H} + i O_{nm}^{A}
\end{align*}
$$

Una parte hermitica y una parte antihermitica

$$
\begin{align*}
O_{nm}^H = \frac{\ket{n}\bra{m} + \ket{m}\bra{n}}{2}
\end{align*}
$$

$$
\begin{align*}
O_{nm}^A = \frac{\ket{n}\bra{m} - \ket{m}\bra{n}}{2i}
\end{align*}
$$


## Mediciones generalizadas 


Posibles resultados $m_k$, a cada uno de estos le asociamos operadoeres de medicion ($M_k\geq 0$ esto depronto no es necesario pero no queda claro), entonces deben ser hermiticos. Los operadores de medicion deben satisfacer que:


$$
\begin{align*}
\sum_k M_k^{\dagger} M_k = 1 \qquad \text{Garantiza un resultado}
\end{align*}
$$

Esto significa que para cada posible resultado de la medicion yo asocio un operador de medicion. Ademas:

$$
\begin{align*}
tr(M_k\rho M_k^\dagger) = tr(M^\dagger M \rho)
\end{align*}
$$


Para $m_l$ como resultado:


$$
\begin{align*}
\frac{M \rho M^\dagger}{tr(M\rho M^\dagger)}
\end{align*}
$$

Estos $M_k$ pueden ser proyectores, pero no necesariamente van a ser proyectores. 


**Nota:** Los qbits arrancan en cero por que es el estado mas sencillo de preparar

## Positive operator value measured.

$$
\begin{align*}
E_k = M^dagger M_k \geq 0
\end{align*}
$$
Tambien satisfacen que:

$$
\begin{align*}
\sum_k E_k = \mathbb I
\end{align*}
$$

$$
\begin{align*}
p(O_k) = tr(\rho E_k)
\end{align*}
$$

### Evolcuion

La evolucion de sistemas aislados es unitario, dado $\ket{\psi_0}$ existe un operador unitario tal que:

$$
\begin{align*}
    \ket{\psi_0} \to \ket{\psi_t}= U_t \ket{\psi_0}
\end{align*}
$$

y ademas 

$$
\begin{align*}
    \rho_o \to \rho_t = U_t \rho U_t^\dagger
\end{align*}
$$

Tenemos que:


$$
\begin{align*}
U_t = \exp (iHt)
\end{align*}
$$

$H$ es el hamiltoniano del sistema, lo cual surge de o da lugar a:


$$
\begin{align*}
i\frac{d}{dt} \ket{\psi_t} = H\ket{\psi_0}\qquad \text{Ec. schrodinger}
\end{align*}
$$

$$
\begin{align*}
    \frac{d\rho_t}{dt} = i[H,\rho_t]  \qquad \text{Von Neumann}
\end{align*}
$$

Y cuando el hamiltoniano depende del tiempo:

$$
\begin{align*}
U_t = \mathcal T\exp\left[-\int dt' H(t')\right]
\end{align*}
$$
Aqui se escribe $\mathcal T$ para representar lo que esta abajo.


$\Delta t = \frac t{N}$

$$
\begin{align*}
U_t = \lim_{N\to \inf} e^{-i H(t_N) \Delta t}e^{-i H(t_{N-1}) \Delta t}\dots e^{-i H(t_{0}) \Delta t}
\end{align*}
$$

en las integrales de camino los caminos que mas pesan son los clasicos es decir los que respetan la ecuaciones de euler-lagrange.