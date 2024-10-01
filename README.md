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
![8a89ed62-7b30-4b42-a7df-bc425921af43](https://github.com/user-attachments/assets/3a1fb141-bfce-415c-a09c-ea2cd7cf2571)

### Histogram of Grayscale Image and any channel of Color Image
![0c871302-beea-4a16-8ec5-ff41c84343b1](https://github.com/user-attachments/assets/20693939-48e1-4f0f-bfd1-1d3bc7669e3b)




### Histogram Equalization of Grayscale Image.
![f3089203-0cea-49c7-8ceb-60789399774d](https://github.com/user-attachments/assets/5e524c7c-37cc-469b-bc1d-746518dc950c)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV
