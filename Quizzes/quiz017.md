# Quiz 017

![Quiz 017  World Lenght](https://user-images.githubusercontent.com/112055062/197686183-5569b57a-ff0f-42c4-8631-44e969cad798.jpg)

```.py
def averageLength(given:list)->int:
    list_amount = len(given)
    sum = 0
    for i in given:
        sum = sum + len(i.strip())
    out = sum/list_amount
    print(out)

out = averageLength(given=["hello   ","main",])
```

## Results:

<img width="739" alt="Quiz017" src="https://user-images.githubusercontent.com/112055062/197686491-eb9699b0-a5e6-41b7-b255-dfda2f672dd2.png">

## Flowchart:

![quiz017 flowchart](https://user-images.githubusercontent.com/112055062/197688026-7d9c4603-56c8-46c2-9cba-d51459153c44.jpg)

## Truth table

![IMG_ABC567097B62-1](https://user-images.githubusercontent.com/112055062/202136907-b7da835f-568b-4e65-84cc-e880e718cfc3.jpeg)

