# **EXPERIMENT NO. 6: EDGE DETECTION**
# **NAME : ROGITH. K**
# **REG NO : 212223110042**
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
### ORIGINAL IMAGE
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Rogith.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### SOBEL EDGE DETECTOR
<img width="373" height="496" alt="Screenshot 2025-09-29 112251" src="https://github.com/user-attachments/assets/d1bdc674-d8ef-491d-98e8-0f46b9c88607" />

### LAPLACIAN EDGE DETECTOR
<img width="373" height="497" alt="Screenshot 2025-09-29 112259" src="https://github.com/user-attachments/assets/b5f349c2-640f-4262-8adb-67fab62180a6" />

### CANNY EDGE DETECTOR
<img width="377" height="499" alt="Screenshot 2025-09-29 112309" src="https://github.com/user-attachments/assets/93a5e676-a220-42f7-967a-665926988a70" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
