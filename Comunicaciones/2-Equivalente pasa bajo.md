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
