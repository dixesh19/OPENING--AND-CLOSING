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


<img width="938" height="642" alt="image" src="https://github.com/user-attachments/assets/0341e195-db1f-4d39-a985-3a775f666487" />


### Display the result of Opening

<img width="937" height="632" alt="image" src="https://github.com/user-attachments/assets/36a089a8-8cfc-4edf-814b-6e1590064fd5" />



### Display the result of Closing

<img width="965" height="641" alt="image" src="https://github.com/user-attachments/assets/cc275cdf-75ba-4fab-86db-a99bb9ea907c" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
