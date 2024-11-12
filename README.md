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
```python
# Developed By: NAVEEN.S
# Register Number: 212222240070

import cv2
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('ajith.jpg')

# Convert the image to grayscale
gray_image = c
v2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])



```
## Output:
### Input Grayscale Image and Color Image
![c1c68ad1-2755-4321-acc4-14a94f807b60](https://github.com/user-attachments/assets/d0c69295-851c-4996-9976-d6588fb3eec1)


### Histogram of Grayscale Image and any channel of Color Image
![87ae7b1d-53b7-466e-8588-a1ad8cf7e620](https://github.com/user-attachments/assets/1e712c45-b092-4f64-8cf0-53f848c496ed)





### Histogram Equalization of Grayscale Image.
![f3089203-0cea-49c7-8ceb-60789399774d](https://github.com/user-attachments/assets/5e524c7c-37cc-469b-bc1d-746518dc950c)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV
