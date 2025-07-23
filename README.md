# Sea Creatures Image Classifier (Deep Learning)

This project is an end-to-end deep learning solution that classifies images of sea creatures into one of 23 categories. It includes data cleaning, model experimentation, and final deployment as an Android app targeted at helping children learn about marine life.

##  Project Goal

To develop an interactive and user-friendly image classifier that helps children identify various types of sea creatures through a mobile application.

---

## Dataset

- Source: Kaggle
- Classes: 23 sea animal classes
- Challenges: Class imbalance, duplicates, blurry images, dark underwater images

---

## Data Preprocessing

- Used `CleanVision` (open-source Python library) to detect and remove:
  - Duplicate images
  - Near-duplicates across classes
  - Blurry and too-dark images
- Performed resizing, normalization, and data sampling
- Split data into train, test, and validation sets using `train_test_split`

---

##  Model Development

### 🔹 Baseline: LeNet-5
- Severe overfitting: Train Acc: 99.6%, Val Acc: ~29%

### 🔹 Improved Model: VGG-19
- Better generalization: Test Acc: ~60.7%

### 🔹 Final Chosen Architecture: DenseNet201
- Extensive experimentation with:
  - Transfer learning (unfreezing layers)
  - GlobalAveragePooling2D instead of Flatten
  - Learning rate tuning
  - Dropout (best value: 0.4)
- **Best Accuracy**:
  - ✅ Train: 97.97%
  - ✅ Validation: 86.81%
  - ✅ Te
