# Credit-Card-Transaction-Fraud-Supervised
Credit card fraud is a burden for organizations across 
the globe. United States is the most credit card fraud 
prone country in the world. According to Federal 
Trade Commission’s (FTC), instances of credit card 
fraud in the US increased by 44.6% from 271,927 in 
2019 to 393,207 in 2020 which resulted in a loss of 
approximately 3.3 billion dollars. Credit card fraud 
also accounted for 393,207 of the nearly 1.4 million 
(~28.08%) reports of identity thefts in 2020. Through 
this report, our goal was to build and highlight efficient 
model to predict fraud. We analyzed a real-world 
dataset that contained a list of government related 
credit card transactions over the 2010 calendar year. 
The data presented a supervised problem as it 
included a labeled input “Fraud” which indicated if a
particular transaction is fraudulent or not. The dataset contained identifying information about 
each transaction such as the credit card number, merchant, merchant state, etc. The dataset had 
96,753 records and 10 data fields. We performed exploratory data analysis and visualized each 
of the 10 data fields, cleaned the dataset, and imputed missing values. Then we created 1000+ 
candidate variables and performed feature selection. Finally, we created a variety of models using 
several algorithms (both linear and nonlinear) and highlighted our results. 
Through our data analysis, we found there are nine categorical variables and one numeric 
variable. We provided a histogram or table for each data field to better understand its distribution.
Many of the variables had a right skewed distribution. Overall, the dataset had 1,059 fraudulent 
transactions of the total 96,753 records (1.09%). The dataset required cleaning before we could 
move to the variable creation phase. We removed one outlier record due to its extremely high 
value. Also, we only analyzed records that had a transaction type equal to “P” (purchase) to work 
with a more focused dataset. Lastly, the “Merchnum”, “Merch state”, and “Merch zip” data fields 
contained missing values which required careful data imputation.
Once the dataset was cleaned, we attempted to create as many candidate variables as possible 
(amount variables, frequency variables, days-since variables, velocity change variables, 
Benford’s Law variables, and a day-of-the-week risk table variable.) After the variable creation 
process, we performed feature selection via filter and wrapper methods to reduce dimensionality
and determine the best variables for use in the development of machine learning models to predict 
potentially fraudulent activity. Kolmogorov-Smirnov (KS) and Fraud Detection Rate (FDR) at 3% 
were used to eliminate effective variables as a filtering method, while the average results of three 
different tree-based methods was used as our wrapper method. Once the final variables were 
chosen, the data was divided into three sections for model development and analysis: training, 
testing, and out-of-time (OOT). 
To find the best model, the variables were tested in several different models. First, we started 
with a baseline model Logistic regression. Next, we explored multiple nonlinear models such as 
Random Forest, Boosted Trees, and Neural Network to compare against the Logistic regression 
model. Parameter tuning was also performed on each model to get better results. Overall, our 
best model was Light Gradient Boosting which caught 55.86% fraud at a 3% FDR after 
hyperparameter tuning.
