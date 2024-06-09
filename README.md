# Sign Language Detection Using YOLOv5

## Detect Sign Language with YOLOv5

Welcome to the Sign Language Detection project! This application utilizes YOLOv5 to detect and classify sign language gestures in real-time. The project is designed to aid in communication for the deaf and hard-of-hearing community by providing a tool to translate sign language into text.

## What This Project Does

This project leverages the power of the YOLOv5 object detection model to accurately detect and classify various sign language gestures. By using a webcam or video input, the model can identify specific signs and translate them into text, making communication more accessible.

## Demonstration (Picture)

![Sign Language Detection Demo Pic](https://github.com/atandritC/Demo-GIFs-Pictures/blob/main/Sign%20Language%20Detection.jpeg)

## Installation and Usage Instructions 

If you would like to run the application locally or contribute to its development, follow these steps:

### Prerequisites

Ensure you have Python 3.x installed on your machine. You can download it from [python.org](https://www.python.org/downloads/).

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

### File Descriptions

- `data-collection.ipynb`: Notebook for collecting and labeling sign language images.
- `sign-lang-detection.ipynb`: Notebook for training the YOLOv5 model on the collected sign language data.
- `yolov5`: Directory containing the YOLOv5 model and related scripts.

## Contributor Expectations

If you would like to contribute to the Sign Language Detection project, please follow these guidelines:

1. **Fork the repository** and create your feature branch (`git checkout -b feature/AmazingFeature`).
2. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`).
3. **Push to the branch** (`git push origin feature/AmazingFeature`).
4. **Open a pull request**.

Before contributing, ensure your code adheres to the existing style and includes tests where appropriate. Contributions that improve the application's functionality, performance, or usability are highly appreciated.

## Credits

This project was created following the excellent tutorials in the [Sign Language Detection YouTube Playlist](https://youtube.com/playlist?list=PLkz_y24mlSJYWpwFbU8fyaBSwihoVHiJz&si=ssh-POaD9XPm4Q8g). Special thanks to the content creator for providing comprehensive guidance on building this project.

Thank you for using the Sign Language Detection project!

