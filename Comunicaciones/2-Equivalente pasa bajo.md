## Transformada de Hilbert:
Operador lineal en forma de Transformada Integral. Se puede empleaar para calcular el contenido de frecuencia de una señal de energía o potencia.

Su análisis es:
$$
\hat{x}(t) = \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{x(\tau)}{t - \tau} d\tau = \frac{1}{\pi}\int_{-\infty}^{\infty}  \frac{x(t - \tau)}{\tau} d\tau
$$
Y en síntesis:
$$
x(t) = \frac{1}{\pi}\int_{-\infty}^{\infty}\frac{\hat x(\tau)}{t - \tau} d\tau
$$
Se le llama Transformador de Hilbert ó Filtro de Hilbert ó Filtro en Cuadratura.

### Espectro de la Transformada de Hilbert:

La transformada de Fourier de la transformadda de Hilbert es:
$$
\hat X(f) = \mathcal{F}[\hat x(t)] = -jSign(f) X(f)
$$
Y de allí se deduce:
$$
H_H(f) = \frac{\hat X(f)}{X(f)} = jSign(f) = j\big[u(-f)- u(f)\big] = \Bigg\{ \begin{array}{l} +j = e^{j\frac{\pi}{2}}: \hspace{7px} f < 0 \\ 0: \hspace{7px} f = 0 \\ -j = e^{-j\frac{\pi}{2}} \hspace{7px} f > 0   \end{array}
$$

### Propiedades de la T.H.

1.  $$x(t)$$ y $$\hat x(t)$$ tienen la misma densidad espectral de potencia.
	-  Si $$x(t)$$ es limitada en banda entonces $$\hat x(t)$$ también.
	- Ambas tienen la misma energía o potencia.
2. Tienen la misma función de autocorrelación $$R_x(\tau)$$
3. Ambas son ortogonales entre sí, es decir, $$\int_{-\infty}^{\infty} x(t) \hat x(t) dt = 0 $$
4. No tiene función inversa, pero se puede usar la siguiente propiedad: $$\hat x(t) = \mathcal{H}\{x(t)\} \Rightarrow \mathcal{H}\{\hat x(t)\} = -x(t)$$
5. Si $$x(t)$$ es par $$\hat x(t)$$ es impar y viceversa.

### Tabla de la T.H.

![[Pasted image 20241006123058.png]]

## Señales Analíticas y Equivalente Pasa Bajo

### Señales analíticas:

Una señal real pasabanda $$x(t)$$ tiene su señal analítica $$g_a(t)$$ que es compleja y nula para frecuencias negativas, y proporcional a la señal real en los positivos, también existe $$g_a^*(t)$$ que cumple lo mismo que la señal analítica definida anteriormente pero cambiando los roles entre frecuencias negativas y positivas.

A partir de ellas dos, se puede definir el espectro de la señal pasabanda como: $$X(f) = X_+(f) +X_-(f)$$ $$X_+(f) = \Bigg\{ \begin{array}{l} X(f): \hspace{1em} f > 0 \\ 0: \hspace{2.5em} f \leq 0 \end{array} \hspace{.5em}; \hspace{2em} X_-(f) = \Bigg\{ \begin{array}{l} X(f): \hspace{1em} f < 0 \\ 0: \hspace{2.5em} f \geq 0 \end{array}$$
El Espectro de las Señales Analíticas poseen el doble de los espectros positivos y negativos respectivamente.
$$G_a(f) = 2X_+(f)$$ $$G_a^*(f) = 2X_-(f)$$
La señal analítica también puede ser obtenida a través de la transformada de Hilbert:
$$g_a(t) = x(t) + j\hat x(t)$$
$$g_a^*(t) = x(t) - j\hat x(t)$$
###  Equivalente pasabajo:

El equivalente pasabajo de una señal pasabanda o envolvente compleja es la señal analítica desplazada al origen de coordenadas.
$$G(f) = G_a(f + f_c)$$
Tal que la señal pasabanda se construye como:
$$x(t) = Re\{g(t)e^{j\omega_ct}\}$$
El espectro se reconstruye, recordemos ue si :  $$z = a+jb \Rightarrow Re[z] = \frac{1}{2}z + \frac{1}{2}z^* = a$$
$$x(t) = Re\{g(t)e^{j\omega_ct}\} = \frac{1}{2}g(t)e^{j\omega_ct} + \frac{1}{2}g^*(t)e^{-j\omega_ct}$$
$$X(f) = \frac{1}{2}\mathcal{F}[g(t)e^{j\omega_ct}] + \frac{1}{2}\mathcal{F}[g^*(t)e^{-j\omega_ct}] = \frac{1}{2}\Bigg[G(f - f_c) + G^*(f + f_c) \Bigg]$$
$$X(f) = \frac{1}{2}[2X_+(f) + 2X_-(f)] = X_+(f) + X_-(f)$$
Definimos $$g(t) = x_i(t) + jx_q(t)$$ y obtenemos la forma cartesiana de la señal a partir de su equivalente asabajo, esta también se conoce como su representación fase-cuadratura:
$$x(t) = x_i(t)\cos(\omega_ct) - x_q(t)\sin(\omega_ct)$$
$$x_i(t) = Componente \hspace{.23em} en \hspace{.25em} fase$$
$$x_q(t) = Componente \hspace{.23em} en \hspace{.25em} cuadatura$$
Perteneciendo ambos componentes a los reales, luego, la forma polar o representación envolvente-fase de la señal se define a partir de:

$$x(t) = R(t)\cos[\omega_ct + \theta(t)]$$
$$g(t) = x_i(t) + jx_q(t) = |g(t)| e^{j\angle{g(t)}} \equiv R(t)e^{j\theta(t)}$$
$$x_i(t) = Re\{g(t)\} \equiv 