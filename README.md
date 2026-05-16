# 🚁 VisDrone YOLOv8 Object Detection

A computer vision project using **YOLOv8** for aerial object detection on the **VisDrone Dataset**.  
This project focuses on detecting:

- 👤 Humans
- 🚗 Cars

The project includes:
- Dataset preprocessing
- YOLO dataset conversion
- Model training
- Validation
- Inference
- Performance visualization

---

# 📌 Project Overview

This notebook implements an end-to-end object detection pipeline using the Ultralytics YOLOv8 framework.

The workflow includes:

1. Dataset analysis
2. Annotation preprocessing
3. YOLO dataset preparation
4. Model training
5. Evaluation
6. Inference on test images
7. Visualization of predictions and metrics

The project is optimized for execution on **Kaggle GPU environments**.

---

# 🗂️ Project Structure

```bash
VisDrone-YOLOv8-Detection/
│
├── organized_visdrone_yolo_project.ipynb
├── README.md
│
├── dataset/
│   ├── train/
│   │   ├── images/
│   │   └── labels/
│   │
│   ├── val/
│   │   ├── images/
│   │   └── labels/
│   │
│   └── test/
│       ├── images/
│       └── labels/
│
├── results/
│   ├── weights/
│   │   ├── best.pt
│   │   └── last.pt
│   │
│   ├── results.csv
│   ├── results.png
│   └── confusion_matrix.png
│
└── graphs/
    ├── map_graph.png
    └── loss_curve.png
```

---

# 🔍 What This Project Does

## 1️⃣ Dataset Analysis
The notebook analyzes:
- Number of images
- Number of annotations
- Dataset structure

---

## 2️⃣ Dataset Preprocessing

The original VisDrone dataset contains multiple object classes.

This project filters them into two target classes:

| Original Class | Converted Class |
|---|---|
| pedestrian | human |
| people | human |
| car | car |

The labels are converted into YOLO format.

---

## 3️⃣ Annotation Visualization

The project visualizes:
- Bounding boxes
- Class labels
- Sample images

This helps verify preprocessing correctness.

---

## 4️⃣ YOLOv8 Training

The model is trained using:

- YOLOv8s pretrained weights
- Image size: `640`
- Batch size: `16`
- Epochs: `30`

Training is performed using the Ultralytics framework.

---

## 5️⃣ Model Validation

After training, the model is evaluated using:
- Precision
- Recall
- mAP@0.5
- mAP@0.5:0.95

---

## 6️⃣ Inference

The trained model performs:
- Object detection on test images
- Bounding box prediction
- Confidence score generation
- Human counting

---

## 7️⃣ Performance Visualization

The notebook generates:
- Training loss curves
- Validation loss curves
- Precision and recall graphs
- mAP performance graphs

---

# 🧠 Technologies Used

- Python
- YOLOv8
- Ultralytics
- OpenCV
- NumPy
- Pandas
- Matplotlib

---

# 📂 Dataset

Dataset Used: **VisDrone Dataset**

Official Repository:  
https://github.com/VisDrone/VisDrone-Dataset

---

# ⚙️ Installation

Install dependencies:

```bash
pip install ultralytics supervision opencv-python
```

---

# ▶️ How to Run

## Step 1 — Clone Repository

```bash
git clone https://github.com/your-username/VisDrone-YOLOv8-Detection.git
```

---

## Step 2 — Open Notebook

```bash
organized_visdrone_yolo_project.ipynb
```

---

## Step 3 — Update Dataset Paths

Update dataset paths if needed.

---

## Step 4 — Run All Cells

Execute all notebook cells sequentially.

---

# 📈 Training Output

The project generates:
- Best model weights
- Detection predictions
- Training statistics
- Evaluation metrics
- Performance graphs

---

# 🎯 Sample Capabilities

The trained model can:
- Detect humans in aerial drone footage
- Detect cars from aerial views
- Generate real-time predictions

---

# 🚀 Future Improvements

Possible future improvements:
- Multi-class detection
- Object tracking
- Video inference
- Real-time surveillance system
- YOLOv8m / YOLOv8l training
- Multi-GPU optimization

---

# 📊 Example Metrics

The notebook evaluates:
- Precision
- Recall
- mAP@0.5
- mAP@0.5:0.95

These metrics help measure detection performance.

---

# 👨‍💻 Author

Developed for computer vision research and object detection experimentation using YOLOv8 and the VisDrone dataset.

---
