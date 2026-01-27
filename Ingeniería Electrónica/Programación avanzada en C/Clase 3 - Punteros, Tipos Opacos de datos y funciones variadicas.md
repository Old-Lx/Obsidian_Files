---
aliases:
---
# Punteros:
Es un tipo de dato especfico que apunta a un lugar de memoria donde podemos almacenar datos de otro tipo de dato especfico.

    int *
    float *
    double *
    short *

La memoria de una computadora opera almacenando datos en espacios físicos

![[Pasted image 20260127170643.png]]

El cómo se accede la memoria, cuánto pesa cada dato y el tamaño de los apuntadores depende de la arquitectura del procesador.

La memoria de un computador es data contínua, con los apuntadores podemos seleccionar algún espacio dentro de esa data

El OS reserva el espacio en rojo para nuestro programa (como ejemplo) y a partir de allí opera.

![[Pasted image 20260127170911.png]]

"A pointer is a variable that stores the memory address of another variable. Instead of holding a direct value, it holds the address where the value is stored in memory. It is the backbone of low-level memory manipulation in C."
<https://www.geeksforgeeks.org/c/c-pointers/>

-  Simples
	Apunta a un tipo de dato.

- Dobles
	Apunta a otro apuntador

- Arreglos
	Su implementación es un puntero especial que permite acceder a través de números a las posiciones de memoria que guardó.

 ```int arreglo []; // similar a int* arreglo```
 
- Memoria

# Tipos Opacos de datos:
Datos de cuyo tipo no estamos seguros al principio.

https://www.geeksforgeeks.org/cpp/opaque-pointer-in-cpp/

https://www.ibm.com/docs/en/informix-servers/14.10.0?topic=cdt-opaque-data-type

Mediante los tipos opacos se implementa la ofuscación de código y el typecasting

stdint.h la usaremos bastante

https://www.geeksforgeeks.org/cpp/address-operator-in-c/

https://www.geeksforgeeks.org/cpp/cpp-polymorphism/

Acá sale lo de signatures:
https://www.codecademy.com/learn/learn-c-functions-and-structures/modules/functions-c/cheatsheet

### typedef:
"The ****typedef**** is a keyword that is used to provide existing data types with a new name. The C typedef keyword is used to redefine the name of already existing data types. When names of datatypes become difficult to use in programs, typedef is used with user-defined datatypes, which behave similarly to defining an alias for commands."

https://www.geeksforgeeks.org/c/typedef-in-c/

Se puede usar con funciones:
![[Pasted image 20260127174151.png]]
![[Pasted image 20260127174303.png]]

# Funciones variadicas:
"In C, variadic functions are functions that can take a variable number of arguments. This feature is useful when the number of arguments for a function is unknown. It takes one fixed argument and then any number of arguments can be passed."

Se pueden crear con `stdarg.h`

Donde `int n` es el número de argumentos
![[Pasted image 20260127175038.png]]
![[Pasted image 20260127175141.png]]

https://www.geeksforgeeks.org/c/variadic-functions-in-c/


# Parte práctica
![[Pasted image 20260127175907.png]]
