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

Se requiere un sumador y un multiplicador. El multiplicador podría realizarse con multiplicadores analógicos o con dispositivos no lineales.

#### Modulador de ley de potencias o modulador de ley cuadrática:

Requiere un sumador, un elemento no lineal y un filtro pasabanda.

![[Pasted image 20241117112425.png]] 
Se pueden usar diodos o transistores en las regiones donde $x_{out}(t) = a_1x_{in}(t) + a_2x^2_{in}(t)$ 

si $x_{in}(t) = A_c\cos(\omega_c t)) + x(t)\Rightarrow x_{out}(t) = a_1(A_c\cos(\omega_c t) + x(t)) + a_2(A_c\cos(\omega_c t) + x(t))^2$ luego:
$$x_{out} = a_1 A_c\cos(\omega_c t) + a_1x(t) + a_2A_c^2cos^2(\omega_c t) + 2a_2 A_c x(t)\cos(\omega_c t) + a_2 x^2(t)$$

Veamos los términos que nos sobran para que $x_{out}(t)$ sea una señal AM:

- $a_1x(t)$ y $a_2x^2(t)$ están entre $f = 0$ y $f = B$, es decir, fuera de la banda de AM.
- $a_2 A_c^2 cos^2(\omega(\omega_c t)) = \frac{a_2 A_c^2}{2}(1 + \cos(2\omega_c t))$ , está en $f = 0 (DC)$ y $f_c = 2f_c$ 
Tal que al filtrar con $f_{min} = f_c - B$ y $f_{max} = f_c + B$ nos quedará:$$ x_{AM}(t) = a_1 A_c\cos(\omega_c t) + 2 a_2 A_c x(t)\cos(\omega_c t)$$ ![[Pasted image 20241117114733.png]]

$$x_{AM} = a_1A_c\cos(\omega_c t)\Big(1 + \frac{2a_2}{a_1}x(t)\Big)$$

Se observa que $m = {2a_2}{a_1}$, lo que constituye una desventaja ya que en general $a_2 << a_1$ y esto implica que la profundidad de modulación será baja (m pequeñas).

![[Pasted image 20241117115435.png]]

#### Modulador por conmutación (switched)
![[Pasted image 20241117115537.png]]
Cuando el switch esté cerrado sobre R habrá un $v_R \neq 0$, cuando esté abierto $v_R = 0$.

Su ibjetivo fundamental es trasladar el espectro del mensaje a la frecuencia portadora, lo cual se hace mediante $v_i(t) = x(t) + A_c\cos(\omega_c t)$. Se multiplica $v_i$ por una señal periódica de periodo $T = \frac{1}{f_c}$ que cierra y abre el switch cada $T$. MAtemáticamente se puede expresar como: $$v_R = v_i(t)\cdot \sum_{k = -\infty}^{+\infty} \pi(\frac{t - k}{T})$$
donde: $$\sum_{k = -\infty}^{+\infty} \pi(\frac{t - k}{T}) = a_0 + \sum_{n = 1}^{+\infty} a_n\cos(n\omega_c t)$$
siendo la parte derecha la serie de Fourier con $n$ impar.

Suponiendo que para los ciclos positivos de $v_i(t)$, el switch está cerrado $v_R = v_i$ y los ciclos negaticos de $v_i(t < 0)$, el switch está abierto $v_R = 0$, entonces, si $A_c >> x(t)$, no habrá cruces por cero en un $T= \frac{1}{f_c}$. 

Se puede modelar como:

![[Pasted image 20241117121310.png]]

$$v_R(t) = \Big(A_c\cos(\omega_c t) + x(t)\Big)\Big(a_0 + \sum_{n = 1}^{+\infty} a_n\cos(n\omega_c t)\Big)$$ con $n$ impar, luego:
$$v_R(t) = A_c\cdot a_0\cos(\omega_c t) + a_0 x(t) + \sum_{n = 1}^{+\infty} A_c a_n\cos(\omega_c t)\cdot\cos(n\omega_c t) + \sum_{n = 1}^{+\infty}a_n x(t)\cos(n\omega_c t)$$
donde el último término desplaza el mensaje a todos los múltiplos impares de $f_c$, por lo que sobran términos.
![[Pasted image 20241117122212.png]]

- sobran los términos $a_0x(t)$, es decir, la banda base
- los múltiplos de $f_c$, es decir:$$\sum_{n = 1}^{+\infty} A_c a_n\cos(\omega_c t)\cdot\cos(n\omega_c t)$$ donde $f > f_c$, es decir, deltas fuera de la banda de AM
- $$\sum_{n = 1}^{+\infty}a_n x(t)\cos(n\omega_c t)$$
sobran los términos con $\{n = 2k+1/ k \geq1 \}$, por lo que sólo nos sirve $k=0 \Rightarrow n =1$ de donde se obtiene el término $a_1x(t)\cos(\omega_c t)$ 

Luego del filtro, tendremos:

$$x_{AM}(t) = a_0 A_c\cos(\omega_c t) + a_1 x(t)\cos(\omega_c t)$$
agrupando para obtener m:
$$x_{AM}(t) = a_0 A_c\cos(\omega_c t)\Big(1 + \frac{a_1}{a_0 A_c} x(t)\Big)$$
y se observa que $m = \frac{a_1}{a_0 A_c}$, si el pulso rectangular es:

![[Pasted image 20241117123722.png]]

### Receptores de AM

En el caso de AM, también llamada DSB+carry o doble banda lateral con portadora, se tiene el mensaje $x(t)$ en la envolvente de la señal AM.

El método más sencillo es la detección directa de la envolvente de $x_{AM}(t)$.

#### Detector de Envolvente
$v_i(t) = x_{AM}(t)$ 
![[Pasted image 20241117124250.png]]
![[Pasted image 20241117124537.png]]
![[Pasted image 20241117124914.png]]
![[Pasted image 20241117125106.png]]
![[Pasted image 20241117125319.png]]

La sencillez dew este demodulador permite aplicaciones masivas, como radiodifusión comercial, ya que es muy barato.

#### Detector síncrono

![[Pasted image 20241117125630.png]]
Al multiplicar $x_{AM}(t)$ por la portadora:
$$\begin{array}{c}x_i(t) = x_{AM}(t)\cdot\cos(\omega_c t) = A_c \Big(1 + mx(t)\Big)\cos(\omega_c t)\cdot cos(\omega_c t) \Rightarrow x_i(t) = A_c\Big(1 + mx(t)cos^2(\omega_c t)\Big)\\ = \frac{A_c}{2} \Big(1 + mx(t)\Big)\Big(1 + \cos(2\omega_c t)\Big)\end{array}$$
Agrupando:
$$x_i(t) = \frac{A_c}{2}\Big(1 + mx(t)\Big) + \frac{A_c}{2}\Big(1 + mx(t)\Big)\cos(2\omega_c t)$$
donde el término sin $\cos(2\omega_c t)$ es el término en $f = 0$ y el otro es el término en $2f_c$

Al filtrar $x_i(t)$ por un pasabajo con $f_{max} << f_c$, pero $f_{max} > B$, recuperamos el mensaje, obteniendo en la salida: $$x_{out}(t) = \frac{A_c}{2} + \frac{A_c}{2} m x(t)$$

El condensador elimina la parte DC, entonces, quedaremos con:$$x_{salida} = kx(t) = \frac{A_c}{2}mx(t)$$ tal que $k = \frac{A_c}{2}m$ .

En este caso la portadora por la que se multiplica debe estar **en fase** con la señal modulada $x_{AM}(t)$, de otra forma, se generan armónicos que contaminan la recuperación del mensaje.

Para implementar esta demodulación, se debe utilizar un detector de fase y este a su vez enganche la fase del oscilador local con la de $x_{AM}(t)$. El circuito que realiza esto se conoce como **Phase Look Loop** (PLL) o lazo de enganche de fase, como se estudió en electro 3.

