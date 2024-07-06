This project is about predicting the transportation style used by people using multiclass (ternary) classification.

Importing important libraries used in the project like pandas, numpy, tensorflow. And from tensorflow, imported Dense, Sequential. And from sklearn.metrices, imported confusion matrix and f1 score. 

Preprocessing: 
  Dropping the irrelevant columns based on the number of distinct values for each feature. And then filling the null values of each column with mode values of that column. Since, I am going to use neural networks with tensorflow, and some features are categorical so, I need to convert them to numbers so that efficient model can be built. To  handle categorical variables and converting them to binary features, I have used one-hot encoding technique. One-hot encoding converts each categorical value to new binary feature where only one of the possible categories is represented by true, and the rest are represented by false.

Training the model: 
  First I have set a seed for tensorflow so that the results are reproducible.
  Then creating a sequential model of 5 layers with some number of neurons with activation function for each layer is linear. Then compiling the model using loss function SparseCategoricalCrossentropy which is used since output labels are integers and also from logits = true to internally pass the model's ouptut through softmax function. Learning rate is set to 0.01.
  Then model is fitted with epochs = 50. An epoch means one pass through entire dataset during training. 

Testing the model: 
  I have implemented forward propogation using dense and sequential function to test the performance of the model on the testing dataset. Finally we get weighted average F1 score is approximately 0.64 .
