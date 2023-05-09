# KY-012 Buzzer

## OBJETIVO:
Encender el buzzer utilizando Raspberry Pi Pico

## CÓDIGO
```python
from machine import Pin
import time

Buzzer = Pin(14, Pin.OUT)

while True:
    Buzzer.on()
    time.sleep(1)
    Buzzer.off()
    time.sleep(1)
```

## PRUEBAS

## CONCLUSIONES
Fue muy facil hacer encender el buzzer y es algo que encontramos comunmente en nuestra vida cotidiana
