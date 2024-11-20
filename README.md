# Implementation-of-Erosion-and-Dilation
### DATE:
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1: 
Generate a black image of size (300, 600) using np.zeros().

### Step2:
Add the text onto the image using cv2.putText()

### Step3:
Create a 5x5 rectangular kernel using cv2.getStructuringElement() for morphological operations.

### Step4:
Perform erosion and dilation on the image using cv2.erode() and cv2.dilate() with the defined kernel.

### Step5:
Use matplotlib to display the original, eroded, and dilated images side-by-side for comparison.

 
## Program:
```
Developed By: amrutha
Ref No:212222110004
```
```
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Step 1: Load the input image using cv2.imread()
image = cv2.imread("star_9.jpg") 

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 3: Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)

# Step 4: Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

# Plot the original, eroded, and dilated images using Matplotlib

plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")


# Erode the image


plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")


# Dilate the image

plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

```
## Output:

### Display the input Image
![Screenshot 2024-10-21 161004](https://github.com/user-attachments/assets/6caaf9c9-ce43-46ab-8df2-38728ad57152)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
