# Punto 2 — Análisis: de lo ambiguo a lo preciso

## 2.a Preguntas al requerimiento

| # | Pregunta que formularía a la Coordinación | Por qué el algoritmo no puede construirse sin esa respuesta |
|---|---|---|
| 1 | ¿Qué datos identifican a cada solicitante? | No sabe en que dato basarse (código, cédula, correo) por lo tanto no se puede verificar si está registrado. |
| 2 | ¿Qué tipos de falla existen y cómo se identifican? | La clasificacion de las fallas no se puede hacer al no saber los diferentes tipos. |
| 3 | ¿Qué hace que una solicitud sea "urgente" o "crítica"? | Al no haber especificado que una solicitud sea urgente o no o como se identiifican. |
| 4 | ¿Cuántos niveles de prioridad existen y cómo se llaman? | Al algoritmo le faltan valores (ej. alta/media/baja) para saber la prioridad de una y otra. |
| 5 | ¿Cuánto tiempo de respuesta corresponde a cada nivel de prioridad? | Sin definir estos tiempos no se puede ordenar ni saber el tiempo correspondiente a cada una. |

## 2.b Por qué no puede implementarse directamente

El requerimiento describe un objetivo general, pero no cumple con la característica de **precisión** que debe tener un algoritmo: no define con exactitud qué es "urgente" ni qué valores puede tomar la prioridad. Tampoco entrega los datos de **entrada** necesarios (tipo de falla) ni los de **proceso** (reglas de decisión) para producir la **salida** esperada. Mientras esto que falta no se arregle. No se resuelvan con la Coordinación, cualquier intento de escribir el algoritmo sería adivinar reglas que nadie definió.
