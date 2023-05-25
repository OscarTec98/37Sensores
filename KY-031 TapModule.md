Sensor Ky-031 Tap module

INFORMACIÓN

¿Qué es? 
El Módulo KY-031 es mejor conocido como sensor de Impacto, este sensor tiene la capacidad de percibir los impactos que este o una superficie sujeto a este pueda recibir. Trabaja como contacto normalmente abierto y mandando un “1” lógico a través de su terminal de señal en el instante que recibe el contacto físico.

¿Para qué sirve?
Este es útil para detectar situaciones de colisión o de impacto, con esta información podemos tomar decisiones de inhabilitación o alguna otra acción por medio de un microcontrolador.

![imagen](Imagenes/KY-031A.png)

<h2> Diagrama</h2>

## Codigo

```python
import time
from machine import Pin

pico_led = Pin(25, Pin.OUT)
knock = Pin(16, Pin.IN)

while True:
    if(knock.value() == 1):
        pico_led.value(1)
        time.sleep(2)
    else:
        pico_led.value(0)
        time.sleep(2)
```

## Resultado
![imagen](Imagenes/KY-031B.jpg)
