# Quiz 32

![2022  Quizzes (11)](https://user-images.githubusercontent.com/112055062/211053823-aae3e5fb-7c04-44c9-a53c-f3a5370bd77e.jpg)

## Code 
(Could not finish graph 3 because server was not working)

```.py
import requests
import matplotlib.pyplot as plt
import numpy as np

req = requests.get('http://192.168.6.142/readings')
data = req.json()
readings = data['readings'][0]

temp_9=[]
for sample in readings:
    if sample['sensor_id']==9:
        temp_9.append(sample['value'])
print(len(temp_9))
print(temp_9)

x_9 = []
for i in range(len(temp_9)):
    x_9.append(i)

size_window = 12
temp_9_smth = []
x_9_smth = []
for i in range(0,len(x_9),size_window):
    values = temp_9[i:i+size_window]
    temp_9_smth.append(sum(values)/size_window)
    x_9_smth.append(i)
x_9_smth.pop() # remove last value
temp_9_smth.pop()

#sensor 10
temp_10=[]
for sample in readings:
    if sample['sensor_id']==10:
        temp_10.append(sample['value'])
print(len(temp_10))
print(temp_10)

x_10 = []
for i in range(len(temp_10)):
    x_10.append(i)

temp_10_smth = []
x_10_smth = []
for i in range(0,len(x_10),size_window):
    values = temp_10[i:i+size_window]
    temp_10_smth.append(sum(values)/size_window)
    x_10_smth.append(i)
x_10_smth.pop() # remove last value
temp_10_smth.pop()

plt.subplot(2,1,1) #sensor9
plt.plot(x_9_smth,temp_9_smth)

plt.subplot(2,1,2) #sensor10
plt.plot(x_10_smth,temp_10_smth)

plt.show()
```

## What are the three main operators used in boolean logic?
The three main operators are AND, OR, and NOT

![IMG_D565D6D93860-1](https://user-images.githubusercontent.com/112055062/211055249-4da60b01-f278-47f9-b004-b9255e561eae.jpeg)
