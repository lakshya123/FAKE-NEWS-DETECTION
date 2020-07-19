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

* 

# Model

* Model is a simple Multi-Perceptron Layer with a single hidden unit.
* Model is build using Keras.
* 
