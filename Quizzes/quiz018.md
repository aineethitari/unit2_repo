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

![quiz018 flowchart](https://user-images.githubusercontent.com/112055062/198269794-9d56c96b-5d27-4ada-a1da-bf66bca5be33.jpg)

## Image of the result

<img width="540" alt="Quiz018 results" src="https://user-images.githubusercontent.com/112055062/198269809-721bdc36-9e4a-4720-b3f7-04dd4e4235da.png">

## HL: Create truth table

![quiz018 truth table](https://user-images.githubusercontent.com/112055062/198266222-13207a52-d683-4583-9913-bd94893e0a92.jpeg)
