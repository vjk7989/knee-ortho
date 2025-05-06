# ArthoScan Pro

ArthoScan Pro is a deep-learning-based web application that is capable of KNEE OSTEOARTHRITIS DETECTION AND SEVERITY PREDICTION USING MACHINE LEARNING. 

## Algorithms and Model Architecture

The application uses a Convolutional Neural Network (CNN) with the following architecture:

1. **Input Layer**: 
   - Takes 256x256 grayscale knee X-ray images

2. **CNN Layers**:
   - First Layer: 128 filters (3x3 kernel), ReLU activation, MaxPooling
   - Second Layer: 64 filters (3x3 kernel), ReLU activation, MaxPooling
   - Third Layer: 32 filters (3x3 kernel), ReLU activation, MaxPooling

3. **Dense Layers**:
   - Flatten Layer
   - Dropout Layer (0.2)
   - Dense Layer: 128 neurons, ReLU activation
   - Dropout Layer (0.1)
   - Dense Layer: 64 neurons, ReLU activation
   - Output Layer: 5 neurons, Softmax activation

## Classification Categories

The model classifies knee X-rays into five severity levels:
- Normal (0)
- Doubtful (1)
- Mild (2)
- Moderate (3)
- Severe (4)

## Prediction Process

1. **Image Preprocessing**:
   - Conversion to grayscale
   - Resizing to 256x256 pixels
   - Pixel normalization (values divided by 255.0)

2. **Model Performance**:
   - Training Accuracy: ~99%
   - Validation Accuracy: ~89%
   - Trained for 100 epochs
   - Uses categorical crossentropy loss and Adam optimizer

## Requirements for Web Application

The following python modules must be installed to run the Application:
- ```flask```
- ```TensorFlow```
- ```Keras```
- ```OpenCV```

## Setup Instructions

1. **Create and Activate Virtual Environment**:
```bash
# Create a new virtual environment with Python 3.10
py -3.10 -m venv venv_py310

# Activate the virtual environment
.\venv_py310\Scripts\Activate.ps1

# Install the required packages
pip install flask tensorflow keras opencv-python
```

## Running the Application
1. Run ```app.py``` to start the web application:
```bash
python app.py
```
2. Open the browser and go to the started server
3. Upload the X-ray image and see the result

