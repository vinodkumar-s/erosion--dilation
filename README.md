## Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
## Deveolped by: VINOD KUMAR S
## Register NO: 212222240116

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Lifestyle',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:

#### Display the input Image


![Screenshot 2024-04-26 203905](https://github.com/JoyceBeulah/erosion--dilation/assets/113497226/d0b79aee-0ae0-4585-aa5f-8b42755376e6)

#### Display the Eroded Image


![Screenshot 2024-04-26 203911](https://github.com/JoyceBeulah/erosion--dilation/assets/113497226/ca7837e5-f6ca-4b94-9c69-22026fe683e3)

#### Display the Dilated Image

![Screenshot 2024-04-26 203916](https://github.com/JoyceBeulah/erosion--dilation/assets/113497226/c659a7e3-8cc6-4e06-9d96-4286636e0819)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
