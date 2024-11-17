## Single Side Band(SSB)
También llamada banda lateral única, recordemos que para la modulación AM teníamos para ![[Pasted image 20241116075020.png]]
un Double Side Band(DSB) tal que:![[Pasted image 20241116074821.png]]
teníamos dos bandas laterales, de tipo USB (Upper Side Band) y LSB(Lower Side Band).

Para este caso tendremos una sola, quedando:![[Pasted image 20241117161332.png]]
![[Pasted image 20241117161447.png]]

Durante el análisis de este caso es más sencillo partir de su espectro y luego pasar al dominio del tiempo. Se puede ver que a partir de $X(f) = X_+(f) + X_-(f)$ donde $X_+(f) = X(f)\cdot U(t)$ y $X_-(f) = X(f)\cdot U(-f)$  ![[Pasted image 20241117163214.png]]

como $|X_-(f)|$ y $|X_+(f)|$ no son funciones pares, $x_-(t)$ y $x_+(t)$ son funciones complejas.

Para que la fase de $X(f)$ sea impar $X_-(f)$ y $X_+(f)$ deben ser complejas conjugadas $X_-(f) = x_+^*(f)$ y por lo tanto $x_-(t) = x_+^*(t)$ tal que:
$$\Bigg\{\begin{array}{c} x_+(t) = \frac{1}{2}(x(t) + j\hat{x}(t)) \\ x_-(t) = \frac{1}{2}(x(t) - j\hat{x}(t))\end{array}$$ donde $\hat{x}(t)$ es la transformada de Hilbert de $x(t)$. ^ede2bc

Si $X_+(f) = X(f)\cdot U(f)$ y $U(f)$ lo escribimos como $U(f) = \frac{1 + sign(f)}{2} \Rightarrow X_+(f) = X(f)\cdot \frac{1 + sign(f)}{2}$ y de allí, obtenemos que:
$$X_+(f) = \frac{1}{2} X(f) + \frac{1}{2}X(f)sign(f)$$
Luego comparando $x_+(t) = \frac{1}{2}x(t) + j\hat{x}(t)$ con $X_+(f) = \frac{1}{2}X(F) + \frac{1}{2}X(f)sign(f)$ rendremos:
$$X_+(f) = \frac{1}{2}X(f) + \frac{j}{2} X_h(f) \Rightarrow X_h(f) = X(f)\Big[-jsign(f)\Big]$$
donde $X_h(f)$ es la transformada de Fourier de la transformada de Hilbert de $x(t)$, se puede decir entonces:
$$X_h(f) = X(f)\cdot H_Q(f)$$
donde $H_Q(f)$ se conoce como **filtro en cuadratura** o **transformador de Hilbert** , definido como:
$$H_Q(f) = -jsign(f) = e^{-j\frac{\pi}{2}}sign(f)$$
![[Pasted image 20241117165427.png]]

#### Transformada de Hilbert de un coseno:
$$x(t) = A\cos(2\pi f_0 t)$$
$$X_h(f) = \frac{A}{2} \Big[\delta(f - f_0) + \delta(f + f_0)\Big] \Rightarrow \hat{x}(t) = A\sin(2\pi f_0 t)$$
Entonces, si queremos obtener una señal SSB-USB, siendo el mensaje $x(t)$:
$$S_{USB}(f) = \frac{A_c}{2}X_+(f - f_c) + \frac{A_c}{2}X_-(f + f_c)$$
viéndolo en el tiempo $\mathcal{F}^{-1}[S_{USB}(f)] = S_{USB}(t)$, es decir:
$$\begin{array}{c}S_{USB}(t) = \frac{A_c}{2}\Big(x_+(t)e^{j2\pi f_c t} + x_-(t)e^{-j2\pi f_c t}\Big) \\= \frac{A_c}{2} \Big(x_+(t)\cos(2\pi f_c t) + j x_+\sin(2\pi f_c t) + x_-(t)\cos(2\pi f_c t) - j x_-(t)\sin(2\pi f_c t)\Big)\\ = \frac{A_c}{2}\Big[\big[x_+(t) + x_-(t)\big]\cos(2\pi f_c t) + j\big[x_+(t) - x_-(t)\big] \sin(2\pi f_c t) \Big] \end{array}$$ Dado a las   [[4-Modulación SSB#^ede2bc]] dos ecuaciones planteadas en la referencia, tendremos que de $S_{USB}$ al final $x_+(t) - x_-(t) = j\hat{x}(t)$ y $x_+(t) + x_-(t) = x(t)$ por lo que se puede obtener:
$$S_{USB}(t) = \frac{A_c}{2}\Big[ x(t)\cos(2\pi f_c t) - \hat{x}(t)\sin(2\pi f_c t)\Big]$$
Se puede desarrollar un análogo para LSB donde al final se obtendrá:
$$S_{LSB}(t) = \frac{A_c}{2}\Big[ x(t)\cos(2\pi f_c t) + \hat{x}(t)\sin(2\pi f_c t)\Big]$$
en general, un SSB:
$$x_{SSB}(t) = \frac{A_c}{2}\Big[ x(t)\cos(2\pi f_c t) \mp \hat{x}(t)\sin(2\pi f_c t)\Big]$$