# Particle Images: Electron vs Photon Classification 
## Example Notebook:      [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ML4SCIHackathon/ML4SCI/blob/main/ParticleImagesChallenge/ParticleImages.ipynb)
![GitHub Logo](images/CollisionImage.png)

## Introduction
Machine Learning algorithms have become an increasingly important tool for data analysis at the Large Hadron Collider (LHC) from particle identification to the discovery of the Higgs boson.   
The analysis of data collected at the LHC often involves the classification of hadronic jets and particles in collision events.    
The first step to the construction of the detector images is generation of images for the electromagnetic calorimeter (ECAL). For this subdetector, each pixel in the image corresponds to a crystal of ECAL. We have provided you the image dataset which can be accessed as shown in the sample Google Colab Jupyter Notebook provided. 
## Dataset  
The intensity of each pixel is proportional to the energy measured in the corresponding crystal. Other data attribute: timing of the energy deposit are also available, though this may not help the model to improve the classification performance much. 
The dataset contains 32x32 Images of the hit energy and its timing (channel 1: hit energy and channel 2: its timing) in each calorimeter cell (one cell = one pixel) for the two classes of particles: Electron and Photon. 
The dataset contains around four hundred thousand images for electron and photon i.e. around two hundred thousand images each. Please note that besides the model performance on the provided dataset, your model will also be evaluated on an unseen test dataset.
## Algorithm 
Please use a Machine Learning model of your choice to achieve the highest possible classification performance on the provided dataset. Please provide a Jupyter Notebook that shows your solution.
## Evaluation Metrics  
* ROC curve (Receiver Operating Characteristic curve) and AUC score (Area Under the ROC Curve)   
* Training and Validation Accuracy   

The model performance will be tested on a hidden test dataset based on the above metrics.
## Deliverables  
* Google Colab Jupyter Notebook showing your solution along with the final model accuracy (Training and Validation), ROC curve and AUC score. More details regarding the format of the notebook can be found in the sample Google Colab notebook provided for this challenge.  
* The final trained model including the model architecture and the trained weights ( For example: HDF5 file, .pb file, .pt file, etc. ). You are free to choose Machine Learning Framework of your choice.

## Contributors: 
* Sergei Gleyzer (Department of Physics & Astronomy, University of Alabama)    
* Emanuele Usai (Physics Department, Brown University)  
* Michael Andrews (Physics Department, Carnegie Mellon University)  
* Shravan Chaudhari (Birla Institute of Technology & Science - Pilani, Goa Campus, India)   
