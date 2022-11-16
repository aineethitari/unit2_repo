# System Diagrams Task2.1

![System Diagrams unit 2](https://user-images.githubusercontent.com/112055062/202066122-17cfe507-e229-4e69-b60c-9658c3790cf5.jpg)

## List of Materials
1. Breadboard 1
2. Red LED 1
3. Green LED 1
4. Yellow LED 1
5. Resistors 3
6. USB Cable
7. Arduino UNO

## Code

```.py
from pyfirmata import Arduino
import time

board = Arduino('/dev/cu.usbserial-14220')
print("Communication Successfully started")

while True:
    C = True
    B = True
    A = True

    for i in range(8):
        C = not C
        if i % 2 == 0:
            B = not B
        if i % 4 == 0:
            A = not A
        board.digital[5].write(int(A))
        board.digital[9].write(int(B))
        board.digital[12].write(int(C))
        time.sleep(3)
```

## Video Results

https://drive.google.com/file/d/1rSoZcw3huYkyTRlHo4U-QOuEG0N4Gy_x/view?usp=sharing

