# Line Detection with ResNet, U-Net, and Hybrid Models 🚦  

This project explores the effectiveness of different deep learning architectures for **line detection** using the **Cityscapes dataset**. We compare **ResNet**, **U-Net**, and a **ResNet + U-Net hybrid** to evaluate which model performs best in identifying lane/road line structures in urban driving scenarios.  

---

## 📌 Project Overview  
Detecting road lines is a fundamental step in autonomous driving and advanced driver-assistance systems (ADAS).  
This project investigates:  
- **ResNet** as a feature extractor for line detection.  
- **U-Net** as a segmentation-based approach.  
- **ResNet + U-Net hybrid** that combines ResNet’s feature extraction with U-Net’s encoder–decoder segmentation.  

---

## 📂 Dataset  
- **Cityscapes Dataset**: Large-scale dataset focused on semantic understanding of urban street scenes.  
- Contains **images, semantic labels, and fine annotations** useful for line and road structure detection.  
- Preprocessing included resizing, normalization, and label encoding.  

👉 Dataset link: [https://www.cityscapes-dataset.com](https://www.cityscapes-dataset.com)  

---

## ⚙️ Methodology  
1. **Model Architectures**  
   - **ResNet**: Used as a baseline for feature extraction.  
   - **U-Net**: Encoder–decoder segmentation network with skip connections.  
   - **ResNet + U-Net Hybrid**: Leveraged ResNet as the encoder backbone inside U-Net.  

2. **Training**  
   - Optimizer: Adam  
   - Loss function: Cross-entropy / Dice Loss (for segmentation tasks)  
   - Augmentations: Random cropping, flipping, and brightness adjustments  

3. **Evaluation Metrics**  
   - **IoU (Intersection over Union)**  
   - **Pixel Accuracy**  
   - **Precision & Recall** for detected line pixels  

---

## 📊 Results  
- **ResNet**: Good feature extraction but struggled with fine-grained line boundaries.  
- **U-Net**: Strong at capturing spatial details and segmenting lines.  
- **ResNet + U-Net**: Achieved the best balance between **feature richness** and **pixel-wise accuracy**, showing superior performance on IoU and precision.  
---


