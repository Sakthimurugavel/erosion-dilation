# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import necessary packages



### Step2:
Create an empty window and add text to it


### Step3:
create a structuring element


### Step4:
Do the operation


### Step5:
Show the output image


 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
```


### Display the input Image
```Python
color_image = cv2.imread(("p-1.png")
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![out 1 ex 9](https://github.com/Sakthimurugavel/erosion-dilation/assets/118707246/e1d0ada6-121d-40de-9931-ddb2f4712a48)


### Display the Eroded Image
```Python
color_image = cv2.imread("p-1.png")
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)
edges = cv2.Canny (gray_image, 100, 200)
kernel_size = 5
kernel = np.ones((kernel_size, kernel_size), np. uint8)
erosion = cv2. erode (edges, kernel, iterations=1)
dilation = cv2.dilate (edges, kernel, iterations=1)
```
## Output:
![out 2,1 ex 9](https://github.com/Sakthimurugavel/erosion-dilation/assets/118707246/404cb5e4-4738-4776-8c9f-aef451f0e89b)![out 2,2 ex 9](https://github.com/Sakthimurugavel/erosion-dilation/assets/118707246/a0431737-2836-40d7-8f17-df49d3fd6692)


### Display the Dilated Image
```Python
plt.figure(figsize=(15, 10))
plt.subplot(2, 3, 1)
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2, 3, 2)
plt.imshow(gray_image, cmap='gray')
plt.title('Black and White Image')
plt.axis('on')
plt.subplot(2, 3, 3)
plt.imshow(edges, cmap='gray')
plt.title('Edge Segmentation')
plt.subplot(2, 3, 4)
plt.imshow(erosion, cmap='gray')
plt.title('Erosion')
plt.axis('on')
plt.subplot(2, 3, 5)
plt.imshow(dilation, cmap='gray')
plt.title('Dilation')
plt.axis('on')
plt.show()
```
## Output:
![out 3 ex 9](https://github.com/Sakthimurugavel/erosion-dilation/assets/118707246/24faf57b-e5e1-4d48-8f11-43efe7faec42)

![out 3 2 ex 9](https://github.com/Sakthimurugavel/erosion-dilation/assets/118707246/643d6817-f5df-4bd6-a245-14fefee972ff)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
