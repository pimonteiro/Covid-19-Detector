# Model and Hyper-parameters

<!-- First Model -->

## Importing pre-trained model with standard *dataset*
Standard VGG16 freezed with the following added:
    
    - Dense of 512 nodes, using relu
    - Dropout of 0.5
    - Dense of 256 nodes, using relu
    - Dense of 3 nodes, using softmax

Learning Rate of 0.001 using Adam, with decaying callback on keras.


Link to access the model weights: https://drive.google.com/drive/folders/1-4MAlVo15gQ2NsU6DbHAKwqRSdROk6hK?usp=sharing

### Results


#### Confusion Matrix
![Confusion Matrix](vgg16_cr.png "Confusion Matrix")

#### Classification Report
![Classification Report](vgg16_cm.png "Classification Report")

<!-- Second Model -->

__________________________________

## Importing pre-trained model with balanced *dataset*
Standard VGG16 freezed with the following added:
    
    - Dense of 512 nodes, using relu
    - Dense of 3 nodes, using softmax

Learning Rate of 0.0001 using Adam, with decaying callback on keras.


Link to access the model weights: https://drive.google.com/drive/folders/1-3CbhseqNYk-pg2FeSKJp-JBZIp_vAsa?usp=sharing

### Results

#### Training
![Accuracy](acc_vgg16_1.png "Accuracy")
![Loss](loss_vgg16_1.png "Loss")

#### Confusion Matrix
![Confusion Matrix](vgg16_1_cr.png "Confusion Matrix")

#### Classification Report
![Classification Report](vgg16_1_cm.png "Classification Report")



<!-- Third Model -->

__________________________

## Retraining pre-trained model with balanced *dataset*
Standard VGG16 with the following added:
    
    - Dense of 512 nodes, using relu
    - Dense of 3 nodes, using softmax

Learning Rate of 0.0001 using Adam, with decaying callback on keras.


Link to access the model weights: https://drive.google.com/drive/folders/1C6r2tBEIAO8A04ilf4iL2FlsKw_wyqsu?usp=sharing
### Results

#### Training
![Accuracy](acc_vgg16_2.png "Accuracy")
![Loss](loss_vgg16_2.png "Loss")

#### Confusion Matrix
![Confusion Matrix](vgg16_2_cr.png "Confusion Matrix")

#### Classification Report
![Classification Report](vgg16_2_cm.png "Classification Report")


<!-- Fourth Model -->

_________________________

## Training from *scratch* the VGG16 architecture with the balanced *dataset*
Standard VGG16 with the following added:
    
    - Dense of 512 nodes, using relu
    - Dense of 3 nodes, using softmax

Learning Rate of 0.0001 using Adam, with decaying callback on keras.


Link to access the model weights: https://drive.google.com/drive/folders/1-MIoGgn2CsW7fVwbsxckTncmXarkeK_E?usp=sharing
### Results

#### Training
![Accuracy](acc_vgg16_3.png "Accuracy")
![Loss](loss_vgg16_3.png "Loss")

#### Confusion Matrix
![Confusion Matrix](vgg16_3_cr.png "Confusion Matrix")

#### Classification Report
![Classification Report](vgg16_3_cm.png "Classification Report")
