¿Qué es? <br>
El sensor Hall magnético analógico KY-035 es un módulo que reacciona en presencia de un imán. Puede medir la polaridad y la fuerza relativa de un campo magnético.

¿Para qué sirve? <br>
El módulo del sensor Hall es un interruptor muy sensible que se activa mediante un campo magnético. Puede ser activado por un imán natural o un electroimán. Las altas tasas de respuesta permiten tomar lecturas incluso a frecuencias de 100 kHz. Los usos más populares son la detección de proximidad para detectar velocidades de objetos giratorios o como sensores de puertas. Debido a la naturaleza de la detección (sin contacto), el módulo del sensor hall es muy duradero y no se desgasta con el uso. Los sensores generalmente vienen sin enclavamiento, sin embargo, las versiones con enclavamiento son posibles (el sensor mantiene el estado después de que se retira el imán hasta que se introduce la polaridad opuesta).


## Codigo

```python
import RPi.GPIO as GPIO

GPIO.setmode(GPIO.BCM)
GPIO_PIR = 24
print "KY-003 Module Test (CTRL-C = exit)"

GPIO.setup(GPIO_PIR, GPIO.IN, pull_up_down = GPIO.PUD_UP)
def printFunction(channel):
    print("Detected")
    GPIO.add_event_detect(GPIO_PIR, GPIO.RISING, callback=printFunction)
try:
    while True :
        Current_State = GPIO.input(GPIO_PIR)
        except KeyboardInterrupt:
GPIO.cleanup()
```

## Resultado
![](./Imagenes/Circuito 3.jpeg)
