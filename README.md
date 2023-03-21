# APS360_ML_Pneumonia_X-ray_image_classification
# 1 INTRODUCTION
Pneumonia, as it has been discovered by human beings, has been affecting millions of people every year, and brought about four million people to death. In many developing countries, pneumonia is still the major cause of death among old and young people. The goal that the team wants to achieve is to develop a machine learning model to diagnose pneumonia is that by training a model to detect pneumonia through X-ray images could improve the efficiency and the accuracy of diagnosis compared to doctors checking it themselves. Currently, the model is forged with a convolutional neural network (CNN) to extract the features from the image imputed, after the feature extraction and flattening, the output would be connected to an artificial neural network (ANN) which contains two fully connected layers for classification.

# 2 ILLUSTRATION / FIGURE
The purpose of the model is to classify chest X-rays into two classes, which are X-rays with pneumonia and without pneumonia. The team plans to use a convolutional neural network (CNN) to extract certain features from X-ray images and connected an artificial neural network to it for classification. The figure below briefly shows the overall idea of our project. A more detailed demonstration of the model can be found in a later part.

# 3 BACKGROUND AND RELATED WORK
Pneumonia detection has been a problem for years. In a traditional convolutional neural network, the structure of the model is convolutional layers, activation functions, pooling layers, flattening and fully connected layers, and algorithms (Kaushik et al., 2020). Amongst the steps, algorithms of CNN classifiers as the core of the program attract various types of deep learning methodologies. Four approaches are used as transfer learning to detect pneumonia of COVID-19, which are AlexNet, ResNet18, DenseNet20, and SqueezeNet (Tawsifur Rahman et al., 2020). The comparison and visualization of each approach help the team have a better understanding of the architectures of each of the approaches while providing the team with some potential options for the structures of the model. Besides, GoogLeNet applies inception blocks with dimension reduction are introduced in order to control the computational complexity. The improvement of the performance can be evidenced by the result of the final accuracy (Rohit Kundu et al., 2021). In addition, the VGG19 network can be used to develop the proposed Deep CNN by improving its accuracy to as high as 0.98 (Rajasenbagam et al., 2021). This paper introduces Convolutional Generative Adversarial Network (DCGAN) to create augmented images, which is especially inspiring and useful for the team (Rajasenbagam et al., 2021). Last but not least, the detailed explanations in the research help the team explore the usages of the confusion matrix. The calculation and analysis of accuracy, precision, recall, F1 score, ROC (receiver operating characteristic) and AUC (area under the curve), etc are all useful tools to translate numeric data into helpful information for improvement (Kareem et al., 2022).

# 4 DATA PROCESSING
The data of chest X-Ray images of pneumonia is from patients aged 1 to 5 years from Guangzhou Women’s and Children’s Medical Center by accessing the public data platform, Kaggle, publishe by PAUL MOONEY in 2018(Mooney, 2018) . Although the data is already divided into testing, training, and validation including normal chest X-Ray images and pneumonia chest X-Ray images, the team reclassified the images for testing, training, and validation in a more proper proportion.

The chest X-Ray images from Kaggle published by PAUL MOONEY are in JPEG format, which basically has no effect on the project compared with JPG format. There are 5856 images in the dataset, with 1583 normal and 4273 pneumonia. Since the inputs of the neural networks should be of the same size, the team resized images into the same size to easily get these images loaded and processed. As exceeded shrinking will lead to deformation of features and patterns inside the image, the team resized the original images with dimensions of 1500 *1400 to 100*100.

After cleaning and resizing all the images to a considerably smaller size (100*100), the team decided to use 70% of each class to be in the training set, 15% to be in the validation set, and 15% to be in the testing set. Therefore, there would be 1110 normal and 2990 pneumonia in the training dataset; 237 normal and 642 pneumonia in the validation dataset; and 236 normal and 641 pneumonia in the test dataset.

To ensure randomness in the splitting process, the team randomly selected the images that appear first from the datasets. For example, the team used the first 1110 normal images from the datasets as the training dataset.

Since machine learning algorithms cannot operate on label data directly, the team converted all input variables and output variables to be numeric. The one-hot encoding would be applied to change the label ‘normal’ to 0, and ‘pneumonia’ to 1.
