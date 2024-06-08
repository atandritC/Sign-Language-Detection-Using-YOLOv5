# Sign Language Detection Using YOLOv5

## An Efficient Solution for Real-Time Sign Language Recognition

This repository contains the code and resources for building a sign language detection system using YOLOv5. The project is designed to detect and classify various sign language gestures in real-time using a deep learning approach.

## What This Repository Contains

- **Data Collection**: Scripts for collecting and labeling image data for training.
- **Model Training**: Notebooks for setting up and training the YOLOv5 model on the collected data.
- **Detection**: Code for running the trained model to detect sign language gestures.

## Project Playlist

This project was developed by following the "Sign Language Detection Using YOLOv5" tutorial on YouTube. You can find the complete playlist [here](https://youtube.com/playlist?list=PLkz_y24mlSJYWpwFbU8fyaBSwihoVHiJz).

## How to Use This Repository

### Data Collection

1. Open `data-collection.ipynb` in Jupyter Notebook or Google Colab.
2. Follow the instructions to collect and label images of various sign language gestures.
3. Save the collected data in the specified directory.

### Model Training

1. Clone the YOLOv5 repository:
   ```bash
   !git clone https://github.com/ultralytics/yolov5.git
   ```
2. Navigate to the `yolov5` directory and install the necessary dependencies:
   ```bash
   %cd yolov5
   !pip install -qr requirements.txt
   ```
3. Open `sign-lang-detection.ipynb` in Jupyter Notebook or Google Colab.
4. Follow the instructions to configure and train the YOLOv5 model using the collected data.
5. The trained model weights will be saved in the `runs/train/yolov5s_results/weights` directory.

### Model Inference

1. Enter the `yolov5` directory.
2. Run the `run.py` file using your preferred code editor or via the terminal:
   ```bash
   python run.py
   ```
   
Happy coding and good luck with your sign language detection journey!
