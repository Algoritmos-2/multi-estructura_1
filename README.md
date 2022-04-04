# Multi-estructuras - Ejercicio 1
Se desea construir un programa que haga de cola de prioridad de tareas en donde se pueda:
- Añadir una nueva tarea (se pasa el id y su prioridad).
- Obtener la tarea más prioritaria y eliminarla de la cola de prioridad.
- Eliminar tarea dado un id.

Se sabe ademas de que la cola de prioridad tiene un limite de C tareas que puede almacenar.
1 <= C <= 1000000

Se pide implementar las operaciones en estos ordenes:
- Añadir: O(1) caso promedio.
- Tarea más prioritaria: O(LogN) caso promedio, siendo N la cantidad de elementos dentro de la cola de prioridad.
- Eliminar tarea: O(LogN) caso promedio, siendo N la cantidad de elementos dentro de la cola de prioridad.

Notas: 
- La prioridad es un numero que mientas menor sea, mayor es la prioridad.
- De existir dos tareas con la misma prioridad entonces se usa el orden de llegada.

## Formato de entrada
| Entrada           |
| ----------------- |
| C                 |
| N                 |
| Operacion 1       |
| Operacion 2       |
| Operacion 3       |
| ...               |
| Operacion N       |


La primer linea indica la capacidad de la cola de prioridad.
La segunda linea la cantidad de operacion que se realizaran.
Las N siguientes lineas son las operaciones a realizar. Estan pueden ser:
- Añadir: "insert [id] [prioridad]"
- Tarea más prioritaria: "next" 
- Eliminar tarea: "delete [id]"

## Formato de salida
Imprime por cada linea la salida de la cola de prioridad ("next")

## Ejemplos
### Ejemplo 1
| Entrada      |
| ------------ |
| 10           |
| 5            |
| insert abc 6 |
| insert bca 3 |
| next         |
| insert xyz 1 |
| next         |

| Salida      |
| ----------- |
| bca         |
| xyz         |
