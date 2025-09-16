This repository contains the code and resources used in the paper:
Title:Automated Classification of Dental Treatments in Radiographs Using Computer 
Vision: A Tool for Enhancing Dental Education

The notebook(s) provided here demonstrate how the dataset was preprocessed, the YOLOv8 model was trained.


Dataset Information

Dataset: Dental Radiography Dataset"https://www.kaggle.com/datasets/imtkaggleteam/dental-radiography"

Number of images: 1,196 (train: 1,075, validation: 121)

Format: Annotated with bounding boxes (converted to YOLO format).

Code Information

preprocessing.ipynb → Converts original CSV annotations into YOLO format.

training.ipynb → Trains the YOLOv8 model with specified hyperparameters.


Requirements

Python 3.10+

Libraries: ultralytics,torch, numpy, pandas, matplotlib

Methodology

Convert annotations into YOLO format.

Apply YOLOv8 training (The YOLOv8 model (yolov8n) was trained for 50 epochs with a batch size of 4 and input image size of 416x416 pixels. Training was performed on CPU using the Ultralytics YOLOv8 library (v8.3.94)).

Evaluate model performance with standard metrics.

