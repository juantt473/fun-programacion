# Punto 1 — ¿Esto es un algoritmo?

## 1.a Tabla de clasificación

| # | Procedimiento | ¿Es algoritmo? | Justificación |
|---|---|---|---|
| a | Reiniciar el router | No | Incumple **finitud**: el paso "espere hasta que el LED de estado quede fijo en verde" no existe un límite de tiempo, si el LED nunca cambia el procedimiento podría no terminar nunca. |
| b | Limpiar el equipo | No | Incumple **precisión**: "hasta que se vea bien" y "la cantidad adecuada" son palabras subjetivas, y se prestan para interpretacion. |
| c | Mostrar ticket de prioridad alta | Sí | Cumple las 5 características: es preciso (revisa un dato, la prioridad), termina al recorrer la lista (finitud), es claro cuando dice mostrar primero que tenga prioridad (determinismo), sirve para cualquier lista (generalidad) y se ejecuta facil (eficiencia). |
| d | Calcular promedio de tres notas | Sí | Cumple las 5 características: cada paso explica bien el procedimiento matematico (precisión), hay un numero de pasos establecido (finitud), da el mismo resultado con los iguales datos (determinismo), sirve para cualquier estudiante con el mismo numero de notas (generalidad) y se calcula con el procedimiento adecuado (eficiencia). |

## 1.b Tablas Entrada – Proceso – Salida

### Procedimiento c

| Entrada | Proceso | Salida |
|---|---|---|
| Lista de tickets abiertos, cada uno con su prioridad determinada | ya en la lista buscar el primer ticket que tenga alta prioridad | mostrar en pantalla el ticket de prioridad alta |

### Procedimiento d

| Entrada | Proceso | Salida |
|---|---|---|
| Las tres notas del estudiante | Sumar las tres notas y dividir el resultado entre tres | El promedio en pantalla |
