# Diabetic Retinopathy Prediction

A Flask web application that uses a pre-trained TensorFlow 1.x model to classify diabetic retinopathy stages from retinal images.

## 🚀 Live Demo
[View Live App on Render](https://diabetic-retinopathy-app-pl1g.onrender.com/)

## 🔑 Credentials
- **Username:** `admin`
- **Password:** `admin`

---

## 🛠️ Performance & Features
- **Model:** Pre-trained Inception-based model (`retrained_graph.pb`).
- **Classification Phases:**
  - Normal ✓
  - Mild ❌
  - Moderate ❌
  - Severe ❌
  - Proliferative ❌
- **Backend:** Flask (Python 3.7)
- **Frontend:** Glassmorphism UI with Bootstrap 5.

---

## 💻 Local Setup

### 1. Prerequisites
- [Anaconda](https://www.anaconda.com/products/distribution) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
- Python 3.7 (Required for TensorFlow 1.14)

### 2. Environment Creation
```bash
# Create a conda environment
conda create -n dr_env python=3.7 -y

# Activate the environment
conda activate dr_env

# Install dependencies
pip install tensorflow==1.14.0 flask==2.2.5 numpy==1.16.6 pandas scikit-learn six protobuf==3.20.3
```

### 3. Running the App
```bash
python app.py
```
Visit `http://127.0.0.1:5000` in your browser.

---

## ☁️ Deployment (Render.com)

This project is configured to deploy via **Docker** on Render.com to ensure compatibility with Python 3.7.

1.  Connect your GitHub repository to [Render](https://render.com/).
2.  Choose **Web Service**.
3.  Render will automatically detect the `Dockerfile` and `render.yaml` to build the environment.

---

## 📄 Project Structure
- `app.py`: Flask application server.
- `label_image.py`: TensorFlow inference logic.
- `retrained_graph.pb`: Pre-trained model weights.
- `templates/`: HTML templates.
- `static/`: CSS, JS, and Images.
- `Dockerfile`: Container configuration for deployment.
