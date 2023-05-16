# KY-018 Photoresistor

## OBJETIVO:

Mostrar la intensidad de luz detectada por una fotorresistencia

## CÓDIGO
```python
from machine import ADC, Pin
from time import sleep

photoPIN = 26

def readLight(photoGP):
    photoRes = ADC(Pin(26))
    
    light = photoRes.read_u16()
    light = round(light/65535*100,2)
    return light

while True:
    print("light: " + str(readLight(photoPIN)) + "%")
    sleep(1)        
```

## PRUEBAS

![](./Imagenes/fotorresistencia.gif)

## CONCLUSIONES
Un sensor muy utilizado sobretodo en los aparatos electronicos como celulares o computadoras, ya que estos tienen una configuracion para ajustar el brillo de pantalla segun que tanta luz haya donde estamos

