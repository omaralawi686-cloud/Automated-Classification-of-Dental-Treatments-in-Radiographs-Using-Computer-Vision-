Overview
This repository contains the complete code and resources associated with the paper:
Title: Automated Classification of Dental Treatments in Radiographs Using Computer Vision: A Tool for Enhancing Dental Education
This project implements an object detection model (YOLOv8) to automatically identify and classify various dental treatments (e.g., fillings, implant) within panoramic dental radiographs. The goal is to provide a reliable tool for educational and research purposes.

The notebook(s) provided here demonstrate how the dataset was preprocessed, the YOLOv8 model was trained.


Dataset Information

Source
The project utilizes the Dental Radiography Dataset, sourced from Kaggle:

Link: https://www.kaggle.com/datasets/imtkaggleteam/dental-radiography

Structure and Preprocessing
Number of Images: 1,196 total images (1,075 for training, 121 for validation).

Format: The original images were annotated with bounding boxes. These annotations were converted from the initial CSV format into the YOLO format required for training.

Preprocessing Script: The preprocessing.ipynb notebook handles the necessary conversion and splitting of the data.


Usage Instructions: Data
To successfully run the code, please follow these data setup steps:

Download: Download the complete "Dental Radiography Dataset" from the Kaggle link provided above.

Organize: Create a directory named data/ in the root of this repository.

Place Files: Place the downloaded images and original annotation files within the data/raw subdirectory.

Process: Execute the preprocessing.ipynb notebook to generate the YOLO-formatted annotation files, which will be saved in a new data/processed folder.

Code and Setup
Requirements
This project requires Python 3.10 or higher. All required libraries and their tested versions are listed below.

For easy setup, use the included requirements.txt file:

Bash

pip install -r requirements.txt
Library	Specific Version (or higher)	Purpose
ultralytics	8.3.94	                Core YOLOv8 implementation
torch	         2.0.1	                 Deep learning backend
numpy		                         Numerical operations
pandas		                        Data manipulation (CSV handling)
matplotlib		                Visualization and plotting

Code Structure
The core functionality is contained within the following files:

preprocessing.ipynb: Jupyter notebook for data preparation, including converting the original CSV annotations to the YOLO-compatible format.

training.ipynb: Jupyter notebook that handles model initialization, training, and configuration based on the final, preprocessed dataset.

README.md: This document.

requirements.txt: List of Python dependencies.

Methodology & Implementation
The implementation follows a standard object detection pipeline using the YOLOv8 framework.

Training Configuration
The final model used in the published results was trained using the following specific hyperparameters, as detailed in the manuscript:

Model: YOLOv8n (YOLOv8 nano, the smallest and fastest variant).

Epochs: 50

Batch Size: 4

Input Image Size: 416×416 pixels.

Library: Ultralytics YOLOv8 library (v8.3.94).

Hardware: Training was performed on a CPU environment.

Usage Instructions: Running the Code
After setting up the data (see Dataset Information above), follow these steps to reproduce the training process:

Execute Preprocessing: Run all cells in the preprocessing.ipynb notebook. This prepares the data for model training.

Execute Training: Open and run all cells in the training.ipynb notebook. This will:

Load the YOLOv8n model.

Configure the training parameters (epochs, batch size, etc.).

Start the training process and save the resulting model weights to the designated output folder.

Evaluation: The training.ipynb notebook includes a section for evaluating the model performance using standard metrics (Precision, Recall, mAP) on the validation set.

Citation (Submitted Manuscript)

As the paper is currently under review, please use the following information to reference the work if you utilize this code or dataset in your research:
Title: Automated Classification of Dental Treatments in Radiographs Using Computer Vision: A Tool for Enhancing Dental Education
Authors: Behnaz Shirgir,Gulsum Asiksoy,Fadi Alturjman
Status: Submitted Manuscript (Under Review at PeerJ Computer Science / Manuscript ID: 124701)

Note: We kindly request that you cite the final published version once it becomes available.

License

The code and associated materials in this repository are released under the [MIT/Apache 2.0] license. This grants permission for academic, non-commercial, and research use.
