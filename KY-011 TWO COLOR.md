# KY-026 Flame
###INSTITUTO TECNOLOGICO DE TIJUANA
###INGENIERIA EN SISTEMAS COMPUTACIONALES
###MATERIA: SITEMAS PROGRAMABLES
###ALUMNO: VALADEZ MELENDEZ CRUZ EDUARDO

## OBJETIVO:

Encendido del LED con dos tonalidades de colores

## CÓDIGO
```python
from machine import Pin
import time

led_pins = [16,17]
leds = [Pin(led_pins[0],Pin.OUT),Pin(led_pins[1],Pin.OUT)]
delay_t = 0.1
while True:
    for led in leds:
        led.high()
        time.sleep(delay_t)
        led.low()
        time.sleep(delay_t)
```

## PRUEBAS

![](./Imagenes/)

![](./Imagenes/)

## CONCLUSIONES
