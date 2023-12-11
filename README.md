# COMP432-GroupM

# Description

This project involves the study of a computer vision task using deep learning CNNs with the aim to solve image classification problems in the real world. The code in this repository trains a ResNet18 CNN model from PyTorch on a dataset from the medical field. This dataset contains Colorectal Cancer images. The results of the training are shown in terms of performance metrics like accuracy, precision, recall, and such. t-SNE is used for visualising feature extraction done by the CNN model and the result can be seen in the code output. This pretrained ResNet18 model along with another CNN model from ImageNet are used to visualise feature extraction done on two new datasets, containing Prostate Cancer and animal faces images. KNN clustering for unsupervised learning and SVM for supervised learning are then applied to the two new datasets for classification and the results are reported.


# Instructions

We developed our project in a Jupyter notebook hosted on Google Colab: 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mkandaleft/COMP432-GroupM/blob/main/Comp432.ipynb)

All library requirements should be automatically fulfilled by running its first cell.

Training and validation of the custom ResNet18 model are handled by the cells in the 'Task 1' section. Run them one sequentially. The necessary data should be downloaded automatically, though the !gdown command may need to be uncommented.

  
To run the pre-trained model on the provided sample test dataset:
-  Load the pre-trained ResNet-18 CNN model trained in Task 1 as done in Task 2 for visualization of features in t-SNE
-  Create a checkpoint using torch.load and set file path to resnet18_weights.pth
-  Need to set the pretrained=True as such torchvision.models.resnet18(pretrained=True)
-  Load the resnet18 model using load_state_dict function
-  Download the sample dataset as done in Task 2 from the filepath "SampleTestDataset/ProstateCancer" for example using torchvision.datasets.ImageFolder and the transforms object
-  The pre-trained model can be run on the desired sample datasets similar to how is done during testing for Task 1

    
A sample dataset (3 times 100 images, each distributed between 3 classes) can be downloaded as part of this repo.
