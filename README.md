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

## i) Write the frame as JPG file
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```



## ii) Display the video
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```



## iii) Display the video by resizing the window

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iv) Rotate and display the video



```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()







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
