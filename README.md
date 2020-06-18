# Covid-19-Detector
<img align="left" src="https://media.giphy.com/media/UUsOy6IWmzw6mmeOpQ/giphy.gif" width="200" height="200" /> 

Covid-19 XRay Detector
This project was made on behalf of a subject on our 4th year of the Master's Degree on Data Science. It's goal is to achieve a model viable enough to produce good results on distinguishing cases of Pneumonia, Covid-19 and the absence of any of these. Due to the lack of a single source of data to use to train our models, we used a data-generator from "COVID-Net: A Tailored Deep Convolutional Neural Network Design for Detection of COVID-19 Cases from Chest Radiography Images", made by Linda Wang, Zhong Qiu Lin and Alexander Wong. Link here: <https://github.com/lindawangg/COVID-Net>. The only part we used was the data-generator provided but with some modifications to attend our needs. Thank you to all the participants of the COVID-Net for their hard-work on making it this far. The reason we didn't simply fork the main repository was to make it simpler for evaluation.





## About Team
The developer team is three master students from University of Minho, Braga, Portugal.

* [Filipe Monteiro](https://github.com/pimonteiro)
* [Mariana Lino](https://github.com/marianalino)
* [Leonardo Silva](https://github.com/leoproject)

## Dataset
The dataset we used, as explained above, was generated using a script from the **COVID-Net** repository. The file was then uploaded to my personal drive, where we must unzip it in order to use it. Link for the dataset: https://drive.google.com/open?id=1EtA92aU1GmcRCR00hTxmyC2kfQIEYx-L

Edit:
A new dataset was made to balance the data between the 3 classe: https://drive.google.com/file/d/1_X_cO5INBY3EfSGEYlMe6hmc4ni2bujH/view?usp=sharing

|Train_Data | Original | Balanced |
|:---------:|:--------:|:--------:|
|  COVID-19 |    223   |   1561   |
| Pneumonia |   5451   |   1700   |
|   Normal  |   7966   |   1700   |

| Test_Data  |  |
|:----------:|:--------:|
|  COVID-19  |    31    |
|  Pneumonia |    594   |
|   Normal   |    885   |

This was created by removing a lot of records with Pneumonia and Normal, randomly and generating new data of COVID-19 using some transformations: each real image was transformed 6 times. This was also made before the computation to speed up the process of training the various models (making image augmentation during the training caused epochs to take between 5 to 10 minutes to complete).

## Models

<img align="right" src="https://media.giphy.com/media/i4NjAwytgIRDW/giphy.gif" width="150" height="150"/> 

This section is about the models created by group 7 for the work of detecting COVID-19 in x-ray images. All notebooks with their respective model follow the pipeline exposed in the standard notebook, [Covid_19_Standard_Notebook.ipynb](models/Covid_19_Standard_Notebook.ipynb).



Link to model| Short description | Articles About| 
--- | --- | --- | 
[Covid_19_First Example](models/FirstExample/) | This notebook was the first developed to test and understand the augmentation techniques, transfer learning. | [Article](https://medium.com/analytics-vidhya/cnns-architectures-lenet-alexnet-vgg-googlenet-resnet-and-more-666091488df5)
[Covid_19_VGG16](models/VGG16/) | This notebook use the  VGG16 network architecture.| [Article](https://arxiv.org/abs/1409.1556)
[Covid_19_VGG19](models/VGG19/) | This notebook use the  VGG19 network architecture.|[Article](https://arxiv.org/abs/1409.1556)
[Covid_19_XCeption](models/XCeption/)| This notebook use the  XCeption network architecture |[Article](https://arxiv.org/abs/1610.02357)
[Covid_19_ResNet50](models/ResNet50/)| This notebook use the  ResNet50 network architecture | [Article](https://arxiv.org/abs/1512.03385)
[Covid_19_LeNet](models/LeNet/)| This notebook use the  LeNet network architecture.| [Article](https://www.pyimagesearch.com/2016/08/01/lenet-convolutional-neural-network-in-python/)

