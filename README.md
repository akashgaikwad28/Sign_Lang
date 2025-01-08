# Sign Language Detection Application

## Overview
This application is designed to detect sign language gestures using a trained machine learning model. It utilizes a webcam to capture images, processes the data into a usable format, trains a model, and finally predicts gestures in real-time.

---

## Features
- Collect gesture data via webcam.
- Convert images into NumPy arrays for training.
- Train a model to recognize sign language gestures.
- Real-time gesture prediction.

---

## Requirements

Before running the application, ensure you have the following:

- Python (>=3.6)
- OpenCV
- NumPy
- TensorFlow/Keras
- Other dependencies (install via `requirements.txt` if provided)

To install the required libraries, run:

```bash
pip install -r requirements.txt
```

---

## How to Use

### 1. Gather Training Data
Run the following command to collect data for training:

```bash
python collectdata.py
```

- A webcam window will open.
- In the blue window, make the appropriate sign.
- Press the character key associated with the sign on your keyboard.
- The application will record an image for each key press.
- The number of key presses equals the number of images recorded.

### 2. Convert Images to NumPy Array
Run the following command to preprocess the collected images:

```bash
python data.py
```

This will convert the images into NumPy arrays, making them ready for model training.

### 3. Train the Model
Run the following command to train the model on the preprocessed data:

```bash
python trainmodel.py
```

The trained model will be saved for later use in predictions.

### 4. Predict Gestures
Run the following command to start real-time gesture prediction:

```bash
python app.py
```

- A webcam window will open.
- Show a sign to the webcam.
- The application will predict the gesture based on the trained model.

---

## Note
- Ensure the `functions.py` file is present in the project directory, as it contains important utility functions used by the application.
- For best results, ensure consistent lighting and clear gestures while collecting data and testing the application.

---

## Project Structure

```plaintext
.
├── collectdata.py      # Script to collect gesture data using webcam
├── data.py             # Script to convert images into NumPy arrays
├── trainmodel.py       # Script to train the sign language detection model
├── app.py              # Script to predict gestures in real-time
├── functions.py        # Utility functions for the application
├── requirements.txt    # Dependencies for the project
└── README.md           # Project documentation (this file)
```

---

## License
This project is open-source and available for personal and educational use. Please attribute the author when using or modifying this code.

---

## Contributing
Feel free to open issues or submit pull requests to improve this project. Contributions are welcome!
