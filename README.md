
# Smart Security and Surveillance System

A real-time security monitoring system developed as a Computer Engineering capstone project using **YOLOv8 and OpenCV**.

The system detects people, guns, and knives through a webcam and generates automated alerts when potentially dangerous objects are identified.

## Project Overview

The project combines computer vision and deep learning to support automated security monitoring.

- Trained a custom YOLOv8 model for three object classes.
- Combined and processed datasets from multiple sources.
- Implemented real-time webcam detection and security alerts.
- Applied confidence thresholds and frame-based filtering to improve detection stability.

## Technologies

**Python | YOLOv8 | OpenCV | Ultralytics | Computer Vision**

## Detection Classes

| Class ID | Object |
|---|---|
| 0 | Person |
| 1 | Gun |
| 2 | Knife |

## Model Performance

The trained YOLOv8 model was evaluated using object detection metrics.

| Metric | Result |
|---|---:|
| Precision | 81.8% |
| Recall | 65.7% |
| mAP@50 | 72.7% |

### Performance Analysis

- **Precision (81.8%):** Indicates how often predicted detections are correct.
- **Recall (65.7%):** Measures the proportion of actual objects successfully detected.
- **mAP@50 (72.7%):** Summarizes detection performance across the three classes at an IoU threshold of 0.50.

The model achieved higher precision than recall, suggesting that reducing missed detections is an important area for improvement.

## Project Structure

```text
capstone_project/
├── best.pt                 # Trained YOLOv8 model
├── last.pt                 # Final training checkpoint
├── realtime_detection.py   # Webcam detection and alerts
├── merge_and_remap.py      # Dataset preparation
├── merge_extra.py          # Additional data merging
├── negative_add.py         # Negative sample preparation
├── data.yaml               # Class configuration
└── README.md
```

## Getting Started

Install the required libraries:

```bash
pip install ultralytics opencv-python
```

Run real-time detection:

```bash
python realtime_detection.py
```

Ensure that `best.pt` is located in the repository's root directory and that a webcam is connected.

## Future Improvements

- Improve recall to reduce missed detections.
- Expand the dataset with more diverse environments.
- Optimize inference speed for embedded hardware.
- Evaluate performance under different lighting and camera conditions.

---

## Author

**Sude İlhan** — Computer Engineering Graduate



