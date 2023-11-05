#1 Earliest date in case_info table?

SELECT

MIN(c_info_data.DateRepConf) as min_date

  

FROM dabc10-387511.mock_exam.case_info AS c_info_data;

  

#2 How many rows are there in total in the 'testing_aggregates' table?

#no need for query

  

#3 Which table is better suited to find the profile of people infected with COVID?

#no need for query

  

#4 How many unique non-null regions are there in the case_info table?

SELECT

COUNT(DISTINCT(c_info_data.RegionRes)) as number_of_unique_regions

  

FROM dabc10-387511.mock_exam.case_info AS c_info_data

  

WHERE c_info_data.RegionRes IS not null;

#6 Which table is better suited to find the profile of people infected with COVID?

#no need for query

  

#7 How many unique non-null facilities are there in the testing_aggregates table??

SELECT

COUNT(DISTINCT(ta_data.facility_name)) as number_of_unique_facilities

  

FROM dabc10-387511.mock_exam.testing_aggregates ta_data

  

WHERE ta_data.facility_name IS NOT NULL;

  

#8 Show the split between gender in the total confirmed cases. Include only the following months: March 2020, June 2020, Sept 2020, Dec 2020. Order results by earliest date first, then by gender ascending (i.e. Female before Male).

#What will be the date and gender in the first row of your output?

SELECT

c_info_data.DateRepConf,

c_info_data.Sex,

  

FROM dabc10-387511.mock_exam.case_info AS c_info_data

  

WHERE

FORMAT_TIMESTAMP('%Y-%m', c_info_data.DateRepConf) IN ('2020-03','2020-06','2020-12')

  

ORDER BY

c_info_data.DateRepConf ASC, c_info_data.Sex ASC;

  

#9 Which months and facilities registered a total monthly increase in positive tests > 5000? Order results by highest monthly increase first.

#What is the facility name of the first row of your output?

SELECT

DATE_TRUNC(ta_data.report_date,MONTH) AS Month,

ta_data.facility_name,

SUM(ta_data.daily_output_positive_individuals) AS monthly_sum_positive_individuals

FROM dabc10-387511.mock_exam.testing_aggregates ta_data

GROUP BY

1,2

HAVING

monthly_sum_positive_individuals > 5000

ORDER BY

monthly_sum_positive_individuals DESC;

  

#10 Which months and regions registered more than 2000 unique male cases? Consider only 'NCR' and 'Region IV-A: CALABARZON'. Order results by count of unique male cases ascending

#What is the count of the unique male cases in the first row of your output?

SELECT

DATE_TRUNC(c_info_data.DateRepConf,MONTH) as Month,

c_info_data.RegionRes,

COUNT(c_info_data.CaseCode) as count_of_male_cases

  

FROM dabc10-387511.mock_exam.case_info AS c_info_data

  

WHERE

c_info_data.Sex ='MALE'AND

c_info_data.RegionRes IN ('NCR','Region IV-A: CALABARZON')

  

GROUP BY

1,2

  

ORDER BY count_of_male_cases ASC;

  

#11. As of October 31,2020, which facility registered the highest cumulative positivity rate? Show the negativity rate as well. For facilities where cumulative tests is 0, assume that the positivity rate is 0, and negativity rate is 1.

SELECT

ta_data.report_date,

ta_data.facility_name,

  

ta_data.cumulative_negative_individuals/cumulative_unique_individuals as cumulative_negativitiy_rate,

#cumulative_positivity_rate

CASE

      WHEN  ta_data.cumulative_unique_individuals > 0 THEN ta_data.cumulative_positive_individuals/cumulative_unique_individuals

      ELSE 0

END AS cumulative_positivity_rate,

#cumulative_negativity_rate

CASE

      WHEN  ta_data.cumulative_unique_individuals > 0 THEN ta_data.cumulative_negative_individuals/cumulative_unique_individuals

      ELSE 1

END AS cumulative_negativitiy_rate,

  

FROM dabc10-387511.mock_exam.testing_aggregates ta_data

  

WHERE

DATE(ta_data.report_date) = DATE('2020-10-31') AND

cumulative_unique_individuals > 0

  

ORDER BY cumulative_positivity_rate DESC;