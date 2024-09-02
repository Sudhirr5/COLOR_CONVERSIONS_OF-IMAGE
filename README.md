# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

## Program:
#### Developed By: SUDHIR KUMAR. R
#### Register Number: 212223230221


## Output:

### i) Read and display the image
```python
import cv2
img = cv2.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
resized_img = cv2.resize(img, None, fx=1, fy=1)
cv2.imshow('212223240087', resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-02 130957](https://github.com/user-attachments/assets/5d46a97c-c27d-4cb4-9067-074ea259c0dd)

### ii)Write the image
```python
import cv2 as cv
img = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
cv.imwrite('d.jpg', img)
```

![Screenshot 2024-09-02 131509](https://github.com/user-attachments/assets/956ffb67-0447-4051-b759-4f5b748075dd)

### iii)Shape of the Image
```python
import cv2 as cv
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
print(image.shape)
```

![Screenshot 2024-09-02 131819](https://github.com/user-attachments/assets/3045fe33-bbe7-4ad6-9036-93a533b1231f)

### iv)Access rows and columns
```python
import cv2 as cv
import random
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (400, 400))
    
for i in range(150, 200):
    for j in range(image.shape[1]):
        image[i, j] = [random.randint(0, 255), random.randint(0, 255), random.randint(0, 255)]
    
cv.imshow('Modified Image', image)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 132031](https://github.com/user-attachments/assets/843c396a-f030-4c81-a10b-29558e26c29f)

### v)Cut and paste portion of image
```python
import cv2 as cv
# Load and resize the image
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (400, 400))
   
# Cut a portion of the image
tag = image[130:200, 110:190]
   
# Paste the cut portion in a new location
image[110:180, 120:200] = tag
   
# Display the modified image
cv.imshow('Cut and Paste', image)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 132410](https://github.com/user-attachments/assets/0ceba433-c885-4daa-93bf-8907ead1b505)

### vi) BGR and RGB to HSV and GRAY
```python
import cv2 as cv
    
# Load and resize the image
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (720, 720))
    
# Convert and display the image in different color spaces
hsv1 = cv.cvtColor(image, cv.COLOR_BGR2HSV)
hsv2 = cv.cvtColor(image, cv.COLOR_RGB2HSV)
gray1 = cv.cvtColor(image, cv.COLOR_BGR2GRAY)
gray2 = cv.cvtColor(image, cv.COLOR_RGB2GRAY)
    
cv.imshow('Original Image', image)
cv.imshow('BGR to HSV', hsv1)
cv.imshow('RGB to HSV', hsv2)
cv.imshow('BGR to GRAY', gray1)
cv.imshow('RGB to GRAY', gray2)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 132410](https://github.com/user-attachments/assets/ca2bb60a-96d9-4f63-b4ba-86a279f32fee)

![Screenshot 2024-09-02 132637](https://github.com/user-attachments/assets/0fe5a2be-1fb6-4074-a2d9-7f2dff8ae5cc)

![Screenshot 2024-09-02 132646](https://github.com/user-attachments/assets/8a7dc521-9c60-41f7-95ca-2606c0c20cdd)

![Screenshot 2024-09-02 132656](https://github.com/user-attachments/assets/dac66636-a6ef-4a81-a754-7335b91ecae3)

![Screenshot 2024-09-02 132709](https://github.com/user-attachments/assets/5421a389-000a-4117-8a61-3501f5031a0b)

### vii) HSV to RGB and BGR
```python
import cv2 as cv
  
# Load and resize the image
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (720, 720))
  
# Convert HSV to RGB and BGR
rgb_image = cv.cvtColor(image, cv.COLOR_HSV2RGB)
bgr_image = cv.cvtColor(rgb_image, cv.COLOR_RGB2BGR)
  
# Display the images
cv.imshow('HSV Image', image)
cv.imshow('RGB Image', rgb_image)
cv.imshow('BGR Image', bgr_image)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 133202](https://github.com/user-attachments/assets/21d91b91-be75-4669-8d28-f13b5d1570db)

![Screenshot 2024-09-02 133213](https://github.com/user-attachments/assets/338fddeb-cab8-41b1-bc80-d566cfb08fe0)

![Screenshot 2024-09-02 133221](https://github.com/user-attachments/assets/b63c282e-23dc-4b00-9eb3-79e9e5396f36)

### viii) RGB and BGR to YCrCb
```python
import cv2 as cv
# Load and resize the image
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (720, 720))
   
# Convert RGB to YCrCb
ycrcb_image = cv.cvtColor(image, cv.COLOR_RGB2YCrCb)
   
# Display the YCrCb image
cv.imshow('YCrCb Image', ycrcb_image)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 133449](https://github.com/user-attachments/assets/c159b6ae-dbdc-4d3b-bfc8-6c0e9d3ff02d)

### ix) Split and merge RGB Image
```python
import cv2 as cv
    
# Load and resize the image
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (720, 720))
    
# Split and merge the channels
blue, green, red = cv.split(image)
merged_image = cv.merge([blue, green, red])
    
# Display the images
cv.imshow('Original Image', image)
cv.imshow('Merged Image', merged_image)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 133736](https://github.com/user-attachments/assets/86febec5-993d-4c77-8bbb-c3e74dfefafb)

### x) Split and merge HSV Image
```python
import cv2 as cv
    
# Load and resize the image
image = cv.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\fie.jpg")
image = cv.resize(image, (720, 720))
   
# Convert BGR to HSV and split channels
hsv_image = cv.cvtColor(image, cv.COLOR_BGR2HSV)
hue, saturation, value = cv.split(hsv_image)
    
# Merge the channels back
merged_hsv_image = cv.merge([hue, saturation, value])
merged_bgr_image = cv.cvtColor(merged_hsv_image, cv.COLOR_HSV2BGR)
    
# Display the images
cv.imshow('Original HSV Image', hsv_image)
cv.imshow('Merged BGR Image', merged_bgr_image)
cv.imshow('Merged HSV Image', merged_hsv_image)
cv.waitKey(0)
cv.destroyAllWindows()
```

![Screenshot 2024-09-02 133944](https://github.com/user-attachments/assets/c1da0e41-eed1-4159-8da4-74cf050e4c06)

![Screenshot 2024-09-02 133931](https://github.com/user-attachments/assets/369e3690-e67d-452a-b12b-ef028f2be43c)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







