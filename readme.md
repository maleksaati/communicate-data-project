# Prosper Loan Exploration¶
## by Abdulmalek Alsaati

## Intro

> Prosper Marketplace is America's first peer-to-peer lending marketplace, with over $7 billion in funded loans. Borrowers request personal loans on Prosper and investors (individual or institutional) can fund anywhere from $2,000 to $40,000 per loan request. Investors can consider borrowers’ credit scores, ratings, and histories and the category of the loan. Prosper handles the servicing of the loan and collects and distributes borrower payments and interest back to the loan investors.
please refer to : https://en.wikipedia.org/wiki/Prosper_Marketplace for more info.


## Dataset

>The data set that has been analysed contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (interest rate), current loan status, borrower income, borrower employment status and many other features.
The variable that will be explored in this analysis are only 16.

The dataset can be download from udacity website from the following link  
https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv

and the feature documentation available from the following link: 
https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit


## Summary of Findings

> this exploration has devided into Univariate Exploration, Bivariate Exploration and Multivariate Exploration

> the numerical dataset variables which is used are:
. LoanOriginalAmount
. EstimatedReturn
. BorrowerAPR
. BorrowerRate
. StatedMonthlyIncome

> and the categorical variables are :
. Term
. EmploymentStatus
. ProsperRating (Alpha)
. LoanOriginationDate

> this analysis is trying to figuring out the Estemated Return and what variable that affect on it like the Original Loan Amount, Prosper Score and Employment status.

> The result taht extracted from the first part of this exploration (Univariate Exploration):
1-  the distribution of LoanOriginalAmount shows most loan amount are derived from 5k values , and 5k is most frequent loan amount, then 15k and 10k
2- the distribution of Estimated Return shows most of the loans have an estimated return between 4% and 20%, and there is peak point at 8% and 12%, if we zoom estimated Loss, also there is Loss distribution between -17% to 1%, top loss frequency is -2.5% and -5%.
3- The Borrower APR range from 0.1 to 0.4, most frequencies for Borrower APR is 35%, there is slightly difference between Interest Rate and Borrower APR, since borrower APR is always more that intrest rate.
4 - The StatedMonthlyIncome is highly right skewed, so the chart scale has been limited get more clear picture, the most frequent monthly income is 5000.
5- the most loan term (more than 75%) is 36 months (3 years) , and less people take loan for five year (less than 25%).
6- Most of the Borrowers are Employed (60%), and Full-time (23.6%).
7- Most frequent Prosper Score by order are C, B , A and D.

> the second part (Bivariate Exploration) shows that:
1- the paired scatter plots shows poorly correlation between vairables like ( Estimated Return and Loan Origainal Amount). Also it shows a positive correlation between BorrowerAPR and EstematedReturn.
2- the scatter plot for estimated return and Original Loan Amount shows negative correlation , as the Loan Original amount increase, the estimated return is decrease. The second plot shows that most density (dark blue areas) is for Loan Amount (5k) with estimated return 10%, also there is less density for loan Amount 15K and 10% with same estimated return 5%.
3- the violin plot shows the relation between employement status and Loan Amount, the chart shows the mean for loans are 5K, there is more verities in values for (self-employed and Employeed) borrowers as thhere is density of value in 10k and 15k. Also for employed borrower, the mean is differ than other borrowers and it's 10K.
4 - the clustered bar chart shows that most frequent loan term for employed and full-time borrower is 3 years, also for employed borrower, the next frequent Loan Amount is 5 years.
5- the heat map shows most frequent completed Loan is for Employed Borrowers, and Full-time.
6- the point plot shows that even though the Loan Amount has decreased from 2011 to 2014 , the standard deviation for the return has decreased also, which reflect more safe Loan investment.
7- the box plot suggests that investing in borrowers with proser Class D and E will produce the highest returns. but this need more exploration as it might combined with higher risk.

> the final part of this project (Multivariate Exploration) conclude that:
1 - How monthly payment is derived from Loan Amount and Interest rate, a larger payment are linked to larger loan amount and lower interest rate.
2- Each Prosper rating is group with specific return, there is lot of vaiabilities for High risk borrower and there is chance for mony loss. Also it suggest a safe range borrower classes which are (AA, A and B), the classes (C and D) are linked to higher return but also linked to small chance of mony losss. In addition it suggest borrwing limit for each classes, which to invist more in safe classes, but less in risky classes.
 
## Key Insights for Presentation

> For the presentation, I just focus on features that could affect the estimated Return, which are original loan amount, Prosper rating, Loan Status and employement status. I started by showing the distribution of estimated return and estimated loss. Then, I showed the relationship between Loan Status vs. Employenment Status for the borrower and focus on completed loan status, this give insight what employement status to choose when invisting. Then I show the affect of Prosper Rating on estimated Return.  Finally I have consider Loan amount with Prosper rating to figure out what prosper rating should be consider and what Loan Amount limited for each prosper group.
