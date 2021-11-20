# Assignment-3_part_a.ipynb
HW3 Part-A Numpy - Relu Non-linear Implementation 

1. Generate data: 3 dimensions input and 2 dimensions output 
2. Create Non Linear Data Model
3. Train the 3dim and 2output generated data using Linear model 
4. Add ReLu function to learn the non-linear data, we need non-linearities in our model.
5. Train the new non-linear model.
6. Fit the model and compute the cost function.
7. Plot the output post training as well as the real data  using tsne.
   Result: Similar plots but different values
 
# Assignment-3_part_b1.ipynb
HW3 Part-B2 Pytorch - no auto-differentiation Implementation
1. Generate data: 3 dimensions input and 2 dimensions output 
2. Add ReLu function to learn the non-linear data, we need non-linearities in our model but didn't use it (no auto-differentiation)
3. Train the 3dim and 2output generated data using Pytorch
4. Fit the model and compute the cost function using Pytorch
5. Plot the output post training as well as the real data  using tsne.
   Result: Similar plots but different values

# Assignment-3_part_b2.ipynb
HW3 Part-B2 Pytorch - Relu Non-linear, with auto-differentiation primitive Implementation

1. Generate data: 3 dimensions input and 2 dimensions output 
2. Add ReLu function to learn the non-linear data, we need non-linearities in our model.
3. Train the 3dim and 2output generated data using Pytorch, Test just one forward and backward step.
4. Test just one forward and backward step
5. Fit the model and compute the cost function using Pytorch
6. Plot the output post training as well as the real data  using tsne.
   Result: Similar plots but different values
 
# Assignment-3_part_b3.ipynb
HW3 Part-B3 Pytorch - Relu Non-linear, with auto-differentiation high level primitive implementation
1. Generate data: 3 dimensions input and 2 dimensions output 
2. Add Linear function using 10samples training input and two samples for training output.
3. Perform Training Loop Function.
4. Add ReLU Function.
5. Train again the model after performing MSE cost function computation and adding ReLU and optimization. 
6. Sequential Function using ReLU activation function in Hidden Layer
7. Fit the model using the cost function and optimization using Pytorch.
8. Plot the output post training as well as the real data using tsne with 10 input/2 output training sample. Result: Similar plots but different values.

# Assignment-3_part_c1.ipynb
HW3 Part-C1 Tensorflow - no auto-differentiation Implementation
1. Generate data: 3 dimensions input and 2 dimensions output and utility functions
2. Train the model and compute the cost function for each epoch.
3. Compute the Model predictions
4. Add ReLu function to learn the non-linear data
5. Train the 3dim and 2output generated data with Relu function and cost function
6. Fit the model again
7. Plot the output post training as well as the real data using tsne. Result: Similar plots but different value.

# Assignment-3_part_c2.ipynb
HW3 Part-C2 Tensorflow - Relu Non-linear, with auto-differentiation primitive Implementation
1. Generate data: 3 dimensions input and 2 dimensions output and utility functions
2. Train the model and compute the cost function for each epoch.
3. Compute the Model predictions
4. Add ReLu function to learn the non-linear data
5. Train the 3dim and 2output generated data with Relu function and cost function
6. Fit the model again
7. Plot the output post training as well as the real data using tsne. Result: Similar plots but different value.

# Assignment-3_part_c3.ipynb
HW3 Part-C3 Tensorflow - Model Subclassing, Relu Non-linear, with auto-differentiation high level primitive implementation
1. Createad a Class Linear, MLPBlock with Relu in forward pass and ActivityRegularizationLayer to add loss method.
2. Then retrieve the loss via OuterLayer class.
3. Added OuterLayerWithKernelRegularizer for loss regularization.
4. The add_metric() method Similarly to add_loss(), layers also have an add_metric() method for tracking the moving average of a quantity during training.
5. Add a "logistic endpoint" layer. It takes as inputs predictions & targets, it computes a loss which it tracks via add_loss(), 
   and it computes an accuracy scalar, which it tracks via add_metric().
7. Just like for add_loss(), these layer metrics in Logistic endpoint are tracked by fit() method.
8. Plot the summary model and the TSNE ( true value and predicted TSNE )
   Added Tensorboard for loss tracking.


