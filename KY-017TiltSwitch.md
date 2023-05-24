# KY-017 Tilt Switch

## OBJETIVO:

Mostrar en la consola de Thonny si el sensor esta activado realizando inclinaciones

## CÓDIGO
```python
from machine import Pin
import time

TiltSensor = Pin(17, Pin.IN)

while True:
    value = TiltSensor.value()
    print(value, end = " ")
    if  value== 0:
        print("The switch is turned on")
    else:
        print("The switch is turned off")
    time.sleep(1)      
```

## PRUEBAS

https://github.com/OscarTec98/37Sensores/assets/124211870/ec6ec9ee-9dfa-4383-b2ea-ce7d5682a52f

## CONCLUSIONES
Un sensor muy utilizado sobretodo en dispositivos moviles, ya que es capaz de detectar el nivel de inclinacion que le damos
