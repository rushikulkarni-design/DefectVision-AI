# 🔬 DefectVision AI
Industrial Surface Defect Classification & Explainability using Deep Learning.

DefectVision AI is an intelligent industrial surface inspection system based on the Deep Learning and Explainable AI.

The system is constructed with PyTorch, EfficientNet-B0, Grad-CAM and Gradio and it detects six different types of surface defects and illustrates the areas of the images that affect the system's output.

## 🚀 Key Features

- Industrial defect classification in 6 classes.
- Fine-tuning EfficientNet-B0 pre-trained model.
- Preprocessing and augmentation of images.
Confidence level in prediction and class probability distribution.
Explainable AI with Grad-CAM.
Interactive image analysis interface with Gradio.
- Training performance visualization.
- Confusion matrix and classification metrics.

## 🧠 Supported Defect Categories

1. Crazing
2. Inclusion
3. Patches
4. Pitted Surface
5. Rolled-in Scale
6. Scratches

## 📊 Model Performance

The results are based on the data from the official test sets.

| Metric | Score |
|---|---:|
| Test Accuracy | **95.83%** |
| Macro Precision | 96.34% |
| Macro Recall | 95.83% |
| Macro F1-score | 95.80% |
| Best Validation Accuracy | 97.57% |

- Training images: 1,440
- Internal validation images: 288
- Official testing images: 360
- Number of classes: 6

## 🏗️ Model Architecture

EfficientNet-B0 Transfer Learning ImageNet

- Pretrained feature extractor.
- Inability to become responsive to training.
Individual 6 class classification head.
- Dropout regularization.
- AdamW optimizer.
Cross-Entropy Loss with Label Smoothing.

Input image size: 224 × 224 × 3.

## 🔍 Explainable AI

For classification prediction, DefectVision AI visualizes the regions in the image that are important for the prediction by using Grad-CAM.

It generates:
- Original surface image.
- Grad-CAM activation heatmap.
- Explainability overlay.

Grad-CAM gives an approximate explanation of the model and is not a precise segmentation of the defects.

## 🛠️ Technology Stack

| Technology | Application |
|---|---|
| Python | Programming |
| PyTorch | Deep Learning |
A model-based image processing system for the TorchVision project.A model-based image processing system for the TorchVision project.
| EfficientNet-B0 | Classification |
| OpenCV | Image processing |
| Grad-CAM | Explainable AI |
| Gradio | Interactive interface |
| Scikit-learn | Evaluation |
| Matplotlib & Seaborn | Visualization |
GPU training | Google Colab

## 📂 Project Structure

```text
DefectVision-AI/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebook/
│   └── DefectVision_AI.ipynb
│
├── models/
│   └── defectvision_best.pth
│
├── results/
│   ├── confusion_matrix.png
│   ├── training_curves.png
│   ├── gradcam_example.png
│   └── metrics.json
│
├── screenshots/
   ├── dashboard.png
   ├── prediction.png
   ├── gradcam.png 
│
└── src/
    └── model_config.json
```

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/DefectVision-AI.git
cd DefectVision-AI
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the Training Booklet.

Open:

`notebook/DefectVision_AI.ipynb`

Run the notebook on Google Colab with GPU acceleration.

### 4. Run the application

An interactive Gradio interface is provided in the notebook, which can be executed directly in Google Colab.

## 📈 Results and Limitations

The model successfully tested on the final test set of NEU-DET images with 95.83% accuracy.

The largest observationally related mix-up was between Inclusion and Scratches (12 Inclusion samples were classified as Scratches).

Performance is dataset-specific. Model is not to be used in place of industrial quality-control validation.

## 🔮 Future Enhancements

- Edge detection using Canny Edge Detector.
- Defect localization and segmentation.
More extensive and varied industrial data sets.
- Optimize the Models for edge deployment.
- Production-ready inference API.
- Industrial camera integration.

## 👨‍💻 Authors

**Rushi Manikrao Kulkarni**

AI & Data Science Engineering Student

GitHub: https://github.com/rushikulkarni-design


**Revati Dhananjay Patki**
AI & Data Science Engineering Student

GitHub: https://github.com/revatipatki-creates

## 📜 License

The purpose of this project is to provide education and research. Check the original license and pretrained-weights terms of the data set prior to redistribution.

---

DefectVision AI: Industrial Surface Inspection that is Smarter with Deep Learning.