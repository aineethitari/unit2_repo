# Quiz 19

![Quiz 019  L3tt3r](https://user-images.githubusercontent.com/112055062/202072448-c6f11661-21a3-4d02-a229-233d1c606e51.jpg)

## Code

```.py
def get_l3tt3r(msg)->str:
    out=""
    for letter in msg:
        if letter == "a":
            out += "4"
        elif letter == "e":
            out += "3"
        elif letter == "i":
            out += "1"
        elif letter == "o":
            out += "0"
        elif letter == " ":
            out += "_"
        else:
            out += letter
    print(out)
    return out

case1 = get_l3tt3r(msg="Hello World")
```

## Results

<img width="337" alt="quiz19 result" src="https://user-images.githubusercontent.com/112055062/202181216-5689d273-4a56-4ec2-87b2-7bbe0be7ef66.png">

## Circuit

![Quiz019 Circuit](https://user-images.githubusercontent.com/112055062/202074857-6270e9eb-752f-4e1f-aa4e-7e1526402da6.jpeg)
