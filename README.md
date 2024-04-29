# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>


### Step2:
<br>Import the necessary pacakages



### Step3:
<br>Create the text using cv2.putText



### Step4:
<br>
Create the structuring element


### Step5:
<br>
Erode the image


 
## Program:

# Import the necessary packages
```
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"REVERIE!",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```



# Create the structuring element
```
kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


# Erode the image

```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode, cmap = 'gray')
plt.axis("off")
```


# Dilate the image

```

img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate, cmap = 'gray')
plt.axis("off")
```
## Output:

### Display the input Image
<br>
<br>
<br>
<br>![Screenshot 2024-04-29 215525](https://github.com/Aravindsamy04/erosion--dilation/assets/113497037/b8b1f94e-5974-4c07-91e5-2ffa35b1e574)

<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>![Screenshot 2024-04-29 215532](https://github.com/Aravindsamy04/erosion--dilation/assets/113497037/8cf01e8e-df14-4eda-aae0-a17a5acd11c0)

<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<br>![Screenshot 2024-04-29 215541](https://github.com/Aravindsamy04/erosion--dilation/assets/113497037/eb5f5ca2-0a2b-41f4-ae43-f98170166ca0)

<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
