# Melanoma Detection Assignment

## Overview
This assignment involves developing a Convolutional Neural Network (CNN)-based model to accurately detect melanoma. The project aims to classify skin lesions into nine distinct categories, using a dataset of pre-categorized images of skin cancer types. The model focuses on detecting melanoma, a potentially fatal type of skin cancer, while addressing challenges such as class imbalance and overfitting.

---

## Table of Contents
1. [General Information](#general-information)
2. [Importing Libraries](#importing-libraries)
3. [Data Preparation and Initial Assessment](#data-preparation-and-initial-assessment)
4. [Data Visualization](#data-visualization)
5. [Model Development](#model-development)
   - Model #1: With Normalization
   - Model #2: With Data Augmentation, Normalization & Dropout
   - Handling Class Imbalance
   - Model #3: With Augmented (Class Balanced) Data
   - Model #4: With Regularization & Class Balanced Data
6. [Findings and Conclusions](#findings-and-conclusions)
7. [Acknowledgements](#acknowledgements)
8. [Contact](#contact)

---

## General Information

### Background
This project is part of the PG Program in AI & ML within the Deep Learning course. It focuses on leveraging machine learning techniques to assist in melanoma detection.

### Goal
To build a CNN-based model capable of accurately detecting melanoma.

### Business Problem
Melanoma accounts for 75% of skin cancer deaths, making early detection critical. Automating the detection process can help dermatologists by reducing manual effort, expediting diagnosis, and improving patient outcomes.

### Dataset
The dataset comprises 2,357 images sourced from the International Skin Imaging Collaboration (ISIC). It contains images representing the following nine categories of skin lesions:
- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion

---

## Importing Libraries
The project utilizes essential libraries such as TensorFlow, Keras, Matplotlib, and others for model building, visualization, and performance optimization.

---

## Data Preparation and Initial Assessment

### Dataset Summary
The images are organized into training and test directories with slight class imbalance. Preprocessing steps include:
- Resizing images to `180x180` pixels.
- Normalizing pixel values between `0` and `1`.
- Visualizing class distributions to identify imbalances.

---

## Data Visualization
- Visualized sample images from each class to understand dataset composition.
- Analyzed class distributions using bar plots to highlight imbalance.

---

## Model Development

### Model #1: With Normalization
- Initial CNN with three convolutional layers.
- No data augmentation, dropout, or regularization applied.
- Findings: Model suffered from overfitting.

### Model #2: With Data Augmentation, Normalization & Dropout
- Introduced data augmentation techniques such as flip, rotation, zoom, brightness, and contrast adjustments.
- Added dropout layers to mitigate overfitting.
- Findings: Overfitting resolved, but underfitting emerged.

### Handling Class Imbalance
- Augmentor library used to balance classes by generating augmented images.
- Resulted in equal distribution across all classes in the training dataset.

### Model #3: With Augmented (Class Balanced) Data
- Retrained model using balanced dataset.
- Findings: Training and validation accuracy improved significantly (95% and 94%, respectively), but test accuracy remained low (~40%).

### Model #4: With Regularization & Class Balanced Data
- Added regularization to further enhance generalization.
- Findings: Enhanced stability in training but test accuracy still required improvement.

---

## Findings and Conclusions

### Technical Findings
1. **Model Iterations:**
   - Model 1 suffered from overfitting.
   - Model 2 mitigated overfitting but introduced underfitting.
   - Model 3 addressed class imbalance, significantly improving training and validation accuracy.
   - Model 4 incorporated additional regularization but test accuracy still lagged.
2. **Class Imbalance Mitigation:**
   - Augmentor library effectively balanced the training dataset, improving overall performance.

### Business Conclusions
- The developed model demonstrates potential for automating melanoma detection but is not yet ready for clinical use.
- Test accuracy (~40%) highlights the need for further exploration of advanced architectures or transfer learning.
- Future research with larger, diverse datasets and optimized models could significantly enhance diagnostic capabilities.

---

## Acknowledgements
Thanks to UpGrad and IIITB instructors for their guidance and support in this project.

---

## Contact
Created by [@sinsasanderink] – feel free to reach out with questions or feedback!
