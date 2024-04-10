# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the image

### Step2:
Read the colour image and convert it into grayscale

### Step3:
Perform edge detection using canny

### Step4:
Define the kernel size for erosion and dilation

### Step5:
Display all images

 
## Program:
 
# Import the necessary packages
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
```

# Create the Text using cv2.putText
```
input_image_path = 'hema.jpg'
color_image = cv2.imread(input_image_path)
gray_image=cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)
edges = cv2.Canny(gray_image, 100, 200) # you can adjust the thresholds as needed
kernel_size = 5
kernel = np.ones((kernel_size, kernel_size), np. uint8)
erosion = cv2.erode(edges, kernel, iterations=1)
dilation = cv2.dilate(edges, kernel, iterations=1)
```

# Create the structuring element
```
plt.figure(figsize=(15, 10))
plt.subplot(2, 3, 1)
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2, 3, 2)
plt.imshow(gray_image, cmap="gray")
plt.title('Black and white Image')
plt.axis('on')
plt.subplot(2, 3, 3)
plt.imshow(edges, cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')
```
# Erode the image
```
plt.subplot(2, 3, 4)
plt.imshow(erosion, cmap = 'gray')
plt.title('Erosion')
plt.axis('on')
```

# Dilate the image
```
plt.subplot(2, 3, 5)
plt.imshow(dilation, cmap='gray')
plt.title('Dilation')
plt.axis('on')
plt.show()

```
## Output:

### Display the input Image
![image](https://github.com/Sangavi-suresh/erosion-dilation/assets/118541861/e6e3b794-af73-4fb0-8466-1e6821a300df)


### Display the Eroded Image
![image](https://github.com/Sangavi-suresh/erosion-dilation/assets/118541861/ed033f43-9df5-4b2c-ac05-1bc063fb608f)


### Display the Dilated Image
![image](https://github.com/Sangavi-suresh/erosion-dilation/assets/118541861/01da8c70-1189-4caf-86ab-695361261e18)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
