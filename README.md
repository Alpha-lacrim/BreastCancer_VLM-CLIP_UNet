# Breast Cancer Detection and Segmentation: High-Performance Framework

**Best Performance and Accuracy on Question 1 (Image Processing) of the Olympic of Technology Contest**

## Overview

This project presents an advanced framework for the **detection and precise segmentation of cancerous regions** in medical imagery, specifically designed for breast cancer analysis. This entire framework was the subject of the **first question** of the Olympic of Technology contest, where my solution achieved the **highest accuracy** among all participants.

My approach integrates the power of a **Vision-Language Model (CLIP)** for robust preliminary **detection** with a refined **U-Net architecture** for accurate pixel-level **segmentation**.



## Key Features and Technologies

| Feature | Description | Primary Technology |
| :--- | :--- | :--- |
| **Contest-Leading Accuracy** | Demonstrated superior results on the image processing task against competing models in the contest. | Metrics: IoU, Dice Score, F1-Score |
| **Robust Detection** | Initial classification of the image (cancer present/absent) using a foundation model to leverage zero-shot capabilities. | **Vision-Language Model (CLIP)** |
| **Precise Segmentation** | Accurate delineation of tumor boundaries for surgical planning and precise diagnosis. | **U-Net Architecture** |
| **High Performance** | Optimized model architecture and training regimen for speed and accuracy. | PyTorch/TensorFlow, Custom Augmentations |


## Getting Started

Follow these steps to set up the environment and run the models on your local machine.

### Prerequisites

* Python 3.8+
* Git

### Installation
First of all before you start using CLIP, you'll need to set it up properly. to do that please follow these steps:
1. **Clone the CLIP repository:**
    ```bash
    git clone https://github.com/openai/CLIP.git
    cd CLIP
    ```
    
2. **Install CLIP's required packages**
     ```bash
    pip install -r requirements.txt
    ```
     
Now for confirming the installation run the following cmd:
    ```bash 
    python -c "import clip; print('CLIP is installed!')"
    ```


If everything went correctly open a new terminal and run the following commands as well to clone my repo:
     
1.  **Clone my repository:**
    ```bash
    git clone https://github.com/Alpha-lacrim/BreastCancer_VLM-CLIP_UNet
    cd BreastCancer_VLM-CLIP_UNet
    ```

2.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Dataset

* **Source:** [Download or import the Dataset from Google Drive](https://drive.google.com/drive/folders/1H4DaaJjEEDJLMJAp-eZmrnKTxs5B4In9).
* **Structure:**:
    ```
  └── initial/
    ├── train/
    │   ├── benign/
    │   │   ├── images/
    │   │   └── masks/
    │   │
    │   ├── malignant/
    │   │   ├── images/
    │   │   └── masks/
    │   │
    │   │   ├── normal/
    │   │   ├── images/
    │   │   └── masks/
    │   │
    │   └── train.csv
    │
    └── test/
        ├── images/
        └── test.csv
    ```

