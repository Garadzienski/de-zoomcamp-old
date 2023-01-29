# The code from the first homework SQL/DOCKER 

### **Question 3. Count records**
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

### **Question 4. Largest trip for each day**
#### Which was the day with the largest trip distance Use the pick up time for your calculations?
\
SELECT
	lpep_pickup_datetime::DATE
	,MAX(trip_distance) AS max_distance
FROM
	green_taxi_data
GROUP BY
	lpep_pickup_datetime::DATE
ORDER BY
	max_distance DESC
LIMIT 1

### **Question 5. The number of passengers**
#### In 2019-01-01 how many trips had 2 and 3 passengers?
