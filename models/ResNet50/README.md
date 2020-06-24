# Model and Hyper-parameters
Link to access the models weights: https://drive.google.com/drive/folders/1-G_RMiavFqebwgmJxSrFXQu-GdzEQFFa?usp=sharing

# ResNet50 1

Standard ResNet freezed with the following added:
    
    - Dense of 128 nodes, using relu
    - Dropout of 0.2
    - Dense of 64 nodes, using relu
    - Dropout of 0.2
    - Dense of 3 nodes, using softmax


Learning Rate of 0.0001 using Adam, with decaying callback on keras.




### Results

![Accuracy during Training](ResNet50_1accuracy.png "Accuracy during Training")

![Loss during Training](ResNet50_1loss.png "Loss during Training")


### Confusion Matrix
![Confusion Matrix](ResNet50_1.png "Confusion Matrix")

### Classification Report
![Classification Report](ResNet50_2.png "Classification Report")

# ResNet50 2

This model was training all the architecture ResNet 50 and add three layers equal ResNet50 1.

### Results

![Accuracy during Training](ResNet50_2accuracy.png "Accuracy during Training")

![Loss during Training](ResNet50_2loss.png "Loss during Training")


### Confusion Matrix
![Confusion Matrix](ResNet50_3.png "Confusion Matrix")

### Classification Report
![Classification Report](ResNet50_4.png "Classification Report")


# Conclusion

The frozen ResNet architecture was a horrible performance for this case. For ResNet 50 1 we did many editions in the architecture, but the has is same results.  Thus, we are training the all architecture the result was better. However, the ResNet50 2 still has a very false positive.
