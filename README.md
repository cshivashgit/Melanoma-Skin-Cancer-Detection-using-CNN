# Project Name - Melanoma-Skin-Cancer-Detection-using-CNN
## Brief Description :
* Skin Cancer detection from images using Multiclass Image Classification with Custom CNNs in TensorFlow
* Python Notebook present in this repo has been executed with GPU acceleration.

## Table of Contents
* [General Info](#general-information)
* [DataSet](#dataset)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- The project is aimed at developing a CNN-based model for detecting melanoma in skin images. The dataset used in the project consists of 2357 images of malignant and benign oncological diseases, collected from the International Skin Imaging Collaboration (ISIC).
- Melanoma is a type of skin cancer that can be deadly if not detected early. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce manual effort in diagnosis.
- The aim is to develop a model that can accurately detect melanoma in skin images and reduce manual efforts in diagnosis.
- The business problem that the project is trying to solve is the manual effort required in the diagnosis of melanoma, a type of skin cancer. The manual process of evaluating images to detect melanoma can be time-consuming and prone to human error. The aim of the project is to develop a CNN-based model that can accurately detect melanoma in skin images and reduce the manual effort required in the diagnosis process. The deployment of the model in a dermatologist's workflow has the potential to increase efficiency and accuracy, potentially leading to better patient outcomes.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## DataSet
The model is trained on the ISIC Archive dataset, which contains a large number of dermoscopic images of skin lesions, including both benign and malignant melanomas. The dataset is pre-processed and split into training and validation sets.
```
    * Actinic keratosis
    * Basal cell carcinoma
    * Dermatofibroma
    * Melanoma
    * Nevus
    * Pigmented benign keratosis
    * Seborrheic keratosis
    * Squamous cell carcinoma
    * Vascular lesion
```

## Conclusions

- In the beginning, we experimented without utilizing the ImageDataGenerator, which led to a high degree of overfitting in the data.
- Subsequently, we implemented ImageDataGenerator and dropout, which helped to reduce overfitting.
- Finally, we incorporated Augmentation technique, which proved to be extremely effective in moving forward.
- The rebalancing of the class played a significant role in mitigating overfitting of the data, resulting in a decrease in loss.

#### Summary of Accuracies and Losses:

| Method | Training Accuracy | Training Loss | Validation Accuracy | Validation Loss |
| ------- | ---------------- | --------------| ------------------- | --------------- |
| CNN Model | 0.8996 | 0.2246 |  0.5190 | 2.7372 |
| CNN + Data Augmentation Stratergy | 0.6248 | 1.0350 | 0.5548 | 1.4889 |
| CNN + Data Augmentation Stratergy + Dropout | 0.6246 | 1.0608 |0.5638 | 1.3634 |
| Rectifying class Imbalance(Augmentor) + CNN + Dropout | 0.7756 | 0.6020 | 0.7378 | 0.7286 |

 
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- TensorFlow - version 2.17.1
- Keras - version 3.5.0
- Pandas - version 2.2.2
- Matplotlib - version 3.8.0
- Augmentor - version 0.2.12
- Glob - version 0.7
- PIL  version 11.0.0
  
<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## References
- ISIC Archive dataset: https://isic-archive.com/
- TensorFlow: https://www.tensorflow.org/
- CUDA: https://developer.nvidia.com/cuda-zone

## Acknowledgements
- Inspired by IIITB CNN assignment
- Credit to IIITB and Upgrad
- This project is done towards fultilment of partial requirements for MS in AI and ML
  
