# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv.

### Step2:
Read the original Image.

### Step3:
Store the required conversion of the image in a variable.

### Step4:
Show the image stored in the given variable.

### Step5:
Destroy all the windows and end the program.

## Program:
```
# Developed By:DHANUMALYA D
# Register Number:212222230030
```
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
houseImage = cv2.imread('dip1.jpeg')
cv2.imshow('Original Image',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# ii)Convert HSV to RGB and BGR
```
import cv2
houseHSVImage = cv2.imread('dip1.jpeg')
cv2.imshow('Original HSV Image',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iii)Convert RGB and BGR to YCrCb
```
import cv2
houseImage = cv2.imread('dip1.jpeg')
cv2.imshow('Original Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('dip1.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# v) Split and merge HSV Image
```
import cv2
image = cv2.imread('dip1.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow

```

## Output:

### i) BGR and RGB to HSV and GRAY

![Screenshot from 2023-08-18 14-07-09](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/a47ee657-b3b8-460f-aac2-46da207a23ab)

![Screenshot from 2023-08-18 14-07-56](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/59ab8278-3316-4e86-8d51-c6eb26b10f58)

![Screenshot from 2023-08-18 14-08-10](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/ced420dd-2528-40f1-917a-9b81a629b2a4)

![Screenshot from 2023-08-18 14-08-24](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/4059e5be-066b-4fb8-bc4b-72c1026535cb)

![Screenshot from 2023-08-18 14-08-35](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/15a2cae1-ed60-4a26-b67c-a03bc36d01d1)

![Screenshot from 2023-08-18 14-08-48](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/4875165b-1bf6-41d4-9967-deccaff3701a)


### ii) HSV to RGB and BGR

![Screenshot from 2023-09-07 23-20-32](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/41a4b32c-1d89-46d1-b26d-5a7219035008)

![Screenshot from 2023-09-07 23-20-41](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/153e1909-4ac7-4da1-b806-551eae7c3f77)

![Screenshot from 2023-09-07 23-20-49](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/8de9bf5a-b04b-43f6-9ceb-b0de04ef2a57)

![Screenshot from 2023-09-07 23-21-11](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/30d10eab-8e47-47dc-b619-64b17cc8c0d3)

### iii) RGB and BGR to YCrCb

![Screenshot from 2023-09-07 23-23-23](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/d6e968c9-72a3-4826-878d-cfd2548c186e)

![Screenshot from 2023-09-07 23-23-32](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/c4246a88-e598-4b91-bf60-dff632246681)

![Screenshot from 2023-09-07 23-23-40](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/d1bd3a6f-dc3b-4e61-843b-bdbf016d728d)


![Screenshot from 2023-09-07 23-23-55](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/e3f76683-080c-43fe-9eef-40fd2cd8d02c)

![Screenshot from 2023-09-07 23-24-10](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/a521e68d-2548-49ed-b937-3adc4f1c659a)


### iv) Split and merge RGB Image

![Screenshot from 2023-09-07 23-27-30](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/701947e7-05c8-469e-b2d1-2c72e1396355)

![Screenshot from 2023-09-07 23-27-41](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/b26d17d3-1fa3-4c3c-b5e0-f199ef9ac6ff)

![Screenshot from 2023-09-07 23-27-52](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/b7204559-bdba-427b-a621-c6e7aa28f325)


![Screenshot from 2023-09-07 23-28-04](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/1db32480-9386-4cb1-96a4-f583a8317ee8)

![Screenshot from 2023-09-07 23-28-14](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/bf54e850-a0d0-46ba-addd-eb2096e3455a)



### v) Split and merge HSV Image

![Screenshot from 2023-08-18 14-30-40](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/f95182be-f1d1-4f07-adf6-018b58eb9f66)

![Screenshot from 2023-08-18 14-30-50](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/84d4b608-ae0a-408b-8344-b7f9012f7e48)

![Screenshot from 2023-08-18 14-30-59](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/540c57e1-394f-4ba7-bef7-62f0bb060859)

![Screenshot from 2023-08-18 14-31-10](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/cef44121-ef29-4822-89c2-4a5c2648ffb3)

![Screenshot from 2023-08-18 14-31-20](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/e2e77dde-2974-4965-9442-79561b668ba5)

## Result:

Thus the color conversion was performed between RGB, HSV and YCbCr color models.
