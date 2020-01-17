```
from machine import UART
import time
uart = UART(1, 9600)                         # init with given baudrate
uart.init(9600, bits=8, parity=None, stop=1) # init with given parameters

while True:
    if uart.any():
        cmd = uart.read()
        uart.write(cmd)
    time.sleep_ms(50) 
```
