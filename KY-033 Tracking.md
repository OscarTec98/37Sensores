## CODIGO
```python
#Se importan las librerías de micropython para la configuración del sensor.
from machine import Pin
import time

#Se configura el pin GPIO3 como entrada digital
sensor = Pin(3, Pin.IN, Pin.PULL_UP)

#Entra en el loop infinito donde se lee el estado y muestra un mensaje en consola dependiendo el valor obtenido
while True:
    if sensor.value() == 0:
        print("0   Blanco")
    else:
        print("1   Negro")
        #Se espera 0.1 segundos para realizar otra lectura
    time.sleep(0.1)
```