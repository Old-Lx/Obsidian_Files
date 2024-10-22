- Resumen de fórmulas y conceptos:
1- Para parametrizar debes expresar las todas tus variables en función de parámetros pseudo arbitrarios que permitan reducir la cantidad de variables, cabe a destacar que no todas las parametrizaciones son convenientes para un ejercicio dado.
2- Ecuación del plano tangente:
$$
\big<\nabla f(x_{0}, y_{0}), \Bigg(\begin{array}{r} x - x_{0} \\ y-y_{0} \end{array}\Bigg)\big> = z-z_{p}
$$
o
$$
\big<\nabla f(x_{0}, y_{0}, z_{0}), \Bigg(\begin{array}{r} x - x_{0} \\ y-y_{0} \\ z-z_{0} \end{array}
 \Bigg)\big>
$$
3- Área de una superficie:
$$
A(S) = \int\int_{D} ||r_{u} \times r_{v}||d_{A}
$$
Si $$r:D \subseteq \mathbb{R}^2 \rightarrow\mathbb{R}^3$$ es una parametrización de S o
$$
A(S) = \int\int_{D} \sqrt{\Big(\frac{\partial g}{\partial u} \Big)^2 + \Big(\frac{\partial g}{\partial v} \Big)^2 + 1}\hspace{7px} dA
$$ si S es el gráfico de una función $$z = g(x, y) \hspace 7px con \hspace 7px dominio \hspace 7px D = \mathbb R^3$$ 
4- Jacobiano:
$$\frac{\partial(x, y)}{\partial(u, v)} = \Bigg|\begin{array}{c}
\frac{\partial x}{\partial v} \hspace 7px  \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial v} \hspace 7px  \frac{\partial y}{\partial v}
\end{array} \Bigg|$$
## Primer parcial con Libuska

5- Integrales de línea:
- Campo escalar:
$$
\int_\Gamma f(x,y,z)dl = \int_A^B f(\vec r(t))\cdot||\vec r'(t)||dt = \int_A^B f(x(t), y(t), z(t))\cdot||\vec r'(t)||
$$

- Campo vectorial:
$$
\int_\Gamma \vec F(x,y,z)\cdot d\vec l = \int_A^B \vec F(\vec r(t)) \cdot\vec r(t)dt = \int_A^B \Big<\vec F(x,y,z), \vec r(t)\Big>dt
$$
6- Integrales de superficie:
- De campos escalares a superficies:
$$
\int\int_Sf(x,y,z)dS = \int\int_D f(\Phi(u, v))\cdot||\vec r_u \times \vec r_v|| dudv
$$
Donde $$ \Phi(u,v) $$ es la parametrización y $$ ||\vec r_u \times \vec r_v|| = ||\Phi'(u) \times \Phi'(v)|| $$ con cada derivada de siendo la derivada de la parametrización respecto a la variable indicada

## Segundo parcial con Libuska

Con $$F = \Bigg(\begin{matrix}F_1\\ F_2\\ F_3 \end{matrix} \Bigg)$$
Tenemos que su divergencia y su rotacional se definen como:
$$Div(F) = \frac{\partial F_1}{\partial x} + \frac{\partial F_2}{\partial y} + \frac{\partial F_3}{\partial z}$$
$$rot(F) = \Bigg(\begin{matrix}\frac{\partial F_3}{\partial y} - \frac{\partial F_2}{\partial z}\\ \frac{\partial F_3}{\partial x} - \frac{\partial F_1}{\partial z}\\ \frac{\partial F_3}{\partial y} - \frac{\partial F_2}{\partial z} \end{matrix} \Bigg)$$$$

7- Teorema de Gauss:

Sean $$F: \mathbb R^3 \rightarrow \mathbb R^3$$ región cerrada $$\Omega\subset\mathbb R^3$$
$$Si \hspace{0.5em}F \hspace{0.5em} es \hspace{0.5em} \mathcal C^1 \hspace{0.5em} en \hspace{0.5em} \Omega\hspace{0.3em}\cup\hspace{0.3em}front\hspace{0.3em}\Omega \Rightarrow \int\int_{front\hspace{0.3em}\Omega\uparrow}<F, ds> = \int\int\int_\Omega div(F)dxdydz$$
8- Teorema de Stokes:
 Sean $$F: \mathbb R^3 \rightarrow \mathbb R^3$$ superficie orientada $$S\uparrow$$ $$Si \hspace{0.5em}F \hspace{0.5em} es \hspace{0.5em} \mathcal C^1 \hspace{0.5em} en \hspace{0.5em} S\hspace{0.3em}\cup\hspace{0.3em}front\hspace{0.3em}S \Rightarrow \int_{front\hspace{0.3em}S\uparrow}<F, ds> = \int\int_S <rot(F), dS>$$ La orientación de $$S\uparrow$$ viene dada por la regal de la mano derecha
 