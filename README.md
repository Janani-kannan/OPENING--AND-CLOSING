# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

## Step1: Import the necessary packages.

## Step2:  Create the Text using cv2.putText.

## Step3:  Create the structuring element.

## Step4:  Use Opening operation.

## Step5:  Use Closing Operation.

 
## Program:

# DEVELOPED BY : JANANI K
# REGISTER NO  : 212224230102

# Create the Text using cv2.putText
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the structuring element


```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'JANANI K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```

# Use Opening operation

```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```

# Use Closing Operation

```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")

```
## Output:

### Display the input Image

<img width="578" height="140" alt="image" src="https://github.com/user-attachments/assets/6432be43-6726-4c36-8f26-59a63d558c8c" />


### Display the result of Opening

<img width="549" height="149" alt="image" src="https://github.com/user-attachments/assets/1e5bb0b5-cff6-4635-b98d-88215ebe313f" />


### Display the result of Closing

<img width="571" height="147" alt="image" src="https://github.com/user-attachments/assets/5494d044-26f9-4817-95c1-1b1adfeab998" />

## Result

Thus the Opening and Closing operation is used in the image using python and OpenCV.
