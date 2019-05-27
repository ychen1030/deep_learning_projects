# UC Berkeley CS182: Natural Language Processing

In this project, you will learn about processing and generating text. Specifically, you will build a neural network to generate news headlines, through the training of an LSTM-based language model. Then you will train a Transformer to summarize news articles.

# Installation

This project requires Python 3. If you plan to complete this project with a local machine, and not in the Google Colab, please install Python 3.

## Linux / MAC Os

Installing on Linux is very similar to the previous projects. You can run the following:
```bash
virtualenv .env --python=python3
````
To create a virtual environment. Running:
```bash
source .env/bin/activate
```
will install the python requirements for the project. **Make sure that you are running a version of python >= 3.5**. If you are not (which can be checked with `python3 --version`) install an updated version of python using the instructions here: https://www.tecmint.com/install-python-in-ubuntu/

Open one of the .ipynb project files through Jupyter in a browser and make sure you are using the right Python environment by going into the "Kernel" tab "change kernel" and selecting the correct kernel to run the code in (Python 3).

You now must install the required packages for the project. If you are using a GPU-enabled machine:
```bash
pip3 install -r requirements_gpu.txt
```
Otherwise:
```bash
pip3 install -r requirements.txt
```

## Windows

Windows is not officially supported. There is a chance that you will be able to get this working with Anaconda on windows, however we strongly suggest using a virtual machine (virtual box) with an installation of linux, as it will likely be more stable, and the GSIs will be able to provide additional assistance. 

## Colab

You can use our modified Notebooks for the Google Colab. Google Colab notebooks can be used with a CPU, or with a K-80 GPU (on this project, it seems to give a 5x training speed boost).
The Notebooks we have shared on Google Colab have been modified so that it is easy to access the datasets in your Google Drive, and save the model files. If you opt for this option, you will have to duplicate the folder on Google Drive and work on the project in your copy.
However, you must recuperate the models, and verify that they work locally before submitting your files.
he dataset files are available for download in this folder: https://drive.google.com/open?id=1TNhUy9ldZ5mv_GLNNmCBFnLfT3DXwntF
You must be logged in on your UC Berkeley Google account to see the folder, and you must duplicate it (copy it to your own drive) to have write access over the files. The .ipynb can be opened into the Google Colab by double clicked and selecting "Open with Colaboratory".

# Downloading the Data

To download the data, run the following command from the project root directory:
```bash
bash download_data.sh
```
If you get the error "bash: ./download_data.sh: Permission denied" run `chmod +x download_data.sh` and try again. 

# Preparing a Submission

To prepare a submission, run the following command from the project root directory:
```bash
bash prepare_submission.sh
```
This will create a "submission.zip" file which can be submitted for the homework. You may get a warning if the files required do not exist - please pay attention to this, as we will not be responsible if you forget to include these files in the zipped folder.
Check that your submission contains:
- "1 Language Modeling.ipynb" and "2 Summarization.ipynb"
- "capita.py", "transformer.py", "transformer_attention.py", "transformer_layers.py"
- Your model files (.index, .cptk, .data) for each notebook. The names of the models you upload should match the names you put in the Jupyter notebooks. This should be a total of 6 files.

If you get the error "bash: ./prepare_submission.sh: Permission denied" run `chmod +x download_data.sh` and try again. 
