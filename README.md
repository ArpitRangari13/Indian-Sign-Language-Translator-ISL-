# Swar 🤟: AI Sign Language Voice Assistant
**Smart India Hackathon (SIH) Prototype | Theme: MedTech & Social Inclusion**

Swar is a browser-based, real-time artificial intelligence application designed to bridge the communication gap between the speech/hearing impaired and public office workers. It translates Indian Sign Language (ISL) gestures into spoken audio and text instantaneously.

## 🎯 The Problem
In public spaces (hospitals, banks, government offices), individuals with speech and hearing impairments face massive communication barriers. Translators are rarely available, and writing notes is slow and inefficient. 

## 💡 Our Solution
Swar uses a locally-hosted AI model to track hand gestures via a standard webcam. When a gesture (like "Namaste", "Help", or "Water") is recognized with over 90% confidence, the Web Speech API instantly voices the word in an Indian accent. 

* **Zero-Server Architecture:** Runs entirely in the browser using TensorFlow.js. 
* **Privacy First:** No video feeds are sent to the cloud; all processing is done on the edge (the user's device).
* **Accessible UI:** Features a modern Glassmorphism dashboard with visual progress bars and status indicators to provide haptic-like visual feedback to the user.

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3 (Glassmorphism UI), Vanilla JavaScript
* **AI/Machine Learning:** TensorFlow.js, Google Teachable Machine
* **Audio:** HTML5 Web Speech API (`SpeechSynthesisUtterance`)

## 📂 Project Structure
To run this project, your folder structure must look exactly like this:

```text
Swar_SIH_Project/
│
├── index.html             # The main UI and logic script
├── README.md              # Project documentation
│
└── my_model/              # Your exported Teachable Machine files
    ├── model.json         # Neural network architecture
    ├── metadata.json      # Class labels (e.g., "Namaste", "Background")
    └── weights.bin        # Trained AI weights
