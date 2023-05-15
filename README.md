# Thresholding of Images
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.
## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm
### Step1:
Import packages cv2 and matplotlib.

### Step2:
Read the image and convert it into grayscale image.

### Step3:
Perform Global thresholding method.

### Step4:
Perform Adaptive thresholding method.

### Step5:
Perform optimum global thresholding by otsu method.

### Step6:
Run the programs and show the outputs.

## Program
#### Program developed by: Sarankumar J
#### Register number: 212221230087
```py
# Load the necessary packages
import cv2
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale
image=cv2.imread('nissan.jpg')
gray=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
plt.imshow(gray,cmap='gray')
plt.axis('off')

# Use Global thresholding to segment the image
ret, thresh1=cv2.threshold(gray, 100, 200, cv2.THRESH_BINARY)
ret, thresh2=cv2.threshold(gray, 100, 200, cv2.THRESH_BINARY_INV)
ret, thresh3=cv2.threshold(gray, 100, 200, cv2.THRESH_TRUNC)
ret, thresh4=cv2.threshold(gray, 100, 200, cv2.THRESH_TOZERO)
ret, thresh5=cv2.threshold(gray, 100, 200, cv2.THRESH_TOZERO_INV)

# Use Adaptive thresholding to segment the image
th1=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
th2=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)

# Use Otsu's method to segment the image 
ret,th7=cv2.threshold(gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)

# Display the results
plt.imshow(thresh1,cmap='gray')
plt.imshow(thresh2,cmap='gray')
plt.imshow(thresh3,cmap='gray')
plt.imshow(thresh4,cmap='gray')
plt.imshow(thresh5,cmap='gray')
plt.imshow(th1,cmap='gray')
plt.imshow(th2,cmap='gray')
plt.imshow(th7,cmap='gray')
```
## Output:-
### Original Image
![image](https://github.com/SarankumarJ/Thresholding/assets/94778101/59c61a59-a8b0-4789-bb5b-01c2d5621a2d)

### Grayscale Image
![image](https://github.com/SarankumarJ/Thresholding/assets/94778101/4b0319ce-a22e-43d6-9825-75e683432b3b)

### Global Thresholding
![3](https://github.com/SarankumarJ/Thresholding/assets/94778101/dbd9bb26-fc30-4635-a789-bf32e9418d2b)

![4](https://github.com/SarankumarJ/Thresholding/assets/94778101/cedaba89-99db-49d6-984b-7ee07f1eace7)

![5](https://github.com/SarankumarJ/Thresholding/assets/94778101/dd9e69aa-a2a6-4a35-b702-28d84931c152)

![6](https://github.com/SarankumarJ/Thresholding/assets/94778101/46e4de41-8432-43ad-b29e-eaf253f7147e)

![7](https://github.com/SarankumarJ/Thresholding/assets/94778101/07d6449b-91c9-4fec-980f-a8a7140b6212)

### Adaptive Thresholding
![8](https://github.com/SarankumarJ/Thresholding/assets/94778101/44681672-ba75-47c9-977d-b1fd276f75f2)

![9](https://github.com/SarankumarJ/Thresholding/assets/94778101/f1e66a3d-1df4-4aa8-af84-180c84cbf9ba)

### Optimum Global Thesholding using Otsu's Method
![10](https://github.com/SarankumarJ/Thresholding/assets/94778101/08b44c4c-fb2b-4765-9f1b-32783bd978aa)


## Result:-
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
