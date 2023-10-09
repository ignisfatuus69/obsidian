*Definition: A machine learning model which divides the data into **categories of 2** and keeps expanding depending on the **number of leaf nodes/tree depth**. The prediction point (last piece of the decision tree) is called a **leaf**.

### [Coding]
#### Steps in making a model of a decision tree

###### Selecting Data For Modeling
* Pick out prioritized variables as **features** by using statistical techniques 
* View the columns property of the dataframe in order to see them:
	* **(sample_data.columns)**

###### Selecting Features
* Pick out from the prioritized variables which features we want to select for the prediction target 
	* **sample_data_features = ['f1',f2,f3,f4]**
	* **x = sample_data[sample_data_features]**

###### Selecting The Prediction target
* Pick out the column that we are predicting which is stored in a Series: 
	* **y(prediction target) = sample_data.Price**

###### Building The Model
* **Define** : What kind of model?
	* **sample_data = DecisionTreeRegressor(random_state=1)**
* **Fit** : Capture patterns (plug in the features and prediction target) #fit
	* **sample_data.fit(X, y)**
* **Predict** : Call out predict function after fitting #predictModel
	* **print(sample_data.predict(X.head())**
* **Evaluate** : Determine how close the prediction is to the actual value with the use of [[Model Validation]]
* **Experiment** : Based on data validation, adjust parameters (tree depth, separation of training and validation data, and etc.)
* **Finalize**: After testing and experimenting with test data and validating the model, you can now use the model on all of the data including the parameters that you have tested that resulted in the best mae score
#### Kinds of Decision Trees 

**Classic Single Decision Tree** 
* One tree with tree depths
* Can be prone to inaccuracy and has to take into account [[Model Validation]] for a better MAE
* Tree depth needs to be considered to be more accurate with the concept of [[Underfitting and Overfitting]]

![[Pasted image 20231002223149.png]]

**Random Forests** 
* Many trees (as indicated random forests)
* Makes a prediction by averaging the predictions of each component tree
* Better predictive accuracy than a single decision tree

*![[Pasted image 20231002223103.png]]