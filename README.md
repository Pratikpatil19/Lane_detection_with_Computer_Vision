Autonomous Car Lane Detection with Raspberry Pi
This repository contains a project demonstrating autonomous car lane detection and steering control using Raspberry Pi. It employs a Raspberry Pi camera, stepper motors, and the OpenCV library to detect lanes and adjust the steering of the car.

Features
Real-time Lane Detection: Uses HSV color filtering, Canny edge detection, and Hough Line Transform to detect lane lines in real-time from a video feed.
Autonomous Steering: Adjusts the steering angle based on the detected lanes, allowing the car to follow lanes automatically.
Hardware Components
Raspberry Pi (any recent model with GPIO support)
Raspberry Pi Camera
Stepper Motor
Servo Motor
Motor Driver Board
Power Supply (e.g., battery pack)
Code Overview
The code is organized as follows:

Image Processing: Captures frames from the camera and applies image processing techniques using OpenCV.
Lane Detection:
HSV Color Filtering: Filters the blue lane lines.
Canny Edge Detection: Detects the edges in the filtered image.
Hough Line Transform: Detects lane lines based on the edges.
Steering Calculation: Determines the angle required to steer based on the lane lines detected.
Motor Control: Adjusts the speed and steering of the car using the detected lane information.
Datasets
No external datasets are required for this project as it processes live video feed from the camera mounted on the Raspberry Pi.

Installation
To run this project, you need to install the following libraries on your Raspberry Pi:

OpenCV
NumPy
Imutils

You can install these libraries using pip: pip install opencv-python numpy imutils
Usage
1.Hardware Setup: Connect the camera, motors, and motor driver to the Raspberry Pi following the wiring diagram provided in the project documentation.
2.Run the Script: Start the lane detection and autonomous driving by running: python ptowncar_final.py
3.The car will start moving and adjust its steering based on the detected lane lines.
How it Works
The camera captures real-time video frames, which are processed using HSV color filtering to isolate the blue lane lines.
Canny edge detection is applied to highlight the edges, followed by Hough Line Transform to detect lane lines.
The steering angle is computed based on the position and slope of the detected lines, and the car adjusts its direction accordingly.
Requirements
Raspberry Pi (with Raspbian OS installed)
Raspberry Pi Camera Module
Stepper Motor and Servo Motor for driving and steering control
Future Enhancements
Obstacle Detection: Add obstacle detection sensors to avoid collisions.
Advanced Lane Detection: Improve lane detection for curved roads and different lighting conditions.
GPS Navigation: Integrate GPS to allow the car to follow a pre-defined route.
