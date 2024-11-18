# EXP-3-Record-Histogram processing 
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
#### Developed By: Thiyagarajan A
#### Register Number: 212222240110
### Histogram for Bright Image 
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
# Load the color image
image = cv2.imread('cat.jpg')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/a477f062-233e-492d-aee7-34b88ade9d4c)
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/2ef1b38a-d14b-4ad2-98cc-b318dad1208d)
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
![image](https://github.com/user-attachments/assets/a5d7502b-0b88-4b6c-8d42-25134cff465a)
```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.show()
```
![image](https://github.com/user-attachments/assets/e5c0e193-141f-4f9d-aa6a-474255b7a650)

### Histogram for Daerk Image 
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
```
# Load the color image
image = cv2.imread('dog.jpg')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/57c4e74d-bffe-4920-a427-3bcf45fa6f2c)

```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/d5ce3c3e-0317-465b-a5c3-142640a6c184)
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

```
![image](https://github.com/user-attachments/assets/a2211579-3614-402b-92a6-bc44b91e88d7)

```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.show()
```
![image](https://github.com/user-attachments/assets/bbc53bca-7cf1-42a4-b08d-dd723fad1e0b)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
