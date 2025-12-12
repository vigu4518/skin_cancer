# 🩺 Melanoma Classification for Skin Cancer

A deep learning project for classifying skin lesions into **benign (non-cancerous)** or **malignant (cancerous)** using dermoscopic images.  
Early detection of melanoma significantly improves treatment outcomes, and this project demonstrates how machine learning can assist dermatologists with fast, consistent, and accurate classification.

---

## 📌 Problem Statement
- Skin cancer is one of the most common cancers worldwide.  
- Manual diagnosis is time-consuming and subjective, with risks of misdiagnosis.  
- Limited availability of dermatology experts increases challenges.  
- **Objective:** Build a deep learning model to classify lesions into benign or malignant categories.  

---

## 📊 Dataset Overview
- **Source:** Melanoma Skin Cancer Dataset (Kaggle)  
- **Size:** ~10,000 dermoscopic images  
- **Classes:**  
  - Benign (non-cancerous)  
  - Malignant (cancerous)  
- **Split:** Training & Testing sets  
- **Diversity:** Variations in color, shape, and texture  

---

## 🔄 Workflow
1. Load dataset (Kaggle → Google Colab)  
2. Data preprocessing & augmentation  
3. Model building (CNN, VGG16, ResNet50, Ensemble)  
4. Training with callbacks & class balancing  
5. Evaluation (accuracy, confusion matrix, precision/recall)  

---

## 🛠️ Data Processing
- **Resizing:** Images → 224 × 224  
- **Augmentation:** Random flips, rotations, zoom, contrast adjustments  
- **Normalization:** Pixel values scaled to [0,1]  
- **Class Balancing:** Applied class weights  

---

## 🧠 Model Architectures
- **Custom CNN:** 3 conv layers, batch norm, dropout, dense classifier  
- **VGG16 (Transfer Learning):** Pretrained on ImageNet, custom head with GAP + dense layers  
- **ResNet50 (Transfer Learning):** Pretrained on ImageNet, strong recall for malignant cases  
- **Ensemble Learning:** Combines CNN, VGG16, ResNet50 → robust predictions  

---

## ⚙️ Training Setup
- **Loss Function:** Categorical Cross-entropy  
- **Optimizer:** Adam  
- **Callbacks:** EarlyStopping, ReduceLROnPlateau, ModelCheckpoint  
- **Epochs:** 20  

---

## 📈 Results & Performance
- **Custom CNN:** ~87–89% accuracy  
- **VGG16:** ~89% accuracy, balanced performance  
- **ResNet50:** ~90% accuracy, better recall for malignant cases  
- **Ensemble (CNN + VGG16 + ResNet50):** ~90% accuracy, stable precision/recall  

---

## ✅ Conclusion
- Deep learning shows strong potential in medical imaging.  
- ResNet50 and Ensemble models achieved the best performance.  
- High recall for malignant cases is crucial for cancer detection.  

---

## 🔮 Future Work
- Train on larger, more diverse datasets  
- Apply hyperparameter tuning & advanced architectures  
- Explore clinical testing for real-world adoption  

---

