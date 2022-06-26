## EX NO:07
## DATE:12.5.22
# <p align="center">Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
For performing edge detection on a image.
Sobel
```python
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```
Laplacian
```python
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
```
Canny
```python
canny=cv2.Canny(img,120,150)
```
### Step3:
Display all the images with their respective edge detected images.
 
## Program:

``` Python
 Developed by:Prashethaa R
 Register No :212220230036
 
# Import the packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
image1=cv2.imread ('23.jpg') 
gray = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)
plt.title('GRAY IMAGE')
plt.imshow(gray,cmap = 'gray')

# SOBEL EDGE DETECTOR
img = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()


# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()

# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
![pr](https://user-images.githubusercontent.com/75234942/168728209-9f9f863a-1c8b-4df8-9a37-7f60614a051b.png)


### LAPLACIAN EDGE DETECTOR
![pr1](https://user-images.githubusercontent.com/75234942/168728227-5920fd33-033b-4afe-acb6-4b5729a8f12a.png)



### CANNY EDGE DETECTOR
![pr2](https://user-images.githubusercontent.com/75234942/168728246-615e0518-c39b-4c33-8545-34b78a7eaaa1.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
