# 🦋 MobileNet Butterfly Classifier

An advanced image classification model built with TensorFlow and Keras that identifies 100 different species of butterflies with **95% accuracy**. 

## 🧠 Project Overview
This project leverages **Transfer Learning** using the `MobileNetV2` architecture. By fine-tuning a model pre-trained on ImageNet, the classifier quickly and accurately learns the distinct wing patterns, shapes, and colors of 100 butterfly species.

### Key Features
* **Transfer Learning:** Utilized `MobileNetV2` for high-efficiency feature extraction.
* **Data Augmentation:** Implemented dynamic scaling, zooming, flipping, and rotation to prevent model overfitting.
* **Exploratory Data Analysis (EDA):** Visualized dataset distributions using Matplotlib to ensure balanced training and validation classes.
* **High Accuracy:** Achieved a 95% success rate on the test dataset.

## 🏗️ Model Architecture
This project uses **MobileNetV2** as its base model. 
* **Why MobileNetV2?** It uses "depthwise separable convolutions," making it incredibly fast, lightweight, and computationally efficient. It is the perfect choice for edge devices, mobile apps, or web deployments.
* **Custom Classification Head:** We removed the original 1000-class ImageNet head (`include_top=False`) and attached a custom `Dense` layer with `softmax` activation to classify our specific 100 butterfly classes.

## 🛠️ Tech Stack
* **Language:** Python
* **Deep Learning Framework:** TensorFlow / Keras
* **Data Visualization:** Matplotlib
* **Environment:** Jupyter Notebook / VS Code

## 📁 Repository Contents
* `Butterfly Classification.ipynb`: The main notebook containing the EDA, data preprocessing, model building, and training process.
* `butterfly_expert_95pct.keras`: The saved, fully-trained model. Ready to be deployed into applications.
* `.gitignore`: Configured to ignore the heavy image datasets during upload.

## 📊 The Dataset
The dataset consists of high-quality images of 100 distinct butterfly species.
* **Source:** [Kaggle - Butterfly Image Classification (100 Species)](https://www.kaggle.com/datasets/gpiosenka/butterfly-images40-species)

*(Note: The raw image files are not included in this repository due to GitHub size constraints, but you can download them directly from Kaggles using the link above).*

## 🚀 How to Use
To test the model yourself:
1. Clone this repository and download the dataset from Kaggle.
2. Ensure you have TensorFlow and Matplotlib installed (`pip install tensorflow matplotlib`).
3. Load the `.keras` model directly using `tf.keras.models.load_model('butterfly_expert_95pct.keras')`.
4. Pass a resized image (224x224x3) into the model to get the predicted species!
