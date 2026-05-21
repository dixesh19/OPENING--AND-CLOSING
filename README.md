# OPENING--AND-CLOSING
### Name -  DINESH R
### Register Number - 212224240037
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:


## Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
## Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, ' DINESH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
## Create the structuring element
```
kernel = np.ones((3, 3), np.uint8)
```
## Display the input image
```
print(" DINESH R")
print("212224240037")
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```

## Opening is erosion followed by dilation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
## Display the result of Opening
```
print(" DINESH R")
print("212224240037")
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```



## Closing is dilation followed by erosion
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Display the result of Opening
```
print(" DINESH R")
print("212224240037")
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
# Output:

### Display the input Image


<img width="691" height="512" alt="image" src="https://github.com/user-attachments/assets/3b629991-6271-47f6-86a4-0012f9a12c82" />


### Display the result of Opening

<img width="721" height="515" alt="image" src="https://github.com/user-attachments/assets/99c97d0a-becc-437d-b54b-ca6c3a78c1d1" />



### Display the result of Closing

<img width="723" height="513" alt="image" src="https://github.com/user-attachments/assets/8706b309-3353-4703-8896-c47dec524a90" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
