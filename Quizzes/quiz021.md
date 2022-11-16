# Quiz 21

![2022  Quizzes (3)](https://user-images.githubusercontent.com/112055062/202182058-aebf96e7-c699-4747-8a6c-33f5e65fa4c3.jpg)

## Code

```.py
def get_truth()->str:
    title = print(f"| A | B | C | AB + not B + notB C |")
    C = True
    B = True
    A = True
    for i in range(8):
        C = not C
        if i%2==0:
            B = not B
        if i%4 == 0:
            A = not A
        out = (A and B) or not B or (not(C and B))
        out_str = str(int(out)).center(19)
        print(f"| {int(A)} | {int(B)} | {int(C)} | {out_str} |")

table = get_truth()
```

## Result

<img width="381" alt="quiz21 result" src="https://user-images.githubusercontent.com/112055062/202181688-5aece1b9-e259-4843-b14f-f0b0c92378cc.png">

## Truth table and circuit

![IMG_44C408DF78DF-1](https://user-images.githubusercontent.com/112055062/202183020-124e9645-22a3-4ba7-ba34-a1581c6481c7.jpeg)
