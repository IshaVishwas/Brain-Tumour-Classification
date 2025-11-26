# 🧠 Brain Tumour MRI Classification Using Deep Learning (ResNet50 · CNN)

This project implements an automated system for **brain tumour classification from MRI scans** using **Deep Learning and Transfer Learning (ResNet50)**.

The model is trained to classify MRI images into **four categories**:

- 🧩 **Glioma**
- 🧩 **Meningioma**
- 🧩 **Pituitary Tumour**
- ✅ **No Tumour**

With transfer learning and proper preprocessing, the model achieves **~95% accuracy**, making it suitable for research and academic applications.

---

## 📌 Motivation

Early detection of brain tumours is crucial, but:

- MRI interpretation requires expert radiologists
- Manual diagnosis is time-consuming
- Human error may occur

Deep learning provides an automated, fast, and efficient solution by identifying tumor patterns from MRI images.

This project demonstrates a **complete end-to-end workflow**, including:

- Dataset preparation
- Preprocessing & Augmentation
- CNN/ResNet50 model training
- Evaluation & visualization
- Model saving for deployment

---

## 📂 Project Structure

```bash
brain_tumour/
│
├── notebooks/
│   └── BRAINTUMOUR.ipynb              # Main notebook (training + evaluation)
│
├── data/
│   ├── Training/                      # Training dataset
│   ├── Testing/                       # Testing dataset
│   └── cropped/                       # Preprocessed / cropped MRIs
│
├── models/
│   ├── best_model.keras               # Best performing model saved via callback
│   └── model_resnet50_trained.keras   # Final trained model
│
├── plots/
│   └── confusion_matrix.png           # Evaluation visualization
│
└── README.md
```

## 📊 Dataset

The dataset consists of MRI images categorized into **4 tumour classes**:

| Class Name |
|------------|
| Glioma |
| Meningioma |
| Pituitary |
| No Tumour |


📎 Dataset Location: Google Drive  
`https://drive.google.com/drive/folders/1MSWRGPBCsO0XBpX5RJYPPYQDKG7NdW0_?usp=sharing`

---

## 🛠️ Technologies Used

| Component | Technology |
|-----------|------------|
| Language | Python |
| Deep Learning | TensorFlow · Keras |
| Model | ResNet50 (Transfer Learning) |
| Notebook | Jupyter / Google Colab |
| Storage | Google Drive |

---

## 🚀 Features

✅ Classifies 4 tumour types  
✅ Google Drive dataset integration  
✅ Image preprocessing + augmentation  
✅ Transfer Learning (ResNet50)  
✅ High accuracy (~99%)  
✅ Confusion matrix evaluation  
✅ Saved `.keras` models for deployment  

---

## 🧠 Model Architecture
```bash
ResNet50 (pretrained)
↓
GlobalAveragePooling2D
↓
Dense Layer
↓
Dropout
↓
Dense Output (4 classes)
↓
Softmax

```


Why ResNet50?

- Excellent feature extraction
- Works well with medical images
- Faster training

---

## 🧹 Data Preprocessing

- Image resizing (224×224)
- Normalization (0–1)
- Data Augmentation:
  - Rotation
  - Zoom
  - Flips
  - Shifts
- Optional cropping

---

## 📈 Training Details

- Loss: `categorical_crossentropy`
- Optimizer: `Adam`
- Epochs: 10–30
- Batch size: 32

Callbacks:

✅ ModelCheckpoint  
✅ EarlyStopping  
✅ ReduceLROnPlateau (optional)

---

## ✅ Results

🎯 Final Accuracy: **~99%**  
🧠 Able to classify all 4 tumour types correctly






