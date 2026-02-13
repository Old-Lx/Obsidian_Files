# Alojador de tipo pool

Se organiza en chunks de $2^n$, básicamente son bloques predeterminados equivaluados donde guardamos variables.

Se determina un header y se multiplica por el número de items que queremos en la piscina

Para un header de 16bits/2bytes $2bytes*16*16*256$ donde el header son 2bytes

Su complejidad de inserción es O(1)

No tiene que liberarse en orden secuencial

# Alojador freelist:

Es como el stack pero se libera como en el pool, de cualquier forma y a diferencia del pool, los bloques pueden ser de tamaños distintos. Cuando bloques subsecuentes de memoria se liberaan, se asimilan en un sólo bloque

Su complejidad es O(h) donde h es el número de elementos