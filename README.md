# Emotion Detection Web Application

## Overview

This project is an AI-powered Emotion Detection Web Application built using Python, Flask, and IBM Watson Natural Language Processing (NLP) services. The application analyzes user-provided text and identifies the emotions expressed in the text, including anger, disgust, fear, joy, and sadness.

The project demonstrates the development lifecycle of an AI-enabled web application, including API integration, application packaging, testing, web deployment, error handling, and static code analysis.

## Features

- Detects emotions from user-provided text
- Identifies the dominant emotion
- RESTful web interface using Flask
- Unit test coverage
- Error handling for invalid inputs and API failures
- Static code analysis using Pylint
- Modular and reusable package structure

## Project Structure

```text
.
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py
│
├── server.py
├── test_emotion_detection.py
├── requirements.txt
└── README.md
```

## Technologies Used

- Python 3.x
- Flask
- Requests
- IBM Watson NLP
- unittest
- Pylint

## Installation

### Clone the Repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Running the Application

Start the Flask server:

```bash
python server.py
```

The application will be available at:

```text
http://localhost:5000
```

Example request:

```text
http://localhost:5000/emotionDetector?textToAnalyze=I am very happy today
```

Example response:

```text
For the given statement, the system response is {'anger': 0.01, 'disgust': 0.02, 'fear': 0.01, 'joy': 0.93, 'sadness': 0.03}. The dominant emotion is joy.
```

## Running Unit Tests

Execute the test suite:

```bash
python -m unittest test_emotion_detection.py
```

Expected output:

```text
Ran X tests in X.XXXs

OK
```

## Static Code Analysis

Run Pylint against the project files:

```bash
pylint EmotionDetection/emotion_detection.py
pylint server.py
```

The goal is to maintain high code quality and compliance with Python best practices.

## Error Handling

The application includes validation for:

- Empty user input
- Invalid requests
- API communication failures
- Unexpected response formats

Appropriate error messages are returned to the user when issues occur.

## API Endpoint

### GET /emotionDetector

#### Parameters

| Parameter | Description |
|-----------|-------------|
| textToAnalyze | Text to analyze for emotions |

#### Example

```http
GET /emotionDetector?textToAnalyze=I am excited about this project
```

## Learning Objectives

This project demonstrates:

- AI service integration
- REST API development
- Flask web deployment
- Python package creation
- Unit testing
- Error handling
- Static code analysis
- Software engineering best practices

## Author

Developed as part of an AI Application Development project using Python, Flask, and IBM Watson NLP.
