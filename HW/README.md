# cmpe-258-hw1
Homework 1 - Deep Learning Class

part 1 - Blackbox Deep Learning using Fast AI colab https://github.com/fastai/fastbook/blob/master/01_intro.ipynb

Write Colab for illustrating use of SOTA(state of the art) model architectures of fast ai using 

1. cnn_learner for image classification
2. unet_learner for segmentation, 
3. text_classifier_learner for sentiment analysis
4. tabular-learner for decision tree
5. collab_learner for ranking

part 2 - Whitebox Deep Learning read and perform the codelab https://codelabs.developers.google.com/codelabs/cloud-tensorflow-mnist#0

Follow the colab training instructions will updates only with the deliverables.Follow the instructions below:

#3.  Run through all the cells - no error encountered except it runs without GPU connect eventhough the runtime setting selected is GPU.
#6.  Adding layer Sigmoid function resulted to poor model performance. 
#7.  Special care for deep networks

   Replace all activation sigmoid function with RELU ( Rectified Linear Unit ), and optimizer = 'sgd' with optimizer = 'adam'
    
   Result : 99% accuracy
    
    
#8 Learning rate decay 

   a. Increase the learning rate default value of 0.001 to 0.01 with an actual instance of Adam optimizer
      optimizer=tf.keras.optimizers.Adam(lr=0.01)
      
   b. Change the zoom factor from 1 to 5. Retrain the model and check the result.
      Result : The loss or training curve  is too bad like it is jumping from up to down.
      
   c. Implement a good solution using learning rate scheduler callback
   
   d. Add the lr_decay_callback to model.fit callbacks[plot_training, lr_decay_callback]. Retrain the model and check the result.
      Result: Accuracy is above 98% and noise in the data is gone.
   
#9 Dropout, overfitting

   a. Increase the depth of the model to at least 4 dense layers and retrain using the following number of neurons 200, 100, 60, 10.
   
   b. Bump the zoom factor to 10 in PlotTraining. Then retrain the model and check the result. Does it help? No
      Result: Accuracy is stuck to 98% and the validation loss goes up. It does not work on validation data and validation loss stops dropping and bounce up.
      This disconect from validation data is called overfitting the data. If this happens we need to apply dropout a regularization technique.
      
   c. Apply regularization techniques call dropout when training the data. Dont add after softmax layer because it will dropped the predicted probabilities.
      Then re-train the model. Check the results, Did it work. No. The accuracy went down to 75% which is not good and the validation loss is not going up but 
      still higher more with no droput thechnique.
      
#11. A convoultional network

   a.  Reshape back the imsges flattened vector into 28x28x1 images(1 channel for grayscale images)
   
   b.  Modify your model into a convolutional model. Remove the dropout. Flatten the curve into a vector so it can be consumed by dense layer.
   
   c.  Please bump up the zoom in PlotTraining to 16. Then retrain the model and run the prediction. Check the results of retraining model.
       Result: Accuracy is more than 99% which is pretty amazing but the validation loss is still going up(overfitting.
       The prediction shows only the 3rd and 6/9 of 4th rows were classified wrong and overfitting. 
       
 #12.  Dropout again
    a. Add a dropout layer between the two dense layers in your network. Use a drop rate of 40% (0.4)
       Retrain the model and check the result
       Result: Accuracy is 99% and the validation loss is not going up. Overfitting was fixed by dropout regularization technique.
       
 #13. Batch Normalization 
 
   a.  Modify each layer: remove the activation from the layer itself. Set use_bias=False
       The scale factor can be turned off for Relu activation. 
       Use the syntax tf.keras.layers.BatchNormalization(scale=False, center=True),
       Finish with the activation. Use the syntax tf.keras.layers.Activation('relu').
       
   b.  Change dropout rate to 0.3, learning rate decay parameter to 0.666, and BATCH_SIZE=64. 
        Retrain the model and check the result.
        Result: Accuracy achieved only 99.35% and the validation loss converge perfectly(not going up).
       
  #14. Train in the cloud on powerful hardware: AI Platform using this tutorial.
  
   https://github.com/GoogleCloudPlatform/tensorflow-without-a-phd/tree/master/tensorflow-mnist-tutorial/mlengine
      
   a. Created a Google Cloud Account and enable billing.
      
   b. Install the GCP command line tools see GCP link: https://cloud.google.com/sdk/docs/install#interactive
      
   c. Created a Google Cloud Storage bucket storage ( put in us-central1 ), it will be used to stage the training code.
      
   d. Enabled the API GCP AI Platform see link https://cloud.google.com/ai-platform/
      
   Result: Successfully submit the jobs with the runtime Tensorflow version 1.15. The current Tensorflow version 2.4 did not work. 
   
   See attached document for the complete documentation of this tutorial in the cloud. 
   
   https://github.com/jocelynbaduria/Assignment_1-part-1-assignment-1-part-2/blob/main/Jocelyn_Baduria_Assignment_part2_Train%20in%20the%20Cloud.docx
   
   
   
       
         
                   
  
      
      
