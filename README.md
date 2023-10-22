# Tampering-detection-and-localization-on-Copy-Move-Images-using-Deep-Learning-Approaches
Table of Contents
Introduction
Types of Image Manipulation
Methodology
Datasets
Image Pre-processing
Convolutional Neural Networks (CNN)
ResNet-50
VGG16
Results and Discussion
Conclusion and Future Work
1. Introduction<a name="introduction"></a>
The availability of powerful image editing tools has led to a rise in image manipulation in the digital age. Image tampering involves altering images for various purposes, including deception, misinformation, and hiding information. This project focuses on detecting tampering in images and precisely locating copied and pasted portions in copy-move tampered images. It is crucial for maintaining trust and credibility in fields such as journalism, law enforcement, and digital marketing.

2. Types of Image Manipulation<a name="types-of-image-manipulation">
Image manipulation can be broadly categorized into two types: active and passive techniques. Active techniques leave prior information like watermarks, while passive techniques, also known as image forensics, do not require any prior information. This project primarily deals with passive techniques, including copy-move image forgery.

3. Methodology<a name="methodology">
Datasets<a name="datasets">
CASIA V2.0 Dataset: This dataset contains various copy-move, cut-paste tampered images and slicing images. It consists of 12,614 images, including both authentic and tampered ones. To avoid bias, this project uses 2,000 authentic and 2,000 tampered images from this dataset in JPG format.

COMOFOD Dataset: This dataset contains 10,402 copy-move images from different places. It is used as the tampered dataset for this project.

MICC-F220 Dataset: This dataset is utilized for copy-move detection and localization. It contains 220 images under varying lighting conditions and image settings, all of which are copy-move images.

Image Pre-processing<a name="image-pre-processing">
Error Level Analysis (ELA): ELA is used to detect digital alterations in images. It involves encoding an image, compressing it, and decoding it to identify differences between the original and compressed versions. ELA highlights areas with significant pixel value changes, indicating potential tampering.

Image Resizing: Images are resized to lower dimensions for efficient processing. This step helps ensure uniform image dimensions and improved model efficiency.

Convolutional Neural Networks (CNN)<a name="convolutional-neural-networks-cnn">
CNN is used to detect tampering in images. It employs convolutional layers, pooling layers, and fully connected layers to extract features and classify images as tampered or authentic. The input image size is resized to 128 x 128 x 3, achieving 88% accuracy.
ResNet-50<a name="resnet50">
ResNet-50 is a deep learning model consisting of 50 layers. It is employed for tampering detection with an image size of 224 x 224 x 3, achieving 98% accuracy.
VGG16<a name="vgg16">
VGG16 is a convolutional neural network with 16 layers. However, it provides lower accuracy (49%) compared to CNN and ResNet-50, so it is not considered for further testing.
4. Results and Discussion<a name="results-and-discussion">
The proposed CNN model achieved an accuracy of 88% on the CASIAv2 dataset and 98% on the COMOFOD dataset. The loss decreased significantly with each epoch, indicating improved accuracy over time. The CNN model outperformed ResNet-50 and VGG16 in tampering detection on the CASIAv2 dataset, making it the chosen model.

5. Conclusion and Future Work<a name="conclusion-and-future-work">
In conclusion, this project focuses on passive image tampering detection, specifically copy-move forgery, using deep learning models. While the proposed model achieved good results, future work could involve extending the model's capabilities to actively manipulated images and improving the accuracy further. Additionally, techniques like EMT-NET for tampering detection on the CASIAv2 dataset could be further explored for more efficient and memory-friendly solutions.
