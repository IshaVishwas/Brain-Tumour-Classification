# 🧠 Brain Tumour Classification (Deep Learning · ResNet50)

A deep learning system to classify brain MRI images into **four tumour types**:
- Glioma  
- Meningioma  
- Pituitary  
- No Tumor  

This model is built using **Transfer Learning (ResNet50)** and achieves **~99% accuracy** with **AUC = 1.00** for all classes.

---

## 📌 Project Overview
This project implements a complete deep learning pipeline including:
- MRI preprocessing (denoising, cropping using contours, pseudocoloring)
- Data augmentation (rotation, zoom, shift, brightness, flips)
- Transfer learning + full fine-tuning using ResNet50
- Learning rate scheduling, early stopping, model checkpointing
- Evaluation using confusion matrix, ROC curves, classification report

---

## 📁 Project Structure (Suggested)

