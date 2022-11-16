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
    - Encoding Categorical Variables
    - Data Normalization
- Predictive Analysis
    - Sampling
    - Classification Models and Results
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
