# Autoencoder_generator
Autoencoder Generator
This Jupyter Notebook demonstrates the implementation and training of both fully-connected and convolutional autoencoders using TensorFlow and Keras, primarily for image reconstruction on the MNIST dataset.

Features
Data Loading and Preprocessing: Loads the MNIST dataset and preprocesses the images by normalizing pixel values and reshaping them for compatibility with different autoencoder architectures.
Fully-Connected Autoencoder:
Constructs a deep fully-connected autoencoder with an encoding dimension of 32.
Uses ReLU activation functions for hidden layers and a sigmoid activation for the output layer.
Compiled with the Adam optimizer and binary_crossentropy loss, suitable for image reconstruction.
Convolutional Autoencoder:
Includes an architecture for a convolutional autoencoder, leveraging Conv2D, MaxPooling2D, and UpSampling2D layers for feature extraction and reconstruction.
Model Training: Trains the autoencoders on the preprocessed MNIST training data.
Visualization: Visualizes original and reconstructed images to demonstrate the autoencoder's performance.
Getting Started
Prerequisites
Python 3.x
Jupyter Notebook
Required Python libraries:
numpy
tensorflow
matplotlib
You can install these dependencies using pip:

Bash
pip install numpy tensorflow matplotlib jupyter
Usage
Clone the repository (if applicable) or download the Autoencoder.ipynb file.
Navigate to the directory containing the notebook.
Launch Jupyter Notebook:
Bash
jupyter notebook
Open Autoencoder.ipynb in your browser.
Run the cells sequentially to load data, define models, train them, and visualize the results.
Model Architectures
Fully-Connected Autoencoder
The fully-connected autoencoder processes flattened 28x28 MNIST images (784 features).
Encoder:
Input Layer: 784 neurons
Dense Layer 1: 128 neurons, ReLU activation
Dense Layer 2: 64 neurons, ReLU activation
Latent Space (Encoded) Layer: 32 neurons, ReLU activation
Decoder:
Dense Layer 1: 64 neurons, ReLU activation
Dense Layer 2: 128 neurons, ReLU activation
Output Layer: 784 neurons, Sigmoid activation (for image reconstruction)
Convolutional Autoencoder
The convolutional autoencoder uses 2D convolutional layers for encoding and upsampling layers for decoding, designed to work directly with the 2D structure of images.
Encoder: Consists of Conv2D and MaxPooling2D layers.
Decoder: Consists of Conv2D and UpSampling2D layers.
