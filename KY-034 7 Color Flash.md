¿Qué es? <br?
El LED parpadea automáticamente cuando se aplica energía y la luz cambia de color con cada parpadeo. Dicho led es modelo  YB-3120B4PnYG-PM que posee una lente tipo “luz antiniebla blanco” y maneja un voltaje estándar de 3 a 5 Volts de corriente directa.¿Para qué sirve?

¿Para qué sirve? <br>
Este es útil para detectar situaciones de colisión o de impacto, con esta información podemos tomar decisiones de inhabilitación o alguna otra acción por medio de un microcontrolador.


## Codigo

```python
from machine import Pin, Timer

inbuiltLed = 25

led = Pin(inbuiltLed, Pin.OUT)

timer = Timer()

def ledblink(timer):

    led.toggle()

timer.init(freq=2.5, mode=Timer.PERIODIC, callback=ledblink)
```

## Resultado
![Imagen](./Imagenes/Circuito 2.jpeg)
