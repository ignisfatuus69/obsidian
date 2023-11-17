### Madocs Online Health Care Service - Pandas Exercise Exam

#### Section 1: DataFrame Creation and Basic Operations

1. **DataFrame Creation**: Create a DataFrame named `test_df` using the given `test_data` dictionary. Display the first three rows.
    
2. **Descriptive Statistics**: Utilize `co2_emission_data` DataFrame to display the summary statistics for the column 'co2'.
    

#### Section 2: Indexing, Selecting, and Filtering

3. **Basic Indexing**: Extract the first five elements from the 'year' column of `co2_emission_data`.
    
4. **Using iloc**: Using iloc, select the second row and the third column of `co2_emission_data`.
    
5. **Using loc**: Retrieve all rows with columns 'country', 'year', and 'iso_code' from `co2_emission_data`.
    
6. **Filtering with loc**: Filter `co2_emission_data` to show rows where 'country' is 'Zimbabwe' and 'population' is less than or equal to 680,000.
    

#### Section 3: Summary Functions and Maps

7. **Unique Countries**: Find and display all unique country values in the `co2_emission_data` DataFrame.
    
8. **Mean CO2 Emission**: Calculate the mean of CO2 emissions ('co2' column) in metric tons from `co2_emission_data`.
    
9. **Mapping Years**: Apply the `classify_years` function to the 'year' column of `co2_emission_data` and display the result.
    

#### Section 4: Grouping, Sorting, and Data Types

10. **Grouping by Year**: Using `co2_emission_data`, find the minimum population per year using groupby on the 'year' column.
    
11. **Sorting Data**: Sort `co2_emission_data` by 'year' in descending order. Display the first five rows.
    
12. **Data Types**: Check and display the data type of the 'year' column in `co2_emission_data`. Convert this column to float64 data type.
    

#### Section 5: Missing Values and Combining Data

13. **Finding Null Values**: Find and count null values in the 'gdp' column of `co2_emission_data`.
    
14. **Fillna and Replace**: Replace null values in the 'gdp' column with 'Unknown'. Replace 'Zimbabwe' values in the 'country' column with 'Zimb'.
    
15. **Combining Data**: Describe the process of combining data using `pd.concat()` and `DataFrame.join()` functions in Pandas.