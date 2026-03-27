# Pediatric Chest X-Ray Pneumonia Detection

**Description:**  
Deep learning project for detecting pneumonia from pediatric chest X-ray images using CNNs. The model classifies chest X-rays into **Normal** and **Pneumonia** categories with high accuracy.

---

## Table of Contents
- [Dataset](#dataset)
- [Project Overview](#project-overview)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Future Work](#future-work)
- [References](#references)

---

## Dataset
The dataset used is the **Pediatric Chest X-Ray Pneumonia — Balanced Dataset**:

- **Images:** 8,530 frontal chest X-rays  
- **Classes:** Normal (0) and Pneumonia (1)  
- **Balanced & Preprocessed:** Ready for training  
- Source: [Kaggle Dataset](https://www.kaggle.com/datasets/yusufmurtaza01/pediatric-chest-xray-pneumonia-balanced-dataset)

---

## Project Overview
The goal of this project is to build a convolutional neural network (CNN) that can automatically classify pediatric chest X-ray images into normal or pneumonia. This can assist radiologists and healthcare professionals in early detection.

**Workflow:**
1. Load and preprocess images (resize, normalize).  
2. Encode labels (Normal = 0, Pneumonia = 1).  
3. Split data into training, validation, and test sets.  
4. Train a CNN model with BatchNormalization, ReLU activations, and MaxPooling layers.  
5. Evaluate the model performance on unseen test data.

---

## Model Architecture
- **Input:** 100x120 RGB images  
- **Convolutional Blocks:**  
  - Block 1: Conv2D → Conv2D → BatchNorm → ReLU → MaxPool  
  - Block 2: Conv2D → Conv2D → BatchNorm → ReLU → MaxPool  
- **Fully Connected Layers:**  
  - Dense 700 → BatchNorm → ReLU  
  - Dense 500 → BatchNorm → ReLU  
- **Output:** Dense 1 → Sigmoid (binary classification)  
- **Optimizer:** Adam (learning_rate=0.001)  
- **Loss:** Binary Crossentropy  

---

## Installation
Clone the repository and install dependencies:

```bash
git clone <your-repo-url>
cd <repo-folder>
pip install -r requirements.txt
