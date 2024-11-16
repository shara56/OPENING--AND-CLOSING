# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:Read the Image:
Load the input color image from a specified path.

### Step2:Convert to Grayscale:
Transform the color image into a grayscale format for easier processing.

### Step3:Edge Detection:
Apply an edge detection technique to identify the prominent edges in the grayscale image.

### Step4:Create Structuring Element:
Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.

### Step5:Morphological Operations:
Perform morphological operations:
Opening: Remove small objects from the edges to clean up the image.
Closing: Fill small holes in the detected edges to enhance the structure.

### step6:Display Results:
 Show the original grayscale image, along with the results of the opening and closing operations for visual comparison.
## Program:

# Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the structuring element.
```
image = cv2.imread("cute.jpg")  
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
![Screenshot (78)](https://github.com/user-attachments/assets/88b57870-4518-41cc-bb17-a61f6c71f4ee)

# Use Opening operation:
```
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
![Screenshot (79)](https://github.com/user-attachments/assets/fe6eacb8-9af8-4e70-9039-1dea69ed8b4c)

# Use Closing Operation
```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

```
![Screenshot (80)](https://github.com/user-attachments/assets/77efb78c-ffa8-4805-a8d4-da67003ab0dc)

### Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
