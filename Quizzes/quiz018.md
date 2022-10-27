# Quiz 18

![quiz018 problem](https://user-images.githubusercontent.com/112055062/198265715-431e1903-e85b-42a5-9806-fef6d8569dd2.jpg)

## Code 

```.py
def numberMatches(l:int, s:int)->int:
    s_meter = s/100
    out = (l/s_meter) * (1/5)
    import math
    out = math.ceil(out)
    print(out)

matches1 = numberMatches(l=100,s=100)
matches2 = numberMatches(l=250,s=110)
matches3 = numberMatches(l=500,s=150)
matches4 = numberMatches(l=12345,s=123)
```

## Flowchart

## Image of the result

## HL: Create truth table

![quiz018 truth table](https://user-images.githubusercontent.com/112055062/198266222-13207a52-d683-4583-9913-bd94893e0a92.jpeg)