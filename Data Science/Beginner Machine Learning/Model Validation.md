*"Will the model's predictions be close to what actually happens?"*

##### [Metrics]

**Mean Absolute Error (MAE)** #mae
* average of each absolute error ( error = actual - predicted)
	* **from sklearn.metrics import mean_absolute_error**
	* **predicted_home_prices = sample_model.predict(X)
	* **mean_absolute_error(y, predicted_home_prices)**
* **lower mae = more accurate , higher mae = less accurate**
##### [Problems]

**"In-Sample Scores"** 
* Using a single #sample of data for modelling and evaluating it will yield an in-sample score. This in-sample score is only applicable to this specific data/sample and not to others
	* example: The model is trained with data and found a pattern of price increase with green doors. This model still needs to be measured by how accurate that information is by calculating its #mae with data that is different from what we trained it with . If we calculate the #mae with the same data, we are practically not double checking it with other data samples ( not confirming if the pattern holds true for all data samples).
	
* The proper step to avoid this is to split the data set into two: validation and training data/sample
	* 1.) We use the training data to #fit  the model  
	* 2.) We use the validation data to measure the #mae
	
![[Pasted image 20231002211425.png]] 

![[Pasted image 20231002214727.png]]