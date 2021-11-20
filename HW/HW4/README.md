# Deep Learning Assignment-4_part_1_2
MNIST Classifier Using Numpy and Keras

# Part1 - NN MNIST Using Numpy ( Accuracy -> 0.958 )
1. Neural Nets MNIST 3 layer Model with Normalization prior Training
- Training MNIST - Error and Accuracy Without Mini-Batch and dropout with Learning rate(0.005), Iterations ( 350 )

Results : 

I:349 Train-Error:0.108 Train-Accuracy:1.0

Test-Error:0.653, Test-Accuracy:0.7073

# 2. Adding Dropout ( Test Accuracy -> 0.8065 )
The test accuracy improved from 0.7073 ~ 0.8065

Results :

Epoch:299 Training-Error:0.342-> Training-Accuracy:0.883, Test-Error:0.413 -> Test-Accuracy:0.8065

# 3. Adding Minibatch Gradient Descent (minibatch=64, lr=0.005) and experimented learning rate from 0.001 to 0.005 ( Test Accuracy -> 0.8012 )

Results :

First run (minibatch =128, lr=0.001):
Epoch:299 Training-Error:0.712-> Training-Accuracy:0.46, Test-Error:0.652 -> Test-Accuracy:0.6435

Second run (minibatch =64, lr=0.001):
Epoch:299 Training-Error:0.625-> Training-Accuracy:0.611, Test-Error:0.575 -> Test-Accuracy:0.7148

Third run (minibatch=64, lr=0.005):
Epoch:299 Training-Error:0.453-> Training-Accuracy:0.747, Test-Error:0.441 -> Test-Accuracy:0.8012

# 4. Adding Data Augmentation ( Test Accuracy -> 0.8012 )

Results :

First run (minibatch =64, lr=0.001):
Epoch:299 Training-Error:0.625-> Training-Accuracy:0.611, Test-Error:0.575 -> Test-Accuracy:0.7148

Second run (minibatch =64, lr=0.005):
Epoch:299 Training-Error:0.453-> Training-Accuracy:0.747, Test-Error:0.441 -> Test-Accuracy:0.8012

Third run (minibatch =100, lr=0.005):
Epoch:299 Training-Error:0.512-> Training-Accuracy:0.75, Test-Error:0.472 -> Test-Accuracy:0.7804

# 5. Plot the results and Confusion Matrix, update the code with class Linear, Relu and MSE cost function ( Test Accuracy -> 0.958 )
- Update the code using the class Linear, class MSE and class Relu activation function.
- Using the minibatch with data augmentation but no dropout method because it causes some error in dimensions.
- The highest accuracy I got is 95.8% 

# Part2 - NN MNIST Using Keras - Accuracy ( 0.9802 )
1. Perform one-hot encoding, reshaping the mnist data and normalization prior training.

2. Used optimizer = RMSprop(lr=0.001, rho=0.9, epsilon=1e-08, decay=0.0).

3. Set a learning rate annealer
   learning_rate_reduction = ReduceLROnPlateau(monitor='val_accuracy', patience=3, verbose=1, factor=0.5, min_lr=0.00001)
   
4. Set the Keras CNN model -> [[Conv2D->relu] * 2 -> MaxPool2D -> Dropout] * 2 -> Flatten -> Dense -> Dropout -> Out

5. Conduct training without data augmentation results to validation accuracy = 0.9719

   440/440 - 256s - loss: 0.2352 - accuracy: 0.9246 - val_loss: 0.0932 - val_accuracy: 0.9719
   
6. Conduct training with data augmentation results to validation accuracy = 0.9802 ( Better Accuracy)

   439/439 - 255s - loss: 0.1737 - accuracy: 0.9475 - val_loss: 0.0776 - val_accuracy: 0.9802
   
7. Plot the results and confusion Matrix.
