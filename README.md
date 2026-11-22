# Opening and Closing Operations Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

- Morphological Opening
- Morphological Closing

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create or load an input image containing foreground objects.

### Step 3:

Display the original image.

### Step 4:

Create a structuring element (kernel) of suitable size.

### Step 5: Opening Operation

- Apply the Opening operation using the structuring element.
- Opening consists of Erosion followed by Dilation.
- Remove small foreground noises while preserving the shape of larger objects.
- Display the opened image.

### Step 6: Closing Operation

- Apply the Closing operation using the structuring element.
- Closing consists of Dilation followed by Erosion.
- Fill small holes and gaps within foreground objects.
- Display the closed image.

### Step 7:

Compare the original, opened, and closed images.

## Program

## Developed By

**Name:** Kanishka V

**Register No:** 212224100030

### Import Libraries
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Original Image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'KANISHKA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
kernel = np.ones((3, 3), np.uint8)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
### Opening Operation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
```
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```

### Closing Operation
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
```
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')
```



## Output

### Original Image

<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/99d5499b-cfb1-4de6-9501-b4e281e42c7f" />


### Opening Operation
<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/43a8da0f-8dab-41ec-ad48-01e28bfbb756" />



### Closing Operation
<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/0cb62019-7872-42cb-bd6c-cecdbd79a517" />

## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV.
