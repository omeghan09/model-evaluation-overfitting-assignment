# Model Evaluation and Overfitting Assignment

## Overview
This project uses the Fashion-MNIST dataset to compare a baseline convolutional neural network (CNN) with an improved model designed to reduce overfitting.

## Data Preparation
The dataset was split into training, validation, and testing sets using `train_test_split` with stratification to preserve class balance and a fixed random state for reproducibility.

## Models
### Baseline Model
A simple CNN with:
- Convolutional and pooling layers
- One fully connected layer
- No explicit overfitting controls

### Improved Model
A CNN with multiple overfitting mitigation techniques:
- L2 regularization
- Dropout layers
- Batch normalization
- Data augmentation (ImageDataGenerator)
- Early stopping

## Results
- Baseline Test Accuracy: 0.9012  
- Improved Test Accuracy: 0.8580  

### Accuracy Comparison
The baseline model achieved higher validation and test accuracy. The improved model peaked earlier and showed more constrained learning.

### Loss Comparison
The baseline model showed a steady decrease in validation loss, indicating strong fit to the data. The improved model’s validation loss decreased early but then increased slightly, suggesting that the model reached its optimal point quickly and that further training did not improve performance. This pattern reflects the impact of regularization and early stopping in controlling overfitting.

## Key Takeaway
This project demonstrates that while techniques such as dropout, regularization, batch normalization, data augmentation, and early stopping can reduce overfitting, they can also make the model more conservative. In this case, the improved model traded some accuracy for better generalization control, highlighting the importance of balancing model complexity and regularization.

## Files Included
- Jupyter Notebook with all code and outputs
- Plots comparing accuracy and loss over epochs
