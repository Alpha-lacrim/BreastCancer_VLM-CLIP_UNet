# Olympic Of Technology: Breast Cancer Detection and Segmentation

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
* Please note that we only need the train and test folders from the extracted initial zipped file.
* Make sure that train, test, and this notebook are in the same directory.
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
    ├── test/
    │   ├── images/
    │   └── masks/
    │   
    └── notebook.ipynb (We don't need this!)
    ```


## Sample Output of the code for the test dataset:
### Image Comparison

<table>
  <tr>
    <th>Input Image</th>
    <th>Output Image</th>
    <th>Label</th>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/e8baee73-ba16-40bd-87bb-d57d94a51f12"></td>
    <td><img src="https://github.com/user-attachments/assets/96a9bad9-08ad-4c71-b912-732e88673887"></td>
    <td>Benign</td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/19aee29c-f264-4c23-89c3-0918a37d2e48"></td>
    <td><img src="https://github.com/user-attachments/assets/baaf5431-866a-485a-bb2f-e0e150ec5d94"></td>
    <td>malignant</td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/649aabb7-1b7a-4580-9fd2-09322c224df8"></td>
    <td><img src="https://github.com/user-attachments/assets/4525ff67-6181-4550-bfe3-32b8720fb05e"></td>
    <td>Normal</td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/2873ff86-c961-4fa8-bcbe-0986a40bf19e"></td>
    <td><img src="https://github.com/user-attachments/assets/a01dfee9-55a3-44ef-ab18-dc72b3631106"></td>
    <td>Benign</td>
  </tr>
  <tr>
 <td><img src="https://github.com/user-attachments/assets/e45b765f-cd70-42ed-b6cf-de449ef42af4"></td>
    <td><img src="https://github.com/user-attachments/assets/3e812cb6-fc03-4027-b325-3d8c757846a5"></td>
    <td>malignant</td>
  </tr>
</table>

