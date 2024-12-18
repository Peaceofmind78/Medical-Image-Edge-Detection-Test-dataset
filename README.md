# Medical Image Edge Detection Test (MIEDT) dataset


## 1. Dataset Overview
This dataset is organized based on the edge detection task, aiming to provide rich image resources and corresponding edge detection annotation information for related research and applications, which can be used for the testing of edge detection algorithms. In order to evaluate the performance of the edge detection method comprehensively, we created the Medical Image Edge Detection Test (MIEDT) dataset. The MIEDT contains 30 medical images, which were randomly selected from three publicly available datasets, Head CT-hemorrhage, Coronary Artery Diseases DataSet, and Skin Cancer MNIST: HAM10000 . 

## 2. Data Set Structure
### Originals: This folder stores the original image data. It contains 5 Head CT images in PNG format with varying image resolutions; 10 coronary heart disease images in JPG format and with an image resolution of [1024 * 1024]; 15 skin images in JPG format and with an image resolution of [600 * 450]. It covers a variety of medical image materials with different imaging and contrast, providing diverse input data for edge detection algorithms.
### Ground Truth：The data in this folder are the edge detection annotation images corresponding to the images in the "Originals" folder. They are in PNG format. In these images, the white pixels represent the edge parts of the image, and the black pixels represent the non-edge areas. These annotation information accurately outlines the object contours and edge features in the original images and can be used as a benchmark for model training and evaluation.

## Usage Instructions
For users who conduct image processing using Python, they can utilize the cv2 (OpenCV) library to read image data. The sample code is as follows:
'''python
import cv2
#读取原始图像
original_image = cv2.imread('Originals/image1.jpg')
'''


# 读取对应的边缘检测标注图像
ground_truth_image = cv2.imread('Ground Truth/image1.png', cv2.IMREAD_GRAYSCALE)'''
在基于深度学习框架（如 TensorFlow、PyTorch）进行模型训练时，可根据框架的数据加载机制，将数据集路径配置到相应的数据集加载类中，确保模型能够正确读取和处理图像及其标注数据。
四、数据来源与标注
数据来源：原始图像收集自 [具体来源，如公开的图像数据集、网络爬虫抓取的无版权图像网站等]，并经过筛选和预处理，以保证图像的质量和多样性。
标注过程：标注工作由 [专业标注团队 / 个人] 使用 [标注软件名称]，按照严格的边缘定义标准，对每张原始图像进行手工标注，确保标注的准确性和一致性，经过多次审核和校对，以保证数据的可靠性。
五、许可证与引用
本数据集采用 [许可证类型，如 CC BY-NC 4.0] 许可证发布，您可以在遵循许可证条款的前提下自由使用和共享本数据集。如果您在学术研究中使用本数据集，请引用以下文献：
[数据集相关文献或作者信息]
六、联系方式
如果您在使用数据集过程中遇到任何问题，或者对数据集有任何疑问、建议，欢迎通过以下方式与我联系：
邮箱：[邮箱地址]
GitHub：[GitHub 账号链接]
