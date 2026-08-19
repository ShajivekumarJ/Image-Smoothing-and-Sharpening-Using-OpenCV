# Image-Smoothing-and-Sharpening-Using-OpenCV
# Aim
To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.

# The program performs the following operations:
Read and display an input image
Apply Averaging filter
Apply Weighted Averaging filter
Apply Gaussian filter
Apply Median filter
Apply Laplacian sharpening using kernel
Apply Laplacian operator
Display all outputs for comparison
# Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
## Algorithm
# Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

# Step 2:
Read the input image (e.g., image.jpg).

# Step 3:
Convert the image from BGR to RGB format for display.

# Step 4:
Apply Averaging Filter using cv2.blur().

# Step 5:
Apply Weighted Averaging Filter using a custom kernel with cv2.filter2D().

# Step 6:
Apply Gaussian Filter using cv2.GaussianBlur().

# Step 7:
Apply Median Filter using cv2.medianBlur().

# Step 8:
Apply Laplacian Sharpening using Kernel with cv2.filter2D().

# Step 9:
Convert image to grayscale and apply Laplacian Operator using cv2.Laplacian().

# Step 10:
Display all filtered images using a grid layout for comparison.


# Program:

Developed By : Deepak K R


Register Number: 212225040057

# 1. Smoothing Filters
i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("25008695.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

# 2. Sharpening Filters
```

i) Using Laplacian Linear Kernal

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

# OUTPUT:
# 1. Smoothing Filters

i) Using Averaging Filter:

<img width="742" height="382" alt="Screenshot 2026-08-19 194453" src="https://github.com/user-attachments/assets/909ca27b-fe8c-478f-b313-d23a3ed2508f" />

ii)Using Weighted Averaging Filter:

<img width="848" height="431" alt="Screenshot 2026-08-19 194614" src="https://github.com/user-attachments/assets/c75cf420-e793-47ff-97cc-17e42dcb27ff" />

iii)Using Gaussian Filter:

<img width="926" height="499" alt="Screenshot 2026-08-19 194809" src="https://github.com/user-attachments/assets/786ae7b7-facc-4b0c-b3b5-6abda0d2e0c7" />

iv) Using Median Filter:

<img width="1274" height="659" alt="Screenshot 2026-08-19 194916" src="https://github.com/user-attachments/assets/e237c376-e1c7-4dce-b496-27eccf78d9ef" />

# 2. Sharpening Filters

i) Using Laplacian Kernal:

<img width="930" height="500" alt="Screenshot 2026-08-19 195007" src="https://github.com/user-attachments/assets/5030635f-ddce-43ee-874d-edd4cb7e8e02" />

ii) Using Laplacian Operator:

<img width="926" height="480" alt="Screenshot 2026-08-19 195055" src="https://github.com/user-attachments/assets/5a5c7c82-9da2-4122-8c62-a73b97282619" />


# Result :
Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.
