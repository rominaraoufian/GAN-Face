# GAN
## Basic GAN for generating faces

## Data
Data that is used in this project has 202,599 number of face images of celebrities. These images have width equal to 178, height of 208 and channels equal to three. You can access this data from [here](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset)

## Preprocessing
In this project just 10000 number of images used and all of them were converted to Square shape of 128 * 128. after that images were normalised to have value between 0 and 1 for all pixels.

## Generator model
For implementing generator model different layers such as Conv2DTranspose, Dense, Reshape, LeakyReLU, Conv2D are used. Random vector size is 32 which go through flow of variouse convolutional layers and activations to create fake images.

## discriminator model
For implementingdiscriminator model different layers such as  Dense, Reshape, LeakyReLU, Conv2D, Flatten, Dropout, sigmoid activation in last layer and optimizer RMSprop are used. 
Classify an image to real or fake by passing it through out this network.
## GAN model
first use Generator model to implement fake images, then they are sent to discriminator to classify the images while doing, this DiscriminatorModel is untraible. the optimizer in this model is  RMSprop, learning rate is equal to .0001,and binary crossentropy is used for loss.

## Training
First of all,it  generates fake images according to the size of the batch, and take equal size of real images from dataset and train discriminator to classify these images. after that, get a random vector with size of the batch size and train GAN model for 20000 epochs.

## Collaborator
I pair programmed this project with [Niloufar](https://github.com/niloufar79)