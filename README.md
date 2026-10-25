# EXP-2-Record-Image-Acquisition-using-Web-Camera
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.

i) Write the frame as JPG 

ii) Display the video 

iii) Display the video by resizing the window

iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>
Import OpenCV Package.

### Step 2:
<br>
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
<br>
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
<br>
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
<br>
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
<br>
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.

## Program:
### Developed By: SANTHIYA B
### Register No: 212224230247
``` Python

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


## ii) Display the video

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

## iii) Display the video by resizing the window


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
  
## iv) Rotate and display the video

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
<img width="716" height="528" alt="image" src="https://github.com/user-attachments/assets/92a74bd8-85b6-4075-b890-3b6582025202" />



</br>


### ii) Display the video
</br>
<img width="673" height="520" alt="image" src="https://github.com/user-attachments/assets/24bd7dac-c4d7-4971-b509-06aea987e8cc" />



</br>


### iii) Display the video by resizing the window
</br>

<img width="393" height="492" alt="image" src="https://github.com/user-attachments/assets/5dfec15a-dd45-478b-947f-0ac361fe7437" />



</br>



### iv) Rotate and display the video
</br>
<img width="382" height="497" alt="image" src="https://github.com/user-attachments/assets/c3ce3b27-577c-449a-96cd-da8b9d872c5f" />



</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
