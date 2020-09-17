# CNN_Spectrogram_Algorithm
A method to classify spectrograms from raw EEG data using a convolutional neural network (CNN)

To run the code, you must have a data folder of the following structure:

data/
├── train/
    ├── Yes
    ├── No
├── valid/
    ├── Yes
    ├── No
├── test/

The Yes and No subfolders contain positive and negative case images on which we train the model. The test folder contains uncategorized images on which we test the model.

SpectrogramClassificationAlgorithm.ipynb is the code to train and test the CNN on the data described above.
