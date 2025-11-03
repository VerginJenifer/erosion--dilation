# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale
### Step2:
Define a structuring element (kernel) for morphological operations.
### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.
### Step5:
Display and compare the original, eroded, and dilated images.
 
## Program:

``` Python
#Developed by : D VERGIN JNEIFER
#Register No: 212223240174
#exp-9-Erosion & Dilation
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'JENIFER' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')


```
## Output:

### Display the input Image
<img width="413" height="132" alt="image" src="https://github.com/user-attachments/assets/48a99e3b-26e4-452e-aa1c-d70c24a60bdd" />


### Display the Eroded Image
<img width="408" height="128" alt="image" src="https://github.com/user-attachments/assets/7ef5a6f1-d001-4da2-9389-0afda1a1f149" />


### Display the Dilated Image
<img width="420" height="151" alt="image" src="https://github.com/user-attachments/assets/d44f3dde-15b4-4f22-a387-281fa0088fb9" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
