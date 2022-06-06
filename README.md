# Identifying-Leads-for-an-Online-Education-Company-Using-Logistic-Regression

# **Problem Statement**

An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses.

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%.

Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. To make this process more efficient, the company wishes to identify the most potential leads, also known as ‘Hot Leads’. If they successfully identify this set of leads, the lead conversion rate should go up as the sales team will now be focusing more on communicating with the potential leads rather than making calls to everyone. A typical lead conversion process can be represented using the following funnel:

![https://cdn.upgrad.com/UpGrad/temp/189f213d-fade-4fe4-b506-865f1840a25a/XNote_201901081613670.jpg](https://cdn.upgrad.com/UpGrad/temp/189f213d-fade-4fe4-b506-865f1840a25a/XNote_201901081613670.jpg)

**Lead Conversion Process - Demonstrated as a funnel**

As you can see, there are a lot of leads generated in the initial stage (top) but only a few of them come out as paying customers from the bottom. In the middle stage, you need to nurture the potential leads well (i.e. educating the leads about the product, constantly communicating etc. ) in order to get a higher lead conversion.

X Education has appointed you to help them select the most promising leads, i.e. the leads that are most likely to convert into paying customers. The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance. The CEO, in particular, has given a ballpark of the target lead conversion rate to be around 80%.

### Data

Given a leads dataset from the past with around 9000 data points. This dataset consists of various attributes such as Lead Source, Total Time Spent on Website, Total Visits, Last Activity, etc. which may or may not be useful in ultimately deciding whether a lead will be converted or not. The target variable, in this case, is the column ‘Converted’ which tells whether a past lead was converted or not wherein 1 means it was converted and 0 means it wasn’t converted.  

### Highlights:

Columnwise Missing Value Handling -dropped the columns with high number of missing values.

Identifying and dropping the relevant columns with 'Select’ - Identified that the "select" level in some columns is to be considered as a missing value.

identified categorical variables that have just one level and eliminated them from the dataset.

Handled the row-wise missing values and performed the imputations needed and eliminated the last few remaining rows from the data as required.

Missing Value Percentage - Left with a good number of rows to proceed with analysis. It was expected to have atleast 60-70% of the rows remaining.

Dummy Variable Creation - created the dummy variables for the categorical variables present, and eventually dropped the original variables.

Scaled the data after performing the test-train split, so that we're not exposing your test data at all when training the model.

**Model Building and Evaluation**

build the model as expected (both with RFE and manually tuning the model using p-values and VIF), and identified the optimal cut off point and evaluation metrics.

this includes -

Prediction of Probabilities

find the optimal cut off probability by analyzing the trade-off using an ROC curve

translate the cut-off probability to identify the classes

Accuracy, sensitivity and specificity values are all comparable to each other

Identified the top 3 variables from the model 

identified the top 3 categorical variables

Identify the key strategy of lowering the cut-off probability to ensure  capturing and covertingas many leads as possible.
