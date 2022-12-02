# Quiz 30

## Code
```.py
import matplotlib.pyplot as plt
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
x = []
for i in range(len(h)):
    x.append(i)

size_window = 4
h_smth = []
x_smth = []
for i in range(0,len(h),size_window):
    values = h[i:i+size_window]
    h_smth.append(sum(values)/size_window)
    x_smth.append(i)

h_smth_50 = []
x_smth_50 = []
for i in range(0,len(h),size_window//2):
    values = h[i:i+size_window]
    h_smth_50.append(sum(values)/size_window)
    x_smth_50.append(i)


plt.subplot(3,1,1)
plt.plot(x,h,'o-')

plt.subplot(3,1,2)
plt.plot(x_smth,h_smth,'o-')

plt.subplot(3,1,3)
plt.plot(x_smth_50[0:-1],h_smth_50[0:-1],'o-')

plt.ylabel("Relative humidity")
plt.xlabel("Samples")
plt.show()
```

## Result

<img width="637" alt="Quiz030" src="https://user-images.githubusercontent.com/112055062/205202922-7d2c651f-699e-4a6b-a1eb-16b7409ae0ce.png">
