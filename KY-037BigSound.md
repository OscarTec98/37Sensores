# KY-037 Big Sound

## OBJETIVO:

Mostrar la intensidad de sonido detectada por el sensor Big Sound en la consola de Thonny

## CÓDIGO
```python
from machine import Pin, ADC
from time import sleep

bigS = Pin(16, Pin.OUT, value=0)

sensor = ADC(0)
        
while True:
    value = sensor.read_u16()
    print(value)
    sleep(1)        
```

## PRUEBAS

![](./Imagenes/bigSound.gif)

## CONCLUSIONES
Interesante ver como los sensores son capaces de detectar sonidos. Este tipo de sensores tienen muchas aplicaciones en la vida diaria.
