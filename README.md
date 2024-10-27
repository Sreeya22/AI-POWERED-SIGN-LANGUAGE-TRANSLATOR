# AI Powered Sign Language Recognition System
This project is a Sign Language Recognition System developed in Python using OpenCV, CVZone, and machine learning. The system detects hand gestures and translates them into sign language words, such as "Hello," "Yes," "No," "Please," and more. The project includes both data collection and real-time sign recognition components, capturing and labeling hand gestures in real-time and using them to train a sign language recognition model.

## Features
- **Hand Tracking and Cropping:** Utilizes a hand detection module to track and crop the hand region in real-time.
- **Finger Point Marking:** Tracks and marks key finger points on the detected hand, which are crucial for accurate gesture recognition.
- **Real-Time Data Collection**: Captures hand gestures for specific words (like "Hello," "No," "Please") directly from the camera, creating a dataset to train the model.
- **Sign Prediction:** Recognizes gestures in real-time using a trained classification model and displays the corresponding word.

## Project Structure
Part 1:<br/> **Data Collection**
The first script captures real-time hand gesture images, marking finger points for each gesture. These images are saved to a specific folder (e.g., "Hello," "No," "Please") and serve as a dataset for training the sign language model.<br/>

**Hand Detection:** Detects hand and extracts the area of interest.<br/>
**Finger Point Tracking:** Maps and records key finger points for each gesture, ensuring precise hand shape analysis.<br/>
**Resizing and Positioning: **Places the hand image on a 300x300 pixel white background for consistency.<br/>
**Image Saving:** Saves each hand gesture image in folders labeled by gesture name (e.g., "Hello," "No," "Please") when the "k" key is pressed.<br/><br/>
Part 2: <br/>**Real-Time Prediction**
The second script uses a pre-trained Keras model to classify gestures and display the recognized sign language word.<br/>

**Hand Detection:** Tracks the hand and applies the same cropping and resizing as in data collection.<br/>
**Prediction and Display:** The classifier identifies the gesture and displays the word label in real-time.

## Requirements
1. Python 3.x
2. OpenCV: For image processing and camera handling.
3. CVZone: For hand tracking and classification.
4. NumPy and Math: For array manipulation and calculations.
5. Pre-trained Model: A Keras model file (.h5) and labels file (.txt) are required for gesture classification.

## Setup
Clone or download this repository.<br/>
Install required libraries:`pip install cv2 cvzone numpy`<br/>

## Usage
**Data Collection:**
Run the data collection script to capture and save hand images for each gesture.<br/>
Finger points are marked automatically on each captured image, which is saved in folders named for each gesture (e.g., "Hello," "No," "Please").<br/>
Press the "k" key to capture an image for the dataset.

**Real-Time Prediction:**
Run the prediction script, specifying the trained model and labels file.<br/>
The recognized word is displayed on the screen for each detected gesture.<br/>

## Dataset Details
The dataset is collected in real-time, with each gesture saved to a folder named after the gesture ("Hello," "No," "Please," etc.). Each captured image includes finger point tracking, ensuring precise recognition by the model. This structure enables the classifier to analyze hand shape accurately for each gesture.
