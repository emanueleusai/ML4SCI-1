# Cosmic Ray Challenge


## Motivation
- Galactic cosmic rays are energetic particles in deep space that originate from supernova explosions.
- Studies of cosmic rays have revealed the nature of astrophysical processes, and led to the discovery of subatomic particles such as muons and pions. 
- Currently, space-based cosmic ray experiments, including the AMS experiment on the International Space Station, are searching for evidence of dark matter and antimatter.
- So, developing a model for automatic detection of cosmic ray artifacts will help planetary scientists and researchers in effective filtering of data. Besides, identifying cosmic-ray events in images, and classifying their nature and frequency opens a new path for studying cosmic-ray events throughout the solar system.

## Problem Statement
- CCD-based cameras are used extensively in exploration satellites and space telescopes for imaging the surfaces of celestial bodies, and deep-space objects such as stars, extrasolar systems, and galaxies. 
- These sensors are often subjected to constant irradiation by galactic cosmic rays. The interaction of these ionizing radiations with optical sensors leads to confusion and loss of imaging pixels (an ‘artifact’).
- Your goal is to develop a model which automatically locates cosmic ray artifacts by creating bounding boxes around them.
- You are free to make use of machine learning/deep-learning algorithms of your choice. However, we have some suggestions for you at the end!
<br>
Before starting with the problem, let us look at how exactly these artifacts look like! <br>
Here is an example of a cosmic ray artifact in one of the images from MESSENGER mission of NASA:
<p align="center">
<img src="https://github.com/ML4SCI/ML4SCIHackathon/blob/main/CosmicRayImagesChallenge/sample_cosmic_ray.JPG" width="256" height="256">
</p>

Just as a fun exercise to help you appreciate the problem, try locating the cosmic ray artifact in the image below:
<p align="center">
<img src="https://github.com/ML4SCI/ML4SCIHackathon/blob/main/CosmicRayImagesChallenge/EW0220137668G.IMG.jpg" width="256" height="256">
</p>

## Dataset
The dataset for the problem can be accessed in the following link: <br>
https://drive.google.com/drive/folders/1p6m9Do5d2qr51TWxW1xpVNQnd8Lq7uic?usp=sharing 
<br>
Divide it into train and valid splits based on your preference and finally form your folder structure as below: <br>

```
    Provide path to dataset
    Format: PascalVOC

                root
         /     /            \      \ 
    train train_annots  valid  valid_annots

```
**Observe, The size of the dataset is what makes the problem interesting!** 
<br>
You don't have a lot of data, thus your goal is to maximize learning on this scarce data.<br>
Wonder how you can leverage your Deep learning skills to obtain decent results for the problem!
<br>

**Some pointers to help you:**
<br>
1. Browse about existing techniques like few shot learning, and how they are used when the size of datasets is small.
2. Try to learn about object detectors based on backbones like ResNet, which may be efficient in locating small objects.

Feel free to come up with other interesting ideas!

## Notebook
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ML4SCI/ML4SCIHackathon/blob/main/CosmicRayImagesChallenge/CR_Challenge.ipynb)

## Submission Instructions
You need to submit the predictions of your model on the test data as follows:

- For each image in the test folder, you need to write your predictions into a corresponding ".txt" file with the same image name, following the format below:<br>
   ```Positive  <confidence> <left> <top> <right> <bottom>```
    - Class name - Positive (will be constant across all predictions)
    - Confidence score for that prediction (between 0 and 1)
    - left x co-ordinate of the box predicted (between 0 and 1024)
    - top y co-ordinate of the box predicted (between 0 and 1024)
    - right x co-ordinate of the box predicted (between 0 and 1024)
    - bottom y co-ordinate of the box predicted (between 0 and 1024)
    
- An image may contain more than 1 artifact, in which case each prediction instance is to be written on a separate line of the '.txt' file.
- Put all these '.txt' files into a single folder with the name ```predictions/``` 
- Your submission should include the ```notebook``` along with the ```predictions/``` folder. Zip them into ```<Your Team Number>.zip``` before submission.

## Contributors
- Sergei Gleyzer (University of Alabama)
- Patrick Peplowski (John Hopkins University) 
- Nidhi Hegde (Indian Institute of Technology Kanpur)

