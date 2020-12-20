# Prosper loan data exploration


## Dataset

This project explores Prosper Loans dataset as part of the Udacity's Data Analytics Nanogegree. The original dataset consisted of 81 columns and 113937 loan listings. The dataset contains many interesting variables, however, for the purpose of this project my main interest is to find features that could help to predict if the debtors will be able keep their loan obligations or the loan will become default or charged off. 

The original data can be found here https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv, and the Prosper Data Dictionary that explains the dataset's variables can be found here https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv.

The reasoning for deletion of some columns in advance: 
According to Investopedia, the factors considered in the ability to repay a loan include the borrower's income, employment status, liabilities, credit history, and the debt-to-income ratio Source. In addition, I thought the credit rating, and ListingCategory could be interesting variables to look into. I studied the contains of each variable in the Prosper dictionary, and based on this dropped some columns that either were redundant (duplicate information), or irrelevant to the purpose of the exploration. In the end I was able to run the notebook with 30 columns and 113937 rows in the dataset. 

The reason I chose this dataset is that I wanted to remind myself on the financial topic loans. 

## Summary of Findings

In the exploration I investigated the relationships between a predictor variables; grouped on their characteristics to liabilities, features of the loan, borrowers income, employment status, credit rating, and credit history; and the dependent variable loan status.

Within the data, around 71% of the loans are completed and 29% are defaulted, and most common credit rating within the borrowers is credit rating D. The combined credit score variable 'RatingCombined' turned out as one of the most powerful variables predict the outcome of the loan. We could establish that the worse the credit rating, the higher chance the loan had to default, and vice verca. The Prosper Rating and the previous outsourced rating Prosper used before year 2009 proofed themselves as very efficient scoring systems. 

We could also establish the roles of BorrowerRate, stated monthly income, current and historical delinquencies in the outcome of the loan as well as their connection to the credit rating. We found out that as the credit rating decreased the interest rate increased and that defaulted loans had up to credit rating from AA to C higher interest rates than completed loans, but at lower credit rating levels the differences became less obvious.

We also found out in the relationship between stated monthly income, credit rating and loan status, that monthly income decreased as the credit rating got worse. We could also see that the borrowers whose loans defaulted had lower income levels than the borrowers whose loans were completed.

Current delinquencies plotted against credit rating and loan status, showed that borrowers with completed loans had almost no delinquencies up to credit rating of level D, and in level E around twice less, and level HR almost thrice less delinquencies than defaulted loans.

Delinquencies from last 7 years plotted against credit rating and loan status on the other hand illustrated that borrowers with credit rating AA and A had no historical delinquencies in both loan statuses, and that the delinquencies increased for both loan status groupes in stable manner from credit rating B to credit rating HR, defaulted loans having higher numbers of delinquencies than completed loans.


## Key Insights for Presentation

For the presentation, I will focus on just the influence of credit rating to the loan status. I will start by introducing the distribution of the loan statuses defaulted and completed in the dataset.

After this I will introduce the different credit ratings and their distribution in the data using a countplot. 

Next step will plot introduce the found strong relationship between the credit rating and loan status by plotting the proportions in a barplot. I will also give an example of the percentages of the defaulted loans in the worst and the best credit rating category. 

In the final slide I will introduce the interaction effect visible between Loan status, borrower interest rate and the credit rating. The plot will illustrate how the interest rates are increasing as the credit rates are increasing as well as how the interest rates are higher for the loans with worse credit rating.  
