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
Original

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("bird.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

SOBEL EDGE DETECTOR

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

LAPLACIAN EDGE DETECTOR

laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

CANNY EDGE DETECTOR

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')


```
## Output:

## Original Image:

![image](https://github.com/user-attachments/assets/b45b911b-d05c-4eba-a3e0-2db4037bb8bb)



### SOBEL EDGE DETECTOR


![image](https://github.com/user-attachments/assets/0992b2d9-3042-4fac-9582-0b470e38848c)



### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/e9c95b21-41c0-4923-a496-4e77cb26eda6)




### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/868769de-28f2-45c9-94f0-63aee70b7bcd)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
