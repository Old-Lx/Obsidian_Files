# Union:
"A union is a user-defined data type that can hold different data types, similar to a structure.

- Unlike [structures](https://www.geeksforgeeks.org/c/structures-c/), all members of a union are stored in the same memory location. Since all members share the same memory, changing the value of one member overwrites the value of the others.
- Union members can be accessed using the dot (.) operator. Example: u.member.
- Unions are useful when you want to save memory by storing different types of data in the same memory space."
https://www.geeksforgeeks.org/c/c-unions/

# Bitfield:
"In C, we can specify the size (in bits) of the structure and union members. The idea of bit-field is to use memory efficiently when we know that the value of a field or group of fields will never exceed a limit or is within a small range. C Bit fields are used when the storage of our program is limited."

https://www.geeksforgeeks.org/c/bit-fields-c/

Te permite acceder a bits individualmente, definiendo dentro de una estructura valores de data que accedan a información de bits de manera individual.


# Parte práctica
![[Pasted image 20260130152555.png]]
![[Pasted image 20260130153155.png]]
Un micro tiene profundidad de stack limitada, es decir, sólo puede ejecutar 4 funciones anidadas antes de ejecutar en la ram

![[Pasted image 20260130153819.png]]