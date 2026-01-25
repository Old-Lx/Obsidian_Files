### Lenguaje Compilado:

### Lenguaje Interpretado:

### Makefiles:

https://makefiletutorial.com/

Definición:
Es una herramienta para gestionar organizadamente la compilación de archivos en C/C++, permite manejo de requisitos, ejecución de comandos de terminal tipo unix, entre otros.

Para compilar se usa el comando:

    ```
    make -f <archivo makefile>
    ```

La terminación de un archivo make es .mk pero en linux pueden hacerse sin terminación.

Sintaxis:

    # Comentarios van entre numerales #
    
    # Variables #
    SRC := ./src # La convención de variables es mayúsculas #
    BUILD := ./build
    DEBUG := ./debug
    
    # Ejemplo de instrucción default #
    nombre de la instrucción: prerequisito
	    comandos
    
    main: main.o
	    mkdir -p ${BUILD}/bin
	    gcc ${BUILD}/main.o -o ${BUILD}/bin/main
	main.o: ${SRC}/main.c
		mkdir -p ${BUILD}
		gcc -c ${SRC}/main.c -o ${BUILD}/main.o
	clean:
		rm -fr ${BUILD}

### Docker

Sintaxis:


    ```
   
    ```

### Tarea:

![[Pasted image 20260120180722.png]]
![[Pasted image 20260123074819.png]]
![[Pasted image 20260123074946.png]]
![[Pasted image 20260123075237.png]]
![[Pasted image 20260123075330.png]]
![[Pasted image 20260123075525.png]]
![[Pasted image 20260123074724.png]]
![[Pasted image 20260123075641.png]]
