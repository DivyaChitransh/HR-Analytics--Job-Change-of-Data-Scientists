# HR-Analytics--Job-Change-of-Data-Scientists
About Dataset<br>
Context and Content<br>
A company which is active in Big Data and Data Science wants to hire data scientists among people who successfully pass some courses which conduct by the company. Many people signup for their training. Company wants to know which of these candidates really wants to work for the company after training or looking for a new employment because it helps to reduce the cost and time as well as the quality of training or planning the courses and categorization of candidates. Information related to demographics, education, experience are in hands from candidates signup and enrollment.

This dataset designed to understand the factors that lead a person to leave current job for HR researches too. By model(s) that uses the current credentials,demographics,experience data you will predict the probability of a candidate to look for a new job or will work for the company, as well as interpreting affected factors on employee decision.

The whole data divided to train and test . Target isn't included in test but the test target values data file is in hands for related tasks. A sample submission correspond to enrollee_id of test set provided too with columns : enrollee _id , target

Note:<br>
The dataset is imbalanced.<br>
Most features are categorical (Nominal, Ordinal, Binary), some with high cardinality.<br>
Missing imputation can be a part of your pipeline as well.<br>

**Features**

enrollee_id : Unique ID for candidate

city: City code

city_ development _index : Developement index of the city (scaled)

gender: Gender of candidate

relevent_experience: Relevant experience of candidate

enrolled_university: Type of University course enrolled if any

education_level: Education level of candidate

major_discipline :Education major discipline of candidate

experience: Candidate total experience in years

company_size: No of employees in current employer's company

company_type : Type of current employer

last_new_job: Difference in years between previous job and current job

training_hours: training hours completed

target: 0 – Not looking for job change, 1 – Looking for a job change

**ML Operations**<br>
1.imported basic python libraries and modules like numpy and pandas <br>
2.basic exploratory data analysis(check for null values, datatypes, unique data,etc)<br>
3.Used mapping to encode ordinal features(categorical features) to numeric<br>
4.Set of columns to be transformed in different ways<br>

categorical column-->Fill missing values and One Hot Encoder

Numerical Column-->Fill missing values and Scaling<br>
5.made seperate set of categorical and numerical columns <br>
6.Created Pipleline for numerical and categorical Features<br>
7.Created ColumnTransformer to Apply the Pipeline for Each Column Set<br>
8.Added desired model to pipeline by creating a new pipeline<br>
9.combine numerical and categorical features, then split train and test data. After this train the model pipeline<br>
10.we can save and load the<br>
10.we can save and load the pipeline to file to use it whenever we want without going through all the previous steps<br>
11.we can get and then set new parameter for this pipeline to improve this model's accuracy.<br>
12.to find best parameter we will tune the hyperparameter using GridSearchCV<br>
13.set a range of hyperparameters and find the best set among that range<br>
14.With the pipeline, we can create data transformation steps in the pipeline and perform a grid search to find the best step. A grid search will select which step to skip and compare the result of each case.<br>
15.used a list of dictionaries for the grid search parameters(to find which data transformation step is best)<br>
[{case 1},{case 2}]<br>
16.found the best hyperparameter sets and the best data preparation method by adding tuning parameters to the dictionary of each case of the data preparation method.<br>
![image](https://github.com/DivyaChitransh/HR-Analytics--Job-Change-of-Data-Scientists/assets/147910649/5857328a-8756-4fac-9317-feb4b87f6898)<br>
17.Similarly you can check for different ml models and choose that gives highest accuracy.<br>
