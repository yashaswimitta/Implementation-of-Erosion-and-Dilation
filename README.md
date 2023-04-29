# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np

# Create the Text using cv2.putText
img1 = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'YASHASWI.M',(5,70),font,2,(255),5,cv2.LINE_AA)


# Create the structuring element
cv2.imshow("Name Image",img1)


# Erode the image and Dilate the image

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
erodeImage = cv2.erode(img1,kernel1)
dilationImage = cv2.dilate(img1,kernel1)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)
cv2.waitKey(0)

cv2.destroyAllWindows()



```
## Output:

### Display the input Image
![dip 10-1](https://user-images.githubusercontent.com/94619247/235293704-f8f47059-c783-40d5-9409-cdeb955378ba.jpg)


### Display the Eroded Image
![dip 10-2](https://user-images.githubusercontent.com/94619247/235293720-caf47682-5e7f-4da2-88b1-2fcda84fa40f.jpg)


### Display the Dilated Image
![dip 10-3](https://user-images.githubusercontent.com/94619247/235293742-39f94fa3-a0e6-4f3c-9a69-34af4f72d6c6.jpg)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
