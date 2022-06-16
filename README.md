# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages for implementing the code.

### Step2:
Create the text that you want to modify using opening and close filter.

### Step3:
Create the structuring element that you want to use over the image.

### Step4:
Apply the opening and closing operation for the original image.

### Step5:
Show the results using imshow function from cv2
 
## Program:

``` Python
# Developed by: Palamakula Deepika
# Reg.No.: 212221240035
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_SCRIPT_COMPLEX
im=cv2.putText(img,' Pavan GV ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(cv2.cvtColor(im, cv2.COLOR_BAYER_GR2BGRA))

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,Kernel)
plt.imshow(cv2.cvtColor(image1, cv2.COLOR_BAYER_GR2BGRA))

# Use Closing Operation
image1=cv2.morphologyEx(img,cv2.MORPH_CLOSE,Kernel)
plt.imshow(cv2.cvtColor(image1,cv2.COLOR_BAYER_GR2BGRA))




```
## Output:

### Display the input Image
![11 1](https://user-images.githubusercontent.com/94154679/174125659-84350ec9-a8ad-4f9e-ad51-80cfcaafd02a.png)

### Display the result of Opening
![11 2](https://user-images.githubusercontent.com/94154679/174125726-76849555-f761-4b3b-bf1d-3a6d02a7f9dd.png)

### Display the result of Closing
![11 3](https://user-images.githubusercontent.com/94154679/174125816-2904fa8f-f515-497b-afc4-86f197418e8b.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
