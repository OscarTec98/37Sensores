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


https://github.com/OscarTec98/37Sensores/assets/124211870/a47da52f-e93a-4aee-be67-028454c72502


## CONCLUSIONES
Fue muy facil hacer encender el buzzer y es algo que encontramos comunmente en nuestra vida cotidiana
