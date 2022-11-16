# System Diagrams Task2.1

![System Diagrams unit 2](https://user-images.githubusercontent.com/112055062/202066122-17cfe507-e229-4e69-b60c-9658c3790cf5.jpg)

## List of Materials
1. Breadboard 1
2. LED 3
3. Resistors 3
4. Wires 8
5. Arduino UNO 1
6. USB Cable 1
7. USB to USB-C adapter

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

# Systems Diagrams Task 2.2

![System Diagrams unit 2 copy](https://user-images.githubusercontent.com/112055062/202067569-89f6049e-4ec1-4638-a40a-27c7f874edc0.jpg)

## List of Materials
1. Breadboard 1
2. Button 2
3. LED 1
4. Resistors 3
5. Arduino UNO 1
6. Wire 8
8. USB Cable 1
9. USB to USB-C adapter

## Code

```.py
import pyfirmata
from pyfirmata import Arduino
import time

board = Arduino('/dev/cu.usbserial-1420')
print("Communication Successfully started")

it = pyfirmata.util.Iterator(board)
it.start()

buttonA = board.digital[9]
buttonA.mode = pyfirmata.INPUT
button_state = False

LED = board.digital[2]
LED.write(0)
while not button_state:
    time.sleep(0.01)
    print("waiting for the button to be pressed")
    button_state = buttonA.read()

if button_state == True:
    print("Button was pressed ")
    button_state = buttonA.read()
    print("Button was pressed, blinking 5 times and then exiting")
    for i in range(5):
        LED.write(1)
        time.sleep(1)
        LED.write(0)
        time.sleep(1)
```

## Video of the result

https://drive.google.com/file/d/1L22dqk7FxSPSqz_dedatn0zpTmmuxsdO/view?usp=sharing
