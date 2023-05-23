# KY-040 Rotay Encoders

## OBJETIVO:
Obtener el valor que esta mostrando el Rotay Encoders usando Raspberry Pi Pico

## CÓDIGO
```python
from rotary_irq_rp2 import RotaryIRQ
from machine import Pin, I2C
from ssd1306 import SSD1306_I2C
from oled import Write, GFX, SSD1306_I2C
from oled.fonts import ubuntu_mono_15, ubuntu_mono_20
import utime

WIDTH =128
HEIGHT= 64
i2c=I2C(0,scl=Pin(17),sda=Pin(16),freq=200000)
oled = SSD1306_I2C(WIDTH,HEIGHT,i2c)
rotary = RotaryIRQ(14, 15)

def mostrarTexto(texto):
    oled.fill(0)
    write20 = Write(oled, ubuntu_mono_20)
    oled.text(texto, 0, 0)
    oled.show()

mostrarTexto("Iniciando...")
current_val = 0  
while True:
    new_val = rotary.value()  
    
    if current_val != new_val:  
        print('Encoder value:', new_val)  
        mostrarTexto("Valor: " + str(new_val))
        current_val = new_val  
```

## PRUEBAS

https://github.com/OscarTec98/37Sensores/assets/124211870/543a0f72-4fe0-406e-b79d-af6cbc89f54c

## CONCLUSIONES
