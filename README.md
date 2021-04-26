# CNN_Spectrogram_Algorithm
A method to classify spectrograms from raw EEG data using a convolutional neural network (CNN)

SpectrogramClassificationAlgorithm.ipynb: trains the model on data from train and valid folders, tests on data from test folder
Use_pretrained_model.ipynb: uses our model weights from trained model, tests on new test data from test folder

Code in fastai folder comes from fastai version 0.7 by Jeremy Howard: https://www.fast.ai/

## Data Structure

To run either notebook, you must have a data folder of the following structure:

data/

├── train/

    ├── Yes
	
    ├── No
	
├── valid/

    ├── Yes
	
    ├── No
	
├── test/

For SpectrogramClassificationAlgorithm.ipynb:
The Yes and No subfolders contain positive and negative case images on which we train the model. The test folder contains uncategorized images on which we test the model.

For Use_pretrained_model.ipynb:
The test folder contains new test data to be evaluated by our pretrained model (saved_model.pkl). For the code to run with this library, the Yes and No subfolders of train and valid cannot be empty: fill them with a few images from your test data--this will not affect the output.

make_spectra_from_signal.m is MatLab code to break a signal into spectrograms and save in a test folder. To run this, you must have a .mat file containing dEDF (Nx1 vector of the data signal) and tEDF (Nx1 vector of the time signal).

Alternatively, use the notebook make_test_data_imgs_from_csv.ipynb to break the signal into spectrograms and save in a test folder. To run this, you must have a .csv file for dEDF (Nx1 vector of the data signal) and a .csv file for tEDF (Nx1 vector of the time signal)

## Environment

Below is a step-by-step method to prepare an environment capable of running the notebooks:

0. Ensure you have both conda and pip installed

1. In terminal, load in a virtual environment with conda, give it a name (`environment_name`):

`conda env create -f new_enviro.yml -n environment_name`

`conda activate environment_name`

3. Open the jupyter console to run notebooks:

`jupyter notebook` 

4. When done, use `conda deactivate` to deactivate your virtual environment. To reload this environment in the future, use `conda activate environment_name`, skipping step 2.
