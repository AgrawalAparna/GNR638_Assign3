# Scene Recognition using CNN and Grad-CAM Visualization

This project implements a scene classification system using a Convolutional Neural Network (CNN) and visualizes important image regions using Grad-CAM. The model is trained on a dataset containing 21 scene categories.

## Dataset

The dataset consists of images classified into 21 scene categories.
- Images are **256x256 pixels**.
- Data is split into **80% training** and **20% validation**.
- Augmentation techniques like **horizontal flipping** and **rotation** are applied.


## Methodology

### 1. Data Preprocessing
- Images are loaded and normalized to pixel values in the range **[0,1]**.
- Augmentation is applied using `ImageDataGenerator` to improve generalization.

### 2. CNN Model Architecture
The model is built using a **sequential** CNN architecture:
1. **Three convolutional layers** with ReLU activation and max pooling.
2. **Flattening layer** to convert feature maps into a dense layer.
3. **Fully connected layers** with dropout to prevent overfitting.
4. **Softmax output layer** for multi-class classification.

### 3. Training
- Optimizer: **Adam** (learning rate = 0.0001)
- Loss function: **Categorical Crossentropy**
- Metric: **Accuracy**
- Number of epochs: **33**

### 4. Grad-CAM Visualization
Grad-CAM highlights important regions in an image that influence the model’s prediction.
- Computes gradients of the output class with respect to feature maps.
- Generates a heatmap to visualize class-specific activations.
- Overlays the heatmap on the original image.

## Results

- The trained model achieves **validation accuracy >50%**.
- Grad-CAM heatmaps highlight discriminative regions of images for classification.


## Contributors
- Aparna Agrawal
- Shravani Kode

