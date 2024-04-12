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

## Output:
Developed by: Praveen.v

Reg no:212222233004

### SOBEL EDGE DETECTOR
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("135655.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

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
![Screenshot 2024-04-12 144300](https://github.com/praveenv23013808/EDGE-DETECTION/assets/145824728/26a7cd00-5dc7-4511-b00d-5bed63d6b980)
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel y axis")
plt.axis("off")
plt.show()
```
![Screenshot 2024-04-12 190017](https://github.com/praveenv23013808/EDGE-DETECTION/assets/145824728/728286f1-4fc0-48da-8885-123085e8904d)

```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel xy axis")
plt.axis("off")
plt.show()
```
![Screenshot 2024-04-12 190419](https://github.com/praveenv23013808/EDGE-DETECTION/assets/145824728/df552103-abd2-4559-b0ca-68df0a346929)

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("laplacian")
plt.axis("off")
plt.show()
```
![Screenshot 2024-04-12 190517](https://github.com/praveenv23013808/EDGE-DETECTION/assets/145824728/bb1a8c5c-356a-4025-9594-6481e253e2ff)

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(img, 120, 150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny_edges)
plt.title("canny_edges")
plt.axis("off")
plt.show()
```
![Screenshot 2024-04-12 190822](https://github.com/praveenv23013808/EDGE-DETECTION/assets/145824728/2b8ebbac-8e32-46cf-9928-ad651c31d0d0)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
