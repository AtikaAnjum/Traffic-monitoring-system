# Traffic monitoring system using stereo cameras to detect vehicles

This project implements a **vehicle detection and depth estimation system** for traffic monitoring using **stereo vision** and **deep learning**.  
By combining **YOLOv5** (for object detection) and **OpenCV Stereo Matching** (for depth estimation), the system can detect vehicles and estimate their distance from the camera.

---

##  Project Overview

Traffic monitoring is crucial for modern smart cities to analyze congestion, detect violations, and improve road safety.  
This system uses two stereo images (left and right camera frames) to:

1. **Detect vehicles** using a pretrained YOLOv5 model.
2. **Compute disparity maps** using stereo images.
3. **Estimate distance (depth)** of each detected vehicle from the camera.

---

##  Methodology

### 1. **Vehicle Detection (YOLOv5)**
- YOLOv5s model (`yolov5s.pt`) is used for real-time object detection.
- Detects vehicles such as cars, buses, and trucks with bounding boxes and confidence scores.

### 2. **Disparity Map Calculation**
- Converts stereo images to grayscale.
- Uses **OpenCV StereoBM** algorithm to compute disparity (pixel difference between stereo pairs).

### 3. **Depth Estimation**
- Computes depth using: Depth = (focal_length × baseline) / disparity
 
- Larger disparity -> object is closer to the camera.

---



