# Drowsiness and Yawn Detection System

A real-time drowsiness and yawn detection system built with Python, OpenCV, and dlib to help prevent accidents caused by driver fatigue.

## Features

- **Eye Drowsiness Detection**: Monitors eye aspect ratio (EAR) to detect when a person's eyes are closed for too long
- **Yawn Detection**: Measures lip distance to identify when a person is yawning
- **Real-time Alerts**: Visual alerts on screen and audio alerts via system speakers
- **Easy-to-use Interface**: Simple command-line application with webcam support

## Requirements

- Python 3.6+
- OpenCV (`cv2`)
- dlib
- imutils
- numpy
- scipy
- espeak (for audio alerts)

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/9keystrokes/Driver-Drowsiness-Detection-System.git
   cd Driver-Drowsiness-Detection-System
   ```

2. Install the required packages:
   ```
   pip install opencv-python dlib imutils numpy scipy
   ```

3. Download the shape predictor file:
   - Download the 68 facial landmark predictor from [dlib's model repository](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)
   - Extract the file and place it in the project directory

4. Install espeak for audio alerts:
   - **Windows**: Download and install from [espeak official website](http://espeak.sourceforge.net/download.html)
   - **Linux**: `sudo apt-get install espeak`
   - **macOS**: `brew install espeak`

## Usage

Run the program with:

```
python drowsiness_yawn.py --webcam 0
```

Where:
- `--webcam` (or `-w`): specifies the webcam index (default is 0 for the built-in webcam)

## How It Works

1. **Face Detection**: Uses a Haar Cascade classifier to detect faces in the video stream
2. **Facial Landmarks**: Uses dlib's 68-point facial landmark detector to identify key points on the face
3. **Eye Aspect Ratio (EAR)**: Calculates the ratio of distances between facial landmarks to determine if eyes are closed
4. **Lip Distance**: Measures the distance between upper and lower lips to detect yawning
5. **Alert System**: Triggers visual and audio alerts when drowsiness or yawning is detected

## Controls

- Press `q` to quit the application

## Thresholds

- **EYE_AR_THRESH**: 0.3 (Eye aspect ratio threshold below which eyes are considered closed)
- **EYE_AR_CONSEC_FRAMES**: 30 (Number of consecutive frames eyes must be closed to trigger drowsiness alert)
- **YAWN_THRESH**: 20 (Lip distance threshold above which a yawn is detected)

## Files Required

- `haarcascade_frontalface_default.xml`: Haar Cascade classifier for face detection
- `shape_predictor_68_face_landmarks.dat`: Trained model for facial landmark detection

## Acknowledgments

- This project uses the facial landmark detection algorithm from dlib
- Inspired by various computer vision techniques for fatigue detection

## References

1. Richardson, Matt, and Shawn Wallace. Getting Started with Raspberry Pi. O'Reilly Media, 2012.
2. Zhao, C. W., Jegatheesan, J., & Loon, S. C. (2015). Exploring IoT with Raspberry Pi.
3. Halfacree, Gareth, and Eben Upton. Raspberry Pi User Guide. John Wiley & Sons, 2012.
4. Blood Cell Counting Using Image Processing
5. Drowsiness Detection Study - NCBI
