# Handwritten-Digit-Recognition
 This Python script demonstrates a complete workflow for training a convolutional neural network (CNN) to classify handwritten digits using the MNIST dataset, and subsequently making predictions on custom images of handwritten digits.

# Description:
# 1. The script imports necessary libraries including os, cv2 (OpenCV), numpy, matplotlib.pyplot, and tensorflow.
It loads the MNIST dataset from TensorFlow, which consists of 28x28 grayscale images of handwritten digits (0 through 9) along with their corresponding labels.

# 2. Data Preprocessing:
The pixel values of the images are normalized to be in the range [0, 1] for better training performance.
The images are reshaped to include a channel dimension, making them compatible with the CNN input requirements.
Model Definition:

# 3. A CNN model is built using TensorFlow's Keras API. The model architecture includes:
Two convolutional layers with ReLU activation and max pooling layers to extract features from the images.
A dropout layer to prevent overfitting.

A fully connected (dense) layer with 500 units and ReLU activation for further classification.
An output dense layer with 10 units (one for each digit) and a softmax activation function to produce class probabilities.

# 4. Model Compilation and Training:
The model is compiled with the Adam optimizer and sparse categorical cross-entropy loss function.
It is then trained on the MNIST training data for 10 epochs.

# 5. Evaluation:
After training, the model is evaluated on the MNIST test data, and the loss and accuracy are printed.

# 6. Custom Digit Prediction:
The script attempts to predict digits from custom images named digit1.png, digit2.png, and so on. For each image:
The image is read and resized to 28x28 pixels.
The image is preprocessed similarly to the MNIST training data (normalization and reshaping).
The model predicts the digit, and the result is displayed.
The image is shown using Matplotlib for visual confirmation.

# 7. Error Handling:
If an error occurs (e.g., file not found or image read issues), it is caught and printed. The loop breaks in case of an error.
This script provides a practical example of training a digit recognition model and using it to classify new digit images, while also handling potential issues with image files.




