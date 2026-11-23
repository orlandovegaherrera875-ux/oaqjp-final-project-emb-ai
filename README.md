# Final Project: Emotion Detection

A full-stack NLP web application built with **Python** and **Flask** that analyzes user-submitted text using the **IBM Watson NLP Emotion Predict API**, returning granular emotion scores (`anger`, `disgust`, `fear`, `joy`, `sadness`) and identifying the dominant emotion.

## Key Features
- **Modular Python Package:** Core NLP request and JSON parsing logic is encapsulated in the reusable `EmotionDetection` package.
- **RESTful Flask Backend:** Exposes a `/emotionDetector` endpoint that processes query parameters from the frontend and serves formatted responses.
- **Graceful Error Handling:** Intercepts HTTP `400` responses for blank or invalid inputs and returns a clean user-facing error message without crashing the server.
- **Automated Unit Testing:** Includes a `unittest` test suite verifying dominant emotion classification across all five target emotions.
- **PEP 8 & Static Analysis:** Audited with **Pylint** to achieve a **10.00/10** code quality rating.

## Tech Stack
- **Backend:** Python 3, Flask, Requests
- **Frontend:** HTML5, Bootstrap, JavaScript (AJAX)
- **AI / NLP:** IBM Watson NLP Library (`EmotionPredict`)
- **Testing & Quality:** `unittest`, Pylint

## Project Structure
```text
├── EmotionDetection/
│   ├── __init__.py              # Package initializer
│   └── emotion_detection.py     # Watson NLP API client & score parser
├── static/
│   └── mywebscript.js           # Client-side AJAX request handler
├── templates/
│   └── index.html               # Web interface
├── server.py                    # Flask application entry point (Pylint 10/10)
├── test_emotion_detection.py    # Unit test suite
└── README.md
