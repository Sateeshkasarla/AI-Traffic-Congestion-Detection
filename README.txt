# 🚦 AI Traffic Congestion Detection and Analytics

This project implements a complete Machine Learning pipeline using Computer Vision to address increasing urban traffic congestion. The deployed system provides real-time vehicle detection, classification, and density analytics to support dynamic traffic management.

## 🎯 Business Problem Solved
Traditional traffic monitoring methods are often outdated and unable to provide the real-time insights necessary for modern, efficient urban traffic control. This project leverages AI to create a high-speed, accurate detection platform.

## 🛠️ Technical Stack & Approach
* **Model:** **YOLOv8n** (You Only Look Once, Nano version)
* **Frameworks:** Ultralytics, PyTorch
* **Deployment:** Streamlit (via Google Colab and Cloudflared tunnel)
* **Methodology:** Full **CRISP-ML(Q)** pipeline, including data preparation, modeling, and deployment.
* **Core Skills:** Computer Vision (Object Detection), Data Augmentation, MLOps.

## 📊 Project Highlights
| Component | Detail |
| :--- | :--- |
| **Dataset Size** | Over **4,000 augmented images** |
| **Classes Detected** | Car, Bus, Truck, Bike, Auto |
| **Best Model Metric**| mAP (mean Average Precision) $\approx 55\%$ |
| **Inference Speed** | Up to ~35 FPS (YOLOv8n) |
| **Deployment** | Interactive Streamlit App (`app.py`) for live detection on video/image inputs.

## 📁 Repository Contents

| File/Folder | Description |
| :--- | :--- |
| `notebooks/` | [cite_start]Contains the **training** (`final_model_training_code.ipynb`) and **deployment** (`yolov8_deployment_code.ipynb`) notebooks, executed on Google Colab (GPU: T4)[cite: 1970, 1980]. |
| `models/` | [cite_start]The trained weights file: `best8.pt`[cite: 15]. |
| `src/app.py` | [cite_start]Python script for the Streamlit application[cite: 1689]. |
| `data/` | Placeholder for the YOLO dataset (`data.yaml` and image folders). |
| `requirements.txt`| [cite_start]All necessary Python dependencies (e.g., `ultralytics`, `streamlit`, `opencv-python-headless`)[cite: 1689]. |

## 🚀 How to Run the Project

[cite_start]The easiest way to replicate this project is by following the steps in the provided notebooks on **Google Colab** (as indicated by the code structure [cite: 1970, 1989]):

1.  [cite_start]**Preparation:** Open `final_model_training_code.ipynb` to install dependencies (`ultralytics`), upload your dataset ZIP file, and initiate the YOLOv8n model training for 50 epochs[cite: 1970].
2.  [cite_start]**Model Download:** Download the resulting `best.pt` file upon training completion[cite: 1970].
3.  **Deployment:** Open `yolov8_deployment_code.ipynb`. [cite_start]This notebook installs Streamlit and Cloudflared, writes the web application logic to `app.py`[cite: 1689], and launches the live web interface using a public tunnel.

---
[cite_start]**Note:** Ensure your `best8.pt` model is uploaded to the `/models` directory when running the deployment notebook[cite: 1782].