# Brain Tumor MRI Dataset

## Overview
This repository provides **brain MRI images** designed for machine learning classification and detection tasks, particularly targeting brain tumor identification and diagnosis[2][5].

---

## Dataset Structure

- Classes: Glioma, Meningioma, Pituitary, No Tumor
- Images organized in subfolders per class
- Formats: PNG/JPG/DICOM
- Size: Dataset contains over 17,000 images after augmentation[5]

---

## Model Architecture

- Multiple models have been used:
    - **Convolutional Neural Network (CNN):**
        - Custom CNN models for classification
        - Preprocessing includes resizing and normalization
    - **Transfer Learning:**
        - Pretrained models such as VGG16, Inception-V3, and ResNet-50, fine-tuned on MRI datasets[2][5][7]
        - Feature extraction from convolutional layers; classification via fully connected layers
    - **Results:**
        - VGG16 achieved up to 99.2% accuracy on diverse validation sets[5]
        - ResNet-50 achieved 99.88% accuracy in classification tasks[7]
        - Inception-V3 showed competitive results when retrained on MRI data[2]

---

## Technical Details

- **Preprocessing Steps:**
    - Images cropped to focus on the brain region
    - Uniform size (e.g., 200x200 or 240x240 pixels)
    - Pixel normalization (0-1 scale)
    - Data augmentation for improved robustness (rotation, flipping, zoom)[5][9]
- **Data Split:**
    - 70-80% training, 10-15% validation, 10-15% testing
- **Training:**
    - Optimizers such as Adam or SGD
    - Loss function: Categorical cross-entropy
    - Performance metrics monitored: accuracy, precision, recall, F1-score, specificity[5][7]
    - Early stopping and learning rate schedulers to prevent overfitting

---

## Usage

1. Download dataset from Kaggle.
2. Extract images to the `data/` folder.
3. Run scripts for preprocessing, training, and evaluation as documented in `notebooks/` or `scripts/`.

