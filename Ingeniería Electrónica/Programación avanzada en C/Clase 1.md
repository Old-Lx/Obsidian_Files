### Lenguaje Compilado:

### Lenguaje Interpretado:

### Makefiles:
Definición

Sintaxis:

    # Comentarios van entre numerales #
    // Multilínea son con la barrita pero no sé si es \ o /
    
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