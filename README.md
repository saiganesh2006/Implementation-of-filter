# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Install the open cv by using pip install opencv-python

### Step2:
Import cv2 for reading and changing it smooth and sharpen image

### Step3:
Import numpy for give the width and size of a image

### Step4:
import matplotlib.pyplot for display the image.


## Program:
```
### Developed By   : D.B.V.SAI GANESH
### Register Number: 212223240025
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thar.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal = np.ones((11,11),np.float32)/121
img2 = cv2.filter2D(img1,-1,kernal)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')

```
ii) Using Weighted Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thar.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
img2 = cv2.filter2D(img1,-1,kernal2)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')

```
iii) Using Gaussian Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thar.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur =  cv2.GaussianBlur(src=img1,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title('Filtered')
plt.axis('off')

```

iv) Using Median Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thar.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=img1,ksize=11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(median)
plt.title('Filtered')
plt.axis('off')



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thar.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img3)
plt.title('Filtered')
plt.axis('off')

```
ii) Using Laplacian Operator
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thar.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)
new_img = cv2.Laplacian(img1,cv2.CV_64F)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(new_img)
plt.title('Filtered')
plt.axis('off')

```

## OUTPUT:
### 1. Smoothing Filters
</br>

## i) Using Averaging Filter

![image](https://github.com/saiganesh2006/Implementation-of-filter/assets/145742342/74a624f5-4c07-4405-a53e-c643cd3a8af5)

## ii) Using Weighted Averaging Filter
![image](https://github.com/saiganesh2006/Implementation-of-filter/assets/145742342/24eea796-d06d-4a52-922e-cb4486afeb70)

## iii) Using Gaussian Filter
![image](https://github.com/saiganesh2006/Implementation-of-filter/assets/145742342/1e5af0ab-4b72-4fee-952e-7541c6817031)


## iv) Using Median Filter
![image](https://github.com/saiganesh2006/Implementation-of-filter/assets/145742342/25a4f27c-406b-4f8a-b963-1c0a7b41f717)

### 2. Sharpening Filters
</br>

## i) Using Laplacian Kernal
![image](https://github.com/saiganesh2006/Implementation-of-filter/assets/145742342/daa58edf-ef23-4528-b8f8-68d1eac93b82)


## ii) Using Laplacian Operator
![image](https://github.com/saiganesh2006/Implementation-of-filter/assets/145742342/1327c2d3-7af3-492d-b177-afa071dc0f23)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
