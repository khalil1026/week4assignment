# 📌 Week 4 Assignment: Echo Classification

## 🔍 Overview
This project focuses on classifying echoes in **leads** and **sea ice** based on their shape and standard deviation.  
We use **Sentinel-3 altimeter data** and **Sentinel-2 optical data** for feature extraction and analysis.

---

## 📊 Data Processing Workflow
🔹 **1. Load Data**  
   - Import Sentinel-3 and Sentinel-2 datasets  
   - Preprocess raw echo signals  

🔹 **2. Feature Extraction**  
   - Compute **mean** and **standard deviation** of echoes  
   - Apply **unsupervised learning (K-means)** for classification  

🔹 **3. Model Evaluation**  
   - Compare predicted classifications with **ESA official labels**  
   - Use a **confusion matrix** to measure accuracy  

---

## 📌 Visualization
### **🔹 K-Means Clustering on Sentinel-2 Bands**
Example of classified echo data using **K-means clustering**:

![Echo Classification](figure1.png)

✔ **Color Meaning:**  
- 🟣 **Dark Purple:** Cluster 1 (Low Echo Intensity)  
- 🔵 **Teal:** Cluster 2 (Moderate Echo Intensity)  
- 🟡 **Yellow:** Cluster 3 (High Echo Intensity)

---

## 🚀 Installation
Run the following command to install dependencies:
```bash
pip install numpy pandas matplotlib scikit-learn
