Exploratory Data Analysis(EDA)

Exploratory Data Analysis is a process of examining or understanding the data and extracting insights or main characteristics of the data. EDA is generally classified into two methods, i.e. graphical analysis and non-graphical analysis.
EDA is very essential because it is a good practice to first understand the problem statement and the various relationships between the data features before getting your hands dirty.


Exploratory Data Analysis

Technically, The primary motive of EDA is to
1. Examine the data distribution
2. Handling missing values of the dataset(a most common issue with every dataset)
3. Handling the outliers
4. Removing duplicate data
5. Encoding the categorical variables
6. Normalizing and Scaling

Step 1
First, we will import all the python libraries that are required for this, which include NumPy for numerical calculations and scientific computing, Pandas for handling data and Matplotlib and Seaborn for visualization.
          
Step 2
Then we will load the data into the Pandas data frame. For this analysis, we will use a dataset of "World Happiness Report", which has the following columns: GDP per Capita, Family, Life Expectancy, Freedom, Generosity, Trust Government Corruption etc. to describe the extent to which these factors contribute in evaluating the happiness.
You can find this dataset over here.

          
Step 3
We can observe the dataset by checking a few of the rows using the head() method, which returns the first five records from the dataset.
          
Step 4
Using shape, we can observe the dimensions of the data.
          
Step 5
info() method shows some of the characteristics of the data such as Column Name, No. of non-null values of our columns, Dtype of the data and Memory Usage.
          
Step 6
We will use describe() method, which shows basic statistical characteristics of each numerical feature (int64 and float64 types): number of non-missing values, mean, standard deviation, range, median, 0.25, 0.50, 0.75 quartiles.
          
Step 7
Handling missing values in the dataset. Luckily, this dataset doesn't have any missing values, but the real world is not so naive like our case.

So, we can handle the missing values by using a few techniques, which are
1. Drop the missing values - If the dataset is huge and missing values are very few then we can directly drop the values because it will not have much impact.
2. Replace with mean values - We can replace the missing values with mean values, but this is not advisable in case if the data has outliers.
3. Replace with median values - We can replace the missing values with median values, and it is recommended in case if the data has outliers.
4. Replace with mode values - We can do this in case of Categorical feature.
5. Regression - It can be used to predict the null value using other details from the dataset.
For our case, we will handle missing values by replacing it with the median value.
          

Step 8
We can check for duplicate values in our dataset as the presence of duplicate values will hamper the accuracy of our ML model.         
We can remove duplicate values using drop_duplicates()
          
Step 9
Handling the outliers in the data, i.e. the extreme values in the data. We can find the outliers in our data using a Boxplot.
          
So to handle it we can either drop the outlier values or replace the outlier values using IQR(Interquartile Range Method).
IQR is calculated as the difference between the 25th and the 75th percentile of the data. The percentiles can be calculated by sorting the selecting values at specific indices. The IQR is used to identify outliers by defining limits on the sample values that are a factor k of the IQR. The common value for the factor k is the value 1.5.
          
Step 10
Normalizing and Scaling - Data Normalization or feature scaling is a process to standardize the range of features of the data as the range may vary a lot. So we can preprocess the data using ML algorithms. So for this, we will use StandardScaler for the numerical values, which uses the formula as x-mean/std deviation.
          
Step 11
We can find the pairwise correlation between the different columns of the data using the corr() method. (Note - All non-numeric data type column will be ignored.)

The resulting coefficient is a value between -1 and 1 inclusive, where:
1: Total positive linear correlation
0: No linear correlation, the two variables most likely do not affect each other
-1: Total negative linear correlation
Pearson Correlation is the default method of the function "corr".
We can create a heatmap using Seaborn to visualize the correlation between the different columns of our data:
          
     
I hope we all now have a basic understanding of how to perform Exploratory Data Analysis(EDA).

Hence, the above are the steps which I personally follow for Exploratory Data Analysis, but there are various other plots and commands, which we can use to explore more into the data.
Thanks for Reading and Keep Learning.

Contribution
If you have any new ideas for new features or improvements feel free to note them down in pull requests

Contact
Feel free to contact me via email (nkr4nikhilraj@gmail.com) or follow me on LinkedIn (https://www.linkedin.com/in/nkr4nikhilraj)
