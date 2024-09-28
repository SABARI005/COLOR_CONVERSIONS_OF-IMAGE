# COLOR_CONVERSIONS_OF-IMAGE->
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
1.Load an image from your local directory and display it.
### Step2:
1.Draw a line from the top-left to the bottom-right of the image.

2.Draw a circle at the center of the image.

3.Draw a rectangle around a specific region of interest in the image.

4.Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.Convert the image from RGB to HSV and display it.

2.Convert the image from RGB to GRAY and display it.

3.Convert the image from RGB to YCrCb and display it.

4.Convert the HSV image back to RGB and display it.

### Step4:
1.Access and print the value of the pixel at coordinates (100, 100).

2.Modify the color of the pixel at (200, 200) to white.

### Step5:
1.Resize the original image to half its size and display it.
### Step6:
1.Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.Flip the original image horizontally and display it.

2.Flip the original image vertically and display it.

### Step8:
1.Save the final modified image to your local directory.


## Program:
### Developed By: SABARI S
### Register Number: 212222240085

### i)Read and Display an Image
```py
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('image.jpeg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/bbe4d75b-b5cc-4a4e-9056-89047dff6abf)


### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res = cv2.line(image, (0, 0), (206,244), (200, 100, 205), 5)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/48bd96a5-9611-4ac6-aeaa-ed903511b58b)


(2) Draw a circle at the center of the image.
```py

image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image = cv2.resize(image,(500,500))
res = cv2.circle(image,(250,250), 150, (255, 0, 0), 10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/46e1c768-bf14-4a9d-9aa2-582ba457993c)


(3) Draw a rectangle around a specific region of interest in the image.
```py

image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res = cv2.rectangle(image, (206-20,244-20), (0+10,0+20),(200,0, 0), 5)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output


(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
res = cv2.putText(image,"SAMSON", (3,52), font,0.5, (0, 0, 0),1)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![Screenshot 2024-09-28 154319](https://github.com/user-attachments/assets/851f95d6-3660-466a-8e16-a021da5c590b)


### iii)Image Color Conversion
1) Convert the image from RGB to HSV and display it
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
hsv2 = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
plt.imshow(hsv2)
plt.axis('off')
plt.show()
```
### Output
![Screenshot 2024-09-28 154423](https://github.com/user-attachments/assets/a2e97677-cbfa-467a-8e9e-d6ba6079627d)

(2) Convert the image from RGB to GRAY and display it.
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
gray2 = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
plt.imshow(gray2)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/e2b294d1-b247-4f21-a3bb-ca786d4c434c)


3) Convert the image from RGB to YCrCb and display it.
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
YCrCb1 = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
plt.imshow(YCrCb1)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/1bbd1e51-6c6e-4cbb-b8ae-9d4a3843b815)


(4) Convert the HSV image back to RGB and display it.
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
BGR = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(BGR)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/c22a5d4d-c182-4727-ad70-7ada2babd16d)


### iv)Access and Manipulate Image Pixels
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
image[199, 199] = [255, 255, 255]
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/c22a5d4d-c182-4727-ad70-7ada2babd16d)


### v)Image Resizing
```py
img = cv2.imread('wallpaper.jpg', 1)
resized_img = cv2.resize(image, (400, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![Screenshot 2024-09-28 154850](https://github.com/user-attachments/assets/9c6526ca-23d5-474c-a668-572d1e20b64d)


### vi)Image Cropping
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
roi = image[20:20 + 300, 20:20 + 300]
plt.imshow(roi)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/f35c2550-6f96-44a8-a19d-00e15192e746)


### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```py
image = cv2.imread("image.jpeg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res=cv2.rotate(image,cv2.ROTATE_180)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output

![Screenshot 2024-09-28 155503](https://github.com/user-attachments/assets/f5607149-1b0e-44c3-81a6-6fef4db06455)


(2) Flip the original image vertically and display it.
```py

image = cv2.imread("image.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/0996857a-71de-42e0-a6ab-b12bdcb3906f)


### viii)Write and Save the Modified Image
```py
img = cv2.imread("image.jpeg")
cv2.imwrite('sanju_samson.jpeg',img)
```
### Output
![image](https://github.com/user-attachments/assets/07ca2ff0-2f5d-4122-8760-cdbdbbb64db9)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







