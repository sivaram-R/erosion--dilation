## EX 09 Implementation-of-Erosion-and-Dilation
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
```
NAME: Deepika S
REG.NO: 212222230028
```

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
cv2.putText(img ,'Deepika',(60,70),font,2,(255),5,cv2.LINE_AA)
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
![1dipu](https://github.com/deepikasrinivasans/erosion--dilation/assets/119393935/c9c02fa8-c7ff-4457-b075-67880acfa233)
#### Display the Eroded Image
![2dipu](https://github.com/deepikasrinivasans/erosion--dilation/assets/119393935/b5036700-a067-40d2-bd82-bfe4b3c503c3)
#### Display the Dilated Image
![3dipu](https://github.com/deepikasrinivasans/erosion--dilation/assets/119393935/9a91dfaa-76cf-400d-a8d7-ac67c41acf62)
## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
