# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary libraries.

### Step2:
Read the images using imread() function.

### Step3:
Using calcHist() we can find the histogram of the images.

### Step4:
Using equalizeHist() we can equalize the image.

### Step5:

Using matplotlib.pyplot plot the histogram.
## Program:
```python




 

# Write your code to find the histogram of gray scale image and color image channels.


# Developed by: NITHISHWAR S
# Register No: 212221230071








# Display the histogram of gray scale image and any one channel histogram from color image

# Developed By: NITHISHWAR S
# Register Number:212221230071

import cv2
import matplotlib.pyplot as plt
gray=cv2.imread("images.jpg")
color=cv2.imread("car.png")
hist=cv2.calcHist([gray],[0],None,[256],[0,255])
hist1=cv2.calcHist([color],[1],None,[256],[0,255])
plt.imshow(gray)
plt.show()
plt.imshow(color)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel("gvalue")
plt.ylabel("pixel")
plt.stem(hist)
plt.show()
plt.stem(hist1)
plt.show()




# Write the code to perform histogram equalization of the image. 

# Developed by: NITHISHWAR S
# Register No: 212221230071
import cv2
gray_image = cv2.imread("images.jpg",0)
cv2.imshow('grey scale image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows 



```
## Output:
### Input Grayscale Image and Color Image





### Histogram of Grayscale Image and any channel of Color Image
<br>
<br>
<br>
<br>

### Histogram Equalization of Grayscale Image
<br>
<br>
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
