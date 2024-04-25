
# Neural-network-challenge-2
### Doug Francis
### Date: 4/25/2024
### Subject: For ASU Artificial Intelligence Course Work. Modeule 19. Due 4/25/2024

## About The Project
This project predicts if employess are likely to leave the company and tried to select which department employees are best suited to work in the organization. We employe a neural network to solve this problem. 

**Feature Selection:** Prior to using the neural network, data preprocessing was carried out. Ten plus columns of the original 25 were selected. In my case, I used "Pipey" which was our automated classification project produced for this class as "AI Project 2". I looked at what features were most important accoss a few different classification models. The Pipey analysis, as a PDF, is located in the "temp_data" folder.  This was not a required part of the project, but seemed a much better choice than selecting the features at random or presupposing domain knowledge for a dataset we know little about. 

**Preprocessing** This involved encoding any categorical columns and scaling any numeric columns. Of course this also included splitting the data into a training and test set.  Since there was two Y variables (Attrition and Department) these were mapped to numeric values. Since Department was multiclass (three levels), One Hot Encoding was used. 

**Modeling:** The neuro network was a branched model. The input layer corresponding to the number of features, followed by two hidden layers shared by both Y variables and finally by dedicated hidden layers for each Y variable. The branched output layers both used categorical_crossentropy as a loss function, accuracy as the metric to optimize and softmax activation function for the output layer.

**Results:** See the Jupyter Notebook "Attrition.ipynb" for details. In brief, we were more successful at predicting attrition, where the accuracy across the test data was 80.7% versus predicting Department, which had an accuracy across the test data of only 57.1%. See the notebook for more details.


## Location of the Code and Write Up

The file is in the root directory of the Git repository. The file name is "Attrition.ipynb". At the end of the file there are a few questions about the results that are answered. 

## Getting Started

The steps below should get you started to get this project up and running on your local machine.

### Prerequisites

The following are prerequisites for this project. Instructions for pip installation are provided for each of the packages.

* Python - This project was created using Python version 3.11.5. Package compatability has not been tested with other versions of Python. See https://www.digitalocean.com/community/tutorials/install-python-windows-10 as a reference for Python installation.


* pandas (my version is 2.0.3)
  ```sh
  pip install pandas
  ```
* tensorflow (my version is 2.13.1)
  ```sh
  pip install tensorflow[and-cuda] - if using a compatable GPU

  or 

  pip install tensorflow-cpu - if using only your cpu
  ```
* sklearn (my version is 1.4.1.post1)
  ```sh
  pip install -U scikit-learn
  Note: scikit-lean installation encourages the use of a virtual environment. See https://scikit-learn.org/stable/install.html
  ```
* numpy (my version is 1.24.3)
  ```sh
  pip install numpy
  ```
* keras (my version is 2.13.1)
  ```sh
  keras will be automatically installed when you install tensorflow. While it can be installed separately, it is recommended to just use the pip installation of tensor flow to install keras.
  ```

### Installation and Running

_In addition to setting up Python and the required packages, perform the following steps._

1. Clone the repository on your local machine
   ```sh
   git clone https://github.com/DougInVentura/neural-network-challenge-2.git
   ```
2. Open the folder corresponding to neural-network-challenge where you installed in using the repo clone above.

3. Open the file "attrition.ipynb"

4. Make the modifications you desired. Run cell by cell or run the entire Jupyter notebook.

