# 🚀 Real-Time Object Detection using TensorFlow & OpenCV

<p align="center">
  <img src="https://github.com/SinghPriya5/Real-Time-Object-Detection-/blob/main/sample_detection.gif" width="500" />
</p>

## 🔍 Overview

This project demonstrates **real-time object detection** using a webcam feed. It leverages the **TensorFlow Object Detection API** and **OpenCV** to capture frames, detect multiple objects, and display bounding boxes with confidence scores — all live!

## 🛠️ Tech Stack

* **Python 3.11**
* **TensorFlow 2.12.0**
* **OpenCV 4.x**
* **Object Detection API (SSD MobileNet V2)**

## 🔧 Features

* Live webcam feed for object detection
* Real-time bounding boxes and labels
* Adjustable confidence threshold
* Optimized for CPU environments

## 🔼 Installation

```bash
# Clone the repository
git clone https://github.com/SinghPriya5/Real-Time-Object-Detection-.git
cd Real-Time-Object-Detection-

# Create virtual environment
conda create -n tfod_310 python=3.11 -y
conda activate tfod_310

# Install dependencies
pip install tensorflow==2.12.0 opencv-python matplotlib numpy
```

## 📂 Model Setup

1. Download the pre-trained **SSD MobileNet V2** model from TensorFlow Zoo.
2. Extract and place it inside your `Tensorflow/workspace/models/` directory.
3. Load checkpoint using:

   ```python
   ckpt = tf.compat.v2.train.Checkpoint(model=detection_model)
   ckpt.restore(os.path.join(paths['CHECKPOINT_PATH'], 'ckpt-1')).expect_partial()
   ```

## 🔄 How It Works

1. The webcam captures live video frames using OpenCV.
2. Each frame is converted to a tensor and passed through the trained detection model.
3. TensorFlow processes the image, identifies objects, and returns bounding boxes with confidence scores.
4. The results are displayed in real-time using visualization utilities.

## 🎥 Demo Video

> 🎬 Watch the full project demo below:

[![Watch the video](https://github.com/SinghPriya5/Real-Time-Object-Detection-/blob/main/object%20detection.mp4)]

<video width="600" controls>
  <source src="object detection.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## 📊 Output Preview

<p align="center">
  <img src="https://github.com/SinghPriya5/Real-Time-Object-Detection-/blob/main/output_detected_image.jpg" width="600" />
</p>

## 🔬 Future Improvements

* Integrate custom-trained models
* Deploy via Streamlit for browser-based detection
* Add object tracking (SORT / DeepSORT)

## 👩‍💻 Author

**Priya Singh**
Aspiring Data Scientist | AI & ML Enthusiast
[LinkedIn](https://www.linkedin.com/in/singhpriya5) | [GitHub](https://github.com/SinghPriya5)

---

> *"Your webcam just got smarter with TensorFlow!"*
