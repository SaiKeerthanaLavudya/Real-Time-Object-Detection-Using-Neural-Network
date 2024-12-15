# YOLOv5: Real-Time Object Detection

This repository contains the implementation of YOLOv5, a state-of-the-art object detection model designed for real-time detection tasks. YOLOv5 (You Only Look Once, Version 5) provides a fast, accurate, and efficient solution for detecting objects in images and videos in Live .

## Key Features

- **Real-Time Detection**: Optimized for speed and accuracy.
- 
- **Scalability**: Supports multiple model sizes (`n`, `s`, `m`, `l`, `x`) to balance performance and computation.
- 
- **Easy Deployment**: Compatible with PyTorch and supports export to ONNX, CoreML, and TensorFlow Lite.
- 
- **Custom Training**: Fine-tune models on custom datasets with ease.
- 
- **Pre-trained Models**: Leverage pre-trained weights for rapid deployment on the COCO dataset.

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/yolov5.git
cd yolov5
pip install -r requirements.txt
```

## Usage

### 1. Inference
Run inference on images or videos:

```bash
python detect.py --source <source-path> --weights yolov5s.pt --conf 0.4
```

- `--source`: Path to the image or video file. Use `0` for webcam.
- `--weights`: Path to the model weights (e.g., `yolov5s.pt`).
- `--conf`: Confidence threshold for predictions (default: 0.25).

### 2. Custom Training
Train YOLOv5 on your custom dataset:

```bash
python train.py --data <data.yaml> --cfg yolov5s.yaml --weights yolov5s.pt --epochs 50
```

- `--data`: Path to the dataset YAML file.
- `--cfg`: Model configuration file (e.g., `yolov5s.yaml`).
- `--weights`: Path to the pre-trained weights (optional).
- `--epochs`: Number of training epochs.

### 3. Export Models
Export YOLOv5 to different formats for deployment:

```bash
python export.py --weights yolov5s.pt --include onnx coreml tflite
```

## Dataset Preparation
Ensure your dataset follows the YOLO format with the structure:
```
data/
  images/
    train/
    val/
  labels/
    train/
    val/
```

Update the `data.yaml` file with:
- Paths to the `train` and `val` datasets.
- Class names in the dataset.

## Supported Applications
- Real-time object detection in images and videos.
- Use cases: Traffic monitoring, crowd analysis, industrial automation, etc.

## Contributing
We welcome contributions! If you'd like to report issues, suggest features, or submit pull requests, please follow these guidelines:

1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes and push to your branch.
4. Submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

---

Feel free to explore, customize, and contribute to the repository. Let's make object detection faster and smarter together!
