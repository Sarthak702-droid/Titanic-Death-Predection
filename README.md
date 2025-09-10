Titanic Survival Prediction Project

This project aims to predict the survival of passengers on the Titanic using a logistic regression model. The analysis involves exploring the dataset, handling missing values and outliers, performing feature engineering, and training a machine learning model to predict survival probability.

📊 Data Exploration and Analysis

The project begins with a comprehensive analysis of the Titanic dataset to understand its structure and content. Key steps include:

    Initial Data Inspection: We check for the shape of the dataset, missing values, and duplicate entries. A number of columns, including gender, family, fare, and embarked, had missing values, which were handled by dropping the corresponding rows.

    Data Cleaning and Preprocessing: The age column, which contained some non-numeric values, was converted to a numeric type, with missing values imputed using the mean age. The date and fare columns were also converted to appropriate data types.

    Exploratory Data Analysis (EDA): The analysis includes various visualizations to understand the distribution of key features and their relationship with survival:

        Survival Distribution: A bar chart shows the distribution of survivors and non-survivors, indicating that more passengers did not survive than did.

        Age Distribution: A histogram of the age column reveals the frequency of different age groups among the passengers.

        Embarked Distribution: A count plot visualizes the number of passengers who embarked from each port (C, Q, and S).

        Pair Plots: Pair plots of numerical features and a pair plot with survived as a hue were used to visualize relationships between variables.

        Outlier Detection: Box plots were used to identify and handle outliers in numerical columns like fare. The Interquartile Range (IQR) method was applied to remove these outliers, leading to a cleaner dataset.

🛠️ Feature Engineering and Modeling

To prepare the data for the machine learning model, the following steps were performed:

    Label Encoding: The categorical gender column was converted into a numerical format (0 for female, 1 for male) using LabelEncoder.

    One-Hot Encoding: The embarked column was one-hot encoded to create separate binary columns (embarked_Q and embarked_S), which the model can interpret.

    Model Training: A Logistic Regression model was chosen for its interpretability and effectiveness in binary classification tasks. The data was split into training and testing sets (80% training, 20% testing) to evaluate the model's performance on unseen data. The model was trained using the preprocessed data, excluding the date column, which is not relevant for prediction.

📈 Model Evaluation and Results

The performance of the trained model was evaluated using several key metrics:

    Accuracy: The model achieved an accuracy of approximately 76.9% on the test set.

    Confusion Matrix: A heatmap of the confusion matrix provides a clear visual breakdown of true positives, true negatives, false positives, and false negatives.

    Classification Report: The classification report provides detailed metrics for precision, recall, and F1-score for both survival classes (survived and not survived). A bar plot was generated to visualize these metrics.

    Probability Distribution: A scatter plot shows the relationship between the actual survival status and the predicted survival probability, giving insight into the model's confidence in its predictions.

🚀 Live Demo

A user-friendly interface was built using the Gradio library, allowing users to input passenger details and get a real-time prediction of their survival probability. The interface accepts the following inputs: Serial Number, Passenger Class, Gender, Age, Number of Family Members, Fare, and the Embarkation Port.

<img width="1872" height="878" alt="image" src="https://github.com/user-attachments/assets/0abe8846-781b-44f5-90fc-ad699469afe3" />
