# COVID-19 X-Ray Detection

Here, I have implemented two different types of models that classify an X-ray image into three categories: Normal, Viral Pneumonia and COVID-19.

## Dataset
You can find the dataset [here](https://www.kaggle.com/datasets/pranavraikokte/covid19-image-dataset).

It contains around 137 cleaned images of COVID-19 and 317 in total containing Viral Pneumonia and Normal Chest X-Rays structured into the test and train directories.
We have downloaded this dataset from Kaggle and worked on it on the Google Colab Platform. It is a simple directory structure branched into test and train and further branched into the respective 3 classes which contains the images.

![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/a0575d31-fbd9-46a6-a8bc-d22f47dede82)

## Pre-processing
* Images are first resized to a standard size (200 x 200)
* Since X-ray images were used, contrast in the images was increased using histogram equalization.
* We also converted all images from RGB to grayscale, since colors are not relevant for X-rays and this makes training the model much quicker, since the number of parameters reduces.

## Model
Model 1 is a single layered model, which is a CNN model with 4 convolution layers, 4 Pooling and 4 Neural Network layers.
While Model 2 is a two layered model, where each layer is a CNN model with 4 convolution layers, 4 Pooling and 4 Neural Network layers.
THe first layer classifies the image as Normal or Abnormal, and the second layer further classifies an Abnormal image as either COVID-19 or Viral Pneumonia.

Model 1 gives a test accuracy of 91% while Model 2 gives a test accuracy of 87%

The CNN Model Summary:


![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/cf4936e5-e97e-498f-a221-b07e131b9940)

### Model 1
Single-Layered Image Classification Model

Confusion Matrix:

![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/5d308b4d-f3be-42e1-8fce-78b58d406181)

Classification Report:

![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/86da7af0-3cef-4471-b5a6-2d900117eb9f)

### Model 2
Two-Layered Image Classification Model consisting of two CNN-based sub-models

Flowchart of the Model:

![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/69ea9db1-fec3-4144-a8a2-83ce1416df6a)


Confusion Matrix:

![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/065b0ffa-4919-4fe6-8ddc-ada06e23df78)

Classification Report:

![image](https://github.com/omkmorendha/COVID-19-Image-Detection/assets/17925053/b0cceafd-e15e-4081-b328-db9de4ac04be)


