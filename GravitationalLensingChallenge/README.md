# Strong Lensing Challenge

![Lensing illustration](https://github.com/ML4SCIHackathon/ML4SCI/blob/main/GravitationalLensingChallenge/gitimage.jpg)

> Illustration by Sandbox Studio, Chicago with Ana Kova

### Description

Gravitational lensing has been a cornerstone in many cosmology experiments, and studies since it was discussed in Einstein’s calculations back in 1936 and discovered in 1979, and one area of particular interest is the study of dark matter via substructure in strong lensing images. While statistical and supervised machine learning algorithms have been implemented for this task, the potential of unsupervised deep learning algorithms is yet to be fully explored and could prove to be crucial in the analysis of LSST data. The primary aim of this challenge is to design and implement an unsupervised deep learning model to study strong lensing images.

```diff
+ [Update Description]
```

### Datasets

#### 1. Multi-Class Classification

The [Dataset](https://drive.google.com/file/d/1B_UZtU4W65ZViTJsLeFfvK-xXCYUhw2A/view?usp=sharing) consists of three classes, strong lensing images with no substructure, spherical substructure, and vortex substructure. The images have been normalized using min-max normalization, but you are free to use any normalization or data augmentation methods to improve your results.

#### 2. Regression

```diff
+ [Dataset Description]
```

### Evaluation Metrics

#### 1. Multi-Class Classification

* ROC curve (Receiver Operating Characteristic curve) and AUC score (Area Under the ROC Curve)  

#### 2. Regression

```diff
+ [Add Evaluation Metrics]
```

The model performance will be tested on the hidden test dataset based on the above metrics.

### Deliverables

* You are required to submit a Google Colab Jupyter Notebook clearly showing your implementation along with the above-mentioned evaluation metrics for the training and validation data.
* You must also submit the final trained model, including the model architecture and the trained weights ( For example: HDF5 file, .pb file, .pt file, etc. )

You can use the example notebooks provided in this repository as a template for your work.

### Example Notebooks

#### 1. Multi-Class Classification

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/145HVDXeF2rC9q_oMbKoIZoPu4nBTwi52?usp=sharing)

#### 2. Regression

```diff
+ [Add Link to the example notebook]
```

### Contributors

* Sergei Gleyzer<sup>1</sup>
* Michael Toomey<sup>2,3</sup>
* Pranath Reddy<sup>4</sup>
* Yurii Halychanskyi<sup>5</sup>

<sup>1</sup>Department of Physics & Astronomy, University of Alabama, Tuscaloosa, AL 35401, USA

<sup>2</sup>Brown Theoretical Physics Center, Providence, RI 02912, USA

<sup>3</sup>Department of Physics, Brown University, Providence, RI 02912, USA

<sup>4</sup>Birla Institute of Technology & Science, Pilani - Hyderabad Campus, Telangana, India

```diff 
+ [Add affiliation]
```
