# Quiz 20

![Quiz 020  Truth](https://user-images.githubusercontent.com/112055062/201151213-4b8c1e43-ac37-405a-8522-f924c3d99651.jpg)

## Code

```.py
def get_truth()->str:
    title = print(f"| A | B | C |")
    C = True
    B = True
    A = True

    for i in range(8):
        C = not C
        if i%2==0:
            B = not B
        if i%4 == 0:
            A = not A
        print(f"| {int(A)} | {int(B)} | {int(C)} |")

table = get_truth()
```

## Image of the result

<img width="522" alt="quiz020 result" src="https://user-images.githubusercontent.com/112055062/201151523-e71c176b-f171-40a6-8dbb-38ea4d1019c2.png">

## Truth table and circuit
Light = S1S2+(S2+S3(notS1))S1 

![IMG_A342967EA854-1](https://user-images.githubusercontent.com/112055062/202077555-eca9c910-15ba-4619-81b1-0654111d0aa0.jpeg)

![Quiz20 Circuit](https://user-images.githubusercontent.com/112055062/202077317-256dd9b0-320a-4346-a981-867fac2c2d75.jpeg)
