# VisionAssist.AI - Vision Assistance for the Visually Impaired

Empowering independent living through real-time Computer Vision and AI.

VisionAssist is a software application designed to help visually impaired individuals understand their surroundings through their laptop's webcam. It uses YOLO models for object detection and OCR for reading text, all converted into real-time audio feedback.

---

## Overview

VisionAssist bridges the gap between technology and accessibility. By combining real-time computer vision with text-to-speech output, it gives visually impaired users a reliable, private, and easy-to-use tool for understanding their immediate environment — all running locally on their machine without any external server dependency.

---

## Core Features

Object Recognition
Detects and announces everyday objects such as chairs, people, laptops, and more in real-time using YOLOv8.

OCR Text-to-Speech
Instantly reads printed text found in the camera's view, including books, labels, and signs, and converts it to speech.

Proximity Alerts
Announces new objects entering the field of vision every 3 seconds to keep the user continuously informed.

Accessible UI/UX
Designed with modern accessibility standards and a clean glassmorphism interface for ease of use.

Local Privacy
Runs entirely on your local machine. No data is sent to external servers during processing.

---

## Technology Stack

Backend
- Language: Python 3.10+
- Framework: FastAPI
- Computer Vision: OpenCV, Ultralytics YOLOv8
- OCR Engine: EasyOCR
- Text-to-Speech: Pyttsx3

Frontend
- Framework: React 18 with Vite
- Animations: Framer Motion
- Icons: Lucide Icons

Communication
- Video Streaming: MJPEG for low-latency live feed

---

## System Requirements

- Audio: Speakers or headphones (required for audio feedback)
- Video: Built-in or external USB webcam
- Memory: 4GB RAM or more
- Python: Version 3.10 or above
- Node.js: Latest stable version
- Network: Internet required only for initial setup to download AI model weights

---

## Quick Start

Step 1 - Make sure Python and Node.js are installed on your system.

Step 2 - Open your terminal and navigate to the project root folder.

Step 3 - Run the start script:

```bash
./start.sh
```

Step 4 - Open your browser and go to:

```
http://localhost:5173
```

That's it. The application will launch automatically.

---

## Project Structure

```
VisionAssist.AI/
├── backend/          # Python FastAPI logic, AI models, and image processing
├── frontend/         # React application with glassmorphism UI
├── start.sh          # Shell script to automate the entire system launch
└── README.md
```

---

## How It Works

1. The webcam captures a live video feed and streams it to the FastAPI backend.
2. Each frame is processed through the YOLOv8 model to detect objects in real-time.
3. EasyOCR scans the frame simultaneously for any readable text.
4. Detected objects and text are converted to speech using Pyttsx3 and played through the speakers.
5. The React frontend displays the live feed and detection results in an accessible interface.

---

## Privacy and Security

VisionAssist is built with privacy as a core principle. All processing happens locally on your device. No video, image, or audio data is transmitted to any external server. The only network activity occurs during the initial download of AI model weights during setup.

---
