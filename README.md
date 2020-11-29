# COVID19 AND PNEUMONIA classification

## About

The goal of this project is to build deep learning model that can diagnose COVID-19 and Pneumonia cases using chest X-Ray Images.  
The data consists of two classes : 'NORMAL' and 'COVID19 AND PNEUMONIA'. The big challenge of this problem is that data is umbalanced (~1300 samples of 'NORMAL' and ~3500 samples of 'COVID19 AND PNEUMONIA')

Source : [Kaggle competition](https://www.kaggle.com/c/deep-learning-competition-cs-2020) 

## Usage

[Covid19_classification](https://github.com/Altimis/COVID19-AND-PNEUMONIA-CLASSIFICATION/blob/master/Covid19_classification.ipynb) notebook containes the code used to dowload, process and use x-rays images to train a MobileNet model initialized with imagenet data.  
If you are in a hurry and would like to use the model's weights that I trained, feel free to load [the weights](https://github.com/Altimis/COVID19-AND-PNEUMONIA-CLASSIFICATION/blob/master/best_weights.hdf5) directly to the model. The guide is described in a more precise way in the notebook. 

## Results

In this project, we first tried to train a simple model with 5 ConvNets and without using data augmentation.  
As the classes are imbalanced, accuracy won't be the right metric to use for model's performance. Recall, precison and f1 score are good alternative to evaluate the performance of the model (testing the model in Kaggle by submmiting the results is a good way as well). In the first experiment, we got 73% recall and 78% precison which is not good enough (by testing the model on the Kaggle evaluation metric we got 72%).  
  
  Using [MobileNet](https://keras.io/api/applications/mobilenet/) and data augmentation (vertical flip, zoom ...), we could improve the precision and recall to **98%** **97%** (**f1 score = 98% and Kaggle evaluation metric = 93%**).
