#Pixel Coordinate Regression with CNN

# PROBLEM STATEMENT:Using Deep Learning techniques, predict the coordinates (x,y) of a pixel which has a value of
255 for 1 pixel in a given 50x50 pixel grayscale image and all other pixels are 0. The pixel with a
value of 255 is randomly assigned. You may generate a dataset as required for solving the
problem. Please explain your rationale behind dataset choices

#<h2>solution:<h2>
Problem Formulation

#pixel_cordinnates.ipynb(jupitor notebook explaination)

1.Input: 50×50 grayscale image (normalized)

2.output: Continuous (x, y) coordinates

3.Learning Type: Supervised Regression

4.Loss Function: Mean Squared Error (MSE)

#Dataset Generation

Since no dataset is provided, a synthetic dataset is generated:

One bright pixel per image

Uniform random distribution across all coordinates

Pixel values normalized to [0, 1]

# Data Split:

Training: 80%

Validation: 10%

Testing: 10%

This controlled setup ensures unbiased spatial learning and clear supervision.

#Model Architecture

A Convolutional Neural Network (CNN) is used to preserve spatial structure:

Conv2D + ReLU

MaxPooling

Conv2D + ReLU

MaxPooling

Fully Connected Layers

Output Layer → (x, y)

The CNN effectively learns positional information from pixel activations.

#Visualizations Included

Training vs Validation Loss curves

Scatter plot: Ground Truth vs Predicted Coordinates

Image overlays showing true vs predicted pixel locations

These plots verify that the model performs the intended task.

# steps to run the code 
