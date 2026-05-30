*Building an ML Model with neural networks*

This project was aimed at predicting the students' scores based on the features of study hours, sleep hours, attendance, assignments and previous test scores.
This project was approached using the regression model and building a neural network to train the model.

The reason ML was suitable for this problem is that a good number of features with predictive power could be identified. For predicting the score of a fair examination, the amount of effort put in and the past performance of the students were relevant metrics. Regression was a suitable model to predict the numerical value of the score of the student in percentage.

MY APPROACH TO THE PROBLEM AND ITS PERFORMANCE
Preprocessing Steps:
-	The data available in the CSV format was first converted to pandas data frames to filter the relevant columns from the data as features and labels.
-	The features were normalised using a simple Z-score scaling, and the labels were left as they were.
-	The data frames were converted to NumPy arrays to split the data as 60% for training, 20% for validation and the remaining 20% as testing.
-	Then the NumPy arrays were converted to PyTorch tensors to use them in the neural networks.

Training Steps:
-	A class was defined for the neural network using the nn module from PyTorch, with two hidden layers (later tweaked to three to improve performance). The ReLU function was applied to capture nonlinearity. A dropout of 0.05 was used to regularise the model.
-	A loss function of Mean Squared Error was used in the model.
-	SGD was initially used to calculate the gradient descent and later optimised to Adam.
-	Hyperparameters like learning rate and number of epochs were initialised. (these parameters were continuously tweaked throughout each training process to find the optimum model)
-	The model was trained by sending the predictions forward and backpropagating the losses.

Testing the results:
-	The testing data was tested against our model prediction to find out the loss.
-	Mean Absolute Error, Mean Squared Error and the R – squared were measured, and a scatter plot of predictions and true values was plotted.

Results:

Loss Function plot
<img width="754" height="522" alt="image" src="https://github.com/user-attachments/assets/04ef3eef-988d-4828-91dc-f5c53b3dad40" />

Performance
<img width="952" height="746" alt="image" src="https://github.com/user-attachments/assets/07c12b64-1915-4a2d-9b57-430358d1c6fa" />




