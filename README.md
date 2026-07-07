Animal Instance Segmentation using YOLOv8
📌 Project Overview

This project focuses on Animal Instance Segmentation, a computer vision task that detects individual animals in an image and generates a separate segmentation mask for each detected object. Unlike traditional image classification, which only identifies the animal category, instance segmentation provides the exact shape and location of every animal present in the image.

The project is implemented using YOLOv8, one of the latest real-time object detection and segmentation models. It includes the complete machine learning workflow—from dataset preparation and preprocessing to model training, evaluation, visualization, and inference.

🎯 Objectives
Detect multiple animals in a single image.
Generate accurate segmentation masks for each detected animal.
Perform data preprocessing and cleaning.
Train a deep learning segmentation model.
Evaluate model performance using standard metrics.
Visualize prediction results.
Build a scalable computer vision pipeline.
🛠 Technologies Used
Python
Google Colab
YOLOv8 (Ultralytics)
OpenCV
NumPy
Pandas
Matplotlib
Scikit-learn
Kaggle Dataset
Jupyter Notebook
📂 Project Structure
Animal-Instance-Segmentation/
│
├── Dataset/
│   ├── train/
│   ├── valid/
│   └── test/
│
├── notebooks/
│   └── Animal_Instance_Segmentation.ipynb
│
├── models/
│   ├── best.pt
│   └── last.pt
│
├── results/
│   ├── prediction_images/
│   ├── segmentation_results/
│   └── evaluation_metrics/
│
├── README.md
└── requirements.txt
📊 Dataset

The project uses an animal image dataset containing multiple animal species. The dataset is divided into:

Training Set
Validation Set
Testing Set

Each image contains corresponding segmentation annotations required for training the YOLOv8 segmentation model.

🔄 Workflow
Step 1: Data Collection
Download dataset
Verify images
Organize folders
Step 2: Data Preprocessing
Remove duplicate images
Handle missing data
Resize images
Normalize pixel values
Convert annotations to YOLO format
Split dataset into train, validation, and test sets
Step 3: Exploratory Data Analysis (EDA)
Dataset distribution
Class frequency analysis
Image dimension analysis
Sample image visualization
Step 4: Model Training

Train the YOLOv8 segmentation model using the prepared dataset.

Training includes:

Loading pretrained weights
Hyperparameter tuning
Batch training
Validation after every epoch
Saving best model
Step 5: Model Evaluation

Performance is evaluated using:

Precision
Recall
F1-Score
mAP@50
mAP@50-95
IoU (Intersection over Union)
Loss Curves
Step 6: Prediction

The trained model predicts:

Animal class
Bounding Box
Confidence Score
Segmentation Mask
Step 7: Visualization

The output displays:

Original Image
Detected Objects
Segmentation Masks
Confidence Scores
⚙️ Installation

Clone the repository

git clone https://github.com/yourusername/Animal-Instance-Segmentation.git

Move into the project folder

cd Animal-Instance-Segmentation

Install dependencies

pip install -r requirements.txt
▶️ Training
from ultralytics import YOLO

model = YOLO("yolov8n-seg.pt")

model.train(
    data="data.yaml",
    epochs=100,
    imgsz=640
)
▶️ Prediction
from ultralytics import YOLO

model = YOLO("best.pt")

results = model.predict("image.jpg", save=True)
📈 Evaluation Metrics
Metric	Description
Precision	Correct positive detections
Recall	Percentage of detected objects
F1-Score	Balance between precision and recall
mAP@50	Mean Average Precision at IoU 0.50
mAP@50-95	Average precision across IoU thresholds
IoU	Measures overlap between prediction and ground truth
💡 Features
Real-time instance segmentation
Multiple animal detection
High-quality segmentation masks
Deep learning based solution
Easy deployment
Visualization of predictions
Scalable architecture
Modular codebase
📷 Sample Output

The model outputs:

Original Image
Segmentation Mask
Bounding Boxes
Animal Labels
Confidence Scores

Example:

Image
      ↓
YOLOv8 Segmentation
      ↓
Detected Animals
      ↓
Segmentation Masks
      ↓
Final Prediction
🚀 Future Improvements
Increase dataset size
Train with larger YOLOv8 models
Improve segmentation accuracy
Deploy as a web application
Real-time webcam inference
Mobile application support
Cloud deployment
Support for additional animal species
📚 Learning Outcomes

Through this project, the following concepts were explored:

Computer Vision
Deep Learning
Object Detection
Instance Segmentation
Data Preprocessing
Model Evaluation
Image Annotation
Transfer Learning
YOLOv8 Framework
Performance Analysis
📌 Applications
Wildlife Monitoring
Forest Surveillance
Animal Conservation
Smart Zoos
Veterinary Research
Agriculture
Biodiversity Studies
Automated Animal Counting
Ecological Research
📄 Requirements
Python >= 3.10

ultralytics
opencv-python
numpy
pandas
matplotlib
scikit-learn
torch
torchvision
Pillow
PyYAML

Install using:

pip install ultralytics opencv-python numpy pandas matplotlib scikit-learn torch torchvision Pillow PyYAML
🤝 Contribution

Contributions are welcome! Feel free to:

Fork the repository
Create a new branch
Make improvements
Submit a pull request
📜 License

This project is intended for educational and research purposes. You are free to use and modify the code with proper attribution.
