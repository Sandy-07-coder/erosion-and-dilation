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

```
# Image Erosion and Dilation using OpenCV

# Step 1: Import Required Libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Create a Blank Image
img = np.zeros((400, 600), dtype=np.uint8)

# Step 3: Insert Text into the Image
cv2.putText(img, 'IMAGE PROCESSING',
            (60, 200),
            cv2.FONT_HERSHEY_SIMPLEX,
            1.5,
            255,
            3)

# Step 4: Display Original Image
plt.figure(figsize=(6, 4))
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')
plt.show()

# Step 5: Create Structuring Element (Kernel)
kernel = np.ones((5, 5), np.uint8)

# Step 6: Image Erosion
erosion = cv2.erode(img, kernel, iterations=1)

plt.figure(figsize=(6, 4))
plt.imshow(erosion, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')
plt.show()

# Step 7: Image Dilation
dilation = cv2.dilate(img, kernel, iterations=1)

plt.figure(figsize=(6, 4))
plt.imshow(dilation, cmap='gray')
plt.title('Dilated Image')
plt.axis('off')
plt.show()

# Step 8: Compare All Three Images
images = [img, erosion, dilation]

titles = ['Original Image', 'Erosion', 'Dilation']

plt.figure(figsize=(15, 5))

for i in range(3):
    plt.subplot(1, 3, i + 1)
    plt.imshow(images[i], cmap='gray')
    plt.title(titles[i])
    plt.axis('off')

plt.tight_layout()
plt.show()
```

## Developed By

**Name:** Santhosh K

**Register No:** 212225040379

## Output

<img width="1489" height="362" alt="image" src="https://github.com/user-attachments/assets/6b2f6c1c-9a33-4e69-a0a0-b18ffbeed1b9" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
