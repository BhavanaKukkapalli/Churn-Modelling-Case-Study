# ML Case Study on Churn Modelling Dataset
This case study analyzes the Churn Modelling dataset which contains information about customers of a bank. The objective is to build a model that can predict if a customer will leave the bank or not based on various features.

The analysis involves the following steps:

- Importing necessary libraries and loading the dataset.
- Exploratory Data Analysis (EDA) - Using box plots to detect outliers and correlation matrix to identify important features.
- Feature Preprocessing - Encoding categorical variables and scaling the data.
- Feature Selection - Using Chi-square test to select important features.
- Model Building - Building several models and evaluating their performance.

### Dataset
The Churn Modelling dataset contains 10000 rows and 14 columns. The columns are described as follows:

- RowNumber: Row number.
- CustomerId: Unique ID assigned to the customer.
- Surname: Customer's last name.
- CreditScore: Credit score of the customer.
- Geography: Customer's country of origin (France, Spain, or Germany).
- Gender: Customer's gender (Male or Female).
- Age: Age of the customer.
- Tenure: Number of years the customer has been with the bank.
- Balance: Bank balance of the customer.
- NumOfProducts: Number of bank products the customer has.
- HasCrCard: Does the customer have a credit card? (1 = Yes, 0 = No)
- IsActiveMember: Is the customer an active member? (1 = Yes, 0 = No)
- EstimatedSalary: Estimated salary of the customer.
- Exited: Did the customer leave the bank? (1 = Yes, 0 = No)

### Exploratory Data Analysis
Box plots were used to detect outliers in the continuous variables. The results are shown below:

Variable	No. of Outliers
CreditScore	15
Age	359
Tenure	0
Balance	0
NumOfProducts	60
HasCrCard	0
EstimatedSalary	0
Exited	2037

| Variable |  No. of Outliers  |
|:-----|:--------:|
| CreditScore   | 15 |
| Age   |  359  |
| Tenure   | 0 |
| Balance   | 0 |
| NumOfProducts   |  60  |
| HasCrCard   | 0 |
| EstimatedSalary   | 0 |
| Exited   |  2037  |


A correlation matrix was also used to identify important features. The result showed that the following features have a strong correlation with the target variable:

- Age
- NumOfProducts
- IsActiveMember

### Feature Preprocessing
Categorical variables (Geography and Gender) were encoded using label encoding and one-hot encoding. The continuous variables were then scaled using MinMaxScaler.

### Feature Selection
Chi-square test was used to select important features. The results showed that the following features were important:

- CreditScore
- Age
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary


### Model Building
Several models were built and evaluated based on their accuracy, ROC AUC score, and F1 score. The following models were used:

- Logistic Regression
- Naive Bayes
- SVM
- KNN

The performance of the models is shown below:

| Variable |  No. of Outliers  | Variable |  No. of Outliers  |
|:-----|:--------:|:-----|:--------:|
| Logistic Regression  | 0.811 | 0.597   | 0.330 |
| Naive Bayes   |  0.805  | 0.682   | 0.222 |
| SVM   | 0.865 | 0.622   | 0.458 |
| KNN   | 0.848 | 0.597   | 0.438 |

Based on the results, it can be concluded that SVM is the best model for this dataset.