# COVID19 AND PNEUMONIA classification

## Project members 

* KHANNAFOUR ASMAE
* AIT JEDDI YASSINE
* EL GHALBZOURI SARA
* BENGADI SOUFIANE
* AIT ABDELMALEK YOUSSEF
## About

The goal of this project is to build deep learning model that can diagnose COVID-19 and Pneumonia cases using chest X-Ray Images.  
The data consists of two classes : **'NORMAL'** and **'COVID19 AND PNEUMONIA'**. The big challenge of this problem is that the data is unbalanced  (~1300 samples of 'NORMAL' and ~3500 samples of 'COVID19 AND PNEUMONIA')

Source : [Kaggle competition](https://www.kaggle.com/c/deep-learning-competition-cs-2020) 

## Requirements

Run **pip install -r requirements.txt** (Python 2), or **pip3 install -r requirements.txt** (Python 3)

## Usage

[Covid19_classification](https://github.com/Altimis/COVID19-AND-PNEUMONIA-CLASSIFICATION/blob/master/Covid19_classification.ipynb) notebook contains the code used to download, process and use X-ray images to train a MobileNet model initialized with imagenet dataset.  
If you are in a hurry and want to use the weights of the model I trained, feel free to load [the weights](https://github.com/Altimis/COVID19-AND-PNEUMONIA-CLASSIFICATION/blob/master/best_weights.hdf5) directly onto the model. The guide is described more precisely in the notebook. 

## Results

In this project we first tried to form a simple model with 5 ConvNets and without using data augmentation.  
As the classes are unbalanced, the accuracy wont be the right measure to use for the model performance. Recall, precision and f1 score are good alternatives for evaluating the model performance (testing the model in Kaggle by submitting the results is also a good way). In the first experiment, we obtained 73% recall and 78% precision, which is not good enough (by testing the model on the Kaggle evaluation metric, we obtained 72%).  
  
  by Using oversampling, [MobileNet](https://keras.io/api/applications/mobilenet/) and data augmentation (vertical flip, zoom ...), we could improve the precision and recall to **98%** **97%** (**f1 score = 98% and Kaggle evaluation metric = 93% , 3rd classment**).
