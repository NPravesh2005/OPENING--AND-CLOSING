
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: PRAVESH N
### REGISTER NO: 212223230154

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'JANARTHANAN K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
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

<img width="690" height="189" alt="Screenshot 2025-10-24 132656" src="https://github.com/user-attachments/assets/39dd8707-4f39-4619-9ecd-4f2a9901c26a" />



### Display the result of Opening


<img width="655" height="195" alt="Screenshot 2025-10-24 132702" src="https://github.com/user-attachments/assets/7066cdb7-0ab1-4164-ad92-6b0282ff4279" />


### Display the result of Closing

<img width="694" height="191" alt="Screenshot 2025-10-24 132708" src="https://github.com/user-attachments/assets/64dc86de-cfa2-4c1b-9cf9-2cc321e83544" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
