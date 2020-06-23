# Model and Hyper-parameters



## Importing pre-trained model with standard *dataset*
Link to access the three models weights: https://drive.google.com/drive/folders/1thjqwJUspCQRcXoFNlWetGxp6qTrey02?usp=sharing

<!-- First Model -->
## XCeption 1
Standard XCeption freezed with the following added:
    
    - Dense of 3 nodes, using softmax

Learning Rate of 0.001 using Adam, with decaying callback on keras.

### Results
#### Training
![Accuracy & Loss](XCEPTION1_TRAING.png "Accuracy")


#### Confusion Matrix
![Confusion Matrix](XCEPTION1_CR.png "Confusion Matrix")

#### Classification Report
![Classification Report](XCEPTION1_REPORT.png "Classification Report")

<!-- Second Model -->

__________________________________
## XCeption 2

## Importing pre-trained model with balanced *dataset*
Standard XCeption freezed with the following added:
    
    - Dense of 1024 nodes, using relu
    - Dropout of 0.5
    - Dense of 3 nodes, using softmax

Learning Rate of 0.0001 using Adam, with decaying callback on keras.




### Results
#### Training
![Accuracy & Loss](XCEPTION2_TRAINING.png "Accuracy")


#### Confusion Matrix
![Confusion Matrix](XCEPTION2_CR.png "Confusion Matrix")

#### Classification Report
![Classification Report](XCEPTION2_REPORT.png "Classification Report")



<!-- Third Model -->

__________________________
## XCeption 3

## Retraining pre-trained model with balanced *dataset*
Standard XCeption with the following added:
    
    - Dense of 128 nodes, using relu
    - Dropout of 0.5
    - Dense of 3 nodes, using softmax

Learning Rate of 0.0001 using Adam, with decaying callback on keras.



### Results
#### Training
![Accuracy & Loss](XCEPTION3_TRAINING.png "Accuracy")


#### Confusion Matrix
![Confusion Matrix](XCEPTION3_CR.png "Confusion Matrix")

#### Classification Report
![Classification Report](XCEPTION3_REPORT.png "Classification Report")





# Conclusion

Training from scratch the XCeption architecture proved to not wield good results. The better result was second archicture in the case. 