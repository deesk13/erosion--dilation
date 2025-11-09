## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step-1:
Create a black image of size 100x600 pixels.

## Step-2:
Use a specified font to write the word "Lifestyle" on the image at a defined position.

## Step-3:
Show the image containing the text without axis labels.

## Step-4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

## Step-5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.

## Step-6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
### DEVELOPED BY : DEVA DHARSHINI I
### REG NO : 212223240026

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'JANARTHANAN K', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```


# Create the structuring element

```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
## Output:

### Display the input Image
<br>
<br>
<img width="812" height="141" alt="image" src="https://github.com/user-attachments/assets/81857088-6138-41ff-b86a-64ca33d11fc9" />


<br>
<br>
<br>

### Display the structured elements
<br>
<br>
<img width="280" height="550" alt="image" src="https://github.com/user-attachments/assets/4b15c3d3-18b9-40f0-90f3-2ea4021ed1f9" />


<br>
<br>
<br>


### Display the Eroded Image
<br>
<br>

<img width="888" height="162" alt="image" src="https://github.com/user-attachments/assets/126a9ec9-a5df-4d8e-92ac-75cd1bdf5d1f" />


<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>


<img width="926" height="163" alt="image" src="https://github.com/user-attachments/assets/02252c19-b932-42f3-8cd3-e2aca3c9ecc0" />



<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
