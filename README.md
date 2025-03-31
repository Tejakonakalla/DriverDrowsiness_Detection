
# Driver Drowsiness Detection 🚗💤

This project uses **Computer Vision** and **Deep Learning** to detect driver drowsiness in real-time by tracking eye movements from video footage. If the system detects drowsiness, it triggers an alarm to alert the driver.

---

### 🔍 Project Overview

- Extracts eye regions from video frames using **Haar Cascades** and the **CamShift** tracking algorithm.
- Uses a **Convolutional Neural Network (CNN)** (InceptionV3) to generate feature vectors (2048-D) from the eye regions.
- These features are fed into an **LSTM model** (a type of RNN) to learn temporal patterns and detect drowsiness.
- If the driver appears drowsy over time, the system triggers an **alarm**.

---

### 🧪 Technologies Used

- Python 3.x
- OpenCV
- TensorFlow / Keras
- NumPy
- Matplotlib

---

### 📁 Project Structure

```bash
.
├── Haar/                   # Haar cascade XML files
├── data/                  # Input videos or training data
├── eyedetection.py        # Extract eye regions using Haar & CamShift
├── extract_features.py    # Generate CNN features from eye patches
├── models.py              # Build LSTM model
├── data.py                # Dataset preprocessing
├── train.py               # Train the LSTM and trigger alarm
├── run_extract_eyes.sh    # Shell script to automate eye extraction
└── README.md              # You're reading it 🙂

