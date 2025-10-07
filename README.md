# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br> import the neccesary packages


### Step2:
<br> creat the text using cv2.put Text

### Step3:
<br> create the structuting element

### Step4:
<br>  Erodde the image

### Step5:
<br> Dilate the image
 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='actor.jpg'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')



```````
## Output:
<img width="388" height="705" alt="image" src="https://github.com/user-attachments/assets/a8760a3e-6614-4e39-bc59-b9d58fc4e3d0" />
<img width="317" height="337" alt="image" src="https://github.com/user-attachments/assets/26753c98-9491-4246-9dbf-479715261d00" />
<img width="311" height="324" alt="image" src="https://github.com/user-attachments/assets/8060ebe1-822c-4fa5-aaa4-8a25850d70d7" />
<img width="344" height="335" alt="image" src="https://github.com/user-attachments/assets/4cff45fb-44a1-4eb6-b33e-aee0b540ab5b" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.


