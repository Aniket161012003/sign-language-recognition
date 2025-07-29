# 🖐️ Sign Language Recognition System

Welcome to the **Sign Language Recognition** project!  
This system uses **computer vision**, **MediaPipe**, and **deep learning (LSTM)** to recognize hand gestures representing sign language letters. It combines real-time image capture, landmark extraction, sequence modeling, and model training to classify hand gestures into alphabetic signs.

---

## 📁 Project Overview

This project includes four major components:

### 🔸 1. `collectdata.py` - Image Data Collection
Captures hand gesture images for all 26 alphabets (`A–Z`) using a webcam.
- Saves frames in respective folders (e.g., `Image/A/`, `Image/B/`, etc.)
- Allows manual frame capture via keyboard input (`a`, `b`, `c`, ..., `z`)
- Draws a white rectangle (ROI) where users place their hand for consistent input

---

### 🔸 2. `data.py` - Keypoint Extraction & Dataset Preparation
- Uses **MediaPipe Hands** to detect hand landmarks in collected images
- Extracts 3D keypoints (x, y, z) for each hand gesture
- Stores keypoints as `.npy` files for training
- Organizes data into sequences for deep learning models

---

### 🔸 3. `function.py` - Utility Functions
Includes reusable code for:
- Detecting hand landmarks using MediaPipe
- Drawing styled hand landmarks on images
- Extracting and flattening hand landmark data
- Setting configuration: number of sequences, actions, frame length, etc.

---

### 🔸 4. `trainmodel.py` - LSTM Model Training
- Prepares sequences and labels from saved `.npy` keypoint files
- Trains a **Deep LSTM neural network** to classify gestures
- Architecture: 3 LSTM layers + Dense layers + Softmax output
- Uses **TensorBoard** for logging and visualization
- Saves the final trained model (`model.h5` and `model.json`)

---

## 🧠 Features

- 🖼️ Live webcam-based gesture capture
- ✋ 3D hand tracking with MediaPipe
- 📦 Landmark-based dataset generation
- 🔁 Sequential deep learning with LSTM
- 🧠 Real-time gesture classification ready

