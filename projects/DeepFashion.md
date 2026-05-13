---
layout: default
title: DeepFashion CNN Classification & Personality Mapping
---

# DeepFashion CNN Classification & Personality Mapping

## Overview

This project develops a Convolutional Neural Network (CNN) for fashion image classification using a curated subset of the DeepFashion dataset. Beyond traditional classification, the project also explores an interpretive layer by mapping predicted fashion categories to broader “fashion personalities” such as Minimalist, Casual, Elegant, and Bold.

The objective is not only to classify fashion images accurately, but also to investigate how visual fashion styles can be connected to broader personality-oriented interpretations.

## Project Repository

[View GitHub Repository](PASTE_YOUR_GITHUB_LINK_HERE)

---

# Project Components

This project includes:
- Deep Learning
- Convolutional Neural Networks (CNN)
- Fashion Image Classification
- Computer Vision
- Data Preprocessing
- Feature Visualization
- UMAP Dimensionality Reduction
- Model Evaluation
- Personality Mapping
- Fashion Analytics

---

# Dataset Description

The project uses a curated subset of the DeepFashion dataset, a large-scale benchmark dataset for fashion image understanding.

While the original dataset contains approximately 800,000 images, a smaller balanced subset was created for efficient experimentation and training.

## Final Dataset

- 10,000 images total
- 10 fashion categories
- 1,000 images sampled per category
- Balanced class distribution

This balanced setup helps reduce class bias and improves evaluation reliability across categories.

---

# Data Preprocessing

Several preprocessing steps were applied before model training.

## Preprocessing Pipeline

### Invalid Image Removal
Missing or corrupted image paths were identified and removed to ensure dataset quality.

### Dataset Balancing
A balanced dataset was created by sampling:
- 1,000 images per class
- 10 total categories

### Train/Test Split
The dataset was split using:
- 80% training data
- 20% testing data

Stratified sampling was used to preserve equal class distributions.

### Image Resizing
All images were resized to:

224 × 224 × 3

to maintain consistent CNN input dimensions.

### Normalization
Pixel values were scaled from:

[0, 255] → [0, 1]

to improve training stability and convergence.

---

# CNN Model Architecture

A custom Convolutional Neural Network (CNN) was designed for the image classification task.

CNNs are highly effective for image-based learning because they progressively capture:
- edges
- textures
- shapes
- high-level visual patterns

This makes them well-suited for fine-grained fashion classification.

## Model Structure

### Convolution Blocks

| Layer | Filters | Kernel |
|---|---|---|
| Conv Layer 1 | 32 | 3×3 |
| Conv Layer 2 | 64 | 3×3 |
| Conv Layer 3 | 128 | 3×3 |

Each convolution layer used:
- ReLU activation
- MaxPooling layers

to progressively extract spatial features while reducing dimensionality.

### Feature Reduction

A Global Average Pooling layer was applied instead of flattening to:
- reduce parameter count
- improve generalization
- minimize overfitting

### Dense Layers

- Dense layer: 128 units
- Activation: ReLU
- Dropout: 0.3

### Output Layer

The final layer:
- 10 neurons
- Softmax activation

corresponding to the 10 fashion categories.

---

# Training Strategy

The model was trained using a structured optimization strategy.

## Training Configuration

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Batch Size | 16 |
| Maximum Epochs | 50 |

### Early Stopping

Early stopping was implemented to:
- monitor validation loss
- stop training after 3 stagnant epochs
- restore best-performing weights

This helped reduce overfitting and unnecessary computation.

---

# Experiments & Challenges

Several experiments were conducted during development.

## EfficientNet Experiment

Initially, a pre-trained EfficientNet model was tested.

However:
- performance remained near random chance (~10%)
- model behavior was unstable

Due to these limitations, a custom CNN architecture was adopted.

## Data Augmentation

Data augmentation techniques were explored to improve generalization.

Although augmentation increased training diversity, it:
- significantly increased training time
- produced limited performance improvement

As a result, augmentation was excluded from the final pipeline.

## Computational Challenges

Major challenges included:
- large image dimensions (224×224)
- long training times
- visually similar fashion categories

Balancing the dataset helped reduce class imbalance issues.

---

# Results

The final CNN achieved:

## Final Test Accuracy

~31%

This is significantly better than random chance (10% for 10 classes), indicating that the model learned meaningful visual representations.

However, fashion image classification remains challenging because many categories share overlapping visual characteristics.

Factors affecting performance include:
- similar clothing styles
- lighting variations
- pose differences
- background complexity

Overall, the model provides a strong baseline for future improvement.

---

# Personality Mapping

A key extension of this project was the introduction of “fashion personality” mapping.

Predicted fashion categories were associated with broader interpretive labels such as:
- Minimalist
- Casual
- Elegant
- Bold
- Creative

This adds semantic meaning to raw classification outputs.

## Purpose

Rather than displaying only category predictions, the system attempts to interpret:
- style preferences
- aesthetic tendencies
- broader fashion identities

This can support:
- personalized recommendation systems
- AI stylists
- user preference modeling

It is important to note that this mapping is:
- interpretive
- manually designed
- not learned directly by the CNN

---

# Evaluation

The model was evaluated using:
- Classification Report
- Confusion Matrix
- UMAP Visualization

## Classification Performance

Some classes performed better than others.

### Better Performing Categories
- Bold
- Creative
- Elegant

These classes achieved relatively stronger:
- recall
- precision
- F1-scores

### Lower Performing Categories
- Simple
- Minimalist
- Comfort

These visually similar classes frequently overlapped.

## Confusion Matrix Insights

The confusion matrix showed:
- strong overlap between visually similar styles
- improved classification for visually distinctive classes

This highlights the difficulty of fine-grained fashion recognition.

---

# UMAP Visualization

UMAP (Uniform Manifold Approximation and Projection) was used to visualize high-dimensional CNN feature representations in 2D space.

Feature vectors extracted after Global Average Pooling were projected into lower dimensions for interpretability.

## Key Findings

The visualization showed:
- partial clustering of some categories
- overlap between visually similar styles

Classes such as:
- Simple
- Minimalist
- Sporty

showed substantial overlap, supporting the observed classification challenges.

UMAP provided a qualitative understanding of the learned feature space.

---

# Key Insights

This project demonstrates a complete deep learning pipeline for fashion image classification.

## Major Takeaways

- CNNs can learn meaningful fashion representations
- Fine-grained fashion classification remains difficult
- Visually similar categories create significant overlap
- UMAP helps interpret learned feature spaces
- Personality mapping improves interpretability of predictions

The project combines:
- computer vision
- visualization
- interpretability
- fashion analytics

into a unified workflow.

---

# Limitations

Several limitations were identified:

- Moderate classification accuracy (~31%)
- Difficulty separating visually similar classes
- Relatively simple CNN architecture
- Limited feature discrimination
- Computational constraints

---

# Future Work

Several improvements could strengthen future performance.

## Potential Enhancements

- Transfer learning using:
  - MobileNet
  - ResNet
  - VGG
- Advanced data augmentation
- Hyperparameter optimization
- Ensemble methods
- Attention mechanisms
- Improved feature extraction pipelines

These improvements could significantly improve classification robustness and recommendation quality.

---

# Tools & Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- UMAP

---

# Conclusion

This project presents a deep learning-based approach to fashion image classification using a custom CNN architecture trained on a balanced subset of the DeepFashion dataset.

While the model achieved moderate performance, it successfully learned meaningful visual representations and demonstrated the challenges of fine-grained fashion recognition.

The addition of personality mapping and feature-space visualization extends the project beyond standard classification, highlighting how AI systems can connect visual understanding with interpretable human-centered concepts.
