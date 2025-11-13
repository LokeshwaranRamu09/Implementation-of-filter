# EXP NO -5 : Implementation-of-filter
### NAME : LOKESHWARAN.R 
### REG NO : 212224220053




## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

 
Import the required libraries.
### Step2

Convert the image from BGR to RGB.
### Step3

Apply the required filters for the image separately.
### Step4

Plot the original and filtered image by using matplotlib.pyplot
### Step5

End the program.
## Program:
EXP NO -5 : Implementation-of-filter
### Developed By   :LOKESHWARAN.R
### Register Number:212224220053
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ocean.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()


```
ii) Using Weighted Averaging Filter
```Python

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()



```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()




```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
</br>
</br>
</br>
<img width="758" height="267" alt="image" src="https://github.com/user-attachments/assets/f8880760-844a-4eee-8f54-f5602746930d" />

ii)Using Weighted Averaging Filter
</br>
</br>
</br>
</br>
</br>
<img width="792" height="300" alt="image" src="https://github.com/user-attachments/assets/5d2fa40b-2a53-4a0e-96fb-6cbe0effaf81" />

iii)Using Gaussian Filter
</br>
</br>
</br>
</br>
</br>
<img width="756" height="273" alt="image" src="https://github.com/user-attachments/assets/37655353-e07a-4212-960b-8ac9b93f9f09" />

iv) Using Median Filter
</br>
</br>
</br>
</br>
</br>
<img width="837" height="282" alt="image" src="https://github.com/user-attachments/assets/cf423ac2-de27-4da1-b4af-cad4c33c61bd" />

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
</br>
</br>
<img width="787" height="282" alt="image" src="https://github.com/user-attachments/assets/ecbeab61-6f6b-4127-af5c-eba169a1402d" />

ii) Using Laplacian Operator
</br>
</br>
</br>
</br>
</br>
<img width="716" height="270" alt="image" src="https://github.com/user-attachments/assets/2f9ce1f1-0769-41f9-95ad-48640db0bc6d" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
