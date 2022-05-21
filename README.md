# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.
<br>


### Step2:

Create the Text using cv2.putText.
<br>

### Step3:

Create the structuring element.
<br>

### Step4:

Erode and Dilate the image.
<br>

### Step5:

End Program.
<br>

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image= np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,'ESWAR',(5,70), font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Name",image)

# Create the structuring element
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erodeImage = cv2.erode(image,kernel1)
cv2.imshow("Erode Image",erodeImage)

# Dilate the image
dilationImage = cv2.dilate(image,kernel1)
cv2.imshow("Dilated Image",dilationImage)



cv2.waitKey(0)
cv2.DestroyAllWindows
```
## Output:

### Display the input Image
<br>
<img width="301" alt="1" src="https://user-images.githubusercontent.com/93427011/169644466-fce52af1-12da-434d-96c8-b8d72ba86748.png">
<br>


### Display the Eroded Image
<br>
<img width="301" alt="2" src="https://user-images.githubusercontent.com/93427011/169644475-be242ed8-9e6b-4ecb-8bf2-938969e2fdd8.png">
<br>


### Display the Dilated Image
<br>
<img width="301" alt="3" src="https://user-images.githubusercontent.com/93427011/169644482-bb435267-b27a-4ae1-b70a-37d580a59522.png">
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
