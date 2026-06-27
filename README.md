# oaqjp-final-project-emb-ai

## Final Project: Emotion Detection

This is the **Final Project** for the IBM Coursera course **"Developing AI Applications with Python and Flask"**.

## Project Name

**Emotion Detector** — Final Project (oaqjp-final-project-emb-ai)

## Description

This project implements an AI-based web application that detects emotions from text input using the IBM Watson NLP `EmotionPredict` API. The application analyzes text and returns scores for anger, disgust, fear, joy, and sadness, along with the dominant emotion.

## Technologies Used

- Python
- Flask
- Watson NLP Library
- Unittest
- PyLint

## Project Structure

```
EmotionDetection/
├── __init__.py
└── emotion_detection.py
templates/
└── index.html
static/
└── mywebscript.js
test_emotion_detection.py
server.py
README.md
```

## Usage

### Run unit tests

```bash
python3.11 -m unittest test_emotion_detection.py
```

### Run the Flask web application

```bash
python3.11 server.py
```

Open `http://localhost:5000` in your browser.

### Run static code analysis

```bash
pylint server.py
```

## Important Note

The Watson NLP API endpoint used in this project is only accessible from the IBM Skills Network Cloud IDE environment provided in the Coursera course lab.
