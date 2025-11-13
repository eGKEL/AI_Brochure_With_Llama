## 🛰️ EuroSAT Image Classification Model

Deep learning model for satellite image classification using the EuroSAT (RGB) dataset.
Fully TensorFlow/Keras, GPU-ready, and designed to run smoothly in Google Colab.

📚 Overview

This project includes everything required to classify EuroSAT satellite images into 10 land-use categories using a trained TensorFlow model.

Included files:

eurosat_model.h5 — trained TensorFlow model (your working model4)

EuroSAT_Classification.ipynb — simple notebook for running predictions

README.md — documentation

This notebook supports:

✔ Uploading the model in Colab
✔ Uploading a single image
✔ Viewing the prediction with confidence
✔ Viewing all 10 class probabilities
✔ Visual preview of the uploaded image

## 📁 Folder Structure

```
eurosat_classifier/
│
├── eurosat_model.h5               # Trained TensorFlow model (64×64 input)
├── EuroSAT_Classification.ipynb   # Notebook for single-image prediction
└── README.md                      # Documentation
```


## 🧠 EuroSAT Classes

The model predicts one of the following 10 land-use categories:

- **AnnualCrop**
- **Forest**
- **HerbaceousVegetation**
- **Highway**
- **Industrial**
- **Pasture**
- **PermanentCrop**
- **Residential**
- **River**
- **SeaLake**


## 🚀 Running in Google Colab (Recommended)

1. Upload the project folder to **Google Drive**
2. Open **EuroSAT_Classification.ipynb** in Google Colab
3. Go to **Runtime → Change runtime type → GPU**
4. Run all cells in order

The notebook will guide you through:
- Uploading the model (`eurosat_model.h5`)
- Uploading an image for prediction
- Viewing:
  - Predicted class
  - Confidence percentage
  - Full probability distribution
  - Image preview

---

## 🔧 Model Details

- **Framework:** TensorFlow / Keras  
- **Input shape:** `64 × 64 × 3`  
- **Preprocessing:**  
  - Resize image to `64 × 64`  
  - Normalize pixel values to `[0, 1]`  
- **Output layer:** Softmax with **10 EuroSAT classes**

---

## 🖼️ Example Output

**Prediction:** Industrial *(92.14%)*

AnnualCrop → 0.0012
Forest → 0.0000
HerbaceousVegetation → 0.0043
Highway → 0.0001
Industrial → 0.9214
Pasture → 0.0021
PermanentCrop → 0.0665
Residential → 0.0017
River → 0.0002
SeaLake → 0.0025



The notebook also displays the uploaded image.

---

## 📝 Notes

- Only **.h5 TensorFlow/Keras models** are supported  
- Input image must be **RGB** (PNG/JPG)  
- Best performance is on **EuroSAT RGB** images  
- GPU is recommended but not required  
- This project uses the verified working model: **model4.h5**

---

## ✔️ Ready to Use

Upload the model → Upload an image → Get instant predictions  
No training. No configuration. No headaches.
