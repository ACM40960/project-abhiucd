# Handwritten Equation Detection and Evaluation
The  project  is  aimed  at  building  an  AI  system  based on Deep learning model (DCCNN) to identify handwritten mathematical equationsfrom a sheet of paper,
digitizes the steps of solving them and the evaluate to provide feedback.

## Project Outline

![Project Outline](project-abhiucd/project_images/project modules.PNG)
  
Steps of Running the Code:
	+ mnist_data_conversion_images.ipynb loads the MNIST data from ![MNIST](http://yann.lecun.com/exdb/mnist/), converts it in image form and stores in different folders as per the classes.
	+ Data Preprocessing of kaggle's symbol image has been already done in Preprocessing_Kaggle's_Symbol_For_Training_Neural_Network.ipynb file, and DCCNN neural network model has been trained for on 15 classes of images.
Weight and parameters after model training and testing have been saved into DCNN.h5 file.
	+ Next Check the final.ipynb file. Steps to run is given below.

  **Load model** 
	Change the path where DCNN.h5 is saved in you system after downloding the files from git.
```
try:
    model = keras.models.load_model('C:/Users/Abhishek/Desktop/final_project/Autograding-handwritten-mathematical-worksheets-master/models/DCNN.h5', compile=False)

except Exception as e:
    print('Model couldnot be loaded',e)
```
There are two major steps which is done in oreder to detect and solve the equations from the worksheet.
 **Workspace detection** is used to identify correctly the suitable space from the worsheet where equations are solved by a particular person. Output received from this section:
	![Workspce Detection](https://drive.google.com/file/d/1-QNiH4N5giLBKocSwK-itNH9ZxAI8Ljw) 

  **Analysis module** will first detect the lines, predict the characters in each line and finally forms an equation with the predicted 
characters then evaluate them by marking boxes. Each detected line is evaluated.
1. Green Box represents that equation in that particular line is solved correctly.
2. Red Box represents that equation in that particular line is solved incorrectly.

For detailed description on the workflow see [Report.pdf](Report.pdf)

## Important dependencies to install before running the code.

	+ h5py (2.10.0)
	+ Keras (2.3.1)
	+ Keras-Applications (1.0.8)
	+ Keras-Preprocessing (1.1.0)
	+  matplotlib (3.1.1)
	+ numpy (1.17.3)
	+ opencv-python (4.1.1.26)
	+ pandas (0.24.0)
	+ Pillow (6.2.0)
	+ tensorboard (1.14.0)
	+ tensorflow (1.14.0)
	+ tensorflow-estimator (1.14.0)



