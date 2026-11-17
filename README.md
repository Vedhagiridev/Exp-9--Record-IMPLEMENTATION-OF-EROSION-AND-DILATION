# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

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

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Developed By

**Name:** Sharmili V
**Register No:** 212225040405

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a black blank image
img = np.zeros((300, 500), dtype=np.uint8)

# Insert white text onto the image
cv2.putText(
    img,
    "IMAGE PROCESSING",
    (40, 150),
    cv2.FONT_HERSHEY_SIMPLEX,
    1,
    255,
    3
)

plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.show()

# Create a 5x5 kernel
kernel = np.ones((5, 5), dtype=np.uint8)

print(kernel)

# Apply erosion
erosion = cv2.erode(img, kernel, iterations=1)

# Display eroded image
plt.imshow(erosion, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")
plt.show()

# Apply dilation
dilation = cv2.dilate(img, kernel, iterations=1)

# Display dilated image
plt.imshow(dilation, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")
plt.show()

plt.figure(figsize=(12, 5))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(erosion, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(dilation, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()

```
## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

<img width="792" height="662" alt="image" src="https://github.com/user-attachments/assets/71b49712-4660-414f-a6da-8e77cef55f7a" />


### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.
  
<img width="797" height="502" alt="image" src="https://github.com/user-attachments/assets/3268a2a6-5b4c-4d71-b32f-1d7e006ade14" />


### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="825" height="510" alt="image" src="https://github.com/user-attachments/assets/415fecd5-df10-465e-99ca-49a762411c6c" />

## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
