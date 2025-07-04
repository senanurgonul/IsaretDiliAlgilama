# 🤟 SignLanguageDetection

This project is a **computer vision** application designed to visualize the lyrics of MFÖ's song **"Ele Güne Karşı"** through sign language and lip movements. The developed system detects sign language gestures using object detection and makes word-level predictions.

---

## 🎯 Project Objective

The goal is to create a visual dataset containing sign language gestures and enable computer interpretation of sign language using object detection techniques.

---

## 🧠 Technologies Used

- 📦 **TensorFlow 2** – For model training and prediction  
- 🎯 **TensorFlow Object Detection API** – For object detection architecture  
- 🗂️ **TFRecord** – Dataset format  
- 🧰 **Roboflow** – For image labeling and dataset management  
- 🖼️ **1,292 images** – Sign and lip gestures for 93 different words

---

## 🧪 Methods

1. **Dataset Creation:**
   - 1,292 images were captured for the lyrics of MFÖ’s “Ele Güne Karşı”  
   - 93 different sign and lip movement classes were defined  
   - All images were manually labeled using Roboflow

2. **Model Training:**
   - Based on NickNochnack’s [Real-Time Object Detection](https://github.com/nicknochnack/RealTimeObjectDetection) repository  
   - Customized pipeline (batch size, learning rate, etc.)  
   - Data split: 70% training, 20% validation, 10% testing

3. **Model Testing:**
   - Example output: “sormak” predicted with 76% accuracy  
   - Model produced reasonably successful basic results

---

## 🖥️ Usage

1. Install TensorFlow and the Object Detection API  
2. Download the dataset from Roboflow and convert it to `TFRecord` format  
3. Customize the `pipeline.config` file with your dataset paths  
4. Train the model and analyze the results
