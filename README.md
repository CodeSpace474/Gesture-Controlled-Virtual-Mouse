# Gesture Controlled Virtual Mouse

## Project Description

Gesture Controlled Virtual Mouse is a computer vision based application that allows users to control the computer cursor using hand gestures detected through a webcam. Instead of using a traditional mouse or touchpad, the user can move their index finger to control the cursor and perform clicks using a pinch gesture.

The system uses real-time hand tracking to detect the position of the index finger and thumb. Cursor movement is mapped to the screen coordinates, and when the thumb and index finger come close together, a mouse click is triggered.

This project demonstrates how machine learning powered hand tracking can be used to create a touchless human-computer interaction system.

## Objective

The main objective of this project is to develop a gesture-based mouse controller that replaces traditional input devices using computer vision and hand gesture recognition.

The project also demonstrates practical applications of machine learning models in real-time user interfaces.

## Features

* Real-time hand tracking using webcam
* Cursor control using index finger movement
* Pinch gesture detection for mouse click
* Smooth cursor movement using interpolation
* Screen coordinate mapping
* Adjustable movement smoothing
* Reduced camera resolution for faster performance
* Real-time visual feedback through camera window
* Press 'Q' key to exit the program

## Technologies and Libraries Used

Python 3

Libraries:

* OpenCV (cv2) – Used for webcam capture and image display
* MediaPipe – Used for machine learning based hand landmark detection
* PyAutoGUI – Used to control the system mouse cursor and perform clicks
* NumPy – Used for mathematical calculations and coordinate mapping
* OS – Used to locate the hand tracking model file

## Machine Learning Model

The program uses the MediaPipe Hand Landmarker model to detect and track hand landmarks.

The model identifies multiple points on the hand such as fingertips, joints, and wrist. The program primarily uses the following landmarks:

Landmark 8 – Index finger tip (used for cursor movement)
Landmark 4 – Thumb tip (used for click detection)

Required model file:
hand_landmarker.task

The model file must be placed in the same directory as the Python script.

## How the Program Works

1. The webcam captures live video frames.
2. MediaPipe processes the frames to detect hand landmarks.
3. The index finger tip position is extracted and mapped to screen coordinates.
4. Cursor movement is smoothed to avoid jitter.
5. The thumb and index finger distance is measured.
6. When the distance between them becomes very small (pinch gesture), a mouse click is triggered.
7. The cursor moves smoothly across the screen following the finger movement.

## Gesture Controls

Move Index Finger
Controls the mouse cursor movement.

Pinch Gesture (Thumb + Index Finger)
Triggers a left mouse click.

## Keyboard Controls

Press **Q**
Exit the application.

## How to Run the Program

Step 1: Install required Python libraries

pip install opencv-python mediapipe pyautogui numpy

Step 2: Download the MediaPipe hand tracking model

hand_landmarker.task

Step 3: Place the model file in the same directory as the Python script.

Step 4: Run the program

python gesture_mouse.py

Step 5: Allow webcam access.

The webcam window will open and the system will start tracking your hand.

## System Requirements

* Python 3.8 or later
* Webcam
* Screen resolution supported by PyAutoGUI
* Basic CPU capable of real-time video processing

## Possible Improvements / Future Work

* Add support for right-click and double-click gestures
* Implement scroll gesture using two fingers
* Add drag-and-drop gesture support
* Improve gesture recognition accuracy
* Add visual hand landmark overlays
* Allow adjustable sensitivity and smoothing
* Add multi-hand gesture controls

## Conclusion

This project demonstrates how computer vision and machine learning can be used to replace traditional input devices with natural hand gestures. By combining MediaPipe hand tracking with PyAutoGUI, the application enables intuitive and touchless control of the computer mouse.
