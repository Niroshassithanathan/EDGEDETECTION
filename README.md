# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required packages for further process.

### Step 2:
Read the image and convert the bgr image to gray scale image.

### Step 3:
Use any filters for smoothing the image to reduse the noise.

### Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:
Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY : NIROSHA S
REG NO : 212222230097
```
## Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("windows.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
# SOBEL X AXIS :
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
# SOBEL Y AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
# SOBEL XY AXIS :
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
# SOBEL X AXIS :
![f1](https://github.com/Niroshassithanathan/EDGEDETECTION/assets/121418437/23a2376a-cf41-48f5-9dbd-3cf56937a725)

# SOBEL Y AXIS :
![f2](https://github.com/Niroshassithanathan/EDGEDETECTION/assets/121418437/b1914d0e-8b4d-4c0b-ba8c-31070e38cbfb)

# SOBEL XY AXIS :
![f3](https://github.com/Niroshassithanathan/EDGEDETECTION/assets/121418437/25b5e7c8-086c-4f7e-a582-3c4d970988fc)

### LAPLACIAN EDGE DETECTOR
![f4](https://github.com/Niroshassithanathan/EDGEDETECTION/assets/121418437/6e509500-26bd-4ea3-9394-668ed6253fe5)

### CANNY EDGE DETECTOR
![f5](https://github.com/Niroshassithanathan/EDGEDETECTION/assets/121418437/5d2a4866-d94c-42b2-9df3-5b42fa350edc)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
