# FMCNet: Enhancing Anime Image Super-Resolution through Frequency-Aware Multi-Scale Consistency
This code is associated with the manuscript submitted to *The Visual Computer*

Requirements
Python 3.8, PyTorch >= 1.8
BasicSR 1.4.2
Platforms: Ubuntu 18.04, cuda-11
Installation
# Clone the repo
git clone https://github.com/Zheng-MJ/SMFANet.git
# Install dependent packages
cd SMFANet
conda create --name smfan python=3.8
conda activate smfan
pip install -r requirements.txt
# Install BasicSR
python setup.py develop
You can also refer to this INSTALL.md for installation

Data Preparation
Please refer to datasets/REDAME.md for data preparation.

Training
Run the following commands for training:

# train SMFANet for x4 effieicnt SR
python basicsr/train.py -opt options/train/SMFANet/SMFANet_DIV2K_100w_x4SR.yml
# train SMFANet+ for x4 effieicnt SR
python basicsr/train.py -opt options/train/SMFANet/SMFANet_plus_DIV2K_100w_x4SR.yml
Testing
Download the testing dataset.
Run the following commands:
# test SMFANet for x4 efficient SR
python basicsr/test.py -opt options/test/SMFANet_DF2K_x4SR.yml
The test results will be in './results'.
Pretrained Model & Visual Results
Google Drive | Huggingface

TensorRT Optimization
The script for exporting TensorRT model is available at to_tensorrt/READEME.md
Hugging Face Demo
The Hugging Face Demo is available here.
Plotting Script
The script for feature visualization and chart plotting is available at plt/README.md.
Experimental Results
Comparison with CNN-based lightweight SR methods 

Comparison with ViT-based lightweight SR methods 

Memory and running time comparisons on x4 SR 

Visual comparisons for x4 SR on the Urban100 dataset 

Comparison of local attribution maps (LAMs) and diffusion indices (DIs) 

The power spectral density (PSD) visualizations of feature 

