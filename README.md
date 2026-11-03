# Final Project

**Emotion Detector – AI-Based Web Application**, the final project for the IBM course *Developing AI Applications with Python and Flask*.

The application uses the Watson NLP **EmotionPredict** service to score a piece of text for
anger, disgust, fear, joy and sadness, and reports the dominant emotion through a Flask web interface.

## Project structure

```
EmotionDetection/          Python package
  __init__.py
  emotion_detection.py     emotion_detector() – calls Watson NLP and formats the result
server.py                  Flask web server (/ and /emotionDetector routes)
test_emotion_detection.py  Unit tests
templates/index.html       Web interface
static/mywebscript.js      Front-end script that calls /emotionDetector
```

## Running

```bash
python3.11 -m pip install flask requests
python3.11 server.py
```

Then open `http://localhost:5000`.

## Tests and static analysis

```bash
python3.11 test_emotion_detection.py
pylint server.py
```

> The Watson NLP endpoint is only reachable from the IBM Skills Network lab environment.
