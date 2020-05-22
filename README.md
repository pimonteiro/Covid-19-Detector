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




## Models

<img align="right" src="https://media.giphy.com/media/i4NjAwytgIRDW/giphy.gif" width="150" height="150"/> 

This section is about the models created by group 7 for the work of detecting COVID-19 in x-ray images. All notebooks with their respective model follow the pipeline exposed in the standard notebook, [Covid_19_Standard_Notebook.ipynb](models/).



Link to model| Short description | 
--- | --- | 
[First Example](models/FirstExample/FirstExample.ipynb) | This notebook was the first developed to test and understand the augmentation techniques, transfer learning. | 
[VGG16]() |  |
[VGG19](models/VGG19/FirstExample.ipynb) | This notebook use the  VGG19 network architecture.|
[X]()| |

