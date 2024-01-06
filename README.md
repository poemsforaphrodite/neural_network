# Simple Neural Network

This is a simple implementation of a neural network with one hidden layer. The neural network uses sigmoid activation functions and mean squared error loss.

## Features

- Sigmoid activation function and its derivative
- Mean squared error loss function
- A neural network class with methods for feedforward and training
- Training the neural network with gradient descent

## How to Use

1. **Define your dataset**: The `data` variable should be a numpy array where each element is an array that represents an individual sample in your dataset. The `all_y_trues` variable should also be a numpy array where each element represents the true value for the corresponding sample in the `data` array.

2. **Train the neural network**: Create an instance of the `OurNeuralNetwork` class and call the `train` method with your dataset. This will train the neural network using gradient descent.

3. **Make predictions**: You can use the `feedforward` method of the `OurNeuralNetwork` class to make predictions with your trained neural network. The input should be a numpy array that represents a single sample.

## Example

Here's an example of how to use this neural network to make predictions:

```python
# Define dataset
data = np.array([
  [-2, -1],  # Alice
  [25, 6],   # Bob
  [17, 4],   # Charlie
  [-15, -6], # Diana
])
all_y_trues = np.array([
  1, # Alice
  0, # Bob
  0, # Charlie
  1, # Diana
])

# Train the neural network
network = OurNeuralNetwork()
network.train(data, all_y_trues)

# Make some predictions
emily = np.array([-7, -3]) # 128 pounds, 63 inches
frank = np.array([20, 2])  # 155 pounds, 68 inches
print("Emily: %.3f" % network.feedforward(emily)) # 0.951 - F
print("Frank: %.3f" % network.feedforward(frank)) # 0.039 - M
