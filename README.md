# Inception V3 for Pneumonia Detection
This project uses a fine-tuned Inception V3 model to detect pneumonia from chest X-ray images.

## Setup
Clone the repository and install dependencies:

#Hyper-parameter Choices
The following hyper-parameters were selected for training the Inception V3 model for pneumonia detection:

Learning Rate: 1e-4
The Adam optimizer was used with a learning rate of 0.0001, which provides a balance between stable convergence and the ability to fine-tune the pretrained layers effectively.

Batch Size: 32
A batch size of 32 allows efficient use of memory and stable gradient updates during training, and is a commonly recommended value for Inception V3 on image classification tasks.

Epochs: 25
The model was trained for 25 epochs, with early stopping based on validation loss to prevent overfitting.

Callbacks:
EarlyStopping with patience of 5 to halt training if validation loss does not improve.
ReduceLROnPlateau to decrease the learning rate when validation loss plateaus, helping the model converge more effectively.

Class Weights:
Class weights were computed and applied to handle class imbalance in the dataset, ensuring the model does not become biased toward the majority class.

These choices were made based on standard practices for transfer learning with Inception V3 and preliminary experiments. 
