# Model and Hyper-parameters



## Importing pre-trained model with standard *dataset*
Link to access the four models weights: https://drive.google.com/drive/folders/1-9k7zI7oOh3KLzgv7Ee7QsyAnkmgHsnV?usp=sharing

<!-- First Model -->
## BraDetect 1

The BraDetect was designed with the objective of being specially efficient at analyzing chest x-rays. As such, the architecture is composed of the following:
    
    - Conv 3x3 , 16 
    - Conv 3x3 , 16 
    - MaxPooling2D

    - Conv 3x3 , 32
    - Conv 3x3 , 32
    - MaxPooling2D

    - Conv 3x3 , 64
    - Conv 3x3 , 64
    - MaxPooling2D

    - Conv 3x3 , 96
    - Conv 3x3 , 96
    - MaxPooling2D

    - Conv 3x3 , 128
    - Conv 3x3 , 128
    - MaxPooling2D

    - Flatten
    - Dense with nodes 1024
    - Dropout of 0.5
    - Dense with nodes 3 



### Results
#### Training
![Accuracy & Loss](model_1accuracy.png "Accuracy")

![Accuracy & Loss](model_1loss.png "loss")


#### Confusion Matrix
![Confusion Matrix](model1_1.png "Confusion Matrix")

#### Classification Report
![Classification Report](model1_2.png "Classification Report")

<!-- Second Model -->

__________________________________
## BraDetect  2

## Importing pre-trained model with balanced *dataset*
The BraDetect was designed with the objective of being specially efficient at analyzing chest x-rays. As such, the architecture is composed of the following:
    
    - Conv 3x3 , 32
    - Conv 3x3 , 32
    - MaxPooling2D
    - Dropout of 0.2

    - Conv 3x3 , 64
    - Conv 3x3 , 64
    - MaxPooling2D
    - Dropout of 0.2

    - Conv 3x3 , 128
    - Conv 3x3 , 128
    - MaxPooling2D
    - Dropout of 0.2    

    - Flatten
    - Dense with nodes 128
    - Dropout of 0.2
    - Dense with nodes 3 

Learning Rate of 0.0001 using Adam, with decaying callback on keras.




### Results
#### Training
![Accuracy & Loss](model_2accuracy.png "Accuracy")
![Accuracy & Loss](model_2loss.png "loss")


#### Confusion Matrix
![Confusion Matrix](model2_1.png "Confusion Matrix")

#### Classification Report
![Classification Report](model2_2.png  "Classification Report")



<!-- Third Model -->

__________________________
## BraDetect 3

## Retraining pre-trained model with balanced *dataset*
The BraDetect was designed with the objective of being specially efficient at analyzing chest x-rays. As such, the architecture is composed of the following:

    - Conv 3x3 , 64
    - MaxPooling2D
    - BatchNormalization
    - ZeroPadding

    - Conv 3x3 , 96
    - MaxPooling2D
    - BatchNormalization
    - ZeroPadding

    - Conv 3x3 , 128
    - MaxPooling2D
    - BatchNormalization
    - ZeroPadding

    - Flatten
    - Dense with nodes 256
    - Dropout of 0.5
    - Dense with nodes 256
    - Dropout of 0.5
    - Dense with nodes 3 

Learning Rate of 0.0001 using Adam, with decaying callback on keras.



### Results
#### Training
![Accuracy & Loss](model_3accuracy.png "Accuracy")
![Accuracy & Loss](model_3loss.png "loss")


#### Confusion Matrix
![Confusion Matrix](model3_1.png "Confusion Matrix")

#### Classification Report
![Classification Report](model3_2.png  "Classification Report")

## BraDetect 4

## Retraining pre-trained model with balanced *dataset*
This is the third architecture with twice the epochs.



### Results
#### Training
![Accuracy & Loss](model_4accuracy.png "Accuracy")
![Accuracy & Loss](model_4loss.png "loss")


#### Confusion Matrix
![Confusion Matrix](model4_1.png "Confusion Matrix")

#### Classification Report
![Classification Report](model4_2.png  "Classification Report")



# Conclusion

Training from scratch the BraDetect architecture proved to not wield good results. The better result was third archicture was aumentation number epochs. 