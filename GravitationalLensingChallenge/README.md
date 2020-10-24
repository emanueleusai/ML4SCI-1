# Strong Lensing Challenge

![Lensing illustration](https://github.com/ML4SCIHackathon/ML4SCI/blob/main/GravitationalLensingChallenge/gitimage.jpg)

> Illustration by Sandbox Studio, Chicago with Ana Kova

### Description

Gravitational lensing has been a cornerstone in many cosmology experiments, and studies since it was discussed in Einstein’s calculations back in 1936 and discovered in 1979, and one area of particular interest is the study of dark matter via substructure in strong lensing images. While statistical and supervised machine learning algorithms have been implemented for this task, the potential of unsupervised deep learning algorithms is yet to be fully explored and could prove to be crucial in the analysis of LSST data. The primary aim of this challenge is to design and implement an unsupervised deep learning model to study strong lensing images.

The [Dataset](https://github.com/ML4SCI-SLC/SLC_Data) consists of two classes, strong lensing images with no substructure and strong lensing images with substructure. Considering the samples with substructure to be outliers, you are required to train an unsupervised model on a set of strong lensing images with no substructure to solve the task of anomaly detection.

### Evaluation Metrics

* Distribution of Reconstruction Loss
* ROC curve (Receiver Operating Characteristic curve) and AUC score (Area Under the ROC Curve)   

The model performance will be tested on the hidden test dataset based on the above metrics.

### Deliverables 

* You are required to submit a Google Colab Jupyter Notebook clearly showing your implementation along with the above-mentioned evaluation metrics (Distribution of Reconstruction Loss, ROC curve, and AUC score) for the training and validation data.
* You must also submit the final trained model, including the model architecture and the trained weights ( For example: HDF5 file, .pb file, .pt file, etc. )

You can use the example notebook provided in this repository as a template for your work. 

### Example Notebook 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ML4SCIHackathon/ML4SCI/blob/main/GravitationalLensingChallenge/StrongLensingChallenge.ipynb)

> **_NOTE:_**  This notebook also contains a section for a supervised approach for binary classification, this is only for the sake of intuition, and you are required to work only on the unsupervised model.

### Contributors

* Sergei Gleyzer<sup>1</sup>
* Michael Toomey<sup>2,3</sup>
* Pranath Reddy<sup>4</sup>

<sup>1</sup>Department of Physics & Astronomy, University of Alabama, Tuscaloosa, AL 35401, USA

<sup>2</sup>Brown Theoretical Physics Center, Providence, RI 02912, USA

<sup>3</sup>Department of Physics, Brown University, Providence, RI 02912, USA

<sup>4</sup>Birla Institute of Technology & Science, Pilani - Hyderabad Campus, Telangana, India
