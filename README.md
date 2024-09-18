# Exercise-Counter-using-MediaPipe-Human-Pose-Estimation-and-OpenCV

## Technology 
### MediaPipe 
MediaPipe is an open-source machine learning framework developed by Google. It provides a suite of pre-built solutions for computer vision and machine learning tasks one of them being human pose detection. MediaPipe's pose detection solution uses a deep learning model trained on a large dataset of human pose examples to estimate the positions of key points on a human body. These key points, also known as landmarks. It detects 33 landmarks:
<img width="353" alt="image" src="https://github.com/user-attachments/assets/dfcb94ea-b065-43e6-98f1-3e9182a1e1d8">

The landmarks are detected using a convolutional neural network (CNN) that has been trained on a large dataset of labelled images and videos of human poses. The CNN takes as input an image or video frame and outputs a set of confidence scores indicating the likelihood that each landmark is present at a particular location. These confidence scores are then used to estimate the final positions of the landmarks.
Usage: The input (an image or video stream) is fed to the Human Pose Estimation Model and the positions of the key points are displayed in real-time. This can detect human poses, track movements, and recognize specific gestures making it useful for applications such as fitness tracking, gaming, and virtual try-on. MediaPipe's combination of accuracy, speed, ease of use, and customizability makes it a high-performance and powerful tool. 

### OpenCV
OpenCV (Open Source Computer Vision Library) is an open-source computer vision and machine learning software library. It can be used to capture video feed from a variety of sources, such as webcams, USB cameras, and IP cameras. It provides a simple and easy-to-use interface for accessing video streams and capturing frames in real-time and a wide range of tools and algorithms for image and video processing, object detection and tracking for instance.


## Introduction
The project uses the Human Pose Estimation Model from MediaPipe to detect landmarks from a live camera feed. OpenCV is used for capturing the feed. Angles between the relevant joints are calculated for two exercises namely - donkey kicks and weight lifts. Base conditions and logic are built with respect the calculated angles to decide if the movement detected corresponds to the respective exercise. Angles formed by the key points are displayed in real time and a counter display is used to show the number of times the exercise has been correctly performed. OpenCV is also used for these visualisations.

## Methodology
- Importing relevant packages and initializing MediaPipe instances 
- Initializing counter and stage variables. Counter keeps count of the number of times exercise has been done correctly. - -- Each exercise has 2 stages - task has been completed once if both stages have been reached once each.
- Capturing live camera feed using OpenCV and creating a loop of frames for which
- Convert BGR to RGB format (recoloring)
- Make detections
- Converting RGB to BGR (recoloring)
- Extract the landmarks (as per given 33 key points)
- Get coordinates of relevant landmarks
- Calculate angles between the landmarks 
- Build logic to detect task completion 
- Visuals on live feed: Display the counter box and value; Display the angle values in real time 
render the detections and display the same on live feed 
- Close camera by hitting q
Note: The same procedure is repeated for the both exercises with relevant key points and logic.
