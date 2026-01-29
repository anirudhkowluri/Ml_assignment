# Pixel Coordinate Regression with CNN

# PROBLEM STATEMENT:
Using Deep Learning techniques, predict the coordinates (x,y) of a pixel which has a value of 255 for 1 pixel in a given 50x50 pixel grayscale image and all other pixels are 0. The pixel with a value of 255 is randomly assigned. You may generate a dataset as required for solving the problem.

# <h2>solution:<h2>
# <h1>jupitor notebook code summary<h1>
The code implements a complete supervised learning workflow to predict the coordinates of a bright pixel in a grayscale image using deep learning.

First, the code generates a synthetic dataset where each 50×50 grayscale image contains exactly one pixel with maximum intensity. The pixel location is chosen randomly, and the corresponding (x, y) coordinate is stored as the ground truth label. Pixel values are normalized to improve training stability. The dataset is then split into training, validation, and test sets to enable proper model evaluation and prevent data leakage.

Next, a Convolutional Neural Network (CNN) is constructed using TensorFlow and Keras. Convolutional layers are used to extract spatial features from the image, followed by pooling layers to reduce dimensionality and improve generalization. The extracted features are flattened and passed through fully connected layers to regress the final (x, y) coordinate output. Since the task involves predicting continuous values, the model uses a linear output layer.

The model is compiled with the Adam optimizer and Mean Squared Error (MSE) loss, which is suitable for coordinate regression problems. During training, both training and validation losses are tracked to monitor convergence and detect overfitting.

After training, the model is evaluated on a held-out test set. The code generates predictions and visualizes results using scatter plots comparing predicted and ground truth coordinates, as well as image overlays highlighting true and predicted pixel positions. These visualizations provide intuitive confirmation that the model correctly learns the spatial mapping between image input and coordinate output.

Overall, the code emphasizes clarity, correctness, and interpretability, demonstrating how convolutional neural networks can be effectively applied to supervised regression tasks involving spatial data.
 
# Dependencies required to run the code:
numpy
matplotlib
tensorflow
scikit-learn
pandas
seaborn

<h1> #steps to run the file:</h1>

<p><u>git commands:</u></p>

git clone "https://github.com/anirudhkowluri/fake-news-detector.git"

cd "change the path to the destination file"

ls

git status

<h1>#commands activate the virtual enivornment in terminal a</h1>

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
