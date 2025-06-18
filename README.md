<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>E-Waste Image Classification</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Montserrat', sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 0;
      background-color: #f4f6f8;
      color: #333;
    }
    .container {
      max-width: 900px;
      margin: 3rem auto;
      padding: 2rem;
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.05);
    }
    h1, h2, h3 {
      color: #2c3e50;
    }
    h1 {
      text-align: center;
      margin-bottom: 1rem;
    }
    code {
      background: #e8e8e8;
      padding: 2px 4px;
      border-radius: 4px;
    }
    a {
      color: #1e88e5;
      text-decoration: none;
    }
    ul {
      padding-left: 20px;
    }
    .section {
      margin-bottom: 2rem;
    }
    table {
      border-collapse: collapse;
      width: 100%;
      margin: 1rem 0;
    }
    th, td {
      border: 1px solid #ddd;
      padding: 0.75rem;
      text-align: left;
    }
    th {
      background-color: #f0f0f0;
    }
    .footer {
      text-align: center;
      font-size: 0.9rem;
      color: #777;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🔌 E-Waste Image Classification Using EfficientNetV2B0</h1>

    <div class="section">
      <h2>📌 Project Overview</h2>
      <p>Automated classification of e-waste using transfer learning and EfficientNetV2B0. This project supports better sorting, faster recycling, and promotes a sustainable electronic ecosystem.</p>
    </div>

    <div class="section">
      <h2>🎯 Aim</h2>
      <p>To build an accurate image classifier for e-waste using <strong>EfficientNetV2B0</strong> and deploy it with a web-based interface using Gradio.</p>
    </div>

    <div class="section">
      <h2>📚 Learning Objectives</h2>
      <ul>
        <li>Data preprocessing and preparation</li>
        <li>Exploratory Data Analysis (EDA)</li>
        <li>Applying Transfer Learning</li>
        <li>Training & Evaluating Deep Learning Models</li>
        <li>Deploying with Gradio</li>
      </ul>
    </div>

    <div class="section">
      <h2>🧰 Tools & Technologies</h2>
      <table>
        <thead>
          <tr><th>Tool/Library</th><th>Purpose</th></tr>
        </thead>
        <tbody>
          <tr><td>Python</td><td>Core programming and data processing</td></tr>
          <tr><td>TensorFlow & Keras</td><td>Model architecture and training</td></tr>
          <tr><td>Pillow</td><td>Image handling</td></tr>
          <tr><td>Gradio</td><td>Model deployment UI</td></tr>
          <tr><td>Jupyter Notebook</td><td>Development & visualization</td></tr>
        </tbody>
      </table>
    </div>

    <div class="section">
      <h2>🗂 Dataset</h2>
      <p><strong>Source:</strong> <a href="https://www.kaggle.com/datasets/akshat103/e-waste-image-dataset" target="_blank">Kaggle E-Waste Dataset</a></p>
      <ul>
        <li>10 categories: PCB, Player, Battery, Microwave, Mobile, Mouse, Printer, TV, Washing Machine, Keyboard</li>
        <li>Train: 2400 images | Validation: 300 images | Test: 300 images</li>
        <li>Balanced dataset with 30 images/class in test and validation</li>
      </ul>
    </div>

    <div class="section">
      <h2>🛠️ Preprocessing Steps</h2>
      <ul>
        <li>Resizing to <code>128x128</code>, normalization, and augmentation</li>
        <li>Random flips, rotations, and zooms for generalization</li>
        <li>Using <code>preprocess_input</code> for EfficientNet compatibility</li>
      </ul>
    </div>

    <div class="section">
      <h2>🏗️ Model Architecture</h2>
      <ul>
        <li>Base: Pre-trained <strong>EfficientNetV2B0</strong> on ImageNet</li>
        <li>Custom head: <code>GlobalAveragePooling2D → Dropout → Dense(Softmax)</code></li>
        <li>Optimized using <code>Adam</code> with learning rate <code>0.0001</code></li>
        <li>Loss: <code>SparseCategoricalCrossentropy</code></li>
        <li>Training: 15 epochs, batch size 100, early stopping enabled</li>
      </ul>
    </div>

    <div class="section">
      <h2>📈 Evaluation</h2>
      <ul>
        <li><strong>Train Accuracy:</strong> 99.08%</li>
        <li><strong>Validation Accuracy:</strong> 96.00%</li>
        <li><strong>Test Accuracy:</strong> 96.00%</li>
        <li>Strong F1-scores (0.92 - 1.00) across all 10 classes</li>
        <li>Balanced performance, robust generalization</li>
      </ul>
    </div>

    <div class="section">
      <h2>🚀 Deployment</h2>
      <p>Interactive classification using <strong>Gradio</strong>. Upload a sample image and get predicted e-waste class with confidence score.</p>
    </div>

    <div class="section">
      <h2>📌 Conclusion</h2>
      <p>This project demonstrates the strength of EfficientNetV2B0 and transfer learning for classifying e-waste images. With a robust model and real-time deployment via Gradio, it contributes effectively to sustainable electronic waste management.</p>
    </div>

    <div class="section">
      <h2>🧠 Future Enhancements</h2>
      <ul>
        <li>Try deeper EfficientNet variants (B1, B2)</li>
        <li>Experiment with advanced hyperparameter tuning</li>
        <li>Integrate object detection for better localization</li>
      </ul>
    </div>

    <div class="section">
      <h2>👨‍💻 Contributors</h2>
      <p><strong>Your Name</strong><br/>
      📫 Open for collaboration and feedback!</p>
    </div>

    <div class="footer">
      &copy; 2025 E-Waste Classifier | Built with ❤️ using Python and TensorFlow
    </div>
  </div>
</body>
</html>
