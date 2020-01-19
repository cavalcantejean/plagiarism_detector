# Content: Machine Learning Deployment

This repository contains code and associated files for deploying a plagiarism detector using AWS SageMaker.

## Project: Plagiarism Detector

### Install

This project requires **Python 2.7** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. Make sure that you select the Python 2.7 installer and not the Python 3.x installer. 

### Code

Template code is provided in the `1_Data_Exploration.ipynb`, `2_Plagiarism_Feature_Engineering.ipynb` and `3_Training_a_Model.ipynb` notebook files.

### Run

In a terminal or command window, navigate to the top-level project directory `plagiarism_detector/` (that contains this README) and run one of the following commands:

```bash
ipython notebook 1_Data_Exploration.ipynb
ipython notebook 2_Plagiarism_Feature_Engineering.ipynb
ipython notebook 3_Training_a_Model.ipynb
```  
or
```bash
jupyter notebook 1_Data_Exploration.ipynb
jupyter notebook 2_Plagiarism_Feature_Engineering.ipynb
jupyter notebook 3_Training_a_Model.ipynb
```

This will open the Jupyter Notebook software and project file in your browser.

## Data

In this project, you will be tasked with building a plagiarism detector that examines a text file and performs binary classification; labeling that file as either *plagiarized* or *not*, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research; the task is non-trivial and the differences between paraphrased answers and original work are often not so obvious.

This project will be broken down into three main notebooks:

**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.
* This first notebook is **not** required in your final project submission.

**Notebook 2: Feature Engineering**

* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**

* Upload your train/test feature data to S3.
* Define a binary classification model and a training script.
* Train your model and deploy it using SageMaker.
* Evaluate your deployed classifier.
