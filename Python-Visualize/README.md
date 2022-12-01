# Data exploration (Prosper loan dataset)
## by (Duc Truong)


## Dataset

> The Prosper Loan dataset contains 113,937 rows of information of loans with 81 variables on each loan. To serve the purpose of this investigation, I choose to keep the following variables in a new table named main_table: Term, LoanStatus, BorrowerRate, ProsperRating (Alpha), ListingCategory (numeric), EmploymentStatus, DelinquenciesLast7Years, StatedMonthlyIncome, TotalProsperLoans, LoanOriginalAmount, LoanOriginationDate, Recommendations, Investors.


## Summary of Findings

- Most of the loans in dataset are current loans. Loans that are past due are divided into smaller group based on their duration. The defaulted loan (my feature of interest in this dataset) only takes a small proportion of all types of loan status.
- A vast majority of borrowers are Employed. Coming next are Full-time and Self-employed.
- The distribution of StatedMonthlyIncome has skew to the right problem.
- Using Three-Sigma Limit, the stated monthly income is still pretty skewed to the right. Mode (the most frequent value) is around 5000.
- The most frequent rating in both completed and defaulted loans is D
- The Debt Consolidation is the most frequent value in ListingCategory column
- For all rating scores, Employed is the largest group. The Not employed, Self-employed, Retired and Part-time groups have higher counts in rating HR, D, and E than high ratings.
- For defaulted loans, the loan original amount is smaller than completed loans. Most of the loans have the original amount of around 5000-8000$.
- D rating is the most frequent value in any listing categories. Defaulted loans appear more frequently in HR, D, and E ratings.
- All defaulted loans have the maximum loan original amount of 25000. While completed loans have higher range of loan amount, the defaulted loans have higher density in the range of 5000-15000$
- The borrowers who have defaulted loans tend to have lower income than the ones who have completed loans




## Key Insights for Presentation

> There are 2 main threads for presentation after exploring the data
- Default loans have some certain patterns of borrowers. These borrowers tend to borrow more money than the ones with completed loans. However, the defaulted loan owners never borrow more than 25000$. Plus, defaulted loan owners tend to have lower income than completed loan owners. These insights are revealed by using boxplot to see the distribution of LoanOriginalAmount and StatedMonthlyIncome, thus I can make the comparison between Defaulted and Completed group.
- There are some factors of borrowers that affect Prosper Rating. Most of the borrowers are in Employed group. Not employed, Self-employed, Retired and Part-time groups tend to have low ratings, as their income may not be high enough to pay loans. Most of the borrowers also list their loans for Debt Consolidation. These insights are proven by bar charts, to see the number of borrowers in each group of EmploymentStatus and ListingCategory. 
