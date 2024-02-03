### Texas-Salary-Prediction

#### Problem Statement:
Create a predictive model which will help theTexas state government  team to know the payroll information of employees of the state of Texas.<br>

#### Dataset:
This database has salary information for positions at all 113 agencies in the Texas state government. The Tribune obtained this data by requesting salary records from the state comptroller, as allowed by the Texas Public Information Act.<br>

#### Attribute Information : 

•	AGENCY: A business or organization providing a particular service on behalf of another business, person, or group.<br>
•	AGENCY NAME: A person or thing through which power is used or something is achieved.<br>
•	LAST NAME: The last name refers to the identification that an individual is given to represent the family name in the culture name of many societies.<br>
•	FIRST NAME: A personal name given to someone at birth or baptism and used before a family name.<br>
•	MI: Middle initial<br>
•	CLASS CODE: These codes must be established before employees can be added to the system and payrolls processed, since the files contain many of the defaults and codes used in these process.<br>
•	CLASS TITLE:  Means the designation given under these rules to a class and to each position allocated to such class.<br>
•	ETHNICITY: The quality or fact of belonging to a population group or subgroup made up of people who share a common cultural background.<br>
•	GENDER: The term is also used more broadly to denote a range of identities that do not correspond to established ideas of male and female.<br>
•	STATUS: Pay status means an employee ’s right to receive compensation for time worked or leave taken, except when absent on leave-with- out-pay or suspension without pay.<br>
•	EMPLOYEE DATE: Date of joining of an individual.<br>
•	HOURLY RATE: As an hourly employee, you should get paid for all of the hours that you work. If an employer wants more of your time, they’ll have to pay you more.<br>
•	HRS PER WEEK: The number of hours in a week that the employee normally would work for the shared work employer or 40 hours.<br>
•	MONTHLY: A salary is the money that someone is paid each month by thei employer.<br>
•	ANNUAL: Annual salary is the amount of money your employer pays you over the course of a year in exchange for the work you perform.<br>
•	STATE NUMBER: A unique number assigned to a business or organization by the state.<br>
•	DUPLICATED: One of two or more identical things.<br>
•	MULTIPLE FULL TIME JOBS: Individual works on one ore more full time jobs.<br>
•	COMBINED MULTIPLE JOBS: The Combine Jobs feature allows you to merge two or more jobs from the same market view into a single job.<br>
•	SUMMED ANNUAL SALARY: Total salary earned by an individual in a year including multiple full time jobs and combined multiple jobs.<br>
•	HIDE FROM SEARCH: Gives you the option for your searches to be hidden with respect to organization.<br>

##### Dataset Size:
Rows:149481
Columns:21

#### Data Preprocessing:
•	Checking basic informations of the dataset.<br>
•	Checking for the null values, duplicated, multiple_full_time_jobs, combined_multiple_jobs, summed_annual_salary, hide_from_search have more than 95% of them are null values, hence ignored them.<br>
•	AGENCY is a code given to AGENCY_NAME so it does not make sense in prediction,so dropped it.<br>
•	Also LAST_NAME, FIRST_NAME, MI, CLASS_CODE does not make sense in prediction hence those are removed.<br>
•	There is one feature EMPLOY_DATE extract these feature and make difference with current date.<br>
•	There are some categorical features like ETHNICITY, GENDER, STATUS, AGENCY_NAME and CLASS_TITLE all this feature encoded using encoding technique.<br>
•	Now, data is ready to passed to machine learning algorithm.<br>
•	So, Splitting data into train and test.<br>

#### Model building:
##### Trained Machine learning models:
Almost all the regression machine learning algorithm we have tried on the same dataset to get the maximum accuracy, which are:
1.	Linear Regression<br>
2.	KNeighbors Regressor<br>
3.	DecisionTree Regressor
4.	Random forest Regressor
5.	Gradient boosting
   
Applying regression algorithm R2_score is:
| Model | R2_score | Adjusted_R2_score |
|-------|--------- |-------------------|
|Linear Regression|0.91|0.91|
|KNeighbors Regressor|-0.04|-0.04|
|DecisionTree Regressor|0.82|0.81|
|Random forest Regressor|0.88|0.87|
|Gradient boosting Regressor|0.59|0.57|



