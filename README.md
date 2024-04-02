# EX-6 EDGE-DETECTION
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
## PROGRAM:
```
DEVELOPED BY: Shriram S
REGISTER NUMBER: 212222240098
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![Ex-6](https://github.com/ShriramGH/EDGE-DETECTION/assets/117991122/6c57e8bf-c98b-42e8-a05d-ca21ca2f52fd)
### SOBEL EDGE DETECTOR:
![image](https://github.com/ShriramGH/EDGE-DETECTION/assets/117991122/308fb18c-77b4-4f84-a9b9-38161d7044dd)
![image](https://github.com/ShriramGH/EDGE-DETECTION/assets/117991122/a42299fa-11a5-4e3f-ba93-f175a0bcf8fe)
![image](https://github.com/ShriramGH/EDGE-DETECTION/assets/117991122/e74b9b28-8d16-4257-8747-539d4060d189)
### LAPLACIAN EDGE DETECTOR
![image](https://github.com/ShriramGH/EDGE-DETECTION/assets/117991122/94448c7f-4afe-4bb0-ac2f-34c47840a192)
### CANNY EDGE DETECTOR
![image](https://github.com/ShriramGH/EDGE-DETECTION/assets/117991122/2d9f953f-34ca-472e-b0c6-016ef72c0e60)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
