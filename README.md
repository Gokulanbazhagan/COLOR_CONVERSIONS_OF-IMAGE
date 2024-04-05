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

##### Program:
### Developed By:Gokularamanan k
### Register Number: 212222230040


## Output:

### i) Read and display the image
input:
```
import numpy as np
import cv2
image=cv2.imread('dip.jpeg',1)
image=cv2.resize(image,(400,300))
cv2.waitKey(0)
cv2.destroyAllWindows()
```
output:

![Screenshot 2024-02-15 093819](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/f92015f1-d3b8-4804-81e1-6aea79981445)




### ii)Write the image

input:

```
#ex1 color to rgb
img=cv2.imread("rcb.jpg")
print(img.shape)

```
output:

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/c9369091-37c5-4081-891a-cd64a8016ee1)




### iii)Shape of the Image

input:

```

img=cv2.imread("rcb.jpg")
print(img.shape)

```

output:

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/7aaea9ac-2a9c-4760-92df-012d99ff1391)


### iv)Access rows and columns

input:

```
    import random
    image=cv2.imread('rcb.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

```

output:

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/56702a79-e681-4fef-8ed5-86945cbfcbe9)

### v)Cut and paste portion of image

input:
```
   image=cv2.imread('rcb.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()

```

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/f6a5c71f-d2a6-4b07-a7b3-98dadbe8c351)


### vi) BGR and RGB to HSV and GRAY

```

img = cv2.imread('rcb.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
output:
![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/4a6b0b9a-77ce-4706-abcf-280481d3947c)


### vii) HSV to RGB and BGR
```

img = cv2.imread('rcb.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()


```

output:

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/324e7f5c-8f39-4059-a21b-53c45c793d81)


### viii) RGB and BGR to YCrCb

```

img = cv2.imread('rcb.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()


```

output:

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/fbc77567-2d0d-4922-85ae-282e195ea2ec)


### ix) Split and merge RGB Image

```

img = cv2.imread('rcb.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/17b52254-31c8-4d1c-bb7e-e126247566e0)


### x) Split and merge HSV Image
```

img = cv2.imread("rcb.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
output:

![image](https://github.com/Gokulanbazhagan/COLOR_CONVERSIONS_OF-IMAGE/assets/119518996/5d90208d-761c-4779-94eb-7960b35bf403)






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







