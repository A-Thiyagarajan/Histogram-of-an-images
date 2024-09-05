# Histogram-of-an-images
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
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt

gray_image = cv2.imread("dog.jpg")
color_image = cv2.imread("cat.jpg", -1)

color_image_rgb = cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB)

plt.subplot(1, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Gray Image')

plt.subplot(1, 2, 2)
plt.imshow(color_image_rgb)
plt.title('Color Image')

plt.show()
```
![image](https://github.com/user-attachments/assets/2529a4ea-7d3a-4158-b3a5-75938808b177)

### Histogram of Grayscale Image and any channel of Color Image
```
import cv2
Gray_image = cv2.imread("dog.jpg")
Color_image = cv2.imread("cat.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
![image](https://github.com/user-attachments/assets/86978a66-dae6-4039-93c0-31f39f2afd74)

```
import matplotlib.pyplot as plt

plt.imshow(Color_image)
plt.title("Color Image")
plt.show()

plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

```

![image](https://github.com/user-attachments/assets/2add9b21-f0e5-4066-942c-763d2f8681a4)

### Histogram Equalization of Grayscale Image.
```
import cv2
import matplotlib.pyplot as plt

gray_image = cv2.imread("dog.jpg", 0)

plt.imshow(gray_image, cmap='gray')
plt.title('Grey Scale Image')
plt.show()

equ = cv2.equalizeHist(gray_image)

plt.imshow(equ, cmap='gray')
plt.title('Equalized Image')
plt.show()
```

![image](https://github.com/user-attachments/assets/6fa91a9c-f5f8-4472-9539-615485517d6b)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
