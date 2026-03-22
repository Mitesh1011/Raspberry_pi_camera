# Real-Time Object Detection with Raspberry Pi & MediaPipe

# **Overview**

This project implements real-time object detection using a Raspberry Pi camera, powered by MediaPipe Tasks API and OpenCV. The system captures live video, detects objects using a TensorFlow Lite model, and visualizes results with bounding boxes, labels, and confidence scores.

It is particularly useful for robotics applications, such as object recognition, automation, and intelligent systems.

**Features**

Live camera feed using Raspberry Pi Camera

Real-time object detection using MediaPipe

Bounding boxes with labels and confidence scores

Cropping and resizing detected objects

Optimized for embedded systems (Raspberry Pi)

**Technologies Used**

Python 3,
 OpenCV (cv2),
 NumPy,
 MediaPipe Tasks API,
 Picamera2,
 TensorFlow Lite (.tflite model)

**Project Structure**

├── main.py                # Main script

├── model_fp16.tflite     # Object detection model

├── README.md             # Documentation

# **Requirements & Installation**

**System Requirements**

Raspberry Pi (Recommended: Raspberry Pi 4)

Raspberry Pi OS (Bullseye or newer)

Python 3.9+

Raspberry Pi Camera Module

**Required Libraries**

**1. Install Python Dependencies**

```
pip install opencv-python numpy mediapipe
```

**2. Install Camera Support (Important)**

```
sudo apt update
sudo apt install python3-picamera2 libcamera-apps
```
**Model File**

You must include the following file in your project folder:

```
model_fp16.tflite
```

*🔹 Description*

A TensorFlow Lite object detection model
Used by MediaPipe to detect objects in real time

*🔹 Options*

Use a pre-trained model (recommended for testing)

Train your own custom model for specific objects (e.g., ping pong ball, rugby ball)

**Optional Setup (Recommended)**

*Create Virtual Environment*

```
python3 -m venv env
source env/bin/activate

```

*Upgrade pip*

```
pip install --upgrade pip

```

*Usage*

Run the program:

```
python main.py

```

Press *q* to quit the application.

**How It Works**

1. The Raspberry Pi camera captures live frames.

2. Each frame is converted into a MediaPipe-compatible format.

3. The TensorFlow Lite model performs object detection.

4. The system:

Draws bounding boxes

Displays object labels and confidence scores

Crops detected objects for further processing

5. Output is displayed in real time using OpenCV.

**Output**

Live video window titled "Detected Objects"

Bounding boxes around detected objects

Labels with confidence scores (e.g., Ball (0.87))

**Troubleshooting**

Camera not detected

*Run:*

```
sudo raspi-config```

Enable camera under *Interface Options*.

**Picamera2 not working**
```
sudo apt update && sudo apt upgrade
```

*Performance issues*

Reduce resolution (already set to 320x240)

Close background applications

**Future Improvements**

Add object tracking

Save detected images

Improve detection accuracy with custom models

Integrate with robotic systems (e.g., ball collection robot)

Add FPS (frames per second) display

**Contributing**

Feel free to fork this repository and submit pull requests.


**Author**

Mitesh Salvi

MEng (Hons) Intelligent Automation & Robotics

Edge Hill University