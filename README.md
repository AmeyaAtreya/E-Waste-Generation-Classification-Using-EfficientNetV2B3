# 🔌 E-Waste Image Classification Using EfficientNetV2B3 (Transfer Learning)

## 🧠 Project Overview

Electronic waste (e-waste) is an escalating global issue due to its hazardous and non-biodegradable nature. Manual classification is inefficient and error-prone. This project automates the classification of e-waste images using **Transfer Learning with EfficientNetV2B3**, a state-of-the-art convolutional neural network, to support faster and more accurate sorting for sustainable recycling.

---

## 🎯 Aim

To develop a highly accurate and efficient deep learning model using **EfficientNetV2B3** to classify electronic waste images into 10 predefined categories. The project promotes sustainable e-waste management and encourages circular economy practices.

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

- Image resizing (224×224) and rescaling
- Data augmentation (flip, rotate, zoom, contrast, translation, brightness)
- Normalization with `preprocess_input` for EfficientNetV2B3 compatibility

---

## 🏗️ Model Architecture

- **Base:** EfficientNetV2B3 (pretrained on ImageNet)
- **Custom Head:**
  - `GlobalAveragePooling2D`
  - `Batchnormalization`
  - `Dropout (rate=0.3)`
  - `Dense (Softmax activation for 10 classes)`
- **Training Config:**
  - Optimizer: `Adam (lr=0.0001)`
  - Loss: `SparseCategoricalCrossentropy`
  - Metric: `Accuracy`
  - Epochs: `15`
  - ReduceLROnPlateau: `factor=0.5`, `patience=5`, `min_lr=0.00001`
  - Early Stopping: `patience=5`, `restore_best_weights=True`

---

## 📈 Evaluation Metrics 

- ✅ **Training Accuracy:** 0.9757
- ✅ **Validation Accuracy:** 0.9767
- ✅ **Test Accuracy:** 0.9733
- ✅ **Test Loss:** 0.0890
- ✅ **F1 Scores:** 0.97

---

## 🚀 Deployment

A **Gradio** interface allows users to upload an image and get instant predictions from the trained model. This real-time classification tool makes the system usable for practical e-waste sorting applications.

---

## 📌 Conclusion

This project demonstrates the power of **Transfer Learning with EfficientNetV2B3** for accurate and efficient e-waste image classification. The model's performance, combined with a user-friendly web interface, offers a promising solution to automate and scale e-waste management processes.

---

## 📈 Future Scope

- Experiment with custom CNNs, and other models (like MobileNet, XceptionNet etc)
- Apply advanced hyperparameter tuning for optimization
- Integrate object detection for localizing e-waste within images

---

## 👨‍🔬 Contributors

- 👤 Ameya Atreya
- 📫 Feel free to reach out for collaboration or feedback.
- 🔗 [LinkedIn](https://www.linkedin.com/in/ameya-atreya/)

---

