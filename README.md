Climate Data Regression Model

Description: This dataset provides climate statistics and is suitable for regression tasks such as predicting future temperatures or analyzing climate patterns.
This project builds a regression model to predict climate-related metrics (e.g., average temperature) using the Climate Data from Hugging Face. The dataset is preprocessed and split into training and test sets, and the model is built using TensorFlow/Keras.

Dataset: Hugging Face - Climate Data
Features: Multiple climate-related metrics such as year, month, day, and other environmental data.
Target: Average temperature (avg_temp).
The dataset is loaded, split into training and test sets, and preprocessed before training the model.

Model
The model is a neural network built with TensorFlow/Keras that uses climate data features to predict average temperature. The architecture is as follows:

Input Layer: Climate data features (e.g., year, month, environmental data).
Hidden Layers: Dense layers with ReLU activation.
Output Layer: Single neuron for regression output (average temperature).

Preprocessing
Load Climate Data: The dataset is loaded from Hugging Face using the datasets library.
Handle Missing Data: Missing values (NaN) are handled by filling them with the mean of the respective column.
Feature-Target Split: The features (independent variables) and target (dependent variable - avg_temp) are separated.
Train-Test Split: The dataset is split into training (80%) and testing (20%) sets using train_test_split from sklearn.
Normalization: The data is normalized using StandardScaler to ensure better performance during model training.

Training
The neural network model is trained using the normalized data. Key steps include:

Optimizer: Adam with a learning rate of 0.0001.
Loss Function: Mean Squared Error (mse) for regression.
Metrics: Mean Absolute Error (mae).
Validation Split: 20% of the training data is used for validation during training.

Evaluation
The model is evaluated on the test set, and the following metrics are recorded:

Mean Absolute Error (MAE): The average of the absolute errors between predicted and actual values.
Mean Squared Error (MSE): The average of the squared differences between predicted and actual values.

Results
The performance of the model on the test data is displayed after training, providing insights into how well the model predicts average temperature.
