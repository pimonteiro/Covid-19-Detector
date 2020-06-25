# Covid-19-Detector
<img align="left" src="https://media.giphy.com/media/UUsOy6IWmzw6mmeOpQ/giphy.gif" width="200" height="200" /> 

Covid-19 XRay Detector
This project was made on behalf of a subject on our 4th year of the Master's Degree on Data Science. It's goal is to achieve a model viable enough to produce good results on distinguishing cases of Pneumonia, Covid-19 and the absence of these. Due to the lack of a single source of data to train our models, we used a data-generator from "COVID-Net: A Tailored Deep Convolutional Neural Network Design for Detection of COVID-19 Cases from Chest Radiography Images", made by Linda Wang, Zhong Qiu Lin and Alexander Wong. Link here: <https://github.com/lindawangg/COVID-Net>. The only part we used was the data-generator provided but with some modifications to attend our needs. Thank you to all the participants of the COVID-Net for their hard-work on making it this far. The reason we didn't simply fork the main repository was to make it simpler for evaluation.





## About Team
The developer team is three master students from University of Minho, Braga, Portugal.

* [Filipe Monteiro](https://github.com/pimonteiro)
* [Mariana Lino](https://github.com/marianalino)
* [Leonardo Silva](https://github.com/leoproject)

## Dataset
The dataset we used, as explained above, was generated using a script from the **COVID-Net** repository. The file was then uploaded to my personal drive, where we must unzip it in order to use it. Link for the dataset: https://drive.google.com/open?id=1EtA92aU1GmcRCR00hTxmyC2kfQIEYx-L

Being the data so unbalaced, a new dataset was made to fix this problem: https://drive.google.com/file/d/1_X_cO5INBY3EfSGEYlMe6hmc4ni2bujH/view?usp=sharing

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

The exploration of these datasets can be found in the [Covid_19_Data_Exploration.ipynb](dataset/Covid_19_Data_Exploration.ipynb) notebook.

## Models

<img align="right" src="https://media.giphy.com/media/i4NjAwytgIRDW/giphy.gif" width="150" height="150"/> 

Here we discuss the models created by our group. All notebooks with their respective model follow the pipeline exposed in the standard notebook, [Covid_19_Standard_Notebook.ipynb](models/Covid_19_Standard_Notebook.ipynb), and are displayed on the following table:



Link to model| Short description | Articles About| 
--- | --- | --- | 
[Covid_19_First Example](models/FirstExample/) | This notebook was the first developed to test and understand the augmentation techniques, transfer learning. | [Article](https://medium.com/analytics-vidhya/cnns-architectures-lenet-alexnet-vgg-googlenet-resnet-and-more-666091488df5)
[Covid_19_VGG16](models/VGG16/) | This notebook uses the  VGG16 network architecture.| [Article](https://arxiv.org/abs/1409.1556)
[Covid_19_VGG19](models/VGG19/) | This notebook uses the  VGG19 network architecture.|[Article](https://arxiv.org/abs/1409.1556)
[Covid_19_XCeption](models/XCeption/)| This notebook uses the  XCeption network architecture |[Article](https://arxiv.org/abs/1610.02357)
[Covid_19_ResNet50](models/ResNet50/)| This notebook uses the  ResNet50 network architecture | [Article](https://arxiv.org/abs/1512.03385)
[Covid_19_LeNet](models/LeNet/)| This notebook uses the  LeNet network architecture.| [Article](https://www.pyimagesearch.com/2016/08/01/lenet-convolutional-neural-network-in-python/)
[Covid_19_MobileNetV2](models/MobileNetV2/)| This notebook uses the  MobileNetV2 network architecture | [Article](https://arxiv.org/abs/1801.04381)
[Covid_19_CXRP](models/CXRP/)| This notebook uses a newly created architecture - CXRP (Covid Xray Profiler) |
[Covid_19_BraDetect](models/BraDetect/)| This notebook uses a newly created architecture - BraDetect |
[Covid_19_SCNN](models/SCNN/)| This notebook uses a newly created architecture - SCNN (Simple Covid-19 Neural Network) |


## Conclusion


|             | Accuracy |          | Precision |           |          | Recall |           |         Notes         |
|:-----------:|:--------:|:--------:|:---------:|:---------:|:--------:|:------:|:---------:|:---------------------:|
|             |          | Covid-19 |   Normal  | Pneumonia | Covid-19 | Normal | Pneumonia |                       |
|    VGG16    |   0.90   |   0.68   |    0.94   |    0.86   |   0.84   |  0.90  |    0.90   |       Retrained       |
|    VGG19    |   0.92   |   0.68   |    0.96   |    0.87   |   0.84   |  0.91  |    0.93   |       Retrained       |
|   XCeption  |   0.79   |   0.78   |    0.91   |    0.68   |   0.23   |  0.74  |    0.89   |   Freezed; Version 2  |
|   ResNet50  |   0.82   |   0.81   |    0.98   |    0.70   |   0.81   |  0.72  |    0.97   |        Freezed        |
| MobileNetV2 |   0.86   |   1.00   |    0.97   |    0.75   |   0.71   |  0.79  |    0.97   | Retrained; Overfitted |
|   CXRP-3B   |   0.88   |   0.42   |    0.91   |    0.89   |   0.90   |  0.90  |    0.84   |        3 Blocks       |
|    LeNet    |   0.87   |   0.52   |    0.89   |    0.87   |   0.81   |  0.91  |    0.81   |                       |
|     SCNN    |   0.84   |   0.29   |    0.93   |    0.81   |   0.77   |  0.83  |    0.86   |        2 Blocks       |
|  BraDetect  |   0.85   |   0.56   |    0.91   |    0.79   |   0.74   |  0.85  |    0.86   |                       |



Of all the explored models the best one performance wise was the CXRP-3B, with a good balance in *recall* for all the different classes. One might think the VGG19 had a better development, but in fact the model isn't consistent enough to be have trustable predictions - the training appeared very random, even tho the predictions were right. All other models still had a very good performance, all with close numbers of *accuracy*, *precision* and *recall*.
Despite others having better accuracy than the __CXRP-3B__, we tried to focus on the __Recall__ metric because it represents the percentage of positive cases of each class that were correctly assigned - we want to avoid giving false negatives, as well as always try to have the most confident of not having Covid-19 - reason being why we want to maximize the recall of Covid-19.