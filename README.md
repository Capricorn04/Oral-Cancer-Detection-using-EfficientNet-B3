# 🦷 Oral Cancer Detection using EfficientNet-B3

This project implements a deep learning solution for the **binary classification of oral cancer** from medical imagery. The model is designed to distinguish between **CANCER** and **NON-CANCER** cases with high precision, achieving a validation accuracy of approximately **95.79%**.

---

## 🚀 Project Overview

The core of this repository is a **PyTorch-based training pipeline** that utilizes **Transfer Learning** with the EfficientNet-B3 architecture.  

The ultimate goal is to integrate this model into a **full-stack web application** for real-time diagnostic assistance.

---

## 🛠️ Technical Specifications

- **Architecture:** EfficientNet-B3 (Pre-trained on ImageNet)  
- **Framework:** PyTorch  
- **Input Resolution:** 300 × 300 pixels  
- **Data Augmentation:**  
  - Random horizontal flips  
  - Random rotations (±15°)  
- **Optimizer:** Adam Optimizer  
  - Learning Rate: `0.0001`  
- **Loss Function:** Cross-Entropy Loss  

---

## 📊 Performance

The model was trained for **15 epochs**, showing consistent improvement:

- **Best Validation Accuracy:** 95.79%  
- **Final Training Loss:** 0.0093  
- **Final Training Accuracy:** 99.74%  

---

## 📂 Dataset Structure
OC Dataset/
├── CANCER/ # Contains 500 images
└── NON CANCER/ # Contains 450 images


- The dataset is automatically split:
  - **80% Training**
  - **20% Validation**

---

## ⚙️ Setup & Usage

### 1. Mount Dataset (Google Colab)
The notebook is configured to mount Google Drive:
/content/drive/MyDrive/OC Dataset


### 2. Run Training
Execute the training pipeline to fine-tune the EfficientNet-B3 model.

### 3. Export Model
The best-performing model weights are saved as:
oral_cancer_model.pth


---

## 🌐 Future Integration

The exported `.pth` file is ready for deployment in a full-stack application.

Planned features include:

- **🧾 Diagnosis Details**  
  Identification of specific oral cancer types  

- **🏥 Clinical Recommendations**  
  Suggest nearby dental clinics based on results  

- **💊 Treatment Information**  
  Overview of possible treatments and next steps  

---

## 🙏 Acknowledgments

- **Dataset Source:** Kaggle Oral Cancer Dataset  
- **Model Architecture:** EfficientNet (Google Research)  

---

## 📌 Notes

This model is intended for **research and assistive purposes only** and should **not replace professional medical diagnosis**.

The pipeline expects a directory structure compatible with PyTorch's `ImageFolder`:
