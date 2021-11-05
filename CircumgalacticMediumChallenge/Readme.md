## Problem description 

Galaxies are embedded in large gas haloes termed the “circumgalactic medium (CGM)”. The history of a galaxy is encapsulated in the history of its gas cycling between the visible body of the galaxy and the CGM. The CGM is a source for a galaxy’s star-forming fuel, and plays a role in regulating the galactic gas supply. Understanding the CGM and its history thus offers insight into galaxy evolution. 

One way to study galaxy CGMs is through the absorption lines they cause in the spectra of bright background objects, such as quasars. As the light passes through a slab of gas constituting the CGM, the gas absorbs part of the light, resulting in an absorption line in the resulting spectrum, as the figure below illustrates. 

(Note that the light intensity is always **non-negative**).

![image](https://user-images.githubusercontent.com/71390120/131004001-9958b083-11c0-4a62-aedf-073a7b629ad1.png)

The characteristics of the absorption lines depend on the properties and type of the gas itself. Thus, it is plausible that there are some underlying/latent gas characteristics, such as density, temperature, elemental abundances and velocity that result in spectra with similar characteristics. These properties are unobservable, which motivates the search for an underlying latent space — a low-dimensional representation of spectra, which would capture these properties.

Your task will be to find a latent space from which the original spectra can be reconstructed with minimal information loss


# Data

You will be given a dataset of simulated spectra, where a given row corresponds to a single spectrum, and each column corresponds to a wavelength. That is, entry $ x_{i,j} $ in the given data is light intensity for spectrum $ i $ at wavelength $ j $ (so the plot above is a plot of one row of the data).

We provide three datasets:
1. Training data: This should be used for model fitting.
2. Validation data: Hyperparameter tuning should be done using this dataset.
3. Test data: Use your FINAL model to calculate reconstructions for this data. DO NOT use this for model fitting. 

You can do anything with the train and validation datasets (for example, if using cross-validation you can pool them). Test data should be only used once, to generate rconstructions using your final model. 

Note that we will use a separate dataset (which you won't have access to) to assess the submitted models.


# Objective

Given a dataset of spectra, your task is to reduce its dimensionality. For example, starting with 2000 spectra with 100 000 features/wavelengths, your task is to represent these spectra with just a few features. For example, you can end up with a dataset of 2000 specta, each with 6 features (instead of the original 100 000 features).

Below we will refer to the features of the reduced spectra as "latent variables". So in the example above, the reduced spectrum has 6 latent variables.

The dimensionality reduction necessarily involves some information loss. Your aim is to find dimensionality reduction with as small loss as possible. This loss is calculated as a mean squared error of reconstructed spectra, penalised for the number of latent variables used. This penalty is linear in the number of latent variables, but there is an added (large) penalty if you use more than 6 of them (you shouldn't need to use more than 6 of them).



# What you need to submit

**See the end of this notebook for exact requirements for submissions**


The key elements you need to submit:
1. Reconstruction loss on the TEST data using your final model.
2. A function mapping of spectra into a latent space, i.e. function that calculates $ \hat{z} $ for any spectrum (or spectral dataset) $ s $.
3. Your function for calculating reconstructions $ \hat{s} $ from latent representation $ \hat{z} $.

# Summary 

Lastly, the diagram below summarizes the process. For a given spectrum $ s $, you need to find a function "*reduce_dimensionality*" that reduces the dimension of the data, and function "*calculate_reconstructions*", which calculates reconstructed spectra from the reduced dataset. Reconstruction loss is calculated as a MSE of reconstructed vs original spectra, with added penalty for large latent space sizes.

You need to submit the elements highlighted in red, that is the reconstructed spectra (using the test set), and the two functions.

Submission format:

Please email us:
 
1.   The link to your Google Colab Jupyter Notebook (or your Jupyter Notebook). The notebook should containt
  *   The final model.
  *   A function mapping the spectra into a latent space.
  *   Function calculating reconstructions from the latent representations.
  *   The final model weights/parameters should be saved in a file and the two functions should use weights loaded from this file. (This is to make sure that we evaluate the model using the same weights as you).
  *   The loss calculation for the test set.
2. The file storing the model architecture/weights. This can be in any format (as long as it loads correctly in your notebook).
3. The loss you obtained on your test set.

Feel free to choose the ML framework of your choice for this problem.

