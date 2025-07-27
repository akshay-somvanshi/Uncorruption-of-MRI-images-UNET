# Uncorruption of MRI Brain images using UNET

## Description <a name="description"></a>

Our goal is to solve an imputation problem: we will create a neural network architecture that learns how to recover missing portions of an image.

This is an important problem in magnetic resonance imaging (MRI), where patient scans are often limited to a few areas to avoid lengthy scanning times.

In particular, we are going to focus on images of human heads. We have managed to gain access to one hundred images of patient's heads but, unfortunately, these images have 
a significant portion of missing information. The goal of the project is to design a neural network that can recover these missing portions.

We do not have access to the labels for the images we want to recover, so we will have to be a bit creative to obtain a workable dataset on which to train our neural network.

Fortunately for us, we have access to a generative model that has been trained to produce realistic-looking MRI images of patient's heads. Using this model, you will create an 
appropriate dataset to train your architecture.

The corrupted images that we want to recover are contained in the numpy file `test_set.npy` of this repository. The file contains 100 patient images with a size of 64x64 pixels.

### Part 1

Using the provided image-generation network, we create a dataset of brain images that will later be used to train your chosen architecture. 

### Part 2

Using the data generated in **Part 1**, we will create a PyTorch `TensorDataset` and a `DataLoader` for the training set. 

### Part 3

Using the dataset created in **Part 2**, we will design and train an architecture to recover the missing image lines of the provided test dataset.

Additionally, save the test data with the missing values filled in into a numpy file called `test_set_nogaps.npy`. These images will be **in the same order** as those in the `test_set.npy` file and should have the same pixel size of 64x64. 