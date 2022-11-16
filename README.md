# Project2 - Deposit Opening Decision

 ### AGENDA
- DataSet 
    - DataSet Information
    - Attribute Information
- Descriptive Analysis
    - Visualizing
    - Correlations
- Data Manipulation
    - Null-Missing Value Analysis
    - Creating New Column Age
    - String Indexer
    - Label Encoder
    - VectorAssembler
    - Standard Scaler
- Predictive Analysis
    - Sampling
    - Classification Models and Results
    - Saving The Models
- Summary

### Dataset Information

- The data is about an XYZ bank’s direct marketing campaign. Marketing campaigns were driven by telephone calls.
- DataSet Often, more than one contact to the same client was required, in order to access if the product ( deposit) would be ('yes') or not ('no') subscribed.
- The purpose of the classification is to forecast whether the customer will signup (yes/no) a term deposit (variable y).
- The dataset is having 20 entries/columns, sorted by date between May 2008 and November 2010.

### Attribute Information

    1 - Age (numeric)
    2 - Job : type of job (categorical)
    3 - Marital : marital status (categorical)
    4 - Education (categorical)
    5 - Default: has credit in default? (categorical)
    6 - Housing: has housing loan? (categorical)
    7 - Loan: has personal loan? (categorical)

#### Regarding the latest contact in the ongoing campaign:
    8 - Contact: contact communication type (categorical)
    9 - Month: last contact month of year (categorical)
    10 - Day_of_week: last contact day of the week (categorical)
    11 - Duration: last contact duration, in seconds (numeric)

#### Other attributes:
    12 - Campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
    13 - Pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
    14 - Previous: number of contacts performed before this campaign and for this client (numeric)
    15 - Poutcome: outcome of the previous marketing campaign (categorical)

#### Social and economic context attributes
    16 - Emp.var.rate: employment variation rate - quarterly indicator (numeric)
    17 - Cons.price.idx: consumer price index - monthly indicator (numeric) 
    18 - Cons.conf.idx: consumer confidence index - monthly indicator (numeric) 
    19 - Euribor3m: euribor 3 month rate - daily indicator (numeric)
    20 - Nr.employed: number of employees - quarterly indicator (numeric)
    
### Descriptive Analysis
- The dataset given has two types of variables which include continous variables and categorical variables.

#### Continuous Variables

- 'age‘ , 'duration', 'campaign', ‘pdays ‘, 'previous', 'emp.var.rate‘
'cons.price.idx', 'cons.conf.idx', 'euribor3m', 'nr.employed'

#### Categorical Variables

- 'job', 'marital', 'education', 'default', 'housing', 'loan’
'contact', 'month', 'day_of_week', 'poutcome', 'y'

### Visualizing – Continuous Variables

- We can see from below graph for continous variables is that neither of the variable have normal distribution.

![p1](/assets/p1.png) 

### Visualizing – Categorical Variables
- One thing to note from this screenshot is target variable is not balanced.

![p2](/assets/p2.png)     ![p3](/assets/p3.png) 

### Data Manipulation

#### Correlation

From the below screenshot you can see high correlation between 4 columns, which include cons.price.idx, euribor3m, nr.employed,emp.var.rate. Therefore we dropped these columns.

![p4](/assets/p4.png)

#### Null Values

No null values were observed

![p5](/assets/p5.png)

#### Creating new column age

Age was created in to different bins.

![p6](/assets/p6.png)

#### String Indexer

String Indexer was created on categorical variable to map a string column to a index column that will be treated as a categorical column by spark. ( Below Screenshot showing a sample of one of the variable).

![p7](/assets/p7.png)

#### Label Encoder

We used Label Encoder for our tagert variable 'y'.

![p8](/assets/p8.png)

#### VectorAssembler

Vector Assembler was used to combine a list of columns into a single vector column. I was done in order to train ML models like logistic regression, decision trees, random forest etc.

![p9](/assets/p9.png)      ![p10](/assets/p10.png)

#### Standard Scaler

After the vector assembler was performed, we then scaled the vector features using Standard Scaler which standardizes the features by subracting the mean and then scaling to uni variance.

![p11](/assets/p11.png)

### Predictive Analysis

#### Test-Train Data Split

First step is spliting data into two and selected randomly(seed 2018) %80 of data as Training set and %20 of data as Test Set.

#### Logistic Regression

- First Algorithm Logistic Regression was used which is the most commonly used algorithm for solving all classification problems.

![p12](/assets/p12.png)

#### Random Forest

- Second Algorithm Random Forest was used for solving our classification problems.

![p13](/assets/p13.png)

#### Decision Tree

- Third Algorithm Decision Tree was used for solving our classification problems.

![p15](/assets/p15.png)

#### Grandient Boosted Tree

- Third Algorithm Gradient Boosted Tree was used for solving our classification problems.

![p14](/assets/p14.png)

#### Saving The Models

All the models were saved as serialized object, below screenshot shows the code as well as saved model with pickel files.

![p9999](/assets/p9999.png)

