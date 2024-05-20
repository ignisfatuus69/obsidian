
0.) Load data via file or SQL

1.) Make data dictionary

2.) Show all columns (showing dtypes,# of rows) :
*  df.info()
* df.head()
* df.isna().count()

2.5) Data Cleaning Step:
* Fix the datatypes

3.) Checking categorical  & date columns:
* df["column"].value_counts()
* Check the distribution via histogram
* Group binaries into a series/df and check the ratio/value.counts()

3.5) Data Cleaning Step:
* Fix whitespaces by trimming
* Fix inconsistent data based from value_counts


4.) Checking numerical data:
* Put all numeric data into a list then -> df.describe()
* Check the distribution via histogram
* Make a boxplot to detect outliers

4.5) Data Cleaning Step :
* Fix inconsistent data Numbers: decimal/whole/negative/positive
* Fill in missing values 
* Fixing outliers via lower & upper bound when needed

4.) Relationship checking
* Make a correlation matrix w/ heatmap
* Scatter plot necessary relationship variables according to problem

5.) Generate questions to get insights based on problem statement
* Discard unneeded columns
* Group by / Aggregate tables
*  Combine tables needed
*  Make line graphs/analyze trends
* Make predictive analysis/linear regression
* Make bar charts / comparison

