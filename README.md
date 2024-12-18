# Medical Image Edge Detection Test (MIEDT) dataset


## 1. Dataset Overview
This dataset is organized based on the edge detection task, aiming to provide rich image resources and corresponding edge detection annotation information for related research and applications, which can be used for the testing of edge detection algorithms. In order to evaluate the performance of the edge detection method comprehensively, we created the Medical Image Edge Detection Test (MIEDT) dataset. The MIEDT contains 30 medical images, which were randomly selected from three publicly available datasets, Head CT-hemorrhage, Coronary Artery Diseases DataSet, and Skin Cancer MNIST: HAM10000 . 

## 2. Data Set Structure
#### Original image: This folder stores the original image data. It contains 5 Head CT images in PNG format with varying image resolutions; 10 coronary heart disease images in JPG format and with an image resolution of [1024 * 1024]; 15 skin images in JPG format and with an image resolution of [600 * 450]. It covers a variety of medical image materials with different imaging and contrast, providing diverse input data for edge detection algorithms.

#### Ground truth：The data in this folder are the edge detection annotation images corresponding to the images in the "Originals" folder. They are in PNG format. In these images, the white pixels represent the edge parts of the image, and the black pixels represent the non-edge areas. These annotation information accurately outlines the object contours and edge features in the original images and can be used as a benchmark for model training and evaluation.

## 3. Usage Instructions
For users who conduct image processing using Python, they can utilize the cv2 (OpenCV) library to read image data. The sample code is as follows:

```python
import cv2
# Read original image
original_image = cv2.imread('Original image/IMG-001.png')
# Read the corresponding Ground Truth image
ground_truth_image = cv2.imread('Ground truth/GT-001.png', cv2.IMREAD_GRAYSCALE)
```
When performing model training based on deep learning frameworks (such as TensorFlow, PyTorch), the dataset path can be configured into the corresponding dataset loading class according to the data loading mechanism of the framework to ensure that the model can correctly read and process the image and its annotation data. 

## 4. Data Sources and References
#### Data Sources: The original images are collected from public image datasets Head CT-hemorrhage, Coronary Artery Diseases DataSet, and Skin Cancer MNIST: HAM10000 to ensure the quality and diversity of the images.
If you are using this dataset in academic research, please cite the following literature.
#### References: 
[1] Noel Codella, Veronica Rotemberg, Philipp Tschandl, M. Emre Celebi, Stephen Dusza, David Gutman, Brian Helba, Aadi Kalloo, Konstantinos Liopyris, Michael Marchetti, Harald Kittler, Allan Halpern: “Skin Lesion Analysis Toward Melanoma Detection 2018: A Challenge Hosted by the International Skin Imaging Collaboration (ISIC)”, 2018; https://arxiv.org/abs/1902.03368   

[2] Tschandl, P., Rosendahl, C. & Kittler, H. The HAM10000 dataset, a large collection of multi-source dermatoscopic images of common pigmented skin lesions. Sci. Data 5, 180161 doi:10.1038/sdata.2018.161 (2018). 

[3] Classification of Brain Hemorrhage Using Deep Learning from CT Scan Images - https://link.springer.com/chapter/10.1007/978-981-19-7528-8_15

