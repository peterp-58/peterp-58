
Welcome to CIND 820 capstone project. This project is create a machine learning model that help predict bankrupcy. 
This model, based on working knowledge and financial expertise, will use financial ratios to determine if companies are bracing for bankrupcy. 
This will help stakeholders take actions before the company files for actual bankrupcy.
This process is cumulative in with respect to the coding, in datasetprep.ipyn. 

The files in the repository contain:
1. PDF of the code
2. "Attribute analysis" - this is my work that contains all the atttributes in the dataset. It contains a correlation of highly correlated features. This was used to analyze what made sense to me, financially, as well as, what is used in industry. There were mutlple attributes that had different meaning from CFA  and industry and were marked for removal. The list was narrowed from 77 to 32 features. It is currently in simple mode, but full mark up will show my comments on why the attributes were removed. 
3. "Why Company go Bankrupt" -this is my work on how i choose the attributres from the list from "attribute analysis". It came from trying to understand why a company will go bankrupt and narrowing the root causes, which were : 1. Failure of Business Strategy;2. Inefficient use of assets ; 3. Too much debt; 4. Not enough Cash flow. From here it was selecting the best attributes that will fit these 4 points. 

THe project is currently broken down to 9 subsections. 

1. Uploading and setting up the Polish Dataset
2. Variable Additions
3. Initial Descriptive Analysis
4. Approach
5. Spliting Datasets into respective Years+
6. Preparing to model
8. Models
9. Performance Metrics



Progress : 
As of July 22nd, (CIND820_PP_BankrupcyV7) was used as the final result. The additions changed to the last update was the addition of performance metrics, Precision, Recall, False Postive Rate, False Negative Rate, F1 score  and Precision/Recall AUC  . One feature selection for all years. The reason is to build a model that can be applied to any situtions. 


THe code was also changed to show the true postive as 1, instead of 0, hence Specificity was no longer used. 

ALthough more performance metrics were added, I only focused on the Precion, Recall and F1 Score, as i believed these are suitable for different stakeholders: 
Precison: If the stakeholder is a rating agency, they would need a more balanced approach. They would want to ensure that both Precision and Recall are minimized, hence the F1 Score is important in this case, as it takes a harmonic average of both precision and recall.
Recall: an asset management firm, could utilize this model to avoid investing or holding bankrupt companies in their portfolios. A false negative to this stakeholder can lead to monetary loss, so having a high recall is beneficial to this stakeholder.
F1 Score: If the stakeholder is a bank, then Precision would be more important, as a bank would want to limit the amount of false positives, to maximize loan growth and revenue. 

To conclude, based on performance metrics of the three, the following models are the best predictors: 

-	Precision: Random Forest  
-	Recall: Logistic Regression 
-	F1 Score: Gradient Boost 

For the undersampling and over sampling, the impact of either use case was non-existing in the ensemble models. For Logistic Regression, there was a very small impact, with both varing by early. However for the recall test, the Undersampling faired better for Year 4 and Year 5. 

As of July 7th,(CIND820_PP_Bankrupcyv5)  the dataset was broken into their respective years. Before prepare the data for analysis, I've added features that would help determine bankrupcy in companies. Using the existing data, I created new ratios, such as Financial Leverage, Cash to Interest etc. In preparation of which features to select, I examined their signaficances and importance using logistic regression test and random forest. Both test provided a top 10 and based on knowledge, I chose random forest, as they resembled closly to the the objective of "why companies go bankrupt", as well as the features are not highly correlated with one another. To add, both test did result in similar features. i did choose to run a  non-parametric test as all the features are not normally distributed, however the final features selectation that was given were highly correlated with one another and determiend it was not adquate to be selected. 

This was done for each year and each year has different features. A few features are common accross the years, which will be investigated before the project is finsihed. 

I did run the datesets using only one set of features accross all the years, however the peformance was not as good, as individually selecting the features for each year. 

At this point, the Adaboost is currently showing the best results for specificity. 


