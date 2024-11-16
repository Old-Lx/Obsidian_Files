## Modulación lineal:

El espectro que produce está relacionado linealmente con el **Espectro del Mensaje**. Entre los tipos de Modulación Lineal se encuentran:
- AM - Amplitude Modulation.
- DSB - Double Side Band.
- SSB - Single Side Band.
- VSB - Vestigial Side Band.

Utilizaremos las siguientes convenciones:
1.  El mensaje $$x(t)$$ estará **Limitado en Banda**, es decir, es una **señal pasabajo** con ancho de banda $$BW = B$$sólo se mide para $$f>0$$ ![[Pasted image 20241116070226.png]]
2. El mensaje $$x(t)$$ estará normalizado, esto es $$|x(t)| \leq 1$$ En este caso también la potencia promedio será menor que uno si proviene de una fuente ergódica.
3. Muchas veces supondremos que el mensaje es un tono $$x(t) = A_m\cos(\omega_m t)$$ Lo cual tiene sentido considerando el análisis de Fourier.

### Modulación de Amplitud (AM):

Se varía la amplitud de una sinusoide de acuerdo al mensaje que se desea transmitir. A esta Sinusoide se le llama **Portadora** debido a que llevará la información sobre sí. Este tipo de modulación se utiliza en radiodifusión comercial y algunas bandas de radio ciudadana.

Sea $$x(t)$$ el mensaje que cumple con las condiciones anteriores y sea $$x_c(t) = A_c\cos(\omega_ct)$$ la portadora. La señal modulada en amplitud (AM) se expresa como:
$$x_{AM}(t) = A_c(1 + mx(t))\cos(\omega_c t)$$ donde "m"es el índice de modulación.
$$m \in \mathbb{R}, \hspace{1em} 0\leq m \leq 1$$
En el tiempo $$x_{AM}(t)$$ toma la siguiente forma: ![[Pasted image 20241116072229.png]] 
Como el mensaje $$|x(t)| \leq 1 \Rightarrow -1 \leq x(t) \leq 1$$ $$\begin{array}{l}x_{AM_{max}}(t) = A_c (1 + m) \\ x_{AM_{min}}(t) = A_c (1 - m) \end{array} \Bigg\} \begin{array}{c} x_{AM_{max}}(t) + x_{AM_{min}}(t) = 2A_c \\ \hspace{1em} x_{AM_{max}}(t) - x_{AM_{min}}(t) = 2mA_c \end{array}$$ Dividiendo:
$$m = \frac{x_{AM_{max}}(t) - x_{AM_{min}}(t)}{x_{AM_{max}}(t) + x_{AM_{min}}(t)} = \frac{Q}{P}$$