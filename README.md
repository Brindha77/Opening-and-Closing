# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step 1 :
Import the necessary packages.

## Step 2 :
Create the Text using cv2.putText

## Step 3 :
Create the structuring element.

## Step 4 :
Use Opening operation.

## Step 5 :
Use Closing Operation.
 
## Program:
## DEVELOPED BY : R BRINDHA
## REGISTER NO : 212222230023
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
from google.colab.patches import cv2_imshow
```

# Create the Text using cv2.putText
```
img1=np.zeros((300,500),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"R.BRINDHA",(7,77),font,3,(255,0,0),5,cv2.LINE_AA)
cv2_imshow(img2)
```
# Create the structuring element
```
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
```
# Use Opening operation
```
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2_imshow(img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Use Closing Operation
```
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2_imshow(img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image
![1](https://github.com/Brindha77/Opening-and-Closing/assets/118889143/9bac1cc0-d417-4c69-b9cf-8b6b71c847bf)

### Display the result of Opening
![2](https://github.com/Brindha77/Opening-and-Closing/assets/118889143/9b720370-28f3-4ca2-bb19-0e4366eabe57)

### Display the result of Closing
![3](https://github.com/Brindha77/Opening-and-Closing/assets/118889143/9455e788-2953-404d-89c5-52cbded9b9fa)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
