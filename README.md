# YOLOv10-Object-Tracking-with-DeepSORT

This project demonstrates a complete pipeline for real-time object detection and tracking using YOLOv10 and DeepSORT. It processes video input, detects objects, tracks them across frames, and provides optional blurring for specific object classes.

### Features

- Object Detection: Utilizes YOLOv10 for high-accuracy real-time object detection.
- Object Tracking: Employs DeepSORT for robust multi-object tracking.
- Customizable Confidence Threshold: Allows users to set a confidence threshold for object detection.
- Class-Specific Tracking: Enables tracking and counting of specific object classes.
- Gaussian Blur: Optionally applies Gaussian blur to detected objects of a specified class.
- Real-time Performance Logging: Logs processing time for each frame and overall class counts.

### Requirements

- Python >= python3.9
- OpenCV
- PyTorch
- NumPy
- absl-py
- deep_sort_realtime
- ultralytics

## Installation

1.   Make a folder and open an integrated terminal. 
2.   Clone the Yolov10 repo:</br>
      ```https://github.com/THU-MIG/yolov10```</br>
      ```cd yolov10```</br>
     ```pip install .```
3.   Clone the repository (In the integrated folder you created):</br>
   ```git clone https://github.com/your_username/yolo_deepsort.git```

## Usuage

Run the script with the following command:</br>
```python track_objects.py --video <path_to_video_or_webcam_index> --output <output_video_path> --conf <confidence_threshold> --blur_id <class_id_to_blur> --class_id <class_id_to_track>```

### Command-Line Flags

- --video: Path to input video file or webcam index (default: ./data/test_1.mp4).
- --output: Path to save the output video (default: ./output/output.mp4).
- --conf: Confidence threshold for object detection (default: 0.25).
- --blur_id: Class ID to apply Gaussian blur (default: None).
- --class_id: Class ID to track (default: None).

## Code Overview

### Initialization
- Logging Setup: Configures logging for the script.
- Command-Line Flags: Defines flags for video input, output, confidence threshold, and specific class IDs for blurring and tracking.

### Functions 

- initialize_video_capture: Initializes video capture from file or webcam.
- initialize_model: Loads YOLOv10 model and sets the appropriate device (CPU/GPU).
- load_class_names: Loads class names from a file.
- process_frame: Processes each frame to detect objects using YOLOv10 and tracks them with DeepSORT.
- draw_tracks: Draws bounding boxes and labels on the frame, and applies Gaussian blur if specified.

### Main Logic

- main: The main function that ties everything together. It initializes video capture, model, and other resources, processes each frame for object detection and tracking, and handles saving the output video.

## Logging and Output

- Frame Processing Time: Logs the time taken to process each frame.
- Class Counts: Logs the counts of each detected and tracked class at the end of the video.
