# Image Acqusition using Web Camera
## Aim
 
#### To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
##### i) Write the frame as JPG 
##### ii) Display the video 
##### iii) Display the video by resizing the window
##### iv) Rotate and display the video

## Software 

### Anaconda - Python 3.7

## Algorithm

### Step 1:

#### Use cv2.VideoCapture(0) to access web camera

### Step 2:

#### Use cv2.imread to read the video or image

### Step 3:

#### Use cv2.imwrite to save the image

### Step 4:

#### Use cv2.imshow to show the video

### Step 5:

End the program and close the output video window by pressing 'q'.

## Program:

### Developed By: SANJAY T
### Register No: 212222110039

#### i) Write the frame as JPG file
```py
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("San.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
#### ii) Display the video
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('flower',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

#### iii) Display the video by resizing the window
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222110039-Sanjay',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
#### iv) Rotate and display the video

```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222110039_sanjay',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
</br>

![1](https://github.com/sanjaythiyagarajan/Image_Acqusition-_using_Web_Camera/assets/119409242/f5407c87-cacd-4aec-8cfd-0df17c079035)


</br>


### ii) Display the video
</br>

![2](https://github.com/sanjaythiyagarajan/Image_Acqusition-_using_Web_Camera/assets/119409242/27088a80-228a-4642-8a96-00edfebdf485)


</br>


### iii) Display the video by resizing the window
</br>

![3](https://github.com/sanjaythiyagarajan/Image_Acqusition-_using_Web_Camera/assets/119409242/5fce98f0-2fb9-4943-a04c-739e157055a9)



</br>



### iv) Rotate and display the video
</br>

![4](https://github.com/sanjaythiyagarajan/Image_Acqusition-_using_Web_Camera/assets/119409242/24567224-c660-47f3-837c-5a4bc90e0fe0)


</br>





## Result:
### Thus the image is accessed from webcamera and displayed using openCV.
