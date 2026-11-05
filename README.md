# Exp-6--Record-EDGE-DETECTION-212224230284

## Name : SWETHA K 
## Register No. : 212224230284

## Aim

To implement and compare different edge detection techniques such as Sobel, Prewitt, Roberts, Laplacian, and Canny using OpenCV and Python to identify the boundaries and edges present in an image.

## Software Required

Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib


## Algorithm

Step 1: Import the required libraries such as OpenCV, NumPy, and Matplotlib.

Step 2: Read the input image using cv2.imread().

Step 3: Convert the input image into grayscale using cv2.cvtColor().

Step 4: Apply the Sobel operator to detect horizontal and vertical edges.

Step 5: Apply the Prewitt operator using custom horizontal and vertical kernels.

Step 6: Apply the Roberts operator using 2×2 convolution kernels.

Step 7: Apply the Laplacian operator to detect edges based on intensity changes.

Step 8: Apply the Canny edge detector using suitable threshold values.

Step 9: Display the original image and all the edge-detected images using Matplotlib.

## Program

## Developed By

## Name: SWETHA K
## Register No: 212224230284

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r'C:\Users\admin\Downloads\my photo dipt.jpeg') # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```

## Output 

<img width="702" height="540" alt="image" src="https://github.com/user-attachments/assets/7dfcf3b0-9354-4cb5-8e97-8a4521f34b3d" />

<img width="780" height="553" alt="image" src="https://github.com/user-attachments/assets/22926435-9f45-4b33-a85c-9923915d7159" />

<img width="877" height="543" alt="image" src="https://github.com/user-attachments/assets/9b400879-89dc-4ec2-90d8-ae885ef8c6c8" />

<img width="853" height="558" alt="image" src="https://github.com/user-attachments/assets/84ad6afb-41e6-4acd-8105-43df52298e25" />

## Result

Thus, different edge detection techniques, namely Sobel, Prewitt, Roberts, Laplacian, and Canny, were studied and implemented using OpenCV. The output images were obtained successfully, showing the edges and boundaries of the input image using different detection methods.





