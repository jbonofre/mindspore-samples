# Pet Classification example

## Dataset

Download the dataset containing pet images:

https://download.microsoft.com/download/3/E/1/3E1C3F21-ECDB-4869-8368-6DEBA77B919F/kagglecatsanddogs_3367a.zip

For instance:

----
curl -O https://download.microsoft.com/download/3/E/1/3E1C3F21-ECDB-4869-8368-6DEBA77B919F/kagglecatsanddogs_3367a.zip
----

## Preprocessing

Preprocessing step extracts the dataset archive and select the correct images:

----
python preprocessing_dataset.py /path/to/kagglecatsanddogs_3367a.zip
----

## Train model

The train model step does:

* installation of the required dependency to process the image (e.g. `opencv-python` and `maplotlib`)
* before formal training, the script extracts six images from the dataset and load them to the current model file.
* collect data features
* during training, the model accurancy is tested. If the accurancy of the trained model exceeds the current model accurancy, the model with high accurancy is saved.

----
python train.py
----
