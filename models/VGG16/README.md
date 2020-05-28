# Model and Hyper-parameters

Standard VGG16 freezed with the following added:
    
    - Dense of 512 nodes, using relu
    - Dropout of 0.5
    - Dense of 256 nodes, using relu
    - Dense of 3 nodes, using softmax

Learning Rate of 0.001 using Adam, with decaying callback on keras.


Link to access the model weights: https://drive.google.com/drive/folders/1-4MAlVo15gQ2NsU6DbHAKwqRSdROk6hK?usp=sharing

# Results


## Confusion Matrix
![Confusion Matrix](vgg16_cr.png "Confusion Matrix")

## Classification Report
![Classification Report](vgg16_cm.png "Classification Report")
