# 🎵 AI Study companion with Emotion-Based Music Recommendation System 🎵

This project is a seamless blend of **Machine Learning**, **Natural Language Processing (NLP)**, and **Web Development**, designed to provide an interactive and intelligent experience. By leveraging advanced algorithms and APIs, the system detects real-time emotions, generates question-answer pairs, and recommends music tailored to the user's emotional state.

---

## 📖 Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Project Structure](#project-structure)
4. [Prerequisites](#prerequisites)
5. [Setup Instructions](#setup-instructions)
6. [Usage Guide](#usage-guide)
7. [Technical Overview](#technical-overview)
8. [APIs Used](#apis-used)
9. [Troubleshooting](#troubleshooting)
10. [Acknowledgments](#acknowledgments)
11. [License](#license)

---

## 🔍 Introduction

This system offers:
- **Emotion Detection**: Real-time facial emotion analysis using a CNN model.
- **Music Recommendation**: Suggests Spotify playlists based on detected emotions.
- **Text Processing and Q&A**: Converts text or extracted content from images into question-answer pairs using a Large Language Model (LLM).
- **Interactive User Interface**: A responsive web-based platform for seamless user interaction.

---

## 🌟 Features
- **Real-Time Emotion Analysis**:
   - Detects seven emotions: Happy, Sad, Angry, Neutral, Surprise, Fear, and Disgust.
   - Uses a pre-trained CNN model for high accuracy.
   
- **Dynamic Music Recommendations**:
   - Fetches personalized playlists from Spotify based on your mood.
   - Secure API integration using OAuth 2.0.

- **Smart Q&A Generation**:
   - Extracts text from images or accepts direct input.
   - Uses Gemini LLM for creating meaningful question-answer pairs.

- **User Query Resolution**:
   - Handles user queries through an integrated AI-powered LLM.

---

## 📂 Project Structure
```
Emotion-Based-Music-Recommendation/
├── run.py               # Main application script
├── models/
│   └── cnn_model.h5     # Pre-trained CNN model
├── static/
│   ├── css/             # Stylesheets
│   ├── js/              # JavaScript files
│   └── images/          # Static images for UI
├── templates/
│   ├── index.html       # Homepage
│   └── result.html      # Display results
├── requirements.txt     # List of dependencies
├── README.md            # Documentation
└── venv/                # Virtual environment (generated after setup)
```

---

## 🛠️ Prerequisites

1. **Python**: Ensure Python 3.8 or later is installed.  
   [Download Python](https://www.python.org/downloads/)

2. **Spotify Developer Account**:
   - Create a developer account on Spotify.
   - Generate `Client ID` and `Client Secret`.

3. **Hardware Requirements**:
   - A device with a webcam for emotion detection.
   - At least 4GB RAM for efficient real-time processing.

4. **Libraries**:
   - Listed in the `requirements.txt` file.
   - Install using `pip install -r requirements.txt`.

---

## 🚀 Setup Instructions

### Step 1: Clone the Repository
```bash
git clone https://github.com/your_username/emotion-based-music-recommendation.git
cd emotion-based-music-recommendation
```

### Step 2: Set Up Virtual Environment
Create and activate a virtual environment to isolate dependencies:
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Configure Spotify API
1. Log in to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/).
2. Create a new app to obtain `Client ID` and `Client Secret`.
3. Add the credentials to a `config.py` file:
   ```python
   SPOTIFY_CLIENT_ID = 'your_client_id'
   SPOTIFY_CLIENT_SECRET = 'your_client_secret'
   ```

### Step 5: Download Pre-trained CNN Model
Download the `cnn_model.h5` file and place it in the `models/` directory. If unavailable, train your model using the FER2013 dataset.

### Step 6: Run the Application
```bash
python app.py
```
The application will be available at `http://127.0.0.1:5000`.

---

## 💡 Usage Guide

### 1. **Emotion Detection & Music Recommendation**:
   - Allow webcam access.
   - Your facial emotion is analyzed in real-time.
   - A curated Spotify playlist based on your emotion is displayed.

### 2. **Q&A Generation**:
   - Input text manually or upload an image.
   - The system extracts text (if image is uploaded) and generates Q&A pairs.
   - Review the results on the UI.

### 3. **User Query Handling**:
   - Type your question into the search bar.
   - The integrated LLM processes and resolves your query instantly.

---

## 🧠 Technical Overview

### 1. **CNN-Based Emotion Detection**:
- **Dataset**: FER2013.
- **Model**: Pre-trained CNN with multiple convolutional, pooling, and dropout layers.
- **Preprocessing**: Converts frames to grayscale, resizes to 48x48 pixels, and normalizes pixel values.

### 2. **Music Recommendation**:
- **Integration**: Spotify Web API.
- **Authentication**: OAuth 2.0.

### 3. **Text Extraction & Q&A**:
- **OCR Tool**: PyTesseract for extracting text from images.
- **LLM**: Gemini for generating contextually relevant Q&A pairs.

---

## 🔗 APIs Used
- **Spotify Web API**: For fetching music playlists.
- **PyTesseract**: For text extraction.
- **Flask**: For building the backend.

---

## 🛠️ Troubleshooting
- **Webcam Issues**: Ensure browser permissions for webcam access.
- **Spotify API Authentication**: Double-check `Client ID` and `Client Secret`.
- **Module Errors**: Run `pip install -r requirements.txt` to resolve missing dependencies.

---

## 🙏 Acknowledgments
- **FER2013 Dataset**: For training the emotion detection model.
- **Spotify**: For music recommendations.
- **Gemini LLM**: For Q&A generation.
- **OpenAI Community**: For inspiration and support.

---

### Requirements.txt
```plaintext
Flask==2.3.2
tensorflow==2.11.0
opencv-python==4.8.0
PyTesseract==0.3.10
spotipy==2.19.0
numpy==1.24.2
pandas==1.5.3
requests==2.31.0
```
---
