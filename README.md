# FAKE-NEWS-DETECTION
Problem based on Sentimental Classification

# Objective
Building a machine learning model using Natural Langugage Processing to determine the relationship between "Headline" and "Body Text".

The relationship can be classified into four categories: 
* Body 'agree' with Headline
* Body 'disagree' with Headline
* Body 'discuss' Headline
* Body is 'unrelated' to Headline

# Dataset

train_bodies.csv contains {"BodyId" , "articelBody"}  as fields

train_stances.csv contains {"Headline","BodyID", "Stance"} as fields

Both datasets have been merged using Panda.

# Text Preprocessing

The main idea of performing any kind of feature engineering is to find the similarity between Headline and Body.
* Construct a Bag of Words with max_length = 5000
* Construct TF_IDF vectors with max_length = 5000
* Construct Cosine similarity matrix for TF_IDF->Headline and TF_IDF->Body


# Model

Model is a simple Multi-Perceptron Layer with a single hidden unit.
Model is build using Keras. 

Structure of Model
  
  Layer - 1 ----- | TF_Vector of Headline + TF_cosine Similarity + TF_vector of Body |
  
  
  Layer - 2 ----- |  Hidden Layer | (Activation  = 'Relu')
  
  
  Layer - 3 ----- |  Output Layer | (Activation = "Softmax')
  
  
  Layer - 4 ----- |  Activated Output | (Neruons = 4)
  
# Results

The model yields a maximum accuracy of 83% for 2,000 training points. Accuracy may drop to 76% for 5,000 training points.

Why Accuracy Decreases?

* For large training set, the size of vocabulary increases considerably and simultaneously the frequency of zeros in TF_IDF vectors also increases. Thus, finding the cosine similarity using TF_IDF is not a good idea and gives poor test results.
 
