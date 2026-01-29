# Pixel Coordinate Regression with CNN

# PROBLEM STATEMENT:
Using Deep Learning techniques, predict the coordinates (x,y) of a pixel which has a value of 255 for 1 pixel in a given 50x50 pixel grayscale image and all other pixels are 0. The pixel with a value of 255 is randomly assigned. You may generate a dataset as required for solving the problem.

# <h2>solution:<h2>
# <h1>jupitor notebook code summary<h1>

1.Input: 50×50 grayscale image (normalized)

2.output: Continuous (x, y) coordinates

3.Learning Type: Supervised Regression

4.Loss Function: Mean Squared Error (MSE)

# Dataset Generation

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

# Visualizations Included

Training vs Validation Loss curves

Scatter plot: Ground Truth vs Predicted Coordinates

Image overlays showing true vs predicted pixel locations

These plots verify that the model performs the intended task.

<h1> #steps to run the file:</h1>

<p><u>git commands:</u></p>

git clone "https://github.com/anirudhkowluri/fake-news-detector.git"

cd "change the path to the destination file"

ls

git status

<h1>#commands activate the virtual enivornment in terminal and load the streamlit website:</h1>

<h2>#Create the virtual enivironment</h2>
python -m venv .venv

<h2># run the excecution policy ,if activation is blocked by execution policy, run:</h2>
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

<h2>#Activate the virtual enivironment(venv) in PowerShell(Terminal)</h2>
.\.venv\Scripts\Activate.ps1

<h2>#Install  libraries from requirements.txt</h2>
python -m pip install -r .\requirements.txt

<h2>#Verify installed packages (brief)</h2>
python -m pip list

<h2>#Save installed versions</h2>
python -m pip freeze > installed-versions.txt

<h2>#Execute the code files</h2>
Execute the jupytor notebook file
