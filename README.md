# 🐞 Insect Detection & Counting System (YOLO-Based)

AI-powered prototype for automated insect detection, counting, and threshold-based alerting for agricultural monitoring.

---

## 🧪 Project Overview

This project was originally developed as a prototype during my AI & Computer Vision internship in 2022.

The goal was to explore automated insect monitoring using computer vision techniques to assist agricultural systems in detecting abnormal insect population growth.

This repository presents a reconstructed and simplified version of the original system for demonstration and documentation purposes.

---

## 🎯 Problem Statement

Manual insect monitoring in agricultural environments is time-consuming, error-prone, and inefficient.

The objective of this prototype was to:

- Automatically detect insects from images
- Count detected insects per frame
- Trigger alerts when insect population exceeds a predefined threshold
- Enable remote monitoring capabilities

---

## 📥 Data Collection

To build the prototype, insect image data was gathered from publicly available online sources using web scraping techniques.

The collected data was then:

- Cleaned and filtered
- Organized into structured directories
- Split into training and validation datasets
- Preprocessed for model training

---

## 🧹 Data Preprocessing

The preprocessing pipeline included:

- Image resizing and normalization
- Data augmentation (rotation, flipping, scaling)
- Noise filtering
- Dataset balancing where necessary

These steps improved generalization and detection robustness.

---

## 🧠 Model Architecture

The system uses a YOLO-based object detection model for real-time insect detection.

### Why YOLO?

YOLO (You Only Look Once) was selected because:

- Real-time detection capability
- Efficient inference speed
- Strong performance for small object detection
- Suitability for edge and field deployment scenarios

### Approach

- Used pre-trained YOLO weights (transfer learning)
- Fine-tuned on insect dataset
- Adjusted confidence thresholds for precision/recall balance
- Applied Non-Maximum Suppression (NMS) for bounding box refinement

---

## 📊 Training & Evaluation

The model was evaluated using standard object detection metrics:

- Precision
- Recall
- F1-score
- mAP (mean Average Precision)

The prototype achieved strong detection performance while maintaining efficient inference speed suitable for monitoring use cases.

---

## 🔔 Threshold-Based Alerting System

A monitoring layer was implemented on top of the detection model:

- Insects detected per frame are automatically counted
- If the count exceeds a configurable threshold, an email alert is triggered
- A cooldown mechanism prevents repeated alerts within short time intervals

### Configurable Parameters

- `THRESHOLD` → Maximum allowed insect count
- `CONFIDENCE_SCORE` → Minimum detection confidence
- `COOLDOWN_SECONDS` → Prevents alert spam

This feature enables early detection of abnormal insect population spikes.

---

## 🌐 API & Deployment

The system architecture includes:

- Flask-based REST API
- Image upload endpoint for detection
- JSON response with detection results
- Email alert integration
- Cloud deployment simulation (Google App Engine-style architecture)

---

## 🏗 System Pipeline

1. Image input  
2. YOLO object detection  
3. Bounding box extraction  
4. Insect count computation  
5. Threshold check  
6. Email alert trigger (if exceeded)

---

## 🚀 Tech Stack

- Python
- YOLO
- OpenCV
- TensorFlow / PyTorch (depending on YOLO version)
- Flask
- SMTP (Email Alerting)
- Web Scraping (Data Collection)

---

## 📌 Future Improvements

- Real-time video stream processing
- Edge device deployment optimization
- Database logging for historical monitoring
- Dashboard visualization
- Improved dataset size & annotation quality

---

## ⚠️ Disclaimer

This repository presents a reconstructed demonstration inspired by the original internship prototype.

No proprietary company data, internal code, or confidential material is included.

The purpose of this repository is to document the system architecture and technical approach.

---
>Video Demo : https://1drv.ms/v/c/2aec32f2024db85d/IQCjwh21nTg_Q6ru9Pv3T8SeAX1Y7EkMsWh9ZRsPL0vkddM?e=KUZsP4

## 👩‍💻 Author

Latifa Sassi  
AI & Machine Learning Engineer  
M.Sc. Computer Science (Germany)

LinkedIn: linkedin.com/in/latifa-sassi-3a67191a9  
Email: latifa.sassi.work@gmail.com
