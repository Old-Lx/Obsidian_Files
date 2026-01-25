El objetivo de esta clase es crear una función en assembly y usarla en C, esto se hace escribiendo la función en asm y exportándola mediante un .h

### La función a importar en el ejemplo es:
    ```
    #include <string.h>
    
    int sum_array(int number_list[], int size) {
    
	    int total = 0;
			// Para conocer el tamaño de una lista dinámica necesitas dividir el tamaño de la lista entre el tamaño de alguno de sus elementos
		    for (int i = 0; i < size; i++) {
			    total += number_list[i];
		    }
		    
		    return total;
    };
    
    void main() {
	    int number_list[] = {0, 5, 10};
	    
	    printf("%i", sum_array(number_list, sizeof(number_list)/sizeof(number_list])));
    }
    ```

Directiva de asm para el compilador nasm
    ```
    %ifidn OUTPUT_FORMAT,elf64 
	    section .note,GNU-stack noalloc noexe nowrite progbits 
    %endif
    ```
La función en el .h debe tener el mismo nombre que en el .asm
![[Pasted image 20260123175214.png]]
![[Pasted image 20260123174610.png]]
![[Pasted image 20260123173612.png]]


## Makefiles:

## compile.mk:

## debug.mk:


    ```
    BUILD_PATH := ../debug
    OUTPUT_PATH
    
    ```

![[Pasted image 20260123180545.png]]
![[Pasted image 20260123180629.png]]
![[Pasted image 20260123182144.png]]
![[Pasted image 20260123181727.png]]
En esta corregir a NASM_DEPENDENCIES
![[Pasted image 20260123181841.png]]
![[Pasted image 20260123181919.png]]

### El gdb es un debugger de consola:
Revisar flags
`` gdb -tui ./debug/bin/main ``

### Para configurar la barra de acciones en VS Code:
Descargar Activitus Bar (un plugin)

se crea settings.json en .vscode
![[Pasted image 20260123182910.png]]
![[Pasted image 20260123182939.png]]
va es task.build.make
### Se crea task.json
El label debe corresponder a lo que haya después de task. en el settings.json
![[Pasted image 20260123183207.png]]

### Se configura el debugger:
En la misma carpeta, se crea launch.json
![[Pasted image 20260123183444.png]]
![[Pasted image 20260123183629.png]]
![[Pasted image 20260123183645.png]]
en program no aceptó el wildcard, si no logras, dale con main directamente y luego revisas cómo usar el wildcard

## script.sh:


    ```
    echo "Clear the Debug mode compilation"
    make -f debug.mk clean
    
    echo "Build debug mode"
    make -f debug.mk
    
    echo "Clear the Prod mode compilation"
    make -f Makefile clean
    
    echo "Build Prod mode"
    make -f Makefile
    ```
   
![[Pasted image 20260123180037.png]]
### Tarea:
Hacer un programa de assembly que imprima una string que envíe un usuario.

Pista:
![[Pasted image 20260123184455.png]] 