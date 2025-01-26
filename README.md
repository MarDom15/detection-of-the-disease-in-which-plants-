# 🌱 SmartPlantVision

SmartPlantVision is an innovative Android application designed to help farmers and gardening enthusiasts quickly identify plant diseases. Based on machine learning and optimized for offline environments, this solution significantly improves agricultural productivity and efficiency.

---

## 📚 Table of Contents
- [🌟 Introduction](#-introduction)
- [🎯 Objectives](#-objectives)
- [✨ Key Features](#-key-features)
- [🛠️ Technologies Used](#%EF%B8%8F-technologies-used)
- [⚙️ Prerequisites](#%EF%B8%8F-prerequisites)
- [🧪 Methodology](#-methodology)
- [📊 Results](#-results)
- [🚧 Limitations and Challenges](#-limitations-and-challenges)
- [🔮 Future Improvements](#-future-improvements)
- [👥 Team](#-team)
- [📖 References](#-references)

---

## 🌟 Introduction

Agricultural losses caused by plant diseases are a major issue, impacting yields and revenues. 🌾 SmartPlantVision aims to mitigate these losses by providing a fast, affordable, and reliable method to detect plant diseases through leaf images.

The application is specifically designed to work offline, making it usable even in rural areas with limited internet access.

---

## 🎯 Objectives

1. 🧬 Detect leaf diseases for major crops:
   - **Apples**: Black Rot, Cedar Apple Rust, Apple Scab.
   - **Potatoes**: Early Blight, Late Blight.
   - **Tomatoes**: Bacterial Spot, Leaf Mold, Tomato Mosaic Virus.
   - **Corn**: Northern Corn Leaf Blight, Gray Leaf Spot, Rust.

2. 📱 Provide a simple and intuitive user interface.
3. 🚜 Ensure acceptable accuracy for reliable detection in the field.
4. 🌐 Enable offline use.

---

## ✨ Key Features

- **🤖 Disease recognition via TensorFlow Lite**: Image analysis using a neural network to identify leaf diseases.
- **⚡ Optimized model**: Based on `my_ssd_mobilenet50_v2_fpnlite`, offering an ideal balance between speed and accuracy.
- **📱 Ergonomic mobile interface**: App designed with Android Studio, compatible with modern smartphones.
- **🎯 Accuracy and efficiency**:
  - Accuracy ranging between 66% and 94% across different scenarios.
  - Fast processing time enabled by TensorFlow Lite.
- **🔍 Multi-disease analysis**: Simultaneous identification of multiple diseases for a single crop.

---

## 🛠️ Technologies Used

### Frameworks and Libraries
- **TensorFlow 2.7**: Core framework for training and optimizing the object detection model.
- **TensorFlow Lite**: Lightweight version of TensorFlow, integrated into the Android application for optimal performance.
- **Object Detection API**: Used for configuring and training object detection models.

### Development Tools
- **🖼️ LabelImg**: Used to label training images with precision.
- **💻 Android Studio**: Development environment for creating the Android application.
- **📈 TensorBoard**: For evaluating and visualizing model performance during training.

### Machine Learning Model
- **my_ssd_mobilenet50_v2_fpnlite**:
  - Image resolution: 320x320 px.
  - Optimized for a balance between accuracy and execution speed.

### Data
- **📊 Kaggle Dataset**: A collection of images with various diseases, tailored for training and testing.
- **🎨 Data augmentation techniques**:
  - Rotation.
  - Horizontal flipping.
  - Variable lighting.

---

## ⚙️ Prerequisites

### To Use the Application
- An Android smartphone (minimum Android 8.0).
- 📸 Leaf images taken against a neutral background (ideally white).
  
### For Developers
- Python 3.9 or higher.
- TensorFlow and associated dependencies.
- Android Studio for development.

---

## 🧪 Methodology

1. **📂 Data Collection and Preparation**:
   - Selected images from a Kaggle dataset containing common plant diseases.
   - Manually annotated images using tools like LabelImg.
   - Used 600 images per class to balance the dataset.

2. **🏋️ Model Training**:
   - Model based on `my_ssd_mobilenet50_v2_fpnlite`.
   - Key configurations: 320x320 px resolution, batch size of 4, 50,000 training iterations.
   - Regular evaluations with TensorBoard to adjust hyperparameters.

3. **📱 Android App Development**:
   - Integrated the exported TensorFlow Lite model into an Android application.
   - Optimized for fast processing and an intuitive user interface.

4. **🧪 Testing and Validation**:
   - Developed various test scenarios to evaluate performance under real-world conditions.
   - Analyzed results to identify strengths and limitations.

---

## 📊 Results

### Accuracy by Crop and Scenario
- **🍎 Apples**: 66-94% depending on the disease.
- **🥔 Potatoes**: 67-88%.
- **🍅 Tomatoes**: 75-92%.
- **🌽 Corn**: Not evaluated due to technical issues.

### ✅ Observed Benefits
- Good performance for individual leaves in a neutral background.
- Fast execution enabled by TensorFlow Lite.

---

## 🚧 Limitations and Challenges

- **📉 Reduced accuracy for multiple leaves in a single image.**
- **🎨 Background impact**: Performance decreases when image backgrounds are not neutral.
- **🗂️ Limited dataset volume**: Only 600 images per disease, limiting generalization.

---

## 🔮 Future Improvements

- **📈 Dataset Expansion**: Add more images and diversify capture conditions.
- **🖼️ Multi-leaf Recognition**: Enhance the algorithm to detect multiple leaves in a single image.
- **🌱 Additional Crops**: Extend the application to other plant types.
- **🤖 Agricultural Automation**: Integrate with agricultural robots for automatic field monitoring.

---

## 👥 Team

- **👨‍💻 Darius Bonk**  
- **👨‍💻 Vipul Durgade**  
- **👨‍💻 Matial Domche**  
- **👨‍💻 Kiran Krishnakumar**  

**Supervisor**: Vitali Czymmek, Fachhochschule Westküste  
**📅 Submission Date**: January 30, 2022

---

## 📖 References

- Dataset used: [New Plant Diseases Dataset](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset)
- TensorFlow tutorial: [TensorFlow Object Detection API](https://tensorflow-object-detection-api-tutorial.readthedocs.io/)
- GitHub Documentation: [TensorFlow Models Repository](https://github.com/tensorflow/models)
