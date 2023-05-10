# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the text image using cv2.putText().

### Step3:
Create the structuring kernel for image dilation and erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow().

 
## Program:
``` Python

Developed By: Mohamed Aseem P
Register  No: 212221230063

# Import the necessary packages

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,250),dtype = 'uint8')
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(text_image,"Aseem",(5,70),font,2,(255),2,cv2.LINE_AA) 
plt.title("Original Image")
plt.imshow(text_image,'bone')
plt.axis('off')

# Create the structuring element


kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(4,4))


# Erode the image

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'bone')
plt.axis('off')

# Dilate the image

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'bone')
plt.axis('off')

```
## Output:

### Display the input Image

![a1](https://github.com/Mohamedaseem786/Implementation-of-Erosion-and-Dilation/assets/94883005/69d17556-2f89-47cc-96f0-8bd72b20c5d8)


### Display the Eroded Image

![a2](https://github.com/Mohamedaseem786/Implementation-of-Erosion-and-Dilation/assets/94883005/2d78ddc3-7788-44e5-b421-d910df392308)


### Display the Dilated Image

![a3](https://github.com/Mohamedaseem786/Implementation-of-Erosion-and-Dilation/assets/94883005/30c267f3-7e9a-4829-8ce4-340b6c1bdb03)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
