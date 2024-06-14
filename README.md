# YOLOv10-Object-Tracking-with-DeepSORT

This project demonstrates a complete pipeline for real-time object detection and tracking using YOLOv10 and DeepSORT. It processes video input, detects objects, tracks them across frames, and provides optional blurring for specific object classes.

## Features

- Object Detection: Utilizes YOLOv10 for high-accuracy real-time object detection.
- Object Tracking: Employs DeepSORT for robust multi-object tracking.
- Customizable Confidence Threshold: Allows users to set a confidence threshold for object detection.
- Class-Specific Tracking: Enables tracking and counting of specific object classes.
- Gaussian Blur: Optionally applies Gaussian blur to detected objects of a specified class.
- Real-time Performance Logging: Logs processing time for each frame and overall class counts.

### Requirements

- Python 3.x
- OpenCV
- PyTorch
- NumPy
- absl-py
- deep_sort_realtime
- ultralytics

## Installation

1. Clone the repository:
   ```git clone https://github.com/your_username/yolo_deepsort.git
  cd yolo_deepsort```
