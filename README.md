# Respuestas evaluacion 2 introduccion a tecnologias de informacion 

## Aaron Trespalacios 

## pregunta 1 

Respuesta: D. 11.000 milisegundos.
¿Por qué? Porque se suman los tres tiempos del semáforo.

## pregunta 2 

Respuesta: C. Ejecutar el subcomando compile.
¿Por qué? Porque permite compilar el código y detectar errores antes de cargarlo en Arduino.

## pregunta 3 

Respuesta: D. Los LEDs de los bits 0, 2 y 3.
¿Por qué? Porque el número 13 en binario es 1101, donde los bits 0, 2 y 3 tienen valor 1.

## pregunta 4

Respuesta: C. Ignorar nuevas lecturas durante un breve intervalo.
¿Por qué? Porque el antirrebote evita que una sola pulsación se registre varias veces.

## pregunta 5

Respuesta: A. 4 patrones.
¿Por qué? Porque los dos canales que seleccionan los patrones permiten 2² = 4 combinaciones.

## pregunta 6 

Respuesta: D. Nivel LOW.
¿Por qué? Porque al colocar el interruptor en ON, el pin se conecta a tierra y devuelve LOW.

## PREGUNTA 7

- **Respuesta:** 880 milisegundos.
- **Sustentación:** Son 6 LEDs. El recorrido de ida y vuelta da un total de 12 pasos. Al multiplicar 12 × 80 ms se obtienen 960 ms. Restando los extremos que no se repiten por ciclo, el resultado final es 880 ms.

## PREGUNTA 8

- **Respuesta:** A) Agregar el usuario al grupo `dialout` y reiniciar su sesión en Debian 13.
- **Sustentación:** En Linux, el error de «permiso denegado» al interactuar con el puerto serie se soluciona agregando la cuenta de usuario actual al grupo de control de dispositivos serie (`dialout`).

## PREGUNTA 9

- **Respuesta:** 191.
- **Sustentación:** Se utiliza la función `map()` para reescalar la lectura del conversor analógico-digital. Al convertir la entrada de 819 (sobre un máximo de 1023) al rango de salida de 0 a 255, el valor resultante es aproximadamente 191.

## PREGUNTA 10

- **Respuesta:** El monitor muestrea los bits con una tasa distinta a la configurada en el sketch.
- **Sustentación:** Si la velocidad en baudios del monitor serial no coincide con la establecida en el código del programa, la transmisión de datos se sincroniza mal y se visualizan caracteres ilegibles.

## PREGUNTA 11

- **Respuesta:** 4,7 segundos.
- **Sustentación:** La constante de tiempo para un circuito RC se calcula multiplicando la resistencia por la capacitancia (\(\tau = R \times C\)). Al multiplicar 10.000 Ω por 0,00047 F, se obtienen 4,7 segundos.

## PREGUNTA 12

- **Respuesta:** Solo la declaración 1 es verdadera.
- **Sustentación:** Durante la descarga, el voltaje del capacitor disminuye de forma exponencial hacia cero. La segunda declaración es falsa porque, al transcurrir una constante de tiempo, el capacitor alcanza aproximadamente el 63 % de la tensión de la fuente, no el 100 %.

