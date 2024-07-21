
0.) Load data via file or SQL
* Remove duplicates right off the bat

1.) Make data dictionary
* only when needed

2.) Show all columns (showing dtypes,# of rows) :
*  df.info()
* df.head()
* df.describe()
* df.isna().sum()

2.5) Data Cleaning Step:
* Fix the datatypes
* Check how it's currently structured

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

4.) Relationship plotting
* Make a correlation matrix w/ heatmap
* Scatter plot necessary relationship variables according to problem

5.) Generate questions to get insights based on problem statement
* Discard unneeded columns
* Group by / Aggregate tables
*  Combine tables needed
*  Make line graphs/analyze trends
* Make predictive analysis/linear regression
* Make bar charts / comparison

Do EDA:
[Statlog (German Credit Data) - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data)

[Clickstream Data for Online Shopping - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/553/clickstream+data+for+online+shopping)