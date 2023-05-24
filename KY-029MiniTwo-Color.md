# KY-029 Mini Two Color

## OBJETIVO:
Lograr que el led encienda en sus 2 colores posibles utilizando Raspberry Pi Pico

## CÓDIGO
```python
from machine import Pin
import time

led_pins = [16,17]
leds = [Pin(led_pins[0],Pin.OUT),Pin(led_pins[1],Pin.OUT)] 
delay_t = 0.1 
while True: 
    for led in leds: 
        led.high() 
        time.sleep(delay_t) 
        led.low()
        time.sleep(delay_t) 
```

## PRUEBAS

https://github.com/OscarTec98/37Sensores/assets/124211870/f006c196-74ad-492c-a5d4-fc6e1c1fe9a2

## CONCLUSIONES
Se logro encender el led en sus 2 posibles colores (Rojo y Verde)
