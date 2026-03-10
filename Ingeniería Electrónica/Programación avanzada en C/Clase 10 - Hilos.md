# Hilos
Los hilos son subdivisiones del núcleo que proporcionan un algoritmo de paralelización, se le dan espacios de tiempo a los hilos.

Los hilos no son realmente paralelismo, sólo se guarda el stack de cada hilo para seguir trabajando

![[Pasted image 20260310170652.png]]
<[Hilos](https://www.geeksforgeeks.org/operating-systems/what-are-threads-in-computer-processor-or-cpu/)>
<[Núcleos](https://www.hp.com/us-en/shop/tech-takes/cpu-cores-how-many-do-i-need)>

Mediante el ejemplo de contador:
![[Pasted image 20260310171615.png]]

Al usar multihilo, cambia el valor al contar:
![[Pasted image 20260310171638.png]]
![[Pasted image 20260310171808.png]]

Los hilos comparten memoria, por lo que cuando un hilo está escribiendo, se puede cambiar de hilo y puede pasar que se pierdan escrituras de la memoria.

## Spinlock
Función que se queda en un ciclo infinito hasta que le permiten parar

![[Pasted image 20260310172437.png]]


# Mutexes
Variable del procesador que bloquea secciones específicas de có
# Semaphores

# Process

