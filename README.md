# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step 2:
Translate the image.
<br>

### Step 3:
Scale the image.
<br>

### Step 4:
Shear the image.
<br>

### Step 5:

Reflect of image.
<br>

### Step 6:
Rotate the image.
<br>

## Program:
```python
Developed By: Vishranthi A
Register Number: 212221230124
```
i)Image Translation
```python
#Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("cat.png")
input_image = cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M = np.float32([[1, 0, 100],
                [0, 1, 200],
                [0, 0, 1]])
translated_image = cv2.warpPerspective (input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```python
#Image Scaling

S=np.float32([[4,0,0],[0,4,0],[0,0,4]])
scaled_image=cv2.warpPerspective(input_image,S,(cols*4,rows*4))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```
iii)Image shearing
```python
#Image shearing

M_x = np.float32([[1, 0.5, 0],
                  [0, 1 ,0],
                  [0, 0 , 1]])
M_y= np.float32([[1, 0, 0],
                 [0.5, 1, 0],
                 [0, 0, 1]])
sheared_img_xaxis = cv2.warpPerspective (input_image,M_x,(int(cols*1.5), int(rows *1.5))) 
sheared_img_yaxis = cv2.warpPerspective (input_image,M_y, (int(cols*1.5), int(rows *1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()

plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
iv)Image Reflection
```python
#Image Reflection

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```

v)Image Rotation
```python
#Image Rotation

angle=np.radians(80)
M=np.float32([[np.sin(angle),-(np.cos(angle)),0],
               [np.cos(angle),np.sin(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
vi)Image Cropping
```python
#Image Cropping
cropped_img=input_image[15:150,14:150]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
<br>

![image](https://user-images.githubusercontent.com/93427278/231527948-0d0b985c-d11a-42c8-9cca-5871f07a718a.png)

<br>

![image](https://user-images.githubusercontent.com/93427278/231528217-4e5973c1-d93e-4081-a252-c071aaafa17b.png)

### ii) Image Scaling

![image](https://user-images.githubusercontent.com/93427278/231528381-4c3d0f62-cf7b-4661-972f-ba0d74b58fb0.png)


### iii)Image shearing
<br>

![image](https://user-images.githubusercontent.com/93427278/231528536-d04cc95d-ed0b-4040-ad47-9c2b0837d91d.png)

<br>

![image](https://user-images.githubusercontent.com/93427278/231528631-c3797347-b09a-427b-b93d-ec377adb127d.png)



### iv)Image Reflection
<br>

![image](https://user-images.githubusercontent.com/93427278/231528701-77ce4aff-0ca5-46d1-894f-3d9bc523d602.png)

<br>

![image](https://user-images.githubusercontent.com/93427278/231528798-b5c5a48b-53b0-4e96-8738-70d3a434c1bf.png)


### v)Image Rotation



![image](https://user-images.githubusercontent.com/93427278/231528876-6134d5e7-672e-4b06-8e2d-b23a5ab9ee54.png)



### vi)Image Cropping

![image](https://user-images.githubusercontent.com/93427278/231528943-f1b4aa39-e880-4399-a0f6-6a1a8830bb0b.png)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
