# Respuestas evaluacion 2 introduccion a tecnologias de informacion 

## Aaron Trespalacios 
## Kevin Sebastián León Forero
## Roger Steveen Sandoval Negrete
## Sergio Alejandro León Fontecha

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

## Pregunta 13

Respuesta Correcta: B) 4,3 miliamperios.

Justificación:
De acuerdo con la ley de Ohm, la corriente de base (\(I_b\)) se calcula restando la caída de tensión de la unión base-emisor (\(V_{be}=0.7\text{ V}\)) al voltaje de salida del pin de Arduino (\(V_{cc}=5\text{ V}\)), y dividiendo el resultado entre la resistencia de base (\(R_b=1\text{ k}\Omega\)).
- Fórmula:
\[
I_b=\frac{V_{cc}-V_{be}}{R_b}
=\frac{5\text{ V}-0.7\text{ V}}{1000\ \Omega}
=4.3\text{ mA}
\]

## Pregunta 14

Respuesta Correcta: B) Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.

Justificación:
Al interrumpir la corriente en un motor (carga inductiva), el campo magnético colapsa bruscamente generando un pico de alta tensión inversa (ley de Lenz). Esta energía puede destruir el transistor. El diodo 1N4007 colocado en paralelo absorbe y disipa dicha corriente de retorno de manera segura, cumpliendo directamente la función de proteger el componente de conmutación.

## Pregunta 15

Respuesta Correcta: C) Pin digital 9.

Justificación:
Para utilizar la función analogWrite() en un Arduino UNO R3, se requiere un pin con soporte de hardware para Modulación por Ancho de Pulso (PWM). Los pines con esta capacidad en esta placa son únicamente el 3, 5, 6, 9, 10 y 11 (identificados físicamente con el símbolo ~). De las opciones dadas, solo el pin 9 cuenta con esta característica.

## Pregunta 16

Respuesta Correcta: D) Porque la demanda de la bobina excede la capacidad de corriente que soporta el pin.

Justificación:
Los pines digitales de un Arduino UNO R3 pueden suministrar un máximo absoluto de 40 mA de corriente de forma segura. Debido a que la bobina del relé electromecánico demanda 72 mA para activarse, conectarla directamente dañaría o quemaría de forma permanente el pin del microcontrolador. Por ello, se usa un transistor que actúa como interruptor de potencia para controlar la corriente externa requerida.

## Pregunta 17

Respuesta Correcta: B) Solo la declaración 2 es verdadera.

Justificación:
- Declaración 1 es falsa: La bobina del relé (circuito de control) y los contactos que manejan el motor (circuito de potencia) están aislados magnética y galvánicamente; no comparten el mismo circuito eléctrico.
- Declaración 2 es verdadera: Un diodo colocado en paralelo con una bobina actúa como diodo de libre circulación (flyback), limitando y descargando de forma segura el pico de sobretensión destructiva al apagar la corriente.

## Pregunta 18

Respuesta Correcta: A) Los cierres y aperturas repetidos del relé cuando la señal fluctúa alrededor de un único valor.

Justificación:
Establecer dos umbrales de activación diferentes (700 para encender y 600 para apagar) implementa una técnica conocida como histéresis. Esto evita que, si la señal del sensor sufre pequeñas fluctuaciones o ruido eléctrico alrededor de un único valor límite, el relé comience a conmutar destructivamente (abriendo y cerrando de forma repetitiva y muy rápida), lo cual desgastaría y dañaría los contactos mecánicos.

## Pregunta 19

Respuesta Correcta: D) el pin 2 lee nivel LOW y el sketch activa el buzzer con la función tone().

Justificación:
Al estar el circuito configurado con una resistencia pull-down, el pin lee nivel HIGH (5V) mientras la puerta está cerrada porque el interruptor está haciendo contacto directo con la fuente. En el momento en que la puerta se abre, el interruptor se separa y la resistencia pull-down jala el pin directamente hacia tierra, haciendo que el pin 2 lea un nivel LOW (0V). Al detectar este cambio a LOW (apertura), el sketch activa de inmediato la alerta acústica mediante la función tone().

## pregunta 20

​Respuesta: B) La afirmación es verdadera, mientras que la razón es una proposición falsa.

​Justificación: La función tone() sí sirve para que un buzzer emita sonido. Sin embargo, el sonido no se produce dejando la corriente encendida fija en HIGH, sino haciendo que la energía suba y baje miles de veces por segundo para crear una vibración (como la membrana de un parlante). Por eso la afirmación es cierta, pero la explicación de cómo funciona es falsa.
  
## ​PREGUNTA 21

​Respuesta: A) disminuye porque la LDR aumenta su resistencia y la resistencia fija recibe menos tensión.

​Justificación: La LDR es un sensor que se "frena" u opone más al paso de la electricidad entre más oscuro esté el entorno. En el circuito armador (divisor de voltaje), al haber más oscuridad, el sensor ataja casi toda la energía y le deja llegar muy poca señal al pin A0 del Arduino, haciendo que la lectura numérica baje.

## ​PREGUNTA 22

​Respuesta: A) 2 LEDs.

​Justificación: La función map() sirve para convertir una escala en otra, como una regla de tres proporcional. Convierte la escala del sensor (0 a 1023) a la escala de los 5 LEDs (0 a 5). Al hacer el cálculo para el valor 450, la proporción exacta da 2.19. Como el sistema desecha la parte decimal y solo toma números enteros, el resultado final es 2 LEDs encendidos.

## ​PREGUNTA 23

​Respuesta: B) II, I, III, IV.

​Justificación: Sigue el orden lógico de cualquier semáforo real por seguridad vial: primero el vehículo recibe la advertencia en amarillo para frenar (II), luego se le pone el freno total en rojo (I), de inmediato se le da paso al peatón en verde (III), y al terminar el tiempo, el peatón vuelve a rojo mientras el carro recupera el verde (IV).

## ​PREGUNTA 24

​Respuesta: B) La placa se reinicia al abrirse el puerto serie y tarda unos segundos en iniciar el sketch.

​Justificación: Las placas Arduino están diseñadas para reiniciarse automáticamente apenas una computadora abre comunicación con ellas por USB. Si el programa de Python intenta enviar la orden de encender el LED en ese mismísimo milisegundo, la señal se pierde en el aire porque el Arduino apenas está "despertando" y arrancando su memoria.

## ​PREGUNTA 25

​Respuesta: D) Ejecutar core update-index y core install con el paquete arduino:avr.

​Justificación: El sistema avisa que no sabe cómo preparar el programa porque le faltan las "instrucciones del traductor" específicas para el cerebro del Arduino UNO. Para corregirlo, hay que actualizar el catálogo de paquetes e descargar la herramienta de compilación oficial para esa familia de chips (arduino:avr).