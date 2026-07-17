
# 🐾 Animal Instance Segmentation using YOLOv8

## 📌 Project Overview

This project focuses on **Animal Instance Segmentation**, a computer vision task that detects individual animals in an image while generating precise pixel-level segmentation masks for each detected object. Unlike traditional object detection, instance segmentation identifies each animal separately, even when multiple animals belong to the same class.

The model is built using **YOLOv8 Segmentation** and trained on a custom animal dataset containing multiple animal species. The project demonstrates the complete deep learning pipeline, from data preprocessing to model training, evaluation, and inference.

---

## 🎯 Objectives

- Detect multiple animals in a single image.
- Generate accurate segmentation masks for each detected animal.
- Classify detected animals into their respective categories.
- Improve detection accuracy using transfer learning and data augmentation.
- Evaluate the model using standard segmentation metrics.

---

## ✨ Features

- Pixel-level instance segmentation
- Real-time object detection
- Multi-class animal classification
- Automatic mask generation
- Bounding box prediction
- Confidence score estimation
- High-speed inference using YOLOv8
- GPU-supported training

---

## 🗂️ Dataset

The project uses an animal image dataset consisting of multiple animal categories.

**Selected Classes**
- Cat
- Dog
- Lion
- Tiger
- Elephant

Each class contains several hundred annotated images used for training and validation.

---

## 🧠 Model Architecture

- **Model:** YOLOv8 Segmentation
- **Framework:** Ultralytics YOLOv8
- **Language:** Python
- **Deep Learning Library:** PyTorch

The model predicts:

- Bounding Boxes
- Segmentation Masks
- Object Class
- Confidence Score

simultaneously in a single forward pass.

---

## ⚙️ Technologies Used

- Python
- PyTorch
- YOLOv8
- Ultralytics
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

---

## 📂 Project Workflow

1. Dataset Collection
2. Data Preprocessing
3. Image Annotation
4. Data Augmentation
5. Dataset Splitting
6. Model Training
7. Validation
8. Model Evaluation
9. Inference
10. Result Visualization

---

## 📊 Evaluation Metrics

The model performance is evaluated using:

- Precision
- Recall
- mAP@0.5
- mAP@0.5:0.95
- IoU (Intersection over Union)
- F1-Score

---

## 📈 Results

The trained model is capable of:

- Detecting multiple animals in a single image
- Producing accurate segmentation masks
- Identifying animal species
- Performing inference in real-time
- Handling overlapping objects effectively

---

## 📁 Project Structure

```
Animal-Instance-Segmentation/
│
├── dataset/
│   ├── train/
│   ├── valid/
│   └── test/
│
├── notebooks/
│   └── Animal_Instance_Segmentation.ipynb
│
├── models/
│   └── best.pt
│
├── runs/
│
├── results/
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

## 🚀 Installation

```bash
git clone https://github.com/yourusername/Animal-Instance-Segmentation.git

cd Animal-Instance-Segmentation

pip install -r requirements.txt
```

---

## ▶️ Training

```bash
yolo task=segment mode=train \
model=yolov8n-seg.pt \
data=data.yaml \
epochs=100 \
imgsz=640
```

---

## 🔍 Inference

```bash
yolo task=segment mode=predict \
model=best.pt \
source=test_images/
```

---

## 📷 Sample Output

The model outputs:

- Original Image
- Segmentation Mask
- Bounding Box
- Class Label
- Confidence Score

for every detected animal.

---

## 🔮 Future Improvements

- Increase the number of animal classes
- Improve segmentation accuracy
- Deploy using Streamlit or Flask
- Optimize for mobile devices
- Integrate with drone and wildlife monitoring systems
- Train using larger datasets

---

## 🌍 Applications

- Wildlife Monitoring
- Smart Zoos
- Forest Surveillance
- Biodiversity Research
- Animal Population Estimation
- Veterinary Research
- Autonomous Monitoring Systems

---

## 🤝 Contributing

Contributions are welcome. Feel free to fork the repository, create a new branch, and submit a pull request.

---

## 📜 License

This project is developed for educational and research purposes.
