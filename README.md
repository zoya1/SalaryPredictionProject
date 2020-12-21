# Salary Prediction Portfolio
### Salary Predictions on job postings

<img src = "Images/Image%201.jpg" >


<img src = "Images/Predicted%20vs%20observed.PNG" >








      

### Define problem
Organization's fair and well balanced pay structure is one of the top priority for any prospective employee. Good organizations often offer competitive salary and retain well trained employees for years which is more productive than paying less and  keeping  up with high turn over rates of employees who would leave the company for the reason of salary. Salary prediction is an important tool not only for HR department to offer fair salary to potential hires but also to job seekers in making more informed decisions.

In this portfolio project, model was built using provided datasets with 1 million jobpostings (train_features.csv and train_salaries.csv) predicted salaries for 1 million job postings listed in test_features.csv. This analysis does not include deployment process.

### Data Collection
Following were the datasets provided.

* train_features.csv: One million job advertisements. Each row represented metadata for an individual job posting. The job Id column represented a unique identifier for the job posting. The remaining columns described features of the job posting.

* train_salaries.csv: Each row provided corresponding salaries for the jobposting data in train_features.csv.

* test_features.csv: This is similar to train_features.csv, each row represented metadata for an individual job posting.

Testing and training datasets were loaded into pandas dataframes. Both the datasets had identical formats.


<img src = "Images/train%20test%20dataset.PNG" >


<img src = "Images/train%20salary.PNG" >


### Clean Data 

These datasets were clean. Dataset 
 * Did not have duplicate records
 * Did not have missing data
 * There were few invalid data i.e. zero values for salary. 
 
 ###  Exploratory Data Analysis
 
 Distribution of target variable was examined and mostly salary values lied between 70k-150k
and Salary histogram plot had right skewedness.
 

<img src = "Images/Salary%20distribution.PNG" >




Interquartile method was used to look for potential outliers. Upper Bound and lower bound salaries were found to be 220.5 and 8.5 respectively. On further exmination those high earning job types were from Oil and Finance industries and had many more years of experience. Hence none of the data was removed or modified.

#### Correlation Matrix

Categorical variable were encoded to numberical values and heat map studied.

<img src = "Images/Heat%20map.PNG" >

*  Positive correlation between years of experience and salary.
*  Negative correlation between miles from metropolis, job type, degree,major and salary.
*  Other features did not show significant correlation.

### Model Evaluation AND Best Model Selection

In the baseline model prediction, the average salary was calculated based on the data provided without fitting or feature engineering. Next,Supervised Machine Learning algorithms were used to enhance the prediction results of our fairly large dataset. Linear Regression, decision tree models are better in time and simplicity whereas Random forest and gradient boost models are better with accuracy. Models were evaluated using Mean Squared Error (MSE) and lower the MSE, the better the prediction. Gradient Boosting Regressor was selected as the best model.

<img src = "Images/model%20evaluation.PNG" >



### Model Development AND Deploy the Solution








<img src = "Images/Feature%20importance.PNG" >




## References:
1. https://ia.acs.org.au/article/2018/devops-and-contractors--the-trends-shaping-it-salaries.html
2.
