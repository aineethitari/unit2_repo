# Quiz 27

![2022  Quizzes (6)](https://user-images.githubusercontent.com/112055062/204743870-9f314472-802f-4e79-b076-09646dabd2f5.jpg)

## Code
```.py
import matplotlib.pyplot as plt
import numpy as np

sensorA = [16, 24, 24, 9, 23, 26, 26, 23, 25, 14]
sensorB = [2, 19, 25, 10, 11, 24, 17, 7, 24, 17]
sensorC = [15, 11, 24, 21, 6, 2, 18, 27, 1, 16]

x = []
for i in range(len(sensorA)):
    x.append(i)

figure = plt.figure(figsize=(5,8))
plt.subplot(2,1,1)
plt.plot(x,sensorA, color="#8e7cc3")
plt.plot(x,sensorB, color="#ea9999")
plt.plot(x,sensorC, color="#6aa84f")
plt.legend(['sensorA','sensorB', 'sensorC'])

mean = []
standard_dev = []
minimum = []
maximum = []
for i in range(len(sensorA)):
    data = [sensorA[i], sensorB[i], sensorC[i]]
    minimum.append(min(data))
    maximum.append(max(data))
    mean.append(np.mean(data))
    standard_dev.append(np.std(data))

plt.subplot(2,1,2)
plt.fill_between(x,maximum,minimum, alpha=.5,linewidth=0,color="#a7e4d1")
plt.errorbar(x, mean, standard_dev, fmt="o")
plt.show()
```

## Result

<img width="428" alt="Quiz27 graph" src="https://user-images.githubusercontent.com/112055062/208592897-2cb8c5a1-a504-49da-b246-0db1ef551a52.png">

