# Data_Hack- Age Detection of Indian Actors

 Age Detection of Indian Actors - Data Hack Competition
 
 I have solved the problem using 2 methods, first using SVM classification model and second one is a keras sequential model build on Tensorflow. Both the implementations are done in R and use the same image classification code. 

Image Classification:
 OpenCV image classification library implemented in R
 
 Have extracted the image features using Histogram of Gradient (HOG) function which takes image as a raster array input and irrespective   of its size, transforms the image into a 54 dimentional vector of  HOG descriptors.
 
HOG is considered to be faster & efficient image descriptor as against SIFT (Scale Invariant Feature Transform) & SURF (Speeded-Up Robust Features) & GLOH: (Gradient Location and Orientation Histogram). HOG has shown best results amongst conventional blob detection techniques. 

Output is a train and test CSV with HOG features against each image. 
 
 SVM Implementation:
 Next is the implemention of Support Vector Machine which does the image classification using Brute Force (as against FLANN based Matcher which is a slower technique and not required in this context as data is not that much). 
 
 The images are classified within a hyperplabe as actors being as old, yound and middle aged. 
 
 Model Ranked 79 in the competetion for over 600 participants. 
 
 Keras Model on Tensorflow:
 Train data extracted in the above steps haev been used for creating a Keras Sequencial Model with below hyperparameters
 
o	No of Neurons in Input Layer : 54 (no of HOG features per image)
o	No of Hidden Layer : 1
o	No of Neurons in Hidden Layers : 54 (no of HOG features per image)
o	No of Neurons in Output layer : 3 (classification as middle, old or young)
o	Epochs : 50 
o	Batch Size  : 10 
o	Learning Rate – parameter of gradient descent : default (0.2) 
o	Dropout Rate : Adjusted to be 0.4 
o	Optimizer = ‘adam’
o	Loss = 'categorical_crossentropy'
o	metrics = c('accuracy')
o	Activation = ‘softmax’

Model when tested against test data gives the below parameters. Low loss value indicates it has not overfitted (Accuracy can be improved but data is pretty less). 

$loss
[1] 0.9486693
$acc
[1] 0.7419867
