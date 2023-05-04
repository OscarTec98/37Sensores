# KY-026 Flame

## OBJETIVO:

Mostrar En Consola si se detecto o no una llama

## CÓDIGO
```python
from machine import Pin
import utime

flame_sensor = Pin(16, Pin.IN)
utime.sleep(2)

while True:
   if flame_sensor.value() == 1:
       print("Flame Detected")
       utime.sleep(3)
   else:
       print("No Flame")
       utime.sleep(1)
utime.sleep(0.1)
```

## PRUEBAS

![](./Imagenes/)

![](./Imagenes/)

![](./Imagenes/)

## CONCLUSIONES


