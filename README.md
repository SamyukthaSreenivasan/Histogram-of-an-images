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

# Developed By: Samyuktha S
# Register Number: 212222240089

## Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\grey.jpg')
color_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\color.jpg',-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale image
```
import numpy as np
import cv2
Gray_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\grey.jpg')
Color_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\color.jpg')
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
## Histogram of Color image
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\color.jpg',0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/69175ce1-c529-4a2a-b4e6-638e6836d3f3)

![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/1dba056e-afca-457b-a793-40f862501b39)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/0e13bbb8-4167-424a-bc83-919ab0284227)

![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/7364e835-e826-4d4c-bc5c-34730bc668c8)

![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/191b1fa2-41a2-43b6-aec4-a5c1284bbc51)

![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/fa1adc1d-f907-48eb-a1dd-1b523d2f7f57)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/b2372fd2-48c5-4b00-b096-36d4c1f4ced3)

![image](https://github.com/SamyukthaSreenivasan/Histogram-of-an-images/assets/119475703/26a95842-f1d2-44a9-8a99-79e760821bf5)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
