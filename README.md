# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

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

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** MUTHUKUMARAN NM

**Register No:** 212225040268

## Output
### Original Image
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('DIPT.jpg')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```
<img width="943" height="313" alt="image" src="https://github.com/user-attachments/assets/7f0bfe07-f2b2-440f-bd5e-1794c10d032d" />


### Global Thresholding
```
# Apply global thresholding with a threshold value of 127
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

```
<img width="557" height="317" alt="image" src="https://github.com/user-attachments/assets/d98337ed-808e-4db3-befe-197f2b4fb627" />



### Adaptive Thresholding

```python
# Apply adaptive thresholding using Gaussian method
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
<img width="425" height="297" alt="image" src="https://github.com/user-attachments/assets/260c48d7-bc82-4ba0-a9fb-413e964e7620" />


### Otsu's Thresholding
```python
# Apply Otsu's method for optimal thresholding
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

```
<img width="462" height="260" alt="image" src="https://github.com/user-attachments/assets/d781f4ba-ad10-4555-9b50-8fe6d617ebdd" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
