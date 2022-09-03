# Face-Detection

#### Face detection is a computer technology being used in a variety of applications that identifies human faces in digital images. Face detection also refers to the psychological process by which humans locate and attend to faces in a visual scene.
---

![Images](FaceDet.png "Face Detection")

---

## 📃Installation
---

* Clone this repository in your local environment by running the code on your git bash.

`git clone https://github.com/YOUR-USERNAME/Face-Detection.git`

Now, Install the required **packages:**

* `pip install opencv-python`

OpenCV is a library of programming functions mainly aimed at real-time computer vision. Originally developed by Intel, it was later supported by Willow Garage then Itseez. The library is cross-platform and free for use under the open-source Apache 2 License.

Usage:

* To access your webcam through opencv

```python
import cv2

cap = cv2.VideoCapture(0)

while True:
    success, vid = cap.read()
    cv2.imshow("Video", vid)
    cv2.waitKey(1)
```

* To show fps count on the screen

```python
import time
import cv2 as cv

pTime = 0
cTime = time.time()
fps = 1 / (cTime - pTime)
pTime = cTime
cv.putText(flipped, f'FPS:{int(fps)}', (10, 70),
               cv.FONT_HERSHEY_PLAIN, 3, (0, 255, 0), 2)
```


* `pip install mediapipe`

MediaPipe Face Detection is an ultrafast face detection solution that comes with 6 landmarks and multi-face support. It is based on BlazeFace, a lightweight and well-performing face detector tailored for mobile GPU inference. The detector’s super-realtime performance enables it to be applied to any live viewfinder experience that requires an accurate facial region of interest as an input for other task-specific models, such as 3D facial keypoint estimation (e.g., MediaPipe Face Mesh), facial features or expression classification, and face region segmentation. BlazeFace uses a lightweight feature extraction network inspired by, but distinct from MobileNetV1/V2, a GPU-friendly anchor scheme modified from Single Shot MultiBox Detector (SSD), and an improved tie resolution strategy alternative to non-maximum suppression. For more information about BlazeFace, please see the Resources section.

Usage:

```python
import mediapipe as md

mpFaceDetection = mp.solutions.face_detection
faceDetection = mpFaceDetection.FaceDetection()
mpDraw = mp.solutions.drawing_utils
```

![Face Detection](face_dec_gif.gif)