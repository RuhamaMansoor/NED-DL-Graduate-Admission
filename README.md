# Graduation Admission Prediction Model

## Steps Involved:

### 1. Data Loading and Preprocessing
- The data is loaded using `pandas`, and it contains 500 rows and 9 columns.
- The `Serial No.` column is dropped since it doesn't affect predictions.
- Features are split into `x` (input features) and `y` (target variable `Chance of Admit`).
- The dataset is split into training (80%) and testing (20%) sets using `train_test_split`.

### 2. Scaling the Data
- The input features are scaled using the `MinMaxScaler` to ensure all values fall between 0 and 1. This helps in faster convergence during training.

### 3. Building the Neural Network Model
- A simple neural network with 3 layers is created using TensorFlow's Keras API.
  - The first and second layers are fully connected (`Dense`) layers with 7 nodes and `ReLU` activation.
  - The final layer is a single node with a `linear` activation function to predict the chance of admission.
- The model is compiled with the `Adam` optimizer and `mean_squared_error` loss function.

### 4. Training the Model
- The model is trained using the scaled training data for 500 epochs, and the progress is monitored using a validation split of 20%.
- After training, the model achieves a good performance with an **R² score of 0.81**, meaning it can explain around 81% of the variance in the test data.

### 5. Plotting the Loss
- The loss and validation loss during the training process are plotted to check how well the model learns over time.

## How to Run the Code

1. Install the required libraries:
   ```bash
   pip install pandas scikit-learn tensorflow matplotlib
   ```
2. Load your dataset and run the code cell by cell to preprocess, train, and evaluate the model.

## Conclusion

This project demonstrates how to build a simple neural network model to predict the chances of admission to graduate school using a dataset with relevant academic and research features.

