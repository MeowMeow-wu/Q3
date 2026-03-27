# Q3
Q3 (a) Identify input features and target variable.

Input Features (Independent Variables): These are the variables that you will use to predict or explain the target variable. In this dataset, the input features are the pieces of information that would be available before a student's final result is known.

attendance
assignment
quizzes


Target Variable (Dependent Variable): This is the variable you are trying to predict or understand. It's the outcome you're interested in.

final result




Q3 (b) Describe TWO preprocessing steps and explain their purpose.
Data preprocessing is crucial to clean and prepare your data for machine learning algorithms. Here are two common steps:

Handling Missing Values:

Description: Many datasets have missing values (represented as NaN, None, or empty cells). This step involves identifying these missing values and deciding how to treat them. Common strategies include:
Imputation: Replacing missing values with a calculated statistic (e.g., the mean, median, or mode of the column).
Deletion: Removing rows or columns that contain missing values (use with caution, as it can lead to data loss).


Purpose: Machine learning algorithms generally cannot handle missing values directly. Imputing or removing them ensures that the data is complete and can be processed by the algorithms, preventing errors and improving model performance. For example, if a student has a missing assignment score, we might impute it with the average assignment score of other students to avoid discarding that student's entire record.


Feature Scaling:

Description: This involves transforming the numerical features so that they are on a similar scale. Two common methods are:
Standardization (Z-score normalization): Transforms data to have a mean of 0 and a standard deviation of 1. The formula is z=σx−μ​, where x is the original value, μ is the mean, and σ is the standard deviation.
Normalization (Min-Max scaling): Scales data to a fixed range, usually between 0 and 1. The formula is xscaled​=xmax​−xmin​x−xmin​​.


Purpose: Many machine learning algorithms (like Support Vector Machines, K-Nearest Neighbors, and gradient descent-based algorithms) are sensitive to the scale of input features. Features with larger ranges can disproportionately influence the model. Feature scaling ensures that all features contribute equally to the model's learning process, leading to better performance and faster convergence. For instance, if attendance is on a scale of 0-100 and assignment scores are on a scale of 0-10, the attendance feature might dominate the model without scaling.




Q3 (c) Identify ONE pattern from the dataset.
Based on the typical relationships in student performance data, here's a likely pattern:

Pattern: There is a positive correlation between the input features (attendance, assignment scores, quiz scores) and the final result.
Explanation: Students who have higher attendance rates, better assignment scores, and higher quiz scores are likely to achieve a better final result. Conversely, lower performance in these areas would likely lead to a lower final result. This is because attendance, assignments, and quizzes are designed to measure and reinforce learning, directly contributing to the overall understanding and performance reflected in the final result.




Q3 (d) Suggest ONE suitable evaluation metric and justify.
The choice of evaluation metric depends on the nature of the final result variable. Assuming the final result is a categorical variable (e.g., 'Pass', 'Fail', 'Distinction' or letter grades like 'A', 'B', 'C'), then a suitable metric would be Accuracy.

Evaluation Metric: Accuracy
Justification:
Definition: Accuracy is the proportion of correct predictions made by the model out of the total number of predictions.Accuracy=Total Number of PredictionsNumber of Correct Predictions​
Suitability: If the goal is to simply predict whether a student will pass or fail, or to classify them into a grade category, accuracy provides a straightforward measure of how often the model gets the prediction right. It's easy to understand and interpret.
When it's most suitable: Accuracy is a good choice when the classes (e.g., 'Pass' and 'Fail') are roughly balanced in the dataset. If there's a significant imbalance (e.g., 95% pass, 5% fail), accuracy alone might be misleading, and metrics like Precision, Recall, or F1-score might be more informative. However, for a general classification task on a balanced dataset, accuracy is a solid starting point.
