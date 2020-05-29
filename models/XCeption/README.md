# Model and Hyper-parameters

Standard XCeption freezed with the following added:
    
    - Dense of 128 nodes, using relu
    - Dropout of 0.5
    - Dense of 3 nodes, using softmax

Learning Rate of 0.001 using Adam, with decaying callback on keras.

Link to access the model weights: https://drive.google.com/drive/folders/1JWzz6o9a129iwMEJ6J90X1CnQ1c_cVe8?usp=sharing


# Results

![Accuracy during Training](accuracy.png "Accuracy during Training")

![Loss during Training](loss.png "Loss during Training")


## Confusion Matrix
![Confusion Matrix](xception_cr.png "Confusion Matrix")

## Classification Report
![Classification Report](xception_cm.png "Classification Report")
