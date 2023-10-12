*Most machine learning libraries will give an error if you build a model with missing values*
##### [Drop Columns] #dropcolumns
* columns with missing values are automatically dropped/excluded from the model
* should only be used if most values in the dropped columns are missing
* model losses a lot of information with this approach

***VISUAL**
![[Pasted image 20231005212204.png]]

***CODE**
![[Pasted image 20231005213104.png]]
##### [Imputation] #imputation
* missing values are filled automatically. Sometimes we use the mean value along each column.

***VISUAL**
![[Pasted image 20231005212256.png]]

***CODE**
![[Pasted image 20231005213223.png]]

##### [Extension To Imputation] #extensiontoimputation
* Missing values are filled automatically AND we have an extra column that labels if the data for that missing value was auto-filled.

***VISUAL** 
![[Pasted image 20231005212405.png]]

***CODE**
![[Pasted image 20231005213454.png]]