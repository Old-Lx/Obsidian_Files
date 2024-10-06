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

## Espectro de la Transformada de Hilbert:

La transformada de Fourier de la transformadda de Hilbert es:
$$
\hat X(f) = \mathcal{F}[\hat x(t)] = -jSign(f) X(f)
$$
Y de allí se deduce:
$$
H_H(f) = \frac{\hat X(f)}{X(f)} = jSign(f) = j\big[u(-f)- u(f)\big] = \Bigg\{ \begin{array}{l} +j = e^{j\frac{\pi}{2}}: \hspace{7px}  \\ 0 \\ -j = e^{-j\frac{\pi}{2}}   \end{array}
$$