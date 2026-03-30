# Indoor Localization Using WLAN Fingerprinting

Machine Learning Project – Indoor Positioning System  
Course: DSAI 3201 – Machine Learning  

---

## Overview

Indoor localization is a challenging problem due to the absence of reliable GPS signals in indoor environments. This project addresses the problem using **WLAN fingerprinting**, where WiFi signal strengths are used to estimate a device’s location.

The project applies machine learning techniques to:
- **Classify** the building and floor
- **Predict** the precise indoor location (latitude & longitude)

The solution is built using a structured pipeline that includes preprocessing, classification, regression, and evaluation.

---

## Objectives

- Predict the **building ID** and **floor number** using classification models  
- Estimate **latitude** and **longitude** using regression models  
- Analyze model performance and compare approaches  
- Build a complete machine learning pipeline for indoor localization  

---

## Dataset

**Dataset Used:** UCI Indoor Localization WiFi Dataset  

### Features:
- WiFi signal strengths from **hundreds of access points (WAPs)**  
- Building ID  
- Floor number  
- Latitude and longitude coordinates  

### Key Characteristics:
- High dimensional (500+ WAP features)  
- Sparse signals (many missing or weak values)  
- Multi-output prediction problem  

---

## Methodology

### 1. Data Preprocessing

- Replaced missing/weak signal values (e.g., `100`) with appropriate placeholders  
- Normalized signal strength values  
- Split dataset into:
  - Features (WAP signals)
  - Targets:
    - Classification: Building, Floor
    - Regression: Latitude, Longitude  

---

### 2. Classification Models

Used to predict:
- **Building ID**
- **Floor Number**

#### Model:
- **Random Forest Classifier**

### Why Random Forest?
- Handles high-dimensional data well  
- Robust to noise in WiFi signals  
- Captures non-linear relationships  

---

### 3. Regression Models

Used to predict:
- **Latitude**
- **Longitude**

#### Approach:
- Supervised regression model trained on WiFi signals  

---

### 4. Pipeline Structure

The workflow follows:

1. Data Loading  
2. Preprocessing  
3. Feature–Target Split  
4. Model Training:
   - Classification (Building & Floor)
   - Regression (Coordinates)  
5. Model Evaluation  

---

## Evaluation

### Classification Metrics:
- Accuracy  

### Regression Metrics:
- Mean Squared Error (MSE)  
- Prediction error distance (approximation of localization accuracy)  

---

## Key Insights

- WiFi signals can effectively distinguish between **buildings and floors**  
- Predicting **exact coordinates** is more challenging due to signal noise  
- Classification performance is generally stronger than regression  
- High dimensionality requires models that can handle complex feature interactions  

---

## Challenges

- Sparse and noisy WiFi signal data  
- High-dimensional feature space  
- Non-linear relationships between signal strength and location  
- Variability in indoor environments  

---

## Conclusion

This project demonstrates that:
- Machine learning can effectively solve indoor localization problems  
- **Random Forest** performs well for classification tasks  
- Regression models can approximate location, but with some error  
- WLAN fingerprinting is a practical approach for indoor positioning systems  

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  

---

## Keywords

Indoor Localization, WLAN Fingerprinting, Machine Learning, Random Forest, Classification, Regression, WiFi Signals, Positioning Systems
