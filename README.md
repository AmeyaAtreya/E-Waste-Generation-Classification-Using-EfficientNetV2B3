# 🔌 E-Waste Image Classification Using EfficientNetV2B0 (Transfer Learning)

## 🧠 Project Overview

Electronic waste (e-waste) is an escalating global issue due to its hazardous and non-biodegradable nature. Manual classification is inefficient and error-prone. This project automates the classification of e-waste images using **Transfer Learning with EfficientNetV2B0**, a state-of-the-art convolutional neural network, to support faster and more accurate sorting for sustainable recycling.

---

## 🎯 Aim

To develop a highly accurate and efficient deep learning model using **EfficientNetV2B0** to classify electronic waste images into 10 predefined categories. The project promotes sustainable e-waste management and encourages circular economy practices.

---

## 📚 Learning Objectives

- 📂 Understand and preprocess image data
- 📊 Perform exploratory data analysis
- 🔁 Apply transfer learning using EfficientNetV2B0
- 🧠 Train and evaluate deep learning models
- 🌐 Deploy models using **Gradio** for real-time testing

---

## 🧰 Tools & Technologies Used

| Tool/Library       | Purpose                                      |
|--------------------|----------------------------------------------|
| Python             | Primary programming language                 |
| TensorFlow & Keras | Model construction and training              |
| Pillow (PIL)       | Image handling and processing                |
| Gradio             | Web interface for model interaction          |
| Jupyter Notebook   | Interactive development environment          |

---

## 🗂 Dataset

- **Name:** [E-Waste Image Dataset](https://www.kaggle.com/datasets/akshat103/e-waste-image-dataset)
- **Categories:** PCB, Player, Battery, Microwave, Mobile, Mouse, Printer, Television, Washing Machine, Keyboard
- **Structure:**
  - `train/` - 2400 images (240 per class)
  - `validation/` - 300 images (30 per class)
  - `test/` - 300 images (30 per class)

---

## 🛠️ Preprocessing Steps

- Image resizing (128×128) and rescaling
- Data augmentation (flip, rotate, zoom)
- Normalization with `preprocess_input` for EfficientNetV2B0 compatibility

---

## 🏗️ Model Architecture

- **Base:** EfficientNetV2B0 (pretrained on ImageNet)
- **Custom Head:**
  - `GlobalAveragePooling2D`
  - `Dropout (rate=0.2)`
  - `Dense (Softmax activation for 10 classes)`
- **Training Config:**
  - Optimizer: `Adam (lr=0.0001)`
  - Loss: `SparseCategoricalCrossentropy`
  - Metric: `Accuracy`
  - Epochs: `15`
  - Early Stopping: `patience=3`, `restore_best_weights=True`

---

## 📈 Evaluation Metrics

- ✅ **Training Accuracy:** 99.08%
- ✅ **Validation Accuracy:** 96.00%
- ✅ **Test Accuracy:** 96.00%
- ✅ **Test Loss:** 0.1073
- ✅ **F1 Scores:** 0.92 to 1.00 across all classes
- ✅ Balanced class-wise support ensures fair performance evaluation

---

## 🚀 Deployment

A **Gradio** interface allows users to upload an image and get instant predictions from the trained model. This real-time classification tool makes the system usable for practical e-waste sorting applications.

---

## 📌 Conclusion

This project demonstrates the power of **Transfer Learning with EfficientNetV2B0** for accurate and efficient e-waste image classification. The model's performance, combined with a user-friendly web interface, offers a promising solution to automate and scale e-waste management processes.

---

## 📈 Future Scope

- Experiment with larger EfficientNet variants (e.g., V2B1/B2)
- Apply advanced hyperparameter tuning for optimization
- Integrate object detection for localizing e-waste within images

---

## 👨‍🔬 Contributors

- 👤 Your Name
- 📫 Feel free to reach out for collaboration or feedback.

---

