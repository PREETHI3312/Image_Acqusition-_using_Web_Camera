# Image_Acqusition-_using_Web_Camera
## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera.

### Step 2:
Use cv2.imread to read the video or image.

### Step 3:
Use cv2.imwrite to save the image.

### Step 4:
Use cv2.imshow to show the video.
### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:

### Developed By:PREETHI A K 
### Register No:212223230156

## i) Write the frame as JPG file
```
import cv2
import numpy as np
viedoCaptureObject=cv2.VideoCapture(0)
ret,frame=viedoCaptureObject.read()
cv2.imwrite("captured_frame.jpg",frame)
viedoCaptureObject.release()
cv2.destroyAllWindows()
```



## ii) Display the video
```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
cv2.imshow('captured_frame', frame)
cv2.waitKey(10000)
cap.release()
cv2.destroyAllWindows()
```



## iii) Display the video by resizing the window

```
cap=cv2.VideoCapture(0)
ret,frame=cap.read()
width=int(cap.get(3))
height=int(cap.get(4))
image=np.zeros(frame.shape,np.uint8)
smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
image[:height//2, :width//2]=smaller_frame
image[height//2:, :width//2]=smaller_frame
image[:height//2, width//2:]=smaller_frame
image[height//2:, width//2:]=smaller_frame
cv2.imshow('',image)
cv2.waitKey(5000)  
image_dict = {'captured_image1': image}
cv2.imwrite('captured_image1.jpg', image)
cap.release()
cv2.destroyAllWindows()
```


## iv) Rotate and display the video



```
cap=cv2.VideoCapture(0)
ret,frame=cap.read()
width=int(cap.get(3))
height=int(cap.get(4))
image=np.zeros(frame.shape,np.uint8)
smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
image[height//2:, :width//2]=smaller_frame
image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
image[height//2:, width//2:]=smaller_frame
cv2.imshow('',image)
cv2.waitKey(5000) 
image_dict = {'captured_image2': image}
cv2.imwrite('captured_image2.jpg', image)
cap.release()
cv2.destroyAllWindows()







```
## Output

### i) Write the frame as JPG image
</br>
<img width="630" height="510" alt="image" src="https://github.com/user-attachments/assets/b2e9c17b-f8e9-4472-bbe9-1faf7d4e88f8" />


</br>


### ii) Display the video
</br>

<img width="616" height="469" alt="image" src="https://github.com/user-attachments/assets/bdc5231c-59f4-4d9a-8832-6f7f379be8fc" />


</br>


### iii) Display the video by resizing the window
</br>
<img width="307" height="466" alt="image" src="https://github.com/user-attachments/assets/2b93cb8b-a1ed-4f17-a907-726102a99b26" />

</br>



### iv) Rotate and display the video
</br>
<img width="353" height="474" alt="image" src="https://github.com/user-attachments/assets/d5611fa0-af76-4cef-b12f-5f6a2650338b" />

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
