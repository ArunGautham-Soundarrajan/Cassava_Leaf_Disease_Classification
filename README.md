# About the Project
As the second-largest provider of carbohydrates in Africa, cassava is a key food security crop grown by smallholder farmers because it can withstand harsh conditions. At least 80% of household farms in Sub-Saharan Africa grow this starchy root, but viral diseases are major sources of poor yields. With the help of data science, it may be possible to identify common diseases so they can be treated.  Existing methods of disease detection require farmers to solicit the help of government-funded agricultural experts to visually inspect and diagnose the plants. This suffers from being labor-intensive, low-supply and costly. As an added challenge, effective solutions for farmers must perform well under significant constraints, since African farmers may only have access to mobile-quality cameras with low-bandwidth.

# Code and Resources Used
* Python Version: 3.7.
* Packages: pandas, numpy, tensorflow, keras, matplotlib, seaborn, EfficientNetB3.
* Kernal: Kaggle Kernal.
* Data and competition: https://www.kaggle.com/c/cassava-leaf-disease-classification

# Exploratory Data Analysis
This is a classification problem with images. So I did a count plot to check the spreas of the data.


Then here are some pics of the different types of leaves

# Data Preprocessing
As we had lot of images and each image size is so big, it will take lot of computation power, so we had to preprocess it.

* Reshape the image into (224,224,3)
* Generate more samples using ImageDataGenerator to feed the model
* Inside the ImageDataGenerator,
  * Rescaled the image
  * Set a rotation range of 20 to randomnly rotate the image
  * Randomnly shift the width of the image by 10 percent
  * Randomnly shift the height of the image by 10 percent
  * Randomnly zoom the image by 30 percent
  * Randomnly flip images horizontally
  * Filled the missing pixels with nearest pixel caused by tweaking
 
# Model Building

I split the data into train and test split and used ImageDataGenerator to produce data. The output from these generators are directly fed into the model.

* Firstly, I experienced with a simple CNN to check the performance, which didnt work well.
* Hence used *Transfer Learning* to boost the accuracy.
* Implemented state of the art *EfficientNet* model.

# Model performance

The model achieved a test accuracy of *84.2* percent and train accuracy of *90* percent, which can further be improved by tweaking the model

