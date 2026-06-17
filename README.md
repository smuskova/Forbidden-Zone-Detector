# README

````markdown
# Forbidden Zone Detector

## Overview

Forbidden Zone Detector is an intelligent video analytics system designed to detect, track, and analyze pedestrians entering restricted or hazardous areas using artificial intelligence and computer vision technologies.

The system combines YOLOv8 object detection, Kalman Filter tracking, risk assessment algorithms, temporal behavior analysis, and automated reporting to provide real-time monitoring of unauthorized access to protected zones.

This project was developed as part of a Master's Degree thesis in Cybersecurity.

---

## Features

### Human Detection
- Real-time pedestrian detection using YOLOv8
- High detection accuracy and fast inference speed

### Object Tracking
- Kalman Filter-based tracking
- Smooth object movement prediction between detections
- Reduced tracking instability

### Dual-Zone Security Architecture
- Warning Zone (Yellow)
- Violation Zone (Red)

The system distinguishes between approaching individuals and actual intrusions.

### Intelligent Risk Assessment
Dynamic risk score calculation based on:

- Zone occupancy
- Dwell time
- Movement speed
- Crowd density
- Predicted future movement

Risk levels:
- LOW
- MEDIUM
- HIGH

### Predictive Analytics
The system predicts whether a person is likely to enter a forbidden zone before the violation occurs.

### Person Re-Identification (Re-ID)
- Detects returning individuals
- Prevents duplicate counting
- Improves statistical accuracy

### Heatmap Generation
Automatically generates movement heatmaps showing:

- Frequently used paths
- High-risk areas
- Violation hotspots

### Automated Reporting
Generates:

- Annotated output video
- CSV violation logs
- Heatmap images
- Interactive HTML reports

### Email Notifications
Optional real-time alerts containing:

- Screenshot evidence
- Timestamp information
- Violation details

### Temporal Pattern Analysis
Analyzes violation frequency over time and identifies peak-risk periods.

---

## System Architecture

```text
Input Video
      │
      ▼
YOLOv8 Detection
      │
      ▼
Kalman Tracking
      │
      ▼
Zone Evaluation
      │
      ├── Warning Zone
      └── Violation Zone
      │
      ▼
Risk Assessment Engine
      │
      ▼
Event Logging
      │
      ├── CSV Reports
      ├── HTML Dashboard
      ├── Heatmaps
      └── Email Alerts
````

---

## Technologies Used

* Python
* YOLOv8 (Ultralytics)
* OpenCV
* NumPy
* Kalman Filter Tracking
* Computer Vision
* Machine Learning

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/Forbidden-Zone-Detector.git
cd Forbidden-Zone-Detector
```

### Install Dependencies

```bash
pip install ultralytics
pip install opencv-python
pip install numpy
```

or

```bash
pip install -r requirements.txt
```

---

## Usage

Run with graphical file selection:

```bash
python forbidden_zone_detector.py
```

Run from command line:

```bash
python forbidden_zone_detector.py --input video.mp4
```

Example:

```bash
python forbidden_zone_detector.py \
    --input railway.mp4 \
    --model yolov8s.pt \
    --conf 0.4
```

---

## Output Files

After analysis the system generates:

| File             | Description            |
| ---------------- | ---------------------- |
| *_detected.mp4   | Annotated output video |
| *_violations.csv | Violation log          |
| *_heatmap.png    | Movement heatmap       |
| *_report.html    | Interactive report     |

---

## Applications

* Railway safety monitoring
* Trespassing detection
* Smart city surveillance
* Industrial safety systems
* Critical infrastructure protection
* Security operations centers
* Public safety monitoring

---

## Research Contribution

Unlike conventional object detection systems, this project extends video analytics by integrating:

* Predictive risk analysis
* Dynamic risk scoring
* Temporal behavior analysis
* Person re-identification
* Automated incident reporting

The result is a complete intelligent surveillance solution capable of supporting security personnel in real-world environments.

---

## Author

Seyhan Muskova

Master's Degree in Cybersecurity

Technical University in Sofia

---

## License

This project was developed for academic and research purposes.

```
