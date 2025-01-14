# Handwritten Digit Prediction with Flask

This web application, built with Flask, predicts handwritten digits either drawn on a canvas or uploaded as an image. It uses a machine learning model to recognize the digit and display the prediction.

## Features
- **Draw Mode**: Users can draw digits on a canvas and get predictions.
- **Image Mode**: Users can upload an image of a handwritten digit for prediction.
- **Prediction**: The app predicts the digit using a trained machine learning model.
- **Clear**: Clears the canvas for fresh input.

## Technologies Used
- **Flask**: Python web framework to build the backend.
- **HTML5 Canvas**: Captures user input for drawing digits.
- **JavaScript**: Handles canvas drawing logic and image upload.
- **CSS**: Styles the web page.
- **TensorFlow/Keras**: Loads and predicts digits using a pre-trained machine learning model.

---

## Project Structure

```
handwritten-digit-prediction/
├── app.py                # Main Flask application file
├── model.py              # File to load and predict using the ML model
├── digit_model.h5        # Pre-trained model for digit prediction
├── static/
│   └── js/
│       └── script.js      # JavaScript for canvas functionality and form actions
└── templates/
    └── index.html        # HTML file containing the frontend
```

### 1. **`app.py`**
The main Flask application file. It contains routes for:
- Serving the `index.html` page.
- Handling the prediction process for both drawing and image uploads.

### 2. **`model.py`**
This file contains the logic to load the pre-trained model (`digit_model.h5`) and predict the digits.

### 3. **`digit_model.h5`**
A pre-trained model, for example, a neural network trained on the MNIST dataset, used for digit prediction.

### 4. **`static/js/script.js`**
JavaScript file for handling:
- The drawing functionality on the canvas.
- Image upload logic.
- Sending the canvas data or image to the backend for prediction.

### 5. **`templates/index.html`**
The HTML structure for the frontend. It includes:
- A title and styling for the page.
- A canvas for drawing digits.
- Mode selection (Draw or Image).
- Buttons for clearing the canvas and triggering prediction.
- A display for the predicted digit.

---

## Setup Instructions

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone <repository_url>
cd handwritten-digit-prediction
```

### 2. Create a Virtual Environment (Optional but recommended)
It's recommended to create a virtual environment to manage the dependencies:
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
```

### 3. Install Required Packages
Install the necessary packages using `pip`:
```bash
pip install Flask tensorflow numpy
```

### 4. Start the Flask App
Run the Flask application:
```bash
python app.py
```

The app will be available at `http://127.0.0.1:5000/` in your browser.

---

## How to Use the Application

1. **Choose the Mode**:
   - **Draw Mode**: Select "Draw" and draw a digit on the canvas.
   - **Image Mode**: Select "Image" and upload an image of a handwritten digit.

2. **Clear**: Click the "Clear" button to reset the canvas if you're using the drawing mode.

3. **Predict**: After drawing a digit or uploading an image, click the "Predict" button to predict the digit.

4. **Result**: The predicted digit will be shown below the buttons.

---

## How the Prediction Works

1. **Drawing Mode**: When a user draws a digit, the JavaScript captures the canvas data. This data is sent to the Flask backend, which uses the machine learning model to predict the digit.

2. **Image Mode**: When a user uploads an image, it is sent to the backend, where the image is processed and passed through the prediction model to identify the digit.

---

