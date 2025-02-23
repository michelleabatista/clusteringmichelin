# Michelin Guide Restaurants Clustering Analysis with MS Azure

## 📌 Project Overview

This is a clustering analysis to organize Michelin Guide restaurants by location. The goal was to uncover geographic patterns in fine dining using machine learning techniques.

---

## 🌟 About the Michelin Guide

The **Michelin Guide** is a prestigious rating system that awards up to three stars for exceptional cuisine:

- ⭐ **1 Star:** High-quality cooking, worth a stop.
- ⭐⭐ **2 Stars:** Excellent cooking, worth a detour.
- ⭐⭐⭐ **3 Stars:** Exceptional cuisine, worth a special journey.

Originally published in 1900 by the Michelin tire company to encourage travel, the guide is now one of the most influential authorities on fine dining worldwide.

> **Note:** Bib Gourmand and Selected Restaurants were excluded from this clustering analysis.

---

## 🗂️ Dataset Information

The dataset used for this project was sourced from **Kaggle**, featuring restaurants curated from the official Michelin Guide website. Key details:

- **Essential Columns Selected:**
  - Restaurant Name
  - Location
  - Longitude & Latitude
  - Star Rating (1, 2, or 3 stars)

The dataset was preprocessed locally in Python before being uploaded to **Azure ML Designer** for clustering.

---

## 🛠️ Tools & Technologies

- **Azure ML Designer**: For building and training the clustering model.
- **Python**: For local preprocessing of the dataset.
- **K-Means Algorithm**: For clustering analysis.

---

## ⚙️ Project Workflow

### 1. **Data Preparation**

- Cleaned the dataset locally in Python, retaining only essential columns.
- Uploaded the cleaned dataset (**Michelin\_Restaurants**) to Azure ML Designer.

### 2. **Data Configuration in Azure**

- **File format:** Delimited
- **Delimiter:** Comma
- **Encoding:** UTF-8
- **Header:** Present in the first file
- **Schema:** Auto-detected by Azure, irrelevant columns removed.

### 3. **Pipeline Creation**

- Renamed the pipeline to **Michelin\_Restaurants\_Pipeline**.
- Selected relevant columns (Longitude & Latitude).

### 4. **Data Normalization**

- Applied **MinMax normalization** to ensure all numerical values were on a similar scale.

### 5. **Data Splitting**

- **70%** for training and **30%** for validation.
- Set **random seed = 123** for reproducibility.

### 6. **Model Training**

- Used the **K-Means clustering algorithm**.
- Set **number of centroids = 7** to define optimal cluster groupings.

### 7. **Model Evaluation**

- Assigned data to clusters and connected to the trained model.
- Added the **Evaluate Model** component to review performance.

### 8. **Inference Pipeline**

- Built an inference pipeline for future predictions.

### 9. **Model Deployment**

- Deployed the model.
- **Deployment Status:** Healthy ✅

---

## 📊 Key Findings

The clustering analysis revealed:

- **High concentration of Michelin-starred restaurants in Europe**, reflecting the region's deep culinary traditions and influence in fine dining.

---

## 💡 Potential Applications

This clustering model offers valuable insights for:

- **Restaurant Owners & Investors:** Identify underserved regions with fewer Michelin-starred restaurants, uncovering opportunities for expansion.
- **Culinary Researchers & Tourism Boards:** Understand how geography influences culinary excellence and plan gastronomic tourism strategies.
- **Data Analysts:** Apply similar clustering techniques to other industries to discover hidden geographic patterns.

---

## 🔄 Future Work

For future iterations, incorporating additional variables could provide deeper insights into global fine dining trends:

- Cuisine type
- Pricing information
- Customer reviews

