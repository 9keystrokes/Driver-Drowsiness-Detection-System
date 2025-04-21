# 🛣️ Driver Drowsiness Detection System

A real-time driver drowsiness detection system built using Python, OpenCV, dlib, and Raspberry Pi. The system is designed to enhance road safety by detecting early signs of fatigue and yawning, providing timely alerts to the driver to prevent accidents.

---

## 📜 Abstract

Drowsy driving is a major cause of road accidents globally. This project aims to detect drowsiness using visual cues such as eye closure and yawning, and alert the driver using audio warnings. The system integrates facial recognition and computer vision techniques, and is suitable for integration with ADAS (Advanced Driver Assistance Systems).

---

## 📌 Objectives

- 🔧 **System Development:** Create a reliable, easy-to-use drowsiness detection system.
- 🧠 **Algorithm Implementation:** Use facial landmarks, eye aspect ratio (EAR), and lip distance to detect drowsiness and yawns.
- ⏱️ **Real-Time Monitoring:** Ensure real-time response with minimal latency for immediate feedback and alerts.

---

## 🖥️ Tech Stack

| Component       | Details                                                                 |
|----------------|-------------------------------------------------------------------------|
| **Language**    | Python                                                                 |
| **Libraries**   | OpenCV, dlib, imutils, NumPy, scipy, argparse                           |
| **Hardware**    | Raspberry Pi 4B, Webcam                                                 |
| **Software**    | Arduino IDE (for prototyping), shape_predictor_68_face_landmarks.dat   |

---

## 🧩 Features

- Eye Aspect Ratio (EAR) for drowsiness detection
- Lip distance measurement for yawning detection
- Real-time video stream analysis using OpenCV
- Voice alerts using `espeak`
- Works with standard webcams and Raspberry Pi cameras

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clonehttps://github.com/9keystrokes/Driver-Drowsiness-Detection-System.git
   cd Driver-Drowsiness-Detection-System
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the facial landmarks model:
   - [`shape_predictor_68_face_landmarks.dat`](https://github.com/davisking/dlib-models)

4. Run the script:
   ```bash
   python drowsiness_yawn.py --webcam 0
   ```

---

## 🚨 How It Works

- The system calculates the Eye Aspect Ratio (EAR) to detect eye closure.
- It monitors lip distance to detect yawns.
- If drowsiness is detected (EAR < threshold for N frames), an alert is triggered.
- If yawning is detected (lip distance > threshold), a secondary alert is raised.

---

## 📸 Sample Output

![Working of the project](https://github.com/9keystrokes/Driver-Drowsiness-Detection-System/blob/main/demo.bmp)

---

## 📈 Results

- Successfully detects early signs of driver fatigue.
- Performs accurately under standard lighting conditions.
- Effective in alerting users before dangerous micro-sleeps occur.

---

## 📚 References

1. Richardson, Matt, and Shawn Wallace. *Getting Started with Raspberry Pi*. O'Reilly Media, 2012.
2. Zhao, C. W., Jegatheesan, J., & Loon, S. C. (2015). *Exploring IoT with Raspberry Pi*.
3. Halfacree, Gareth, and Eben Upton. *Raspberry Pi User Guide*. John Wiley & Sons, 2012.
4. [Blood Cell Counting Using Image Processing](https://github.com/couldntfindabetterusername/blood-cell-counting-using-image-processing)
5. [Drowsiness Detection Study - NCBI](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8160886/)

---

## 📌 Future Work

- Integration with mobile apps via Bluetooth or Wi-Fi
- Cloud-based driver monitoring dashboard
- Night vision camera compatibility
- Deep learning-based emotion and attention analysis

---

## 🤝 Contributing

Pull requests are welcome! Feel free to open issues and suggest improvements.

---

## 🧠 Developed By

**Nayan Mandal**  
B.Tech CSE (Minor: Data Science and Analytics)  
Indian Institute of Information Technology, Nagpur  
