# 🧠 Brain Tumour MRI Classification Using Deep Learning (ResNet50 · CNN)

This project implements an automated system for **brain tumour classification from MRI scans** using **Deep Learning and Transfer Learning (ResNet50)**.

The model is trained to classify MRI images into **four categories**:

- **Glioma**
- **Meningioma**
- **Pituitary Tumour**
- **No Tumour**

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
| Notebook | Google Colab |
| Storage | Google Drive |

---

## 🚀 Features

✅ Classifies 4 tumour types  
✅ Google Drive dataset integration  
✅ Image preprocessing + augmentation  
✅ Transfer Learning (ResNet50)  
✅ High accuracy (~95%)  
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

The MRI images in this project undergo the following preprocessing steps:

### **1. ROI Cropping (Contour-Based Brain Extraction)**
- Convert to grayscale  
- Gaussian blur  
- Thresholding  
- Erosion + dilation  
- Detect largest contour  
- Find extreme points  
- Crop the brain region from the MRI  

### **2. Noise Reduction**
- Applied **Bilateral Filtering** to reduce noise while preserving important edges.

### **3. Pseudocolor Mapping**
- Converted grayscale images to 3-channel format using **OpenCV COLORMAP_BONE** for compatibility with ResNet50.

### **4. Image Resizing**
- All images resized to **200 × 200 pixels**.

### **5. Normalization**
- Pixel intensities scaled to the **0–1** range.

### **6. Data Augmentation (Used During Training)**
- Rotation  
- Width shift  
- Height shift  
- Horizontal flip  

*(Other augmentations like brightness, vertical flip, shear, zoom were used only in preview visualization, not in final training.)*


---

## 📈 Training Details

- Loss: `categorical_crossentropy`
- Optimizer: `Adam`
- Epochs: 10–30
- Batch size: 32

Callbacks:

ModelCheckpoint  
EarlyStopping  
ReduceLROnPlateau (optional)

---

## ✅ Results

Final Accuracy: **~95%**  
Able to classify all 4 tumour types 






