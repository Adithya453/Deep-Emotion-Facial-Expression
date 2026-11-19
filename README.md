# 😊 Deep Emotion – Facial Expression Recognition Using Attentional CNN

## 📌 Project Overview

**Deep Emotion** is a Facial Expression Recognition (FER) system developed using Python, PyTorch, and Convolutional Neural Networks (CNNs).

The project integrates a **Spatial Transformer Network (STN)** to automatically identify and focus on important facial regions before performing emotion classification. This helps the model extract relevant facial features and improve emotion recognition.

The model is trained on 48×48 grayscale facial images and classifies human expressions into seven different emotion categories.

It also supports TensorBoard visualization and class-weighted loss functions to handle class imbalance during training.

## 🎯 Project Objectives

- Detect and classify human emotions from facial images.
- Improve feature extraction using Spatial Transformer Networks (STN).
- Develop a deep learning model using PyTorch.
- Handle imbalanced datasets using weighted loss functions.
- Monitor and visualize model performance using TensorBoard.
- Improve emotion classification through CNN-based feature extraction.

## 🛠️ Technologies & Tools Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| PyTorch | Deep Learning Framework |
| Torchvision | Image Processing |
| TensorBoard | Training Visualization |
| NumPy | Numerical Operations |
| Pillow (PIL) | Image Processing |
| CUDA | GPU Acceleration |
| CNN | Feature Extraction |
| STN | Spatial Transformation |

## 📂 Project Structure

```text
Deep-Emotion-Facial-Expression-Recognition/
│
├── data_loaders.py      # Dataset loading and preprocessing
├── deep_emotion.py      # CNN and STN model architecture
├── generate_data.py     # Dataset generation and splitting
├── main.py              # Model training pipeline
├── visualize.py         # Visualization utilities
│
└── README.md            # Project documentation
```

## 🧠 Model Architecture

The model uses a Spatial Transformer Network followed by multiple convolutional layers to extract facial features and classify emotions.

### Architecture Workflow

```text
Input Image (48×48 Grayscale)
            |
            ▼
Spatial Transformer Network (STN)
            |
            ▼
Convolution Layer 1
            |
            ▼
Convolution Layer 2
            |
            ▼
Max Pooling
            |
            ▼
Convolution Layer 3
            |
            ▼
Convolution Layer 4
            |
            ▼
Batch Normalization
            |
            ▼
Max Pooling
            |
            ▼
Dropout
            |
            ▼
Fully Connected Layer
            |
            ▼
Output Layer (7 Classes)
```

## 😀 Emotion Categories

The model recognizes the following seven facial expressions:

1. Angry
2. Disgust
3. Fear
4. Happy
5. Sad
6. Surprise
7. Neutral

## ⚙️ Key Features

- Facial Emotion Recognition using Deep Learning.
- Spatial Transformer Network (STN) for spatial attention.
- CNN-based facial feature extraction.
- Seven-class emotion classification.
- TensorBoard training visualization.
- GPU acceleration using CUDA.
- Class-weighted loss for imbalanced datasets.
- Automatic dataset preparation.
- Training and validation accuracy monitoring.

## 📊 Dataset

The project uses a Kaggle Facial Expression Recognition dataset containing grayscale facial images and their corresponding emotion labels.

### Expected Dataset Files

```text
dataset/
│
├── train.csv
└── test.csv
```

During preprocessing, the dataset is organized into the following directories:

```text
dataset/
│
├── train/
├── val/
└── test/
```

The dataset generation utilities handle the preparation and splitting of the images.

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Varunvelagandula/Deep-Emotion-Facial-Expression-Recognition.git
```

### 2. Navigate to the Project Directory

```bash
cd Deep-Emotion-Facial-Expression-Recognition
```

### 3. Install Required Dependencies

```bash
pip install torch torchvision numpy pillow tensorboard
```

## ▶️ Running the Project

### Step 1: Dataset Setup

Generate the training, validation, and testing datasets.

```bash
python main.py --setup True --data dataset_path
```

Replace `dataset_path` with the actual dataset location.

### Step 2: Train the Model

Run the default training configuration:

```bash
python main.py --train True --data dataset_path
```

### Step 3: Train with Custom Hyperparameters

```bash
python main.py \
--train True \
--data dataset_path \
--hyperparams True \
--epochs 100 \
--learning_rate 0.005 \
--batch_size 128
```

### Step 4: Training with Class Weights

```bash
python main.py \
--train True \
--data dataset_path \
--cweights True
```

## 📈 TensorBoard Visualization

TensorBoard is used to monitor and visualize the model's training performance.

Start TensorBoard using:

```bash
tensorboard --logdir=runs
```

Open the following address in your browser:

```text
http://localhost:6006
```

### Metrics Monitored

- Training Loss
- Validation Loss
- Training Accuracy
- Validation Accuracy

## 💾 Model Output

After training, the model weights are automatically saved in a `.pt` file.

**File Naming Format:**

```text
deep_emotion-{epochs}-{batch_size}-{learning_rate}.pt
```

**Example:**

```text
deep_emotion-100-128-0.005.pt
```

## 🎯 Applications

- Human-Computer Interaction
- Smart Surveillance Systems
- Emotion-Aware AI Applications
- Educational Technologies
- Customer Sentiment Analysis
- Social Robotics
- Mental Health Research Applications

## 🔮 Future Enhancements

- Real-time facial emotion detection using a webcam.
- Video-based emotion recognition.
- Integration of advanced architectures such as ResNet and EfficientNet.
- Deployment as a web application.
- Mobile application integration.

## 👨‍💻 Project Summary

Deep Emotion demonstrates the application of Deep Learning, CNNs, and Spatial Transformer Networks in facial expression recognition.

The project focuses on extracting meaningful facial features, classifying seven human emotions, and monitoring model performance through TensorBoard.

It provides a foundation for developing intelligent emotion-aware applications using computer vision.

---

**Technologies:** Python | PyTorch | CNN | STN | Deep Learning | Computer Vision
