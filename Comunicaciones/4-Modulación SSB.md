## Single Side Band(SSB)
También llamada banda lateral única, recordemos que para la modulación AM teníamos para ![[Pasted image 20241116075020.png]]
un Double Side Band(DSB) tal que:![[Pasted image 20241116074821.png]]
teníamos dos bandas laterales, de tipo USB (Upper Side Band) y LSB(Lower Side Band).

Para este caso tendremos una sola, quedando:![[Pasted image 20241117161332.png]]
![[Pasted image 20241117161447.png]]

Durante el análisis de este caso es más sencillo partir de su espectro y luego pasar al dominio del tiempo. Se puede ver que a partir de $X(f) = X_+(f) + X_-(f)$ donde $X_+(f) = X(f)\cdot U(t)$ y $X_-(f) = X(f)\cdot U(-f)$  ![[Pasted image 20241117163214.png]]

como $|X_-(f)|$ y $|X_+(f)|$ no son funciones pares, $x_-(t)$ y $x_+(t)$ son funciones complejas.

Para que la fase de $X(f)$ sea impar $X_-(f)$ y $X_+(f)$ deben ser complejas conjugadas $X_-(f) = x_+^*(f)$ y por lo tanto $x_-(t) = x_+^*(t)$ tal que:
$$\Bigg\{\begin{array}{c} x_+(t) = \frac{1}{2}(x(t) + j\hat{x}(t)) \\ x_-(t) = \frac{1}{2}(x(t) - j\hat{x}(t))\end{array}$$ donde $\hat{x}(t)$ es la transformada de Hilbert de $x(t)$.

Si $X_+(f) = X(f)\cdot U(f)$ y $U(f)$ lo escribimos como $U(f) = \frac{1 + sign(f)}{2} \Rightarrow X_+(f) = X(f)\cdot \frac{1 + sign(f)}{2}$ y de allí, obtenemos que:
$$X_+(f) = \frac{1}{2} X(f) + \frac{1}{2}X(f)sign(f)$$
