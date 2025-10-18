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
### SOBEL EDGE DETECTOR

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("C:\\Users\\admin\\OneDrive\\Desktop\\DIPT\\bunny.jpeg")
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()


sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()


sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()


```

<img width="676" height="358" alt="Screenshot 2025-10-18 102441" src="https://github.com/user-attachments/assets/5bce0e41-11ea-44a7-ad8d-5e1ffb235f47" />

<img width="678" height="369" alt="Screenshot 2025-10-18 102447" src="https://github.com/user-attachments/assets/cd7c2fc3-ac35-4874-babe-f94c32205f61" />

<img width="676" height="353" alt="Screenshot 2025-10-18 102454" src="https://github.com/user-attachments/assets/0a1097ca-67dd-44c3-8f29-dd7be99e13fc" />


### LAPLACIAN EDGE DETECTOR

    lap = cv2.Laplacian(gray, cv2.CV_64F)
    plt.figure(figsize=(8, 8))
    plt.subplot(1, 2, 1)
    plt.imshow(gray, cmap='gray')
    plt.title("Original Image")
    plt.axis("off")
    plt.subplot(1, 2, 2)
    plt.imshow(lap, cmap='gray')
    plt.title("Laplacian Edge Detector")
    plt.axis("off")
    plt.show()



<img width="669" height="358" alt="Screenshot 2025-10-18 102501" src="https://github.com/user-attachments/assets/01dd8da8-c06b-4501-bc76-67cd7dd11191" />


### CANNY EDGE DETECTOR
```
canny = cv2.Canny(gray, 120, 150)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```

<img width="662" height="341" alt="Screenshot 2025-10-18 102510" src="https://github.com/user-attachments/assets/89cf6053-7195-4062-af9d-0f77ed89ed02" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
