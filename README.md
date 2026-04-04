# Sign Language Detection

**Real-Time Sign Language Recognition with YOLOv5**  
A computer vision application that detects and classifies sign language gestures in real-time using YOLOv5 — translating hand signs into text through webcam or video input to bridge communication gaps for the deaf and hard-of-hearing community.

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB.svg?logo=python&logoColor=white)](https://www.python.org)
[![YOLOv5](https://img.shields.io/badge/YOLOv5-Object%20Detection-0066CC.svg?logo=github&logoColor=white)](https://github.com/ultralytics/yolov5)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-EE4C2C.svg?logo=pytorch&logoColor=white)](https://pytorch.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-5C3EE8.svg?logo=opencv&logoColor=white)](https://opencv.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg?logo=jupyter&logoColor=white)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 🛠 Tech Stack

**Core Framework & Model**
- Python 3.8+ — Clean, modular scripts for data collection, training, and inference
- YOLOv5 (Ultralytics) — State-of-the-art real-time object detection architecture (YOLOv5s variant)
- PyTorch — Deep learning backend for model training and GPU acceleration
- OpenCV (`cv2`) — Real-time webcam capture, frame preprocessing, and bounding box rendering

**Development Environment**
- Jupyter Notebook / Google Colab — Interactive notebooks for data collection (`data-collection.ipynb`) and model training (`sign-lang-detection.ipynb`)
- Google Colab GPU — Free cloud-based training with NVIDIA Tesla GPUs for faster convergence
- Ultralytics YOLOv5 repository — Cloned and customized for sign language gesture detection

**Data Pipeline & Annotation**
- Custom image dataset — Collected via webcam with labeled sign language gestures
- YOLO format annotations — Text files with normalized bounding box coordinates (`class x_center y_center width height`)
- Data augmentation — Built-in YOLOv5 augmentations (Mosaic, HSV shifts, flips) for robustness

**Inference & Deployment**
- `run.py` — Standalone Python script for real-time webcam inference with trained model weights
- Pre-trained weights — Saved in `runs/train/yolov5s_results/weights/best.pt` after training
- Confidence thresholding — Filters low-confidence detections for cleaner output

## ✨ Key Features

- **Real-Time Detection** — Processes webcam feed at 20-30 FPS with YOLOv5s optimized for speed
- **Multi-Gesture Recognition** — Detects and classifies multiple sign language gestures simultaneously
- **Visual Feedback** — Draws bounding boxes with class labels and confidence scores on detected hands/gestures
- **End-to-End Pipeline** — Complete workflow: data collection → annotation → training → inference in one repository
- **Cloud-Ready Training** — Google Colab notebooks for GPU-accelerated training without local hardware requirements
- **Lightweight Model** — YOLOv5s variant balances accuracy and speed for real-time applications
- **Accessible Design** — Built to assist deaf and hard-of-hearing individuals with communication

## 📸 Demo

![Sign Language Detection Demo](https://github.com/atandritC/Demo-GIFs-Pictures/blob/main/Sign%20Language%20Detection.jpeg)

## 🏗 Architecture

- **Three-Stage Pipeline** — `data-collection.ipynb` (image capture) → `sign-lang-detection.ipynb` (model training) → `run.py` (inference)
- **YOLOv5 Integration** — Cloned Ultralytics repo customized with sign language dataset in YOLO format
- **Transfer Learning** — Pre-trained COCO weights fine-tuned on custom sign language gestures for faster convergence
- **Bounding Box Normalization** — Annotations stored as normalized coordinates (0-1) relative to image dimensions
- **Modular Training Config** — YAML configuration file defines classes, paths, and hyperparameters for easy modification
- **Inference Optimization** — Model loaded once at startup; frames processed in loop with minimal overhead

## ⚙️ How to Run Locally

No complex setup — just Python, Git, and optional GPU for training.

```bash
# Clone the YOLOv5 repository
git clone https://github.com/ultralytics/yolov5.git
cd yolov5

# Install dependencies
pip install -qr requirements.txt

# For inference (using pre-trained weights):
python run.py

# For training (in Jupyter/Colab):
# 1. Open sign-lang-detection.ipynb
# 2. Upload your dataset or use collected images
# 3. Run all cells to train the model
# 4. Weights saved in runs/train/yolov5s_results/weights/best.pt
```

> 💡 **Google Colab Option**: Upload notebooks to Colab for free GPU training — no local setup required.  
> 📹 **Webcam Required**: Inference script (`run.py`) needs a webcam to capture live video feed.  
> 🎯 **Default Classes**: Modify `data.yaml` to add/remove sign language gestures for your use case.

## 🧠 Challenges Faced & Solutions

| Challenge | Solution |
|---|---|
| Limited labeled sign language datasets for training | Built custom data collection pipeline using webcam capture with manual labeling in YOLO format |
| Real-time performance on CPU-only machines | Used YOLOv5s (smallest variant) with image resizing to 640×640 for acceptable FPS on CPU |
| Hand gesture variations (lighting, angles, skin tones) | Applied YOLOv5's built-in data augmentation (Mosaic, HSV shifts, random flips) to improve generalization |
| Class imbalance between different signs | Oversampled underrepresented gestures and used class-aware sampling during training |
| Bounding box annotation format mismatch | Converted raw pixel coordinates to YOLO's normalized format (`x_center y_center width height` / image_dim) |
| Model overfitting on small dataset | Implemented early stopping, reduced model complexity (YOLOv5s), and increased augmentation intensity |

## 📈 What I Learned

- Implementing end-to-end computer vision pipelines: data collection → annotation → training → deployment
- Customizing YOLOv5 for domain-specific tasks (sign language) beyond standard COCO object detection
- Working with Google Colab for GPU-accelerated deep learning without local hardware investment
- Understanding YOLO's annotation format and converting between coordinate systems (pixel ↔ normalized)
- Balancing model size, accuracy, and inference speed for real-time applications
- The importance of data quality and augmentation in achieving robust gesture recognition across diverse conditions
- Building accessible technology that addresses real-world communication barriers

## 🤝 Contributing

Contributions are welcome! To get started:

1. Fork the repo and create your feature branch:  
   `git checkout -b feature/AmazingFeature`
2. Commit your changes:  
   `git commit -am 'Add some AmazingFeature'`
3. Push to the branch:  
   `git push origin feature/AmazingFeature`
4. Open a Pull Request with a clear description of your changes

**Guidelines**:
- Follow PEP 8 style and include comments for complex data processing logic
- Test inference with various lighting conditions and hand positions
- Document any new sign language gestures added to the dataset
- Preserve backward compatibility with existing YOLOv5 integration

---

**Credits**: This project was built following the comprehensive [Sign Language Detection YouTube Playlist](https://youtube.com/playlist?list=PLkz_y24mlSJYWpwFbU8fyaBSwihoVHiJz&si=ssh-POaD9XPm4Q8g). Special thanks to the creator for exceptional tutorials.
