# Model and Hyper-parameters


<!-- Model -->
## Model 

## Model with balanced dataset

 Lenet arquitecture:
    
    - Two sets: *Convolutional Layers* and *Pooling Layers*
    - One *Flattening Convolution Layer*
    - Two *Fully-Connected Layers*
    - A *softmax* classificator

Learning Rate of 0.0001 using Adam, with decaying callback on keras.

Link to access the model weights: https://drive.google.com/drive/folders/1-G6dT_a3ZxD6INWP_PAIcCN5sBH-Yjcn?usp=sharing



### Results

![Accuracy during Training](acc_lenet.png "Accuracy during Training")

![Loss during Training](loss_lenet.png "Loss during Training")


#### Confusion Matrix
![Confusion Matrix](lenet_cr.png "Confusion Matrix")

#### Classification Report
![Classification Report](lenet_cm.png "Classification Report")



# Conclusion


