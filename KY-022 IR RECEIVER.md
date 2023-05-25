Sensor Ky-022 Receptor

INFORMACIÓN

El Sensor Receptor Infrarrojo IR es un módulo KY-022 que esta construido de un receptor IR TL1838, el cual reacciona a la luz infrarroja de 38 KHz y funciona en conjunto con el emisor KY-005.

Esté modulo KY-022 se utilizan en muchos equipos domésticos, para controles remoto universales, utiliza la codificación NEC, y funciona muy bien principalmente en vehículos con MP3, marco de fotos digital, iluminación equipada.

Nota: Es posible ver la luz del mando mirando el LED infrarrojo con una cámara digital, por ejemplo del celular. La luz del led se muestra como un resplandor morado. Podríamos usar este método para detectar si el mando funciona correctamente.

![imagen](Imagenes/KY-022A.png)

<h2> Diagrama </h2>

## Codigo
```python
from machine import Pin
import time

pico_led = Pin(25, Pin.OUT)
ir = Pin(15, Pin.OUT)
receiver = Pin(16, Pin.IN)


while True:
    ir.value(1)
    
    #Cuando el sensor recibe un valor se prende el led de la Pico
    if(receiver.value() == 1):
        pico_led.value(1)
    else:
        pico_led.value(0)
        
    time.sleep(1)
   ```
## Resultados
![imagen](Imagenes/KY-022C.jpg)
