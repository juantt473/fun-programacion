# Punto 3 — Del lenguaje natural al pseudocódigo

## 3.a Algoritmo en lenguaje natural

1. Leer el código del solicitante, el tipo de falla y si la solicitud es crítica.
2. Verificar si el solicitante está registrado.
3. Si no está registrado, mostrar el mensaje de rechazo por solicitante no registrado y terminar.
4. Si está registrado, verificar que el tipo de falla esté entre 1 y 3.
5. Si el tipo de falla no es válido, mostrar el mensaje de rechazo correspondiente y terminar.
6. Si el tipo de falla es válido, verificar si la solicitud es crítica.
7. Si es crítica, asignar prioridad ALTA y tiempo de respuesta de 2 horas.
8. Si no es crítica, verificar si el tipo de falla corresponde a red.
9. Si es red, asignar prioridad MEDIA y tiempo de respuesta de 8 horas.
10. En cualquier otro caso, asignar prioridad BAJA y tiempo de respuesta de 24 horas.
11. Registrar el ticket con el código del solicitante y la prioridad asignada.
12. Mostrar en pantalla la prioridad asignada y el tiempo de respuesta.

## 3.b Pseudocódigo

```
Inicio
    Leer codigo_solicitante, tipo_falla, es_critico

    registrado <- EstaRegistrado(codigo_solicitante)

    Si registrado = Falso Entonces
        Escribir "SOLICITUD RECHAZADA: solicitante no registrado"
    Sino
        Si (tipo_falla < 1) O (tipo_falla > 3) Entonces
            Escribir "SOLICITUD RECHAZADA: tipo de falla no válido"
        Sino
            Si es_critico = Verdadero Entonces
                prioridad <- "ALTA"
                tiempo_respuesta <- 2
            Sino
                Si tipo_falla = 1 Entonces
                    prioridad <- "MEDIA"
                    tiempo_respuesta <- 8
                Sino
                    prioridad <- "BAJA"
                    tiempo_respuesta <- 24
                FinSi
            FinSi
            RegistrarTicket(codigo_solicitante, prioridad)
            Escribir "Prioridad: ", prioridad
            Escribir "Tiempo de respuesta: ", tiempo_respuesta, " horas"
        FinSi
    FinSi
Fin
```

## 3.c Frase ambigua

La frase del paso 1, "Leer el código del solicitante, el tipo de falla y si la solicitud es crítica", no aclara si son tres lecturas independientes o una sola instrucción con tres datos, ni qué tipo de dato es "si es crítico". Al traducir a pseudocódigo tuve que precisar que es una única instrucción `Leer` con tres variables, y que `es_critico` se compara contra `Verdadero`/`Falso` como define la especificación, no contra texto como "sí"/"no".
