# KY-006 Passive Buzzer

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

https://github.com/OscarTec98/37Sensores/assets/124211870/9cdd84e0-0dca-497d-a04b-b373663ad8f4

## CONCLUSIONES
Fue muy facil hacer encender el buzzer y es algo que encontramos comunmente en nuestra vida cotidiana
