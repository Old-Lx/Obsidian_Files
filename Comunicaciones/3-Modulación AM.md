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

El índice de modulación da una idea de qué tan separada está la envolvente positiva de la negativa.

A veces también se muestra en porcentaje $$m = 30\% = 0,3$$ También se puede escribir la señal AM como:
$$ x_{AM}(t) = A_c(1 + 1 + mx(t))\cos(\omega_c t)$$
$$ x_{AM} = A_c m x(t) \cos(\omega_c t) + A_c \cos(\omega_c t)$$
donde $$A_c m x(t) \cos(\omega_c t) $$ es el mensaje modulado y $$A_c \cos(\omega_c t)$$ es la portadora.

### Espectro de la señal AM:

Supongamos que el mensaje $$x(t)$$ ocupa un ancho de banda B como se muestra:
![[Pasted image 20241116075020.png]]
siendo la señal AM $$x_{AM}(t) = A_c m x(t) \cos(\omega_c t) + A_c\cos(\omega_c t)$$ tal que al aplicar la transformada de Fourier:
$$ X_{AM}(f) = m\frac{A_c}{2} X(f - f_c) + m \frac{A_c}{2} X(f+f_c) + \frac{A_c}{2} \delta(f-f_c) + \frac{A_c}{2}\delta(f+f_c)$$ Graficando: ![[Pasted image 20241116074821.png]] 
Se observa cómo se desplazó el mensaje a $$f_c \hspace{1em} y \hspace{1em} -f_c$$Con un delta en cada una que representa la presencia de la portadora.

La señal AM presenta un **espectro pasabanda** con un ancho de banda $$BW = 2B$$ por definición $$BW = f_{max} - f_{min}, \hspace{1em} f > 0$$ donde $$f_{max} = f_c + B, \hspace{1em} f_{min} = f_c - B$$
**La señal AM ocupa el doble del Ancho de Banda que el mensaje original**. A la parte superior $$f > f_c$$ se le llama **Banda Lateral Superior (Upper Side Band, USB)** y para la parte inferior $$f < f_c$$ se le llama **Banda Lateral Inferior (Lower Side Band, LSB)**.

### Potencia de una señal AM

Recondemos que la potencia promedio de una señal aleatoria coincide con $$P = E[x^2(t)]$$ tal que $$P = E[x^2_{AM}(t)] = \overline{x^2_{AM}(t)}$$
$$\begin{array}{c}P = \overline{[A_c \cos(\omega_c t) + A_c m x(t) \cos(\omega_c t)]^2} = \overline{A_c^2cos^2(\omega_ct) + 2A_c^2 m x(t) \cos(\omega_c t) + m^2 A_c^2 x^2(t) cos^2(\omega_c t)} \\= A_c^2\overline{cos^2(\omega_c t)} + 2m A_c^2 \overline{x(t)\cos(\omega_c t)} + m^2 A_c^2 \overline{x^2(t)cos^2(\omega_c t)}\end{array}$$ evaluando cada término:
$$\overline{cos^2(\omega_c t)} = \overline{\frac{1}{2}(1 + \cos(2\omega_c t))} = \frac{1}{2} + \overline{\frac{1}{2}cos(2\omega_c t)} = \frac{1}{2}$$ debido a que el valos promedio de un coseno es cero.

$$\overline{x(t)\cos(\omega_c t)} = ?$$ No se conoce este valor promedio, pero se sabe que dos señales son ortogonales si:
$$<x(t), y(t)> = \int_{-\infty}^{+\infty}x(t)y(t)dt = 0$$ lo cual es cierto si $$x(t) \hspace{1em} y \hspace{1em} y(t)$$
1. No coinciden en el tiempo
2. No coinciden en frecuencia
3. Tienen simetrías opuestas (par/ impar)

En este caso $$x(t)$$ no coincide en frecuencia con $$\cos(\omega_c t)$$ por lo que al ser ortogonales ek promeduo de su producto se anula.

$$\overline{x(t)\cos(\omega_c t)} = 0$$
de igual forma $$\begin{array}{c}\overline{x^2(t)cos^2(\omega_c t)} = \overline{x^2(t)}\cdot\overline{cos^2(\omega_c t)} = \frac{1}{2}\overline{x^2(t)} \Rightarrow P_{AM} = \overline{x^2_{AM}(t)} = \frac{A_c^2}{2} + m^2 \frac{A_c^2}{2}\overline{x^2(t)}, \\\hspace{1em} \overline{x^2(t)}=P_{mensaje}, \hspace{1em} \frac{A_c^2}{2} = P_c = Pot. \hspace{1em} de \hspace{1em} potadora\end{array}$$ Luego:
$$P_{AM} = P_c + \frac{m^2A_c^2}{2}P_m$$
Podemos llamar a $\frac{m^2A_c^2}{2}P_m = 2PSB$ donde **$PSB$ = Potencia de cada banda lateral** y **$P_c$ = potencia de la portadora** tal que $P_c = \frac{A_c^2}{2}$.

Recordando que en frecuencia:
$$P = \int_{-\infty}^{+\infty}|x(t)|^2df = \int_{-\infty}^{+\infty} S_{xx}(f)df$$
Donde x(t) es aleatoria del lado derecho y no aleatoria en el lado izquierdo.

![[Pasted image 20241116092500.png]]

tal que la potencia de cada banda lateral por separado es $$PSB = \frac{m^2}{4}A_c^2 P_m$$
Podemos definir la eficiencia de potencia de una señal como $$P_{total} = P_c + P_s$$
donde $P_s$ es la potencia contenida en las bandas con $P_s = 2PSB$, $P_c$ es la potencia de la portadora, la eficiencia será: $$\mu = \frac{P_s}{P_{total}}\times 100\% = \frac{2PSB}{P_c + 2PSB}\times 100\%$$
Luego sustituyendo de las relaciones obtenida para $P_c$ y $PSB$ y desarrollando:
$$\mu = \frac{m^2 P_m}{1 + m^2 P_m}\times 100\%$$ Recordando que $0 \leq m \leq 1$ y $x(t)$ está normalizado ($|x(t)| \leq 1$), entonces, $\mu_{max} = 50\%$ cuando $m^2\cdot P_m = 1$

Podemos concluir que A< es un sistema que produce:
- Un ancho de banda de transmisión igual al doble de ancho de banda del mensaje.
- Un gasto de potencia en la portadora que se refleja en que la eficiencia máxima que se puede lograr es del $50\%$.

### Moduladores AM

