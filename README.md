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
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iii)Convert RGB and BGR to YCrCb
```
import cv2
houseImage = cv2.imread('dip1.jpeg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
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
cv2.imshow('Merged BGR image',mergeBgr)
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

![Screenshot from 2023-08-18 14-16-50](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/bb9057f3-8562-40ad-8fb3-41ad51c0dd02)

![Screenshot from 2023-08-18 14-17-02](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/be4840d3-b199-4905-93fd-b678d28fa6c7)

![Screenshot from 2023-08-18 14-17-13](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/f1844ef3-ffd7-4028-b228-b1a6f4ef7107)

![Screenshot from 2023-08-18 14-17-54](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/67275b8d-ecc0-45a4-a18c-0972d1f5dbf3)

### iii) RGB and BGR to YCrCb

![Screenshot from 2023-08-18 14-22-09](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/6a6799a9-670a-4928-b55c-1cda9e3ffb95)

![Screenshot from 2023-08-18 14-22-23](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/a334914d-a4d8-4efe-849c-50ef680904c9)

![Screenshot from 2023-08-18 14-22-37](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/1ad94016-815e-4bcd-93be-deb857fcdaf5)

![Screenshot from 2023-08-18 14-22-59](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/e0ed4a45-b53b-4cd5-b196-8adf77b6414c)

### iv) Split and merge RGB Image

![Screenshot from 2023-08-18 14-27-04](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/e81eabb7-e94c-4215-9aaa-bf18e6a5b9ba)

![Screenshot from 2023-08-18 14-27-15](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/91d449ed-b6a5-468a-964b-0d5e1d293244)

![Screenshot from 2023-08-18 14-27-26](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/fd1fe62d-4333-411a-8483-bbb833b84974)

![Screenshot from 2023-08-18 14-27-39](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/2e566a81-d10f-4cd9-bbae-52053c853bfc)

![Screenshot from 2023-08-18 14-27-57](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/fd9cc3fe-9e11-4440-bd03-25592697f9bf)

### v) Split and merge HSV Image

![Screenshot from 2023-08-18 14-30-40](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/f95182be-f1d1-4f07-adf6-018b58eb9f66)

![Screenshot from 2023-08-18 14-30-50](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/84d4b608-ae0a-408b-8344-b7f9012f7e48)

![Screenshot from 2023-08-18 14-30-59](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/540c57e1-394f-4ba7-bef7-62f0bb060859)

![Screenshot from 2023-08-18 14-31-10](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/cef44121-ef29-4822-89c2-4a5c2648ffb3)

![Screenshot from 2023-08-18 14-31-20](https://github.com/Dhanudhanaraj/COLOR-CONVERSION/assets/119218812/e2e77dde-2974-4965-9442-79561b668ba5)

## Result:

Thus the color conversion was performed between RGB, HSV and YCbCr color models.
