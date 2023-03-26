# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save an image as scolor.jpeg

### Step2:
Use imread to read and display the image

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and view the output image windows

## Program:
```
# Developed By: Y SHAVEDHA
# Register Number:212221230095
```
```
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('img3.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```
#Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
```
#CONVERT HSV TO RGB AND BGR
#HSV TO RGB
rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2,destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2,destroyAllWindows()
```
```
# CONVERT RGB AND BGR TO YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# SPLIT AND MERGE RGB IMAGE
blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()
```
```
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
```

## Output:
### 1. Original image
<img width="350" alt="op1" src="https://user-images.githubusercontent.com/93427376/227774407-d5fba941-33e7-424e-a307-1f348e445ce3.png">

### 2. BGR and RGB to HSV and GRAY
### i) BGR TO HSV
<img width="350" alt="bgr2hsv" src="https://user-images.githubusercontent.com/93427376/227774503-6bd820b0-365f-44ee-a0af-eb63d069b014.png">

### ii) BGR TO GRAY
<img width="344" alt="bgr2gray" src="https://user-images.githubusercontent.com/93427376/227774510-3b4928f9-ee1e-4dd0-91ed-7b5f1689c4ce.png">

### iii) RGB TO HSV
<img width="347" alt="rgb2hsv," src="https://user-images.githubusercontent.com/93427376/227774517-267e784f-91b5-465d-97c8-07f64135ba97.png">

### iV) RGB TO GRAY
<img width="346" alt="rgb2gray" src="https://user-images.githubusercontent.com/93427376/227774528-b3f39a75-b801-432c-8f8d-2f50c1f3e250.png">

### 3. HSV to RGB and BGR
### i) HSV TO RGB
<img width="346" alt="hsv2rgb" src="https://user-images.githubusercontent.com/93427376/227774571-ec6d05ee-a1bc-4ec0-a4de-43997d3652a0.png">

### ii) HSV TO BGR
<img width="346" alt="hsv2bgr" src="https://user-images.githubusercontent.com/93427376/227774583-bbc88e56-7464-4503-843b-078ea467ccb0.png">


### 4. RGB and BGR to YCrCb
### i) RGB TO YCrCb
<img width="346" alt="rgb2ycrcb" src="https://user-images.githubusercontent.com/93427376/227774622-d0ea8841-06b1-420b-9e68-3881979f4a6c.png">

### ii) BGR TO YCrCB
<img width="344" alt="bgrycrcb" src="https://user-images.githubusercontent.com/93427376/227774635-ac9e54c1-2d12-48a0-9453-521847dbc002.png">


### 5. Split and merge RGB Image
<img width="960" alt="split" src="https://user-images.githubusercontent.com/93427376/227774654-108bc85b-3aa7-4db1-afe7-dfc000ab9cc9.png">


### 6. Split and merge HSV Image
<img width="960" alt="splithsvl" src="https://user-images.githubusercontent.com/93427376/227774672-24e44402-12de-4ad3-b74b-489cb1be4662.png">

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
