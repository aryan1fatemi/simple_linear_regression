# simple_linear_regression
This code demonstrates a simple linear regression model using the Salary_Data.csv dataset. Here's a breakdown of the code:

1. Importing the required libraries:
   - `numpy` for numerical operations.
   - `matplotlib.pyplot` for plotting.
   - `pandas` for data manipulation and analysis.

2. Importing the dataset:
   - The `Salary_Data.csv` file is read using `pd.read_csv` function and stored in the `dataset` variable.
   - The independent variable `X` is extracted from the dataset by selecting all columns except the last one.
   - The dependent variable `y` is extracted by selecting only the last column.

3. Splitting the dataset into training and test sets:
   - The `train_test_split` function from `sklearn.model_selection` is used to split the data into training and test sets.
   - `X_train`, `X_test` contain the independent variables for the training and test sets respectively.
   - `y_train`, `y_test` contain the corresponding dependent variables.

4. Training the simple linear regression model:
   - The `LinearRegression` class from `sklearn.linear_model` is imported.
   - An instance of the `LinearRegression` class is created and assigned to the `regressor` variable.
   - The `fit` method is called on the `regressor` object, passing the training data (`X_train`, `y_train`) to train the model.

5. Predicting the test set results:
   - The `predict` method is called on the `regressor` object, passing the test data (`X_test`) to make predictions.
   - The predicted values are stored in the `y_pred` variable.

6. Visualizing the training set results:
   - The training set data points are plotted as red scattered points using `plt.scatter`.
   - The regression line is plotted using `plt.plot`, with `X_train` as the x-axis values and the predicted salary values for `X_train` as the y-axis values.
   - Title, x-axis label, and y-axis label are set using `plt.title`, `plt.xlabel`, and `plt.ylabel` respectively.
   - The plot is displayed using `plt.show`.

7. Visualizing the test set results:
   - Similar to step 6, the test set data points are plotted as red scattered points.
   - The same regression line is plotted, but this time the x-axis values are `X_train`.
   - Title, x-axis label, and y-axis label are set as well.
   - The plot is displayed using `plt.show`.

These visualizations help understand the relationship between salary and years of experience, and how well the trained model fits the data points in the training and test sets.
