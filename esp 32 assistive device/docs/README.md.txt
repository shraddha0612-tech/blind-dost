# ESP32-CAM Assistive Device for Visually Impaired

![Project Banner](https://via.placeholder.com/800x300?text=ESP32-CAM+Assistive+Device)  
Replace with actual project image

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview
An intelligent assistive device that helps visually impaired individuals by converting visual information into audio feedback using ESP32-CAM and AI technologies.

### Problem Being Solved
- Difficulty recognizing people
- Challenges reading printed text
- Lack of environmental awareness

## Key Features

### Face Recognition
- Learns new faces with voice training
- Identifies known individuals with audio announcements
- Stores data locally for privacy

### Document Reader
- Accurate OCR for printed text
- Reads aloud books, labels and documents
- Supports multiple languages

### Scene Interpreter
- AI-powered environment description
- Identifies objects and scenery
- Provides spatial awareness cues

## Hardware Requirements

### Core Components
| Component | Specification | Quantity |
|-----------|--------------|----------|
| ESP32-CAM | OV2640 camera | 1 |
| Tactile Buttons | 6x6mm | 4 |
| 5V Power Supply | 2A | 1 |

### Recommended Add-ons
- PAM8403 Audio Amplifier
- HC-SR04 Ultrasonic Sensor
- 18650 Battery Holder

## Software Requirements

### Server Side
```plaintext
Python 3.8+
Flask 2.0.1
OpenCV 4.5+
Transformers 4.12+
PyTesseract 0.3.8
ESP32 Programming
Install Arduino IDE with ESP32 support

Connect ESP32-CAM via FTDI programmer

Open and upload firmware/main.ino

Configure WiFi credentials in the code

Usage
Basic Operation Flow
Power on the device

Wait for connection confirmation beep

Use the control buttons
Button	Function	LED Feedback
Button 1	Register Face	Blue Blink
Button 2	Recognize Face	Green Blink
Button 3	Describe Scene	Yellow Blink
Button 4	Read Text	White Blink
Training New Faces
Press and hold Register button

Speak the person's name when prompted

Position face in camera view (15-30cm)

Release button after confirmation beep
esp32_assistive_device/
├── server/
│   ├── main.py                 # Flask application
│   ├── requirements.txt        # Python dependencies
│   └── face_db.pkl            # Face database
├── firmware/
│   ├── main.ino               # ESP32 firmware
│   └── camera_pins.h          # Hardware config
├── docs/
│   ├── wiring_diagram.md      # Connection guide
│   └── user_manual.md        # Usage instructions
└── LICENSE                   # MIT License
Contributing
We welcome contributions! Please follow these guidelines:

Fork the repository

Create your feature branch (git checkout -b feature/NewFeature)

Commit your changes (git commit -m 'Add NewFeature')

Push to the branch (git push origin feature/NewFeature)

Open a Pull Request

Coding Standards
Python: Follow PEP 8 guidelines

Arduino: Use consistent 2-space indentation

Document new features thoroughly

License
Distributed under the MIT License. See LICENSE for more information.

Acknowledgements
Special thanks to these amazing projects:

ESP32-CAM by Espressif

Face Recognition by Adam Geitgey

Transformers by Hugging Face

OpenCV community