##### Steps in Importing Data

*Importing panda library as pd*

![[Pasted image 20231002201118.png]]

*Caching the file path and caching the data frame*
* Set index_col=0 so we can use the unnamed column of increasing integers on the left side as the index

![[Pasted image 20231002201242.png]]

##### Exporting Data
![[Pasted image 20231004095827.png]]

##### Creating,Reading and Writing Data
[Exercise: Creating, Reading and Writing | Kaggle](https://www.kaggle.com/code/cliffycodes/exercise-creating-reading-and-writing/edit)*

*DataFrame Creation*

![[Pasted image 20231004095123.png]]

*Series Creation* #series 
* Series contains a single list with an index, Dataframes are a list of series

![[Pasted image 20231004095442.png]]

##### Indexing, Selecting & Assigning


*Native Accessors*

![[Pasted image 20231004155450.png]]

*Pandas Indexing* #series 

*Iloc
* selecting the first row

![[Pasted image 20231005223921.png]]
* row first, column seconds
* the example shows all rows on the 1st column

![[Pasted image 20231004155634.png]]
* this example shows the last 5 rows with all columns

![[Pasted image 20231005224733.png]]
*loc
* label-based selection
* data index 
* this example shows the first row entry for country

![[Pasted image 20231004155743.png]]
* this example shows all columns for all the "labels indicated"

![[Pasted image 20231005225434.png]]

*Manipulating the index*
* using set index to change the index from a number [0] to a named field ["title]"*

![[Pasted image 20231005231429.png]]

*Conditional Selection*
* Selecting all data index with labels of Italy or review points above 90

![[Pasted image 20231007083109.png]]
* .isin function is like doing OR 

![[Pasted image 20231007083817.png]]
* isnull / isnotnull, very useful for Data Cleaning #datacleaning
![[Pasted image 20231007084000.png]]
##### Summary Functions and Maps
*Sometimes we have to do extra work to reformat data to just what we need*

*describe* #pandasdescribe
![[Pasted image 20231009132623.png]]

mean #pandasmean
![[Pasted image 20231009132707.png]]

unique #pandasunique
* unique list of values
![[Pasted image 20231009132735.png]]

*value_counts*
* the count of how often a value appears in the data set
![[Pasted image 20231009132842.png]]