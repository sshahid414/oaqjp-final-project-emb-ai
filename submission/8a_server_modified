"""Deploy a Flask application for emotion detection from text input."""
from flask import Flask, render_template, request
from EmotionDetection.emotion_detection import emotion_detector

APP = Flask("Emotion Detector")


@APP.route("/emotionDetector")
def emotion_analyzer():
    """Analyze text and return detected emotion scores."""
    text_to_analyse = request.args.get('textToAnalyze')

    if not text_to_analyse or not text_to_analyse.strip():
        return "Invalid text! Please try again!"

    emotion_result = emotion_detector(text_to_analyse)

    if emotion_result['dominant_emotion'] is None:
        return "Invalid text! Please try again!"

    anger = emotion_result['anger']
    disgust = emotion_result['disgust']
    fear = emotion_result['fear']
    joy = emotion_result['joy']
    sadness = emotion_result['sadness']
    dominant_emotion = emotion_result['dominant_emotion']

    response_str = (
        f"For the given statement, the system response is "
        f"'anger': {anger}, 'disgust': {disgust}, 'fear': {fear}, "
        f"'joy': {joy}, 'sadness': {sadness}. "
        f"The dominant emotion is <strong>{dominant_emotion}</strong>."
    )
    return response_str


@APP.route("/")
def render_index_page():
    """Render the index page for user input."""
    return render_template('index.html')


if __name__ == "__main__":
    APP.run(host="0.0.0.0", port=5000)
