# Pickup Truck Detection & Cargo Volume Estimation

## 📋 Overview
This project provides a Python pipeline for detecting **pickup trucks** in single image frames from **urban traffic cameras**, segmenting their truck beds, and estimating **cargo volume** in cubic meters.  

It is modular, so you can start with simple detection and progressively add more advanced components like bed segmentation, perspective correction, and depth-based height estimation.

---

## ✨ Features
- **Vehicle detection & classification** using YOLOv8 (or compatible models) with a confidence threshold.
- Filters detections to **pickup trucks only**.
- **Truck bed segmentation** (placeholder for custom model integration).
- Dimension scaling via **known object reference** (e.g., license plate) or **average bed sizes**.
- Volume calculation: `Length × Width × Height`.
- Annotated output image with class, confidence, and estimated volume.
- Console output with structured results.

---

## 🛠 Requirements
- Python 3.8+
- PyTorch 2.x
- Ultralytics YOLOv8
- OpenCV
- NumPy
- Matplotlib

---

## 📦 Installation
```bash
pip install ultralytics opencv-python-headless torch torchvision matplotlib numpy
# Optional: Depth estimation models (e.g., MiDaS)
pip install timm
