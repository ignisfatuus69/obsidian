***Exploratory Data Analysis is just your first look at the data***

[MISRA TURP]
[(7) How to Do Data Exploration (step-by-step tutorial on real-life dataset) - YouTube](https://www.youtube.com/watch?v=OY4eQrekQvs&t=354s)

1.) Make a data dictionary
2.) Explore data:
	- show all columns![[Pasted image 20231120010252.png]]
	- cross reference w/ data dictionary
3.) Filtering out columns
	- set priorities and only get columns that we'll need
4.) Check for null values
![[Pasted image 20231120010600.png]]
![[Pasted image 20231120010656.png]]
5.)Numerical values check
![[Pasted image 20231120010808.png]]
6.) Outliers check
![[Pasted image 20231120011012.png]]
![[Pasted image 20231120011216.png]]![[Pasted image 20231120011423.png]]
7.) Categorical values check
![[Pasted image 20231120011537.png]]8.) Binary columns check
![[Pasted image 20231120011909.png]]






[Alex The Analyst]
[(7) Exploratory Data Analysis in Pandas | Python Pandas Tutorials - YouTube](https://www.youtube.com/watch?v=Liv6eeb1VfE&t=1587s)

1.) Exploring basic data info: ![[Pasted image 20231120062246.png]]![[Pasted image 20231120062309.png]]
*Checking dtypes*
![[Pasted image 20231120065208.png]]
*Checking only numerical columns*
![[Pasted image 20231120065239.png]]
2.) Checking for null values ![[Pasted image 20231120062338.png]]
3.) Checking for unique values ![[Pasted image 20231120062413.png]]
4.) Using min/max on columns 
![[Pasted image 20231120062619.png]]
5.) Looking for correlations (usually numeric values)
*Using df.corr()*
![[Pasted image 20231120063120.png]]
*Using a heatmap*
![[Pasted image 20231120063537.png]]
6.) Grouping Columns
* Having some sort of goal
* Example: "are there certain continents that are growing faster than others and in which ways?"

*Average values of each columns grouped by Continent*

![[Pasted image 20231120064033.png]]
*Average values of each columns grouped by Continent, sorted by 2022 population descending*
![[Pasted image 20231120064313.png]]
*Looking into what Oceana data contains*
![[Pasted image 20231120064151.png]]
7.) Visualizing a use-case 

*Visualizing grouped data by making a line graph of year population values*
![[Pasted image 20231120064537.png]]
* df3 = df2.transpose()
* df3.plot()
![[Pasted image 20231120064623.png]]
8.) Making a boxplot to see outliers
*Doesnt completely apply to this data since it's a population with varying values*
![[Pasted image 20231120065047.png]]