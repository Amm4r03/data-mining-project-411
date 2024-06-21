## Model evaluation
We made use of the following models :
- logistic regression
- random forest
- naive bayes
- neural network

The models were evaluated on the basis of their accuracy and the score they recieved on the test data from kaggle (value between 0 and 1)

### structure of the neural net used
1. **Model Type**: Sequential
   - The model is a Sequential neural network, which means it consists of a linear stack of layers where each layer has exactly one input tensor and one output tensor.

2. **Input Layer**:
   - The first layer is a Dense (fully connected) layer.
   - **Input Dimension**: The number of input features is equal to `x_train_scaled.shape[1]`, which means the model expects input data with this many features.
   - **Units**: 64 neurons
   - **Activation Function**: ReLU (Rectified Linear Unit)
   
3. **Dropout Layer**:
   - Following the first dense layer, there is a Dropout layer with a rate of 0.5.
   - **Dropout Rate**: 0.5, meaning 50% of the neurons are randomly set to zero during each training step to prevent overfitting.

4. **Second Hidden Layer**:
   - Another Dense layer with 32 neurons.
   - **Activation Function**: ReLU
   
5. **Second Dropout Layer**:
   - Another Dropout layer with a rate of 0.5 to further prevent overfitting.

6. **Third Hidden Layer**:
   - A Dense layer with 16 neurons.
   - **Activation Function**: ReLU

7. **Output Layer**:
   - The final layer is a Dense layer with a single neuron.
   - **Activation Function**: Sigmoid
   - This configuration is typical for binary classification tasks, where the output is a probability value between 0 and 1 indicating the likelihood of the positive class.

#### Summary of the Model Architecture:

1. **Input Layer**: Dense layer with 64 neurons, ReLU activation
2. **Dropout Layer**: 50% dropout rate
3. **Hidden Layer 1**: Dense layer with 32 neurons, ReLU activation
4. **Dropout Layer**: 50% dropout rate
5. **Hidden Layer 2**: Dense layer with 16 neurons, ReLU activation
6. **Output Layer**: Dense layer with 1 neuron, Sigmoid activation

#### Purpose and Use:
- **Purpose**: This model is designed for a binary classification problem.
- **Regularization**: Dropout layers are used after the dense layers to prevent overfitting by randomly setting a fraction of input units to 0 at each update during training time.
- **Activation Functions**:
  - **ReLU**: Used in hidden layers to introduce non-linearity, allowing the network to learn complex patterns.
  - **Sigmoid**: Used in the output layer to output a probability score, suitable for binary classification (0 or 1 signifying whether the passenger survived or not)


## comparing model performances
| S. No. | Model Name          | version (if any) | Kaggle Score |
|:------:|:-------------------:|:----------------:|:------------:|
| 1      | Random Forest       | 1                | 0.77511      |
| 2      | Random Forest       | 2                | 0.76076      |
| 3      | Logistic Regression | 1                | 0.76315      |
| 4      | Neural network      | 1                | 0.78468      |
| 5      | neural network      | 2                | 0.77511      |
| 6      | neural network      | 3                | 0.76555      |
| 7      | Naive Bayes         | 1                | 0.75358      |


### Results
From our list of models and approaches, we concluded that the neural networks were able to get the the best score from kaggle standing at 0.78468 with an accuracy of 86% and an F1 score of 0.8021 or 80.21%