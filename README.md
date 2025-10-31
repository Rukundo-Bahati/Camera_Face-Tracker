# Real-Time Face Tracker

A Python application that uses your computer's webcam to detect and track faces in real-time, displaying bounding boxes, movement direction, and estimated speed.

## Features

- Real-time face detection using OpenCV's Haar Cascade classifier
- Bounding box visualization around detected faces
- Movement direction tracking (Left, Right, Up, Down, Stationary)
- Speed estimation in pixels per second
- Smoothed movement data to reduce jitter
- Mirror effect for natural interaction

## Requirements

- Python 3.7+
- Webcam connected to your computer
- Required packages (see requirements.txt)

## Installation

1. Install the required packages:
```bash
pip install -r requirements.txt
```

## Usage

Run the face tracker:
```bash
python face_tracker.py
```

### Controls
- Press 'q' to quit the application

### Display Information
- Green bounding box around detected faces
- Red dot at the center of each face
- Movement direction text above the bounding box
- Speed information in pixels per second
- Face center coordinates below the bounding box

## How It Works

1. **Face Detection**: Uses OpenCV's Haar Cascade classifier to detect faces in each frame
2. **Movement Tracking**: Calculates displacement between consecutive frames
3. **Speed Calculation**: Measures pixels moved per second
4. **Direction Analysis**: Determines primary movement direction based on displacement
5. **Smoothing**: Averages recent movements to reduce noise and jitter

## Troubleshooting

- **Webcam not found**: Make sure your webcam is connected and not being used by another application
- **Poor detection**: Ensure good lighting and face the camera directly
- **Performance issues**: Try reducing the webcam resolution or adjusting detection parameters