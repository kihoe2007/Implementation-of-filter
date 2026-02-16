# Implementation-of-filter
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
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By   :Kishore S M
### Register Number:212224230131
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Kishore.jpeg")
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
</br><img width="784" height="482" alt="image" src="https://github.com/user-attachments/assets/9ff9dcb1-37c6-47b6-a8eb-1e7f3edc971d" />

</br>
</br>
</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br><img width="1053" height="641" alt="image" src="https://github.com/user-attachments/assets/4abd5dd0-a9b2-4d03-b8e0-c61fcac4ecb7" />

</br>
</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
</br>
</br><img width="724" height="494" alt="image" src="https://github.com/user-attachments/assets/90217b6c-1644-48d0-885f-e32bdaaf80d4" />

</br>

iv) Using Median Filter
</br>
</br><img width="1184" height="715" alt="image" src="https://github.com/user-attachments/assets/7714e4ad-2d43-4efe-93f5-160e13f11b3d" />

</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br><img width="854" height="490" alt="image" src="https://github.com/user-attachments/assets/1efe9507-f59d-4066-b9ee-f5ed21790646" />

</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br><img width="1331" height="560" alt="image" src="https://github.com/user-attachments/assets/58f38b8d-1062-4255-9cae-535d4d802153" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
