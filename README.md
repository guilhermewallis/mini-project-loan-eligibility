# Mini Project - Loan Eligibility

## Data Description
#### This dataset contains applicant data from a home loan company. It contains multiple kinds of information such as:
* Personal data - gender, marital status, education
* Finanacial data - income, employment type, credit history, etc
* Loan data - loan status (eligibility), amount, term, property area
#### It is a small dataset containing 614 entries over 13 columns, source file "Loan_Data.csv"

## Goal
#### The goal of this study is to automate the loan eligibility process based on customer details provided
* This model will have as a target the Loan Status column on the dataset, which contains the information of whether or not the existing applicants were eligible for the loan.
* To achieve this, a classification model will be built taking in the several different features contained in the dataset.



## Data Exploration
#### Analyzing the dataset's features
* The dataset is small containing only 614 rows and 13 columns but fairly clean and most of it useble in the model
* most applications are submitted by a single applicant while a few contain a co-applicant
* most loand have a term of **360 months or 30 years**
* **By a large ratio**, most applicants are **male, have a credit history, are graduates and not self-employed**
* 2 for every 1 applicants are married
* **Applicants are mostly equaly distributed by property area**


#### Analyzing relationships amongst features and against the target.
* **Data shows that the amount loaned to the applicant somewhat takes into account their level of income**.
* there is some correlation between the applicant having a credit history and getting the approval on the loan.
* **Semiurban properties have a higher loan approval rate of 76.8%** compared to urban and rural properties at 65.8% and 61% respectively
* Married applicants at a higher rate of approval vs. not married
* Graduate applicants at a higher rate of approval vs. non-graduates

#### The dataset is imbalanced towards the value Y in target feature: most applicants get approval for the loan.
* Attempts to balance the dataset through resampling were considered and tested and scaling tecniques were tested with the model.

## Results
#### LogisticRegression is the preferred model for this problem.
* Best results (confusion matrix):
    * 0.14 / 0.12
    * 0.00 / 0.74
    * classification score of 0.87
* **Overall the application of this ML model fulfills the proposed objective of predicting the eligibility of an applicant for a loan**