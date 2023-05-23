# KY-004 Button

## OBJETIVO:
Muestra un mensaje en consola dependiendo si se presiona o no el botón

## CÓDIGO
```python
  # Librerías necesarias de Micropython
  import machine
  import time
  # Instrucción que configura el componente en el pin GPIO18 
  button_pin = machine.Pin(18, machine.Pin.IN, machine.Pin.PULL_UP)
  # Estructura ciclica infinita que muestra en consola un mensaje 
  # dependiendo si se está presionando el botón o no.
  while True:
    if button_pin.value() == 0:
        print("BOTON PRESIONADO")
    else:
        print("PRESIONA EL BOTON!")
    time.sleep(1)
```

## PRUEBAS


## CONCLUSIONES
Es bastante sencillo hacer funcionar el botón
