# deep-learning-challenge

Overview of the Analysis: The purpose of this analysis is to build a deep learning model using TensorFlow and Keras to predict whether applicants to a charitable organization will be successful if funded. The model utilizes a dataset containing various features about each application, such as application type, classification, and other attributes.

**Results:**

**Data Preprocessing:**

**Target Variable(s):**
* The target variable for the model is "IS_SUCCESSFUL," which indicates whether the applicant was   
  successful in receiving funding (1 for successful, 0 for unsuccessful).

**Variables to Remove:**

* The EIN and NAME column was removed from the first model while EIN was the only column removed from 
  the second model.

* In both models these were identifiers and not relevant for prediction.

![alt text](<Name Binning-1.png>)

**Model Features:**

* APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

**Compiling, Training, and Evaluating the Model:**

* Neurons, Layers, and Activation Functions:

*Model 1:* There were two hidden layers with varying numbers of neurons (80, 30) and ReLU activations 
           functions. 

*Model 2:* There were three hidden layers were used with varying numbers of neurons (7, 14, and 21) and ReLU activation functions. 

![alt text](hidden_layers-1.png)

*Models 1 and 2:* ReLU is chosen as it helps mitigate the vanishing gradient    problem and speeds up the training process.

The output layer consists of a single neuron with a sigmoid activation function, suitable for binary classification tasks.

**Target Model Performance:**

* The model's performance was evaluated using binary cross-entropy loss and accuracy metrics.

**Steps to Increase Model Performance:**

* Dropped only the EIN column vs EIN and Name 

* Binning with 100 vs 1000 for the classifications to be replaced

![alt text](classifications_to_replace-binning-1.png)

**Summary:** In my optimized model I was able to achieve a 78% accuracy rate vs in my first model. By changing the number of hidden layers I noticed a difference in the accuracy.
![alt text](<Optimization -1.png>)

The deep learning model was trained and evaluated for predicting the success of charitable funding applications. While the specific model performance metrics were not provided, further optimization may be required to achieve the target model performance. Additionally, exploring alternative architectures such as convolutional neural networks (CNNs) or recurrent neural networks (RNNs) could be beneficial, especially if there are sequential patterns or spatial dependencies in the data that these architectures can capture effectively.
