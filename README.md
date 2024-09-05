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
img = cv2.imread(r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png")
resized_img = cv2.resize(img, None, fx=1, fy=1)
cv2.imshow('212223240087', resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-05 102324](https://github.com/user-attachments/assets/aec942ee-06bf-40ec-915e-385dba2fc812)

### ii)Draw Shapes and Add Text
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Draw a rectangle
cv2.rectangle(image, (50, 50), (200, 200), (0, 255, 0), 2)

# Draw a circle
cv2.circle(image, (300, 300), 50, (255, 0, 0), 2)

# Add text
cv2.putText(image, 'OpenCV', (100, 400), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 255), 2)

# Display the modified image
cv2.imshow('Shapes and Text', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-05 102145](https://github.com/user-attachments/assets/5526c3fa-6d63-47f5-832a-0e61cf24aaa2)

### iii)Image Color Conversion
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Convert to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('Grayscale Image', gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Convert to HSV
hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('HSV Image', hsv_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# Convert to grayscale
![Screenshot 2024-09-05 102507](https://github.com/user-attachments/assets/f867c7bc-e68b-409f-9867-29b5a3d7e822)

# Convert to HSV
![Screenshot 2024-09-05 102634](https://github.com/user-attachments/assets/a482d165-b872-4c1e-8a6f-0cefae25079d)

### iv)Access and Manipulate Image Pixels
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Access pixel at (100, 100)
pixel = image[100, 100]
print(f'Pixel value at (100, 100): {pixel}')

# Modify pixel value
image[100, 100] = [0, 0, 255]  # Set pixel to red

# Display the modified image
cv2.imshow('Modified Pixel Image', image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

![Screenshot 2024-09-05 103718](https://github.com/user-attachments/assets/39c2cf65-20d5-429f-95d5-3d9d82cd5bf9)

### v)Image Resizing
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Resize image to 300x300
resized_image = cv2.resize(image, (300, 300))
cv2.imshow('Resized Image', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-05 103853](https://github.com/user-attachments/assets/162f4cc9-9207-4826-b7ee-751dcdc2671d)

### vi)Image Cropping
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Crop the image
cropped_image = image[50:200, 50:200]
cv2.imshow('Cropped Image', cropped_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-05 104001](https://github.com/user-attachments/assets/2ddcf057-59d7-4f56-a8b6-f6a3c7ca854f)

### vii)Image Flipping
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Flip image horizontally
flipped_image = cv2.flip(image, 1)
cv2.imshow('Flipped Image', flipped_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-05 104119](https://github.com/user-attachments/assets/0ad29f6c-cce9-4f53-b2e0-674708c4202f)

### viii)Write and Save the Modified Image
```python
import cv2

# Read the image
image_path = r"C:\Users\admin\OneDrive\Pictures\wallpaper\passport size picA.png"
image = cv2.imread(image_path)

# Save the modified image
cv2.imwrite('modified_image.jpg', image)
print('Image saved as modified_image.jpg')
```

![Screenshot 2024-09-05 104246](https://github.com/user-attachments/assets/df53982d-f81c-4d03-9c4d-1038cd4f55a8)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







