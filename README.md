# Object-Tracking

This repository contains code for object detection and tracking in videos using the YOLOv11 object detection model and the DeepSORT algorithm.

## Prerequisite
Need the python wrapper for the zed2.
```
https://www.stereolabs.com/docs/app-development/python/install
```

## Installation
1. Clone this repository:
  ```
   git clone https://github.com/sujanshresstha/Object-Tracking.git
   cd Object-Tracking
  ```
2. Create new environment
  - Using pip
  ```
  python3 -m virtualenv -p python3.11 yolov10-deepsort
  source yolov10-deepsort/bin/activate
  pip install -r requirements.txt
  ```
3. Download model weight
  ```
   mkdir -p weights
   wget -P weights -q https://github.com/ultralytics/assets/releases/download/v8.3.0/yolo11x.pt
   ls -lh weights
  ```
4. Run the code:
   ```
   # Run object tracking
   python object_tracking.py --video ./data/test.mp4 --output ./output/output.mp4

   # Run object tracking on webcam (set video flag to 0)
   python object_tracking.py --video 0 --output ./output/webcam.mp4
