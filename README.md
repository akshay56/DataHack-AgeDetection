# Data_Hack-

 Age Detection of Indian Actors - Data Hack Competition
 Problem Solved using OpenCV image classification library and implemented in R
 
 Have extracted the image features using Histogram of Gradient (HOG) function which takes image as a raster array input and irrespective of its size, transforms the image into a 54 dimentional vector of  HOG descriptors.
 
HOG is considered to be faster & efficient image descriptor as against SIFT (Scale Invariant Feature Transform) & SURF (Speeded-Up Robust Features) & GLOH: (Gradient Location and Orientation Histogram). HOG has shown best results amongst conventional blob detection techniques. 
 
 Next is the implemention of Support Vector Machine which does the image classification using Brute Force (as against FLANN based Matcher which is a slower technique and not required in this context as data is not that much). 
 
 The images are classified within a hyperplabe as actors being as old, yound and middle aged. 
 
 Ranked 79 in the competetion for over 600 participants. 
