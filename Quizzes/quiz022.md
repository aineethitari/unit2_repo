# Quiz 22

![Quiz 022  Data Simulation](https://user-images.githubusercontent.com/112055062/202103084-f336dadc-be69-43f7-83cf-7b5b4e063876.jpg)

## Code

```.py
import random
random.seed(1234)

def produce(n:int,m:int,s:int)->str:
    print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")
    x_out = []
    y_out = []
    for _ in range(n):
        x = random.randint(0, 100)
        x_out.append(x)
        y = x ** (1/2*((m/s)**2))
        y_out.append(y)
        y_str = f"{y:.2f}"
        print(f"|{str(x).center(10)}|{y_str.center(10)}|")

    return y_out, x_out
```

## Result

<img width="366" alt="Quiz022 code" src="https://user-images.githubusercontent.com/112055062/202104081-1d6e2d90-9b67-47fc-a49d-d73385f69d1f.png">

## Proof that A(A+B) = A

![image](https://user-images.githubusercontent.com/112055062/202103768-ce6bcea9-8ab5-41e4-b08c-5e0ac068c27c.png)

