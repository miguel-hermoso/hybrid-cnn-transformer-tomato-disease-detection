# Hybrid CNN-Transformer Approaches for Tomato Leaf Disease Detection in Wild Backgrounds Using PlantDoc

This repository contains the code and supporting materials for a comparative study on tomato leaf disease classification using a ResNet50 baseline and a Hybrid CNN-Transformer model based on MobileViT. The models are trained and evaluated using tomato leaf images from the PlantDoc dataset.

## Project Overview

The study investigates whether a Hybrid CNN-Transformer can classify tomato leaf diseases more reliably than a conventional CNN under natural and visually cluttered conditions. It also aims to compare the image regions used by each model when making predictions through Grad-CAM and Attention Rollout visualizations.

## Research Objectives

The project aims to:

1. Train and evaluate a ResNet50 model as the CNN baseline.
2. Train and evaluate a MobileViT-based Hybrid CNN-Transformer model.
3. Compare the classification performance of both models.
4. Visualize and compare the image regions considered by each model during classification.

## Disease Classes

The study covers the following five tomato leaf classes:

- Early Blight
- Septoria Leaf Spot
- Mosaic Virus
- Yellow Virus
- Healthy

## Models

- **ResNet50:** A conventional convolutional neural network used as the baseline model.
- **MobileViT:** A Hybrid CNN-Transformer model that combines convolutional feature extraction with transformer-based self-attention.

Both models use pretrained ImageNet weights and will be fine-tuned for five-class tomato leaf disease classification.

## Dataset

This project uses the tomato subset of the [PlantDoc dataset](https://github.com/pratikkayal/PlantDoc-Dataset). PlantDoc contains real-world plant images captured under natural conditions with varied backgrounds, lighting conditions, orientations, and visual clutter.

The selected subset contains images from five tomato leaf classes. The notebook currently performs a stratified division of the selected images into training, validation, and testing subsets.

The dataset was introduced in:

> D. Singh, N. Jain, P. Jain, P. Kayal, S. Kumawat, and N. Batra, “PlantDoc: A dataset for visual plant disease detection,” in *Proceedings of the 7th ACM IKDD CoDS and 25th COMAD*, 2020.

All PlantDoc images remain subject to the original dataset’s licensing and attribution requirements. The complete dataset is not directly stored in this repository.


## Evaluation

The models will be evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Macro-averaged classification metrics
- Confusion matrix
- Training and validation loss
- Training and validation accuracy

The following explainability techniques will also be used:

- **Grad-CAM** for ResNet50
- **Attention Rollout** for MobileViT

The same test images will be used when comparing the visual explanations produced by the two models.

## Tools and Technologies

The current implementation uses:

- Python
- Google Colab
- PyTorch
- Torchvision
- NumPy
- Scikit-learn

Additional libraries may be added for MobileViT implementation, performance visualization, confusion matrices, and explainability. The final libraries and their exact versions will be documented in `requirements.txt`.

## Repository Structure

The repository is planned to contain:

```text
├── notebooks/          # Google Colab
├── src/                # Data preparation, training, and evaluation scripts
├── results/            # Tables, graphs, metrics, and visualizations
├── sample_images/      # Selected sample images for demonstration
├── requirements.txt    # Required Python libraries and versions
└── README.md           # Project information and instructions
```

The repository structure may be updated as the implementation progresses.



## Researchers

- Venice Adrienne Ting
- Seth Alain Callos
- Miguel Thomas Hermoso
- Jared Enrico Tan

Department of Biomedical, Manufacturing, and Robotics Engineering  
De La Salle University  
Manila, Philippines

## Project Status

This project is currently under development. The repository will be updated with the completed source code, model configurations, evaluation results, visualizations, and reproducibility instructions as the study progresses.

## Acknowledgment

The researchers acknowledge the creators of the PlantDoc dataset for making the dataset publicly available for plant disease detection research.
