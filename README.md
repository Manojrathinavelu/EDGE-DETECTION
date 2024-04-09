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
Developed by :MANOJ KARTHIK R
Register no  : 212222240061
```

### Convert image to grayscale and remove noise:
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("doggy.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### Sobel Edge Detector:
#### SOBEL X AXIS: 
```python
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

#### SOBEL Y AXIS:
```python 
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

#### SOBEL XY AXIS: 
```python 
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

### laplacian edge Detector:
```python
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

### Canny Edge Detector:
```python 
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
### SOBEL EDGE DETECTOR :
#### SOBEL X AXIS :
![image](https://github.com/Manojrathinavelu/EDGE-DETECTION/assets/119560395/31effa7e-7403-450a-8680-06ec64c7b963)

#### SOBEL Y AXIS :
![image](https://github.com/Manojrathinavelu/EDGE-DETECTION/assets/119560395/7d047e7e-680e-458e-85db-934ba7047965)


#### SOBEL XY AXIS :
![image](https://github.com/Manojrathinavelu/EDGE-DETECTION/assets/119560395/37693805-50a7-4d93-926d-9a8acecdb587)


### LAPLACIAN EDGE DETECTOR :
![image](https://github.com/Manojrathinavelu/EDGE-DETECTION/assets/119560395/3b05eb6e-04d6-452f-a74e-bf2fa1fb7d11)


### CANNY EDGE DETECTOR :
![image](https://github.com/Manojrathinavelu/EDGE-DETECTION/assets/119560395/4eb32a73-8828-4c73-8603-34c3f06fc26f)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
