# Telecom-Customer-Churn-EDA-and-Data-Viz-using-Power-BI
## Customer Churn in Telecom Industry : Basic Exploratory Data Analysis and Data Visualization using Power BI

Operators are losing share in today’s competitive market.
Customer churn occurs when customers or subscribers stop doing business with a company or service, also known as customer attrition , customer turnover, or customer defection. It is also referred as loss of clients or customers. One industry in which churn rates are particularly useful is the telecommunications industry, because most customers have multiple options from which to choose within a geographic location. Customer churn rate is a key business metric in any industry and company providing services to end customers, because the cost of retaining an existing customer is far less than acquiring a new one.



## Procedure

Identifying Problem Statement.

Data Collection.

Exploratory data Analysis

Data Visualization

#### What is Exploratory Data Analysis(EDA)?

Exploratory Data Analysis is an approach to analyze the datasets to summarize their main characteristics in form of visual methods. 
EDA is nothing but an data exploration technique to understand various aspects of the data. 
The main aim of EDA is to obtain confidence in a data to an extent where we are ready to engage a machine learning model.
Basically EDA is important in every business problem, 
it’s a first crucial step in data analysis process.

Steps Involved In EDA

![image](https://user-images.githubusercontent.com/105121789/212865253-05309472-b53e-458f-8121-063b992025a4.png)

#### What is Data Visualization?

Visualization is the presentation of the data in the graphical or visual form to understand the data more clearly. 

Visualization helps us to : 

Easily analyze the data and summarize it.

Easily understand the features of the data.

Help to get meaningful insights from the data.

Help to find the trend or pattern of the data.

## Problem Statement

Factors affecting Customer Churn

What is the most profitable service type?

Is Tenure and Contract duration a factors in determining churn?

## Data Collection and Data Exploration

Data collected from Kaggle.

There are 7043 records in the dataset.

There are 21 features in the dataset - "Churn" is the target/dependent variable (this is what we will try to predict), and rest 30 are independent variables which we need to explore further.

Only 3 features are numeric - "SeniorCitizen" (categorical), and "tenure" and "MonthlyCharges" (continuous).

Datatype of the rest of the features is object, looking at the sample data they look like to be of type string. Some of these features are categorical, which we will map into numerical values.

There is absolutely NO missing data.

Customers who left within the last month – column is called Churn.

Services that each customer signed up for – phone ,multiple lines, internet, online security, online backup, device protection , Tech support ,streaming T.V and movies.

Customer account information – how long they have been a customer , Contract type , payment method , paperless billing , monthly charges and total charges.

Demographic info about customers – gender , age range and if they have a partner or dependents.

![image](https://user-images.githubusercontent.com/105121789/212868606-b9f4c34b-b51b-42ae-8cf1-0539dfc634f9.png)


### Data Exploration

To prepare data for analysis, we will perform:

a. Data exploration : Basic statistical analysis of the data.

b. Data exploration : Explore individual features (by looking at data distribution in dataset) and cleanup data as necessary.

c. Analyze relationship of the target (Churn) and input features through visualization.

![image](https://user-images.githubusercontent.com/105121789/212870008-85aa6dce-d408-4738-bfb2-5f011239d71c.png)

Let us first start with exploring our data set, to better understand the patterns in the data and potentially form some hypothesis. First we will look at the distribution of individual variables and then slice and dice our data for any interesting trends.
Demographics - Let us first understand the gender, age range, partner and dependent status of the customers

#### Churn by Gender

![image](https://user-images.githubusercontent.com/105121789/212870391-a1068045-f457-41f0-8241-68d48b81e2f6.png)

Observations:

Gender Distribution - The dataset has almost equal distribution of male and female customers. Both in the churned or retained category - percentage of males and females are almost equally distributed.
Out of all male customers, approx 26% churned. While among females, the churn percentage is approx 27%. Both are almost at equal level. It can be concluded that probability of churn does not depend on gender of the customer.

#### Churn by age

![image](https://user-images.githubusercontent.com/105121789/212870851-cdc647e1-a870-4e39-9c58-a93eedad98be.png)

Observations:

% Senior Citizens - There are only 16% of the customers who are senior citizens and Non-Senior Citizens (> 80%).Thus most of our customers in the data are younger people. Out of all senior citizen customers, more than 40% churned. While among younger customers, the churn percentage is less than 25%.Hence, senior citizens tend to churn more than younger customers. Thus, Senior Citizen and Churn features seem to be related.

#### Churn by Partner and Dependent

![image](https://user-images.githubusercontent.com/105121789/212871169-829244c0-4acf-48ae-b1da-fb4be9ed1eee.png) 
![image](https://user-images.githubusercontent.com/105121789/212871227-bf84ff3c-4eec-441e-988d-41d3e8bd6cbd.png)

Observations:

Partner and dependent status - The dataset contains almost 70% customers who does not have a dependent, while 30% has one or more dependents. Among the customers who have a partner, only about half of them also have a dependent, while other half do not have any dependents. Additionally, as expected, among the customers who do not have any partner, a majority (80%) of them do not have any dependents . 
Customers without dependents tend to churn more (~30% vs ~20%).
From Partner and Dependents data we can conclude that - customers who are single/independent, i.e. without partners or dependents tend to churn more, while customers with partner and/or dependents, usually continue.

#### Churn by Tenure

Tenure: After looking at the below histogram we can see that a lot of customers have been with the telecom company for just a month, while quite a many are there for about 72 months. This could be potentially because different customers have different contracts. Thus based on the contract they are into it could be more/less easier for the customers to stay/leave the telecom company.   

![image](https://user-images.githubusercontent.com/105121789/212871952-f2b885e0-b9c1-4382-a5d6-ed0b3426b515.png)
![image](https://user-images.githubusercontent.com/105121789/212872013-bbabf7bc-d2d5-4760-9457-b0ea38b1d7de.png)

Observations:

As customer tenure increases, the chance of churn decreases accordingly. Hence, the CSP should concentrate on retaining newly acquired customers. If they can somehow hold the customers for more couple of years, the possibility of those customers continuing with the same CSP increases multifold.
In addition, CSP should try to get customers on contract for longer duration instead of selling monthly plans. This is another important factor for churn determination.

#### Churn by Contract and Churn by Contract and Gender

![image](https://user-images.githubusercontent.com/105121789/212872428-f8d3fc14-db4b-453a-b907-7c0d6194fc1c.png)
![image](https://user-images.githubusercontent.com/105121789/212872477-946279e3-fab0-49f3-9b06-d2f4adbce6e7.png)

Observations:

~55% customer are on month-to-month (or monthly) plans, while little more than 20% each are on 1 or 2 years contract.
The churn rate is high among monthly customers and least among 2-year contracted customers. While this is expected because of the contract duration, this is an alarming signal for CSP since should try to retain contracted customers and bring the churn rate to near zero, in addition to spending effort on month-to-month customers.

#### Churn by Service type

PhoneService , MultipleLines , InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport and StreamingTV, StreamingMovies. These are the different types of services offered by CSP to customers. Here we are plotting 2 diagrams for each service type -on left - we show the distribution of data in the dataset and on right - we look at the percentage of churn in each category of service types.
![image](https://user-images.githubusercontent.com/105121789/212872817-8231762c-6629-443b-b04d-15748baba789.png)

![image](https://user-images.githubusercontent.com/105121789/212872983-6d9c02fb-79f6-4eda-8453-9442b500dee2.png)
![image](https://user-images.githubusercontent.com/105121789/212873020-1bac2194-223e-4fc6-bf2e-6db0e6f2f1d4.png)
![image](https://user-images.githubusercontent.com/105121789/212873074-3fc142ce-6b1f-4f3f-ac5a-e44b25e784d0.png)
![image](https://user-images.githubusercontent.com/105121789/212873134-edeef9e0-5bf6-447f-a61d-7096ecedb418.png)
![image](https://user-images.githubusercontent.com/105121789/212873226-fc9a0afb-34c9-4286-aad9-e2820ce69209.png)
![image](https://user-images.githubusercontent.com/105121789/212873280-7edefdaf-8759-41c8-8674-83a506dd82a1.png)
![image](https://user-images.githubusercontent.com/105121789/212873402-3cf35bfd-3d48-4696-9e53-7ae2b3684dde.png)
![image](https://user-images.githubusercontent.com/105121789/212873477-100d0b31-3dab-4e39-a44c-ff695f892921.png)
![image](https://user-images.githubusercontent.com/105121789/212873554-a8baf5e0-b5da-4d2c-8c48-8c925017439e.png)

Observations:

Phone Service - Almost all (90%) customers have Phone Service. However, the churn rate is very low compared to the volume (~25%). 

On the other hand, churn rate is almost same (~25%) among non-phone service customers as well (though they form only 10% of the population). Thus, selling Phone Service is more beneficial for the CSP.

Multiple Lines - Among Phone Service users, 45% has Multiple Lines while the rest 45% have single line. Churn rate is slightly higher among users with multiple lines, but not that significant (~28%).

Internet Service - Approx 20% customers do not use internet. Among customers using internet, approx 45% use Fiber Optic and 35% use DSL. However, churn among Fiber Optic users is pretty high as well (> 40%), while it is 20% among DSL users. Hence, CSP needs to look into the quality of its internet service.

Online Security - ~50% customers do not use online security service, and churn rate among such users is highest as well (~40%).

Online Backup, Device Protection and Tech Support - Same as above, most of the customers do not use this service and they tend to churn as well.

Streaming TV and Streaming Movies - Among users with internet services (which is mandatory for availing these services), almost half use these streaming services. The rate of churn is more or less same as well (~35%) irrespective of usage of streaming services.

#### Churn by Paperless billing and Payment Method

![image](https://user-images.githubusercontent.com/105121789/212875002-84ffd9ff-6361-4dfd-870e-bd5c247cf002.png)

Almost 60% customers prefer paper-less billing.
Almost 35% of them left the CSP.
Now, apparently a direct relation between bill mode and churn cannot be established, it must be investigated if customers receiving soft copies of bills are getting clear and transparent information on all the charges, and proper service and care if they face any difficulty in interpreting the bills.


![image](https://user-images.githubusercontent.com/105121789/212875042-1c8118b1-4d12-4d98-97ec-10c6243c566f.png)

Customers with payment method as "Electronic Check" is slightly higher than customers with other modes of payment (~35%).
Churn among such customers is highest as well (~45%).
CSP should try to encourage customers to use automated mode of payments.


### Dashboard

![image](https://user-images.githubusercontent.com/105121789/212875469-cf4f5e1a-9887-4fd8-9690-60760d21aabc.png)


### Conclusions

Based on the observations made so far, the key takeaways or highlights are:

Gender – The churn percentage is almost equal in case Male and Female.

The percentage of churn is higher in case of senior citizens.

Customers with Partners and Dependents have lower churn rate compared to those who don’t have Partners and Dependents.

Tenure and Contract duration seems to be strong factors in determining churn. A large percentage of customers with monthly subscription have left when compared to customers with one or two year contract.

Among service types, phone service seems to be most popular and Churn rate is much higher in case of fiber optic Internet services.

Customers who do not have services like No online security , Online backup and Tech support have left the platform in the past month.

Churn percentage is higher in case of customers having paperless billing option.

Customers who have electronic check Payment Method tend to leave the platform more compared to the other options.

### Recommendation

CSP should investigate if customers receiving digital invoice have any concern with understanding the bill details.

Also, they should encourage customers to move to automated payment modes to improve customer experience.

Gender does not play an important role. However, CSPs should take care of the experience of senior citizens.












