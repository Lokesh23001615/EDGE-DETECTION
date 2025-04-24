# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
```
Developed by : Lokesh M
Register Number : 212223230114
```
### Loading the Images :
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('cow.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.subplot(1, 1, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5) 
sobel_combined = cv2.magnitude(sobel_x, sobel_y) 
plt.subplot(1,1,1)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.subplot(1,1,1)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.subplot(1,1,1)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
### Original Image
![image](https://github.com/user-attachments/assets/71564e98-c2f5-4aef-b5f9-1664a9d264a0)


### SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/386ff7c6-a6ec-4b87-85fd-b26a6987a392)



### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/511d2d82-3a23-42df-925a-f18d774c2595)



### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/904ba7f7-e2a1-46ec-92ce-573644ba9663)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
