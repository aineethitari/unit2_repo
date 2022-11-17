# Quiz 26

## Code
```.py
import matplotlib.pyplot as plt
import numpy as np
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
samples = []
for i in range(len(h)):
    samples.append(i)
plt.plot(samples, h, linestyle="none", marker="v")
plt.ylabel("Relative Humidity (%)")
plt.xlabel("Samples")
plt.title("Graph of Relative Humidity")


m,b = np.polyfit(samples,h,1)
x = []
y = []
for i in [0,30]:
    x.append(i)
    temp_y = m * i + b
    y.append(temp_y)

plt.plot(x,y)

plt.show()
```

## Result
