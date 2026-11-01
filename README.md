# YOLOv8 Model Comparison, Hyperparameter Tuning, and Explainable AI

## Overview

This repository contains the implementation of a research study investigating YOLOv8-based object detection through comparative model evaluation, hyperparameter tuning, and Explainable Artificial Intelligence (XAI).

The study evaluates different YOLOv8 model variants to examine the trade-offs between detection performance and computational efficiency. Hyperparameter tuning is performed to investigate the impact of training configurations on model performance. Additionally, Grad-CAM, Grad-CAM++, and EigenCAM are employed to generate visual explanations and analyze the features contributing to model predictions.

The project aims to support a systematic evaluation of object detection architectures while incorporating interpretability into the model analysis process.

## Research Objectives

- Compare the performance of YOLOv8 model variants: YOLOv8n, YOLOv8s, YOLOv8m, and the additional configuration evaluated in the study.
- Investigate the effect of hyperparameter selection on object detection performance.
- Identify effective training configurations through systematic experimentation.
- Evaluate model performance using standard object detection metrics.
- Apply explainability techniques to visualize and interpret model behavior.
- Analyze the trade-offs between detection accuracy, computational requirements, and interpretability.

## Models Evaluated

| Model | Description |
|---|---|
| YOLOv8n | Nano architecture designed for computational efficiency |
| YOLOv8s | Small architecture balancing efficiency and performance |
| YOLOv8m | Medium architecture with increased model capacity |
| Additional YOLOv8 variant | Configuration specified in the experimental setup |

The models are evaluated under the experimental conditions defined in the research methodology.

## Hyperparameter Tuning

Hyperparameter tuning is conducted to investigate the influence of training configurations on model performance.

The parameters considered include:

- **Input Image Size:** Resolution of images supplied to the model.
- **Batch Size:** Number of training samples processed in each batch.
- **Learning Rate:** Controls the magnitude of parameter updates during optimization.
- **Training Epochs:** Number of complete passes through the training dataset.
- **Optimizer:** Optimization algorithm used during training.

The experiments examine how different configurations influence detection performance and training efficiency. The selected configuration is determined using the evaluation criteria established for the study.

## Explainable Artificial Intelligence

Explainability techniques are incorporated to provide visual insights into model behavior and the image regions contributing to model predictions.

### Grad-CAM

Gradient-weighted Class Activation Mapping uses gradients associated with a target prediction to generate heatmaps highlighting image regions relevant to the model's output.

### Grad-CAM++

Grad-CAM++ extends gradient-based activation mapping through an improved weighting mechanism, potentially enabling more detailed localization of important regions.

### EigenCAM

EigenCAM uses principal component analysis of feature activations to generate class-agnostic visual explanations without requiring gradients.

### Explainability Analysis

The generated visualizations support qualitative investigation of model behavior, including:

- Identification of image regions associated with detections.
- Comparison of visual explanations across model configurations.
- Examination of feature localization and prediction behavior.
- Qualitative assessment of model interpretability.

These visual explanations complement quantitative evaluation and do not independently establish model correctness or causal reasoning.

## Evaluation Metrics

Model performance can be assessed using the following metrics, where applicable to the experimental methodology.

| Metric | Description |
|---|---|
| Precision | Proportion of predicted positive detections that are correct |
| Recall | Proportion of ground-truth objects successfully detected |
| mAP@0.5 | Mean Average Precision at an IoU threshold of 0.5 |
| mAP@0.5:0.95 | Mean Average Precision averaged across IoU thresholds from 0.5 to 0.95 |
| Inference Time | Time required to generate predictions |
| Model Size | Storage requirements of the trained model |

Quantitative results should be reported alongside the corresponding model configurations and experimental settings.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Deep Learning Framework | PyTorch |
| Object Detection | Ultralytics YOLOv8 |
| Computer Vision | OpenCV |
| Numerical Computing | NumPy |
| Data Analysis | Pandas |
| Visualization | Matplotlib |
| Explainability | Grad-CAM, Grad-CAM++, EigenCAM |
| Development Environment | Google Colab, Jupyter Notebook |

## Repository Structure

```text
autonomous_vehicle_tool_v8/
├── README.md
├── Autonomous_detection_yolov8_hypertune_xai.ipynb
├── models/
├── results/
└── figures/
```

The directory structure is illustrative. The `models/`, `results/`, and `figures/` directories should be included only if the corresponding files are present in the repository.

## Installation and Execution

### 1. Clone the Repository

```bash
git clone https://github.com/Swaathi-iyer/autonomous_vehicle_tool_v8.git
cd autonomous_vehicle_tool_v8
```

### 2. Install Dependencies

```bash
pip install ultralytics torch torchvision opencv-python numpy pandas matplotlib
```

Additional dependencies may be required by the specific implementations of the explainability methods.

### 3. Open the Notebook

Open `Autonomous_detection_yolov8_hypertune_xai.ipynb` in Google Colab or Jupyter Notebook.

### 4. Configure the Dataset

Configure the dataset paths and annotation files according to the dataset structure used in the experiments. Ensure that the annotations follow the format required by the YOLOv8 training pipeline.

### 5. Run the Experiments

Execute the notebook cells to reproduce the implemented model evaluation, hyperparameter tuning, and explainability analyses.

Reproduction may require access to the original dataset, trained model checkpoints, and suitable computational resources. Exact reproduction also depends on the software versions and experimental configurations used in the study.

## Research Contributions

The study integrates three principal components:

1. **Comparative Model Evaluation:** Investigation of performance differences across YOLOv8 model variants.
2. **Hyperparameter Tuning:** Analysis of training configurations and their influence on object detection performance.
3. **Explainability Analysis:** Application of Grad-CAM, Grad-CAM++, and EigenCAM to visualize model activations and investigate prediction behavior.

This integrated approach enables quantitative and qualitative assessment of object detection models within a unified experimental framework.

## Research Publication

**Paper Title:** [Insert final paper title]

**Conference:** [Insert conference name]

Publication details and citation information will be added when available.

## Author

**Swaathi Iyer**  
B.Tech, Computer Science and Engineering (Internet of Things)  
Vellore Institute of Technology, Vellore, India
