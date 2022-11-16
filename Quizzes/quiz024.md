# Quiz 24

![2022  Quizzes (1)](https://user-images.githubusercontent.com/112055062/202108079-6cd5f190-8024-4d77-8a7c-42d2d6ce0483.jpg)


## Code

```.py
from matplotlib import pyplot as plt
n=100
x = []
y = []
step = -10
for i in range(n):
    x.append(step)
    step += 0.2
    y_temp = 2*((x[-1]+5)**2)
    y.append(y_temp)

plt.plot(x, y)
plt.show()
```

## Result

<img width="464" alt="quiz024 graph" src="https://user-images.githubusercontent.com/112055062/202108165-0fed6c0d-e153-47ae-8876-33d66e9e9ec8.png">

## Circuit

![Quiz024 circuit](https://user-images.githubusercontent.com/112055062/202110239-1d0f1a19-b65e-494b-939f-1862e61ed3ef.jpeg)
