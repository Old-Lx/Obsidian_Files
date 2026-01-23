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

Directiva de asm para un compilador específico (no sé bien cuál)
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

## compile.mk

## debug.mk:


    ```
    BUILD_PATH := ../debug
    OUTPUT_PATH
    
    ```

![[Pasted image 20260123180545.png]]
![[Pasted image 20260123180629.png]]
![[Pasted image 20260123182144.png]]
![[Pasted image 20260123181727.png]]
![[Pasted image 20260123181841.png]]
![[Pasted image 20260123181919.png]]

## script.sh:


    ```
    echo "Clear the Debug mode compilation"
    make -f debug.mk clean
    
    echo "Build debug mode"
    make -f debug.mk
    
    echo "Clear the Debug mode compilation"
    make -f debug.mk clean
    
    echo "Build debug mode"
    make -f debug.mk
    ```
   
![[Pasted image 20260123180037.png]]