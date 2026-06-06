# SaoLa Handsign

![Platform](https://img.shields.io/badge/Platform-Android-green)
![AI](https://img.shields.io/badge/AI-TensorFlow%20Lite-orange)
![Mode](https://img.shields.io/badge/Mode-Fully%20Offline-blue)
![Status](https://img.shields.io/badge/Status-DEMO%20v1.0-yellow)

> Offline Vietnamese Sign Language Recognition for Android

SaoLa Handsign is an experimental Android application that translates Vietnamese Sign Language into Vietnamese text and speech entirely on-device.

Designed for accessibility and privacy, the application performs all computer vision, machine learning, and language processing tasks locally without requiring an internet connection or cloud services.

---

## Download

**Demo APK**

https://drive.google.com/file/d/1hEDiUaRlZRlqFy1-hExlPXPYatjcFxXT/view?usp=drive_link

### Requirements

* Android 8.0 (API 26) or later
* Camera permission required

---

## Key Features

* Real-time Vietnamese Sign Language recognition
* Fully offline operation
* On-device AI inference
* Hand and facial expression recognition
* Vietnamese text reconstruction
* Offline Text-to-Speech (TTS)
* Privacy-focused architecture
* Optimized for consumer Android devices

---

## System Architecture

```text
[ CameraX Live Stream ]
           ↓
[ MediaPipe Hands + Face ]
           ↓
[ Kalman Filter Stabilization ]
           ↓
[ Feature Fusion Engine ]
           ↓
[ Temporal Sequence Buffer ]
           ↓
[ Conv1D Temporal CNN (TensorFlow Lite) ]
           ↓
[ Prediction Smoothing ]
           ↓
[ Vietnamese NLP Pipeline ]
           ↓
[ Text-to-Speech Output ]
```

### Pipeline Overview

The system captures real-time camera input using CameraX and extracts hand and facial landmarks through MediaPipe. Landmark sequences are stabilized using Kalman filtering and combined through a feature fusion engine.

A Temporal Conv1D CNN deployed with TensorFlow Lite performs gesture classification directly on the device. Predictions are refined using temporal smoothing before being processed by the Vietnamese NLP pipeline for text reconstruction and diacritic restoration.

Finally, recognized content can be converted into speech using Android Text-to-Speech services.

All processing is performed locally, ensuring low latency, offline functionality, and strong privacy protection.

---

## Technology Stack

### Android

* Kotlin
* Jetpack Compose
* Material Design 3
* Dynamic Dark Mode

### Computer Vision

* MediaPipe Tasks Vision
* Hand Landmarker
* Face Landmarker
* Face Mesh

### Deep Learning

* Temporal Conv1D CNN
* TensorFlow Lite
* INT8 Quantization
* Multi-threaded CPU Inference

### Vietnamese NLP

* Telex Sequence Segmentation
* Vietnamese Word Reconstruction
* SymSpell-based Correction
* Offline Vietnamese Dictionary
* Text-to-Speech Integration

Example:

```text
toiyeuvietnam
↓
tôi yêu Việt Nam
```

---

## Project Goals

The primary objectives of SaoLa Handsign are:

* Improve accessibility for Vietnamese sign language users.
* Enable real-time sign language recognition on Android devices.
* Preserve user privacy through fully offline processing.
* Explore the integration of Computer Vision, Deep Learning, and Vietnamese NLP in mobile environments.
* Support communication between hearing and hearing-impaired communities.

---

## Screenshots

<p align="center">
  <img src="https://github.com/user-attachments/assets/51d82a6a-765f-4291-9fcc-745ce54f59e9" width="220">
  <img src="https://github.com/user-attachments/assets/c9940da8-c131-4c3a-87a3-7692db879118" width="220">
  <img src="https://github.com/user-attachments/assets/421defe2-945d-48c6-af53-84e180ee8b1d" width="220">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/d0cb15a0-3cdf-4664-a36d-77d073f322ab" width="220">
  <img src="https://github.com/user-attachments/assets/985b0bba-f7d7-445b-bbf3-46c98a9c3510" width="220">
</p>

---

## Development Team

Developed by students of Thai Phien High School, Da Nang, Vietnam.

### System Development & Programming

* Doan Chi Vy

### Data Collection & Annotation

* Nguyen Thanh An
* Nguyen Le Thuy Linh
* Huynh Nhien Khanh
* Nguyen The Kiet

---

## Project Status

**Current Version:** DEMO v1.0

SaoLa Handsign is currently an experimental prototype under active development. Recognition accuracy, vocabulary coverage, NLP reconstruction quality, and user experience are continuously being improved.

### Future Development

* Larger Vietnamese sign language vocabulary
* Improved recognition accuracy
* Enhanced NLP reconstruction
* Additional accessibility features
* Performance optimization for lower-end devices

---

## Feedback

We welcome feedback from developers, researchers, educators, accessibility advocates, and members of the deaf and hard-of-hearing community.

Areas of interest include:

* Computer Vision
* Vietnamese NLP
* Mobile AI Optimization
* Android Development
* UI/UX Design
* Accessibility

---

## Source Code Availability

The source code, training datasets, and AI models are currently private.

This repository is intended to provide project documentation, screenshots, APK releases, technical information, and development updates.

---

## License

All Rights Reserved.

The source code, datasets, trained models, project assets, and documentation may not be copied, redistributed, modified, or used for commercial purposes without explicit permission from the development team.

© 2026 SaoLa Handsign Team
