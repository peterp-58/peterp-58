
Welcome to CIND 820 capstone project. This project is create a machine learning model that help predict bankrupcy. 
This model, based on working knowledge and financial expertise, will use financial ratios to determine if companies are bracing for bankrupcy. 
This will help stakeholders take actions before the company files for actual bankrupcy.
This process is cumulative in with respect to the coding, in datasetprep.ipyn. 

The files in the repository contain:
1. PDF of the code
2. "Attribute analysis" - this is my work that contains all the atttributes in the dataset. It contains a correlation of highly correlated features. This was used to analyze what made sense to me, financially, as well as, what is used in industry. There were mutlple attributes that had different meaning from CFA  and industry and were marked for removal. The list was narrowed from 77 to 32 features. It is currently in simple mode, but full mark up will show my comments on why the attributes were removed. 
3. "Why Company go Bankrupt" -this is my work on how i choose the attributres from the list from "attribute analysis". It came from trying to understand why a company will go bankrupt and narrowing the root causes, which were : 1. Failure of Business Strategy;2. Inefficient use of assets ; 3. Too much debt; 4. Not enough Cash flow. From here it was selecting the best attributes that will fit these 4 points. 

THe project is currently broken down to 7 subsections. 

1. Uploading and setting up the Polish Dataset
2. Variable Additions
3. Initial Descriptive Analysis
4. Approach
5. Preparing to model
6. Performance Metrics
7. Spliting Datasets into respective Years


Progress : 
As of July 2nd, an inital run of the models were performed with the features selected based on "why do companies go bankrupt". THe first run did not yield postive results, which 
leads me to move on to next phase, which is to split the datasets into the years. There are 5 years and i will split into 5 datasets. 

Based on inital review of the results. The confusion matrix shows that the models have missed a good chunk of the bankrupt companies. Logistic regression did not pick up any. 

The pdf, initial code provides a details to each of the steps above, except for #7, which will be the next phase to work on
