# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: M Sanjay
# Register Number: 212222240090
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('Dhanush.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## Output:
### Original Grayscale Image
![Screenshot 2024-10-03 154114](https://github.com/user-attachments/assets/add06e63-407d-49bf-9142-b120a8a2031a)

```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Output:
### Original Histogram
![Screenshot 2024-10-03 154227](https://github.com/user-attachments/assets/68ce4593-f21f-47b8-a191-adc5fb27554d)

```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
## Output:
### Equalized Image
![Screenshot 2024-10-03 154349](https://github.com/user-attachments/assets/7e53eb70-3080-452f-93b4-31af617d90fe)

```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

```
## Output:
### Equalized Histogram
![Screenshot 2024-10-03 154545](https://github.com/user-attachments/assets/40f15b29-d66b-4208-868e-6bb07fd464dd)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
