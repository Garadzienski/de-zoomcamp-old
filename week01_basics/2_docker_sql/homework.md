# The code from the first homework SQL/DOCKER 

## **Question 3. Count records**
#### How many taxi trips were totally made on January 15? 
Tip: started and finished on 2019-01-15. 
\
\
SELECT 
	COUNT(1) 
FROM 
	green_taxi_data 
WHERE 
	lpep_pickup_datetime::DATE = '2019-01-15' 
	AND 
	lpep_dropoff_datetime::DATE = '2019-01-15;
