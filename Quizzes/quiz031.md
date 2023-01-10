# Quiz 31

![2022  Quizzes (10)](https://user-images.githubusercontent.com/112055062/211050260-6f12a6af-38f1-42c3-a994-72cb14450c74.jpg)

## Code
import requests
import matplotlib.pyplot as plt
import numpy as np

req = requests.get('http://192.168.6.142/readings')
data = req.json()
readings = data['readings'][0]

#get only temp
samples = []
temp = []

for sample in readings:
    if sample['sensor_id']==5:
        temp.append(sample['value'])

#slice temp to only region of iinterest
temp = temp[610:800]

for i in range(len(temp)):
    samples.append(i)

plt.scatter(samples,temp)


#linear model for sl
m,b = np.polyfit(samples,temp,1)
x_line = [0,len(temp)]
y_line = []
for i in x_line:
    y_line.append(m*i+b)
plt.plot(x_line,y_line,'black')


#quadratic line
a1,a2,a3 = np.polyfit(samples,temp,2)

plt.show()
y_model_quad = []
for i in samples:
    y_model_quad.append(a1*(i)**2 + a2*(i) + a3)

plt.plot(samples,y_model_quad)
plt.show()

## Results 
Could not get results because server was not working

