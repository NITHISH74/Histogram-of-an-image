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

gray_image = cv2.imread("kitty.jpg")
color_image = cv2.imread("heist.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()






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
![image](https://user-images.githubusercontent.com/94164665/166105098-306acd14-0d4a-4f0c-b919-27613bc93f20.png)
![image](https://user-images.githubusercontent.com/94164665/166105117-fb07537d-c585-4b2b-a687-7c7df32558bc.png)





### Histogram of Grayscale Image and any channel of Color Image
![image](https://user-images.githubusercontent.com/94164665/166105132-ad793d9b-fbc8-4b89-9781-c6e6a1ede9e3.png)
![image](https://user-images.githubusercontent.com/94164665/166105145-a3e241a1-8b07-4838-8c53-a041cf6aaccc.png)





### Histogram Equalization of Grayscale Image
![image](https://user-images.githubusercontent.com/94164665/166105155-e1aa1102-dd39-4c92-92c4-d73a4bfb79b6.png)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
