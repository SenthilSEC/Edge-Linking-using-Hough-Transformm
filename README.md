# Edge-Linking-using-Hough-Transformm
# Name:P.Senthil Arunachalam
# Reg No:212224240147

## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.


# Name: PAVITHRA S
# Regno: 212223230147
# PROGRAM:
Input image and grayscale image

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("/content/deer.jpeg")  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Input Image")
plt.axis('off')

plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
```
```
edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off'
```
```
lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
for line in lines:
    x1, y1, x2, y2 = line[0]  
    cv2.line(image, (x1, y1), (x2, y2), (90, 250, 79), 2)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Result of Hough Transform")
plt.axis('off')

```

## Output

### Input image and grayscale image
<img width="428" height="294" alt="Screenshot 2025-11-02 132132" src="https://github.com/user-attachments/assets/6f98133f-d921-4faf-8f8c-17a1be3fd21e" />


### Canny Edge detector output

<img width="426" height="296" alt="Screenshot 2025-11-02 132139" src="https://github.com/user-attachments/assets/4e0c6827-5c89-46db-a14f-961037e99618" />

### Display the result of Hough transform

<img width="453" height="303" alt="Screenshot 2025-11-02 132145" src="https://github.com/user-attachments/assets/cc2bb9c9-8806-460f-9757-39f0c65d3b80" />

# Result:
Thus, the image has been successfully converted.

