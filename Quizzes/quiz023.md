# Quiz 23

![2022  Quizzes](https://user-images.githubusercontent.com/112055062/202105045-e3ebc0e2-d148-48de-af63-d27706e4fb9e.jpg)

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

data_y, data_x = produce(n=10, m=5, s=2)
from matplotlib import pyplot as plt

plt.plot(data_x,data_y,color = "r", marker = "o")
plt.xlabel("x")
plt.ylabel("y")
plt.ylabel("$y=x^{1/2(m/s)^2}$")
plt.show()
```

## Result

<img width="650" alt="quiz023 graph and result" src="https://user-images.githubusercontent.com/112055062/202105566-f2ccd2c9-b988-4024-90fd-40323e86afeb.png">

## Truth table

![Quiz23 Truth table](https://user-images.githubusercontent.com/112055062/202107323-c17df393-1427-44ac-9ea3-9a707eeac946.jpeg)

