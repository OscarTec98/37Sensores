# KY-002 Shock

## OBJETIVO:
Lograr que el sensor identifique si hay una vibracion o no usando Raspberry Pi Pico

## CÓDIGO
```python
import machine
import utime

pin_shock = machine.Pin(16, machine.Pin.IN)

while True:
    if pin_shock.value() == 1:
        print("¡Se detectó una vibración o golpe!")
    else:
        print("Sin vibraciones o golpes detectados.")

    utime.sleep(1) 
```

## PRUEBAS

https://github.com/OscarTec98/37Sensores/assets/124211870/ed9fe6c2-df66-45a8-86c8-aee6bab2a0bc

## CONCLUSIONES
Logramos crear un programa para que nuestra Raspberry detecte cuando hay algun movimiento o vibracion
