Se encarga de manipular los dígitos binarios que procesa una computadora para poder transmitirlos, la conversión depende del tipo del canal. Ella define todas las especificaciones necesarias para que se pueda conectar al canal y que éste último se mantenga operativo.

Debe tomar en cuenta material de los cables, topología de la red, representación de la señal, etc.

### Principales herramientas
- Análisis de Fourier
- Características de las señales (bandwidth limitado)
- Tasa de transferencia máxima de un canal

### Terminología:
- De punto a punto: Enlace directo entre dispositivos
- Multipunto: más de dos dispositivos
- Simplex: En una sola dirección
- Semi-duplex o half-dupelx: Ambas direcciones pero sólo una vía a la vez
- Duplex o full-duplex: Ambas direcciones al mismo tiempo

### Tipos de comunicación según destino:
- Unicast: Se envía a un destinatario concreto
- Broadcast: Se envía a todos los destinatarios posibles
- Multicast: Se envía a un ggrupo selecto de destinatarios
- Anycast: Se envía a un destinatario cualquiera de un conjunto de posibles destinatarios

### Tipos de transmisión
- En serie: Se envía un bit tras otro mediante un único circuito o hilo de comunicación
- Paralela: Se transmiten simultáneamente una palabra de información, usando tantos hilos de comunicación como bits componen la palabra
- Dato: Entidad que transporta un significado
- Señal: Representación eléctrica o electrónica del dato
- Transmisión: Comunicación de datos por propagación y/o procesamiento de las señales


## Transmisión síncrona y asíncrona:
La sincrónica implica que se debe sincronizar la transmisión con un reloj, pero ambos usan reloj. En la síncrónica siempre se está transmitiendo, en la asincrónica se puede cortar e iniciar la transmisión en cualquier momento. En ambos casos se envía un código que significa que luego se van a enviar bits que tienen significado
![[Pasted image 20250505181605.png]]
![[Pasted image 20250505181801.png]]

### Técnicas de codificación de datos:
Se entiende por codificación al proceso de conversión de un sistema de datos de origen a otro sistema de datos de destino

Para transmitir es necesario codificar los datos en señales

![[Pasted image 20250505182355.png]]

