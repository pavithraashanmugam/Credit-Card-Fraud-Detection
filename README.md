### Description of the Workflow

This workflow is designed to predict whether a credit card transaction is legitimate or fraudulent using a Logistic Regression model. Below is an outline of the steps involved:

1. **Data Import and Loading**:
   - The dataset containing credit card transactions is loaded into a pandas dataframe from a CSV file.
   - The dataset consists of 31 columns, which include various features related to the transaction such as time, transaction amount, and multiple variables labeled as V1, V2, ..., V28.

2. **Exploratory Data Analysis**:
   - We inspect the dataset's shape and preview the first and last few rows to get a better understanding of the data.
   - A check is performed for missing values, which reveals that there are no missing values in the dataset.
   - The distribution of legitimate (Class 0) and fraudulent (Class 1) transactions is explored, showing a highly imbalanced dataset with a very small number of fraudulent transactions.

3. **Data Processing**:
   - The dataset is divided into two groups: `legit` (legitimate transactions) and `fraud` (fraudulent transactions). 
   - Statistical analysis is performed on the transaction amounts for both types of transactions to understand the differences in spending behavior between legitimate and fraudulent transactions.
   - The dataset is further processed by under-sampling the majority class (legitimate transactions) to balance the dataset, ensuring a fair representation of both classes in the model.

4. **Data Preparation for Modeling**:
   - A random sample of 492 legitimate transactions is taken to match the number of fraudulent transactions.
   - The two groups (legit and fraud) are then combined into a new dataset that is balanced, having 492 legitimate and 492 fraudulent transactions.

5. **Model Training**:
   - The dataset is split into features (X) and labels (Y), where 'Class' is the label, indicating whether the transaction is legitimate or fraudulent.
   - The dataset is further divided into training and testing subsets for model validation.
   - A Logistic Regression model is trained using the training data.

6. **Model Evaluation**:
   - The model is evaluated using the testing subset.
   - The **accuracy score** on the **training data** is computed to assess how well the model fits the training set.
   - The **accuracy score** on the **testing data** is computed to assess the model's performance on unseen data.

   **Highlighted Accuracy Scores**:
   - **Training Accuracy Score**: The accuracy score on the training data is **94.4%**.
   - **Testing Accuracy Score**: The accuracy score on the testing data is **94.9%**.

   These accuracy scores provide insight into how well the model is performing both during training and when tested on new, unseen data. A high accuracy score on both the training and testing datasets suggests that the model generalizes well.

7. **Outcome**:
   - The model provides a prediction for new, unseen data, outputting whether a transaction is likely to be legitimate or fraudulent.

