# de-Fungi-Classifier
### About the Dataset
- **Name**: DeFungi
- **Description**: A dataset for direct mycological examination of microscopic fungi images.
- **Image Origin**: Superficial fungal infections caused by yeasts, molds, or dermatophyte fungi.
- **Labeling**: Manually labeled into five classes with expert assistance.
- **Preprocessing**: Images have been cropped with automated algorithms.
- ### Model Summary Tables

#### VGG19 Model Summary
```plaintext
Layer (type)                Output Shape              Param #
==============================================================
vgg19 (Functional)          (None, 7, 7, 512)         20,024,384

flatten (Flatten)           (None, 25088)             0

dropout (Dropout)           (None, 25088)             0

dense (Dense)               (None, 5)                 125,445
==============================================================
Total params: 20,149,829 (76.87 MB)
Trainable params: 125,445 (490.02 KB)
Non-trainable params: 20,024,384 (76.39 MB)
```
![VGG19 Model Summary](https://github.com/Soumyasharmaa/de-Fungi-Classifier/blob/main/Model_summary.png?raw=true)

#### Custom Model
```plaintext
Layer (type)                Output Shape              Param #
==============================================================
conv2d (Conv2D)             (None, 222, 222, 32)      896

batch_normalization (Batch  (None, 222, 222, 32)      128
Normalization)

max_pooling2d (MaxPooling2  (None, 111, 111, 32)      0
D)

conv2d_1 (Conv2D)           (None, 109, 109, 64)      18,496

batch_normalization_1 (Bat  (None, 109, 109, 64)      256
chNormalization)

max_pooling2d_1 (MaxPoolin  (None, 54, 54, 64)        0
g2D)

conv2d_2 (Conv2D)           (None, 52, 52, 64)        36,928

batch_normalization_2 (Bat  (None, 52, 52, 64)        256
chNormalization)
                                                                
 max_pooling2d_2 (MaxPoolin  (None, 26, 26, 64)        0         
 g2D)                                                            
                                                                 
 conv2d_3 (Conv2D)           (None, 24, 24, 128)       73856     
                                                                 
 batch_normalization_3 (Bat  (None, 24, 24, 128)       512       
 chNormalization)                                                
                                                                 
 max_pooling2d_3 (MaxPoolin  (None, 12, 12, 128)       0         
 g2D)                                                            
                                                                 
 flatten (Flatten)           (None, 18432)             0         
                                                                 
 dense (Dense)               (None, 128)               2359424   
                                                                 
 dense_1 (Dense)             (None, 75)                9675
==============================================================
Total params: 2,500,427 (9.54 MB)
Trainable params: 2,499,851 (9.54 MB)
Non-trainable params: 576 (2.25 KB)
```
### Model Training and Evaluation

#### Training and Validation Accuracy For VGG19

- **Validation loss**: 0.9852526783943176
- **Validation Accuracy**: 0.896267831325531

#### Loss vs. Epoch Graph

![Loss vs. Epoch](https://github.com/Soumyasharmaa/de-Fungi-Classifier/blob/main/Train_valid_loss_vs_epochs.png?raw=true)

#### Training and Validation Accuracy For Custom Model

- **Validation loss**: 0.7480524778366089
- **Validation Accuracy**: 0.9319429397583008
- ### Resources
- [Learn More About Fungi](https://www.kaggle.com/datasets/joebeachcapital/defungi/data)

