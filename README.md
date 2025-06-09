

# 🐾 Dog Breed Classifier using CNN (PyTorch)

This repository contains a convolutional neural network (CNN) implemented in PyTorch to classify images of different dog breeds. The model is trained on a custom image dataset using a handcrafted CNN architecture, including data preprocessing, training loop, evaluation, and result visualization.

---

## 📁 Dataset

* **Path**: `archive_4dog`
* The dataset should follow the **ImageFolder** structure:

```
archive_4dog/
  ├── breed1/
  │    ├── img1.jpg
  │    ├── img2.jpg
  ├── breed2/
  │    ├── img3.jpg
  │    ├── ...
```

* Only `.jpg` and `.png` files are supported.
* Corrupted images are **automatically detected and removed** before training.

---

## 🧠 Model Overview

The network includes:

* 5 convolutional layers (with increasing filters: 32 → 512)
* ReLU activations and MaxPooling
* Fully connected classifier with dropout
* Custom image size: **150×150**

---

## 🚀 How to Run

### 1. Install Requirements

```bash
pip install torch torchvision matplotlib Pillow
```

### 2. Confirm Dataset Structure

Make sure the images are sorted into subfolders by class name (breed).

### 3. Run the Training Script

```bash
python train_cnn.py
```

This will:

* Train the model
* Save model as `pet_classifier_final.pth`
* Save training graphs as `training_results.png`

---

## ⚙️ Hyperparameters

| Parameter     | Value        |
| ------------- | ------------ |
| Batch Size    | 32           |
| Image Size    | 150×150      |
| Epochs        | 30           |
| Optimizer     | Adam         |
| Learning Rate | 0.0001       |
| Loss Function | CrossEntropy |

---

## 📊 Output

After training completes, the script generates:

* `pet_classifier_final.pth`: Final trained model weights
* `training_results.png`: Training/validation loss and accuracy curves

Example output:

```
Epoch [30/30]
Train Loss: 0.1734 | Val Loss: 0.2156 | Accuracy: 93.87%
```

---

## 📈 Training Visualization

<img src="training_results.png" width="600"/>

---

## 🛠 Features

* Custom convolutional neural network (from scratch)
* Real-time training statistics
* Automatic removal of corrupted images
* Random rotation, flip, resize, crop augmentation

---


