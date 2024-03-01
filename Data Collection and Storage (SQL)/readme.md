
### **Project description**


### You're working as an analyst for Zuber, a new ride-sharing company that's launching in Chicago. Your task is to find patterns in the available information. You want to understand passenger preferences and the impact of external factors on rides.


### Working with a database, you'll analyze data from competitors and test a hypothesis about the impact of weather on ride frequency.


### **Description of the data**


### A database with info on taxi rides in Chicago:


### `neighborhoods` table: data on city neighborhoods



1. `name`: name of the neighborhood
2. `neighborhood_id`: neighborhood code


### `cabs` table: data on taxis



1. `cab_id`: vehicle code
2. `vehicle_id`: the vehicle's technical ID
3. `company_name`: the company that owns the vehicle


### `trips` table: data on rides



1. `trip_id`: ride code
2. `cab_id`: code of the vehicle operating the ride
3. `start_ts`: date and time of the beginning of the ride (time rounded to the hour)
4. `end_ts`: date and time of the end of the ride (time rounded to the hour)
5. `duration_seconds`: ride duration in seconds
6. `distance_miles`: ride distance in miles
7. `pickup_location_id`: pickup neighborhood code
8. `dropoff_location_id`: dropoff neighborhood code


### `weather_records` table: data on weather



1. `record_id`: weather record code
2. `ts`: record date and time (time rounded to the hour)
3. `temperature`: temperature when the record was taken
4. `description`: brief description of weather conditions, e.g. "light rain" or "scattered clouds"


### **Table scheme**



![alt_text](Table_Scheme.png "image_tooltip")



### Note: there isn't a direct connection between the tables `trips` and `weather_records` in the database. But you can still use JOIN and link them using the time the ride started (`trips.start_ts`) and the time the weather record was taken (`weather_records.ts`).


### **Instructions on completing the project**


### Step 1. Write a code to parse the data on weather in Chicago in November 2017 from the website:


### [https://practicum-content.s3.us-west-1.amazonaws.com/data-analyst-eng/moved_chicago_weather_2017.html](https://practicum-content.s3.us-west-1.amazonaws.com/data-analyst-eng/moved_chicago_weather_2017.html)


### Step 2. Exploratory data analysis



1. Find the number of taxi rides for each taxi company for November 15-16, 2017. Name the resulting field `trips_amount` and print it along with the `company_name` field. Sort the results by the `trips_amount` field in descending order.
2. Find the number of rides for every taxi company whose name contains the words "Yellow" or "Blue" for November 1-7, 2017. Name the resulting variable `trips_amount`. Group the results by the `company_name` field.
3. In November 2017, the most popular taxi companies were Flash Cab and Taxi Affiliation Services. Find the number of rides for these two companies and name the resulting variable `trips_amount`. Join the rides for all other companies in the group "Other." Group the data by taxi company names. Name the field with taxi company names `company`. Sort the result in descending order by `trips_amount`.


### Step 3. Test the hypothesis that the duration of rides from the the Loop to O'Hare International Airport changes on rainy Saturdays.



1. Retrieve the identifiers of the O'Hare and Loop neighborhoods from the `neighborhoods` table.
2. For each hour, retrieve the weather condition records from the `weather_records` table. Using the CASE operator, break all hours into two groups: "Bad" if the `description` field contains the words "rain" or "storm," and "Good" for others. Name the resulting field `weather_conditions`. The final table must include two fields: date and hour (_ts_) and `weather_conditions`.
3. Retrieve from the `trips` table all the rides that started in the Loop (`neighborhood_id`: 50) and ended at O'Hare (`neighborhood_id`: 63) on a Saturday. Get the weather conditions for each ride. Use the method you applied in the previous task. Also retrieve the duration of each ride. Ignore rides for which data on weather conditions is not available.

**Step 4. Exploratory data analysis (Python)**

In addition to the data you retrieved in the previous tasks, you've been given a second file. You now have these two CSVs:

[/datasets/project_sql_result_01.csv](https://practicum-content.s3.us-west-1.amazonaws.com/learning-materials/data-analyst-eng/moved_project_sql_result_01.csv). It contains the following data:

_company_name_: taxi company name

_trips_amount_: the number of rides for each taxi company on November 15-16, 2017.

[/datasets/project_sql_result_04.csv](https://practicum-content.s3.us-west-1.amazonaws.com/learning-materials/data-analyst-eng/moved_project_sql_result_04.csv). It contains the following data:

_dropoff_location_name_: Chicago neighborhoods where rides ended

_average_trips_: the average number of rides that ended in each neighborhood in November 2017.

For these two datasets you now need to



* import the files
* study the data they contain
* make sure the data types are correct
* identify the top 10 neighborhoods in terms of drop-offs
* make graphs: taxi companies and number of rides, top 10 neighborhoods by number of drop offs
* draw conclusions based on each graph and explain the results

**Step 5. Testing hypotheses (Python)**

[/datasets/project_sql_result_07.csv](https://practicum-content.s3.us-west-1.amazonaws.com/learning-materials/data-analyst-eng/moved_project_sql_result_07.csv) — the result of the last query. It contains data on rides from the Loop to O'Hare International Airport. Remember, these are the table's field values:



1. _start_ts_
    1. pickup date and time
2. _weather_conditions_
    2. weather conditions at the moment the ride started
3. _duration_seconds_
    3. ride duration in seconds

Test the hypothesis:

"The average duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays."

Decide where to set the significance level (alpha) on your own.

Explain:



* how you formed the null and alternative hypotheses
* what criteria you used to test the hypotheses and why

## **Conclusion and Recommendations**

Following the analysis conducted for Zuber, the new ride-sharing company in Chicago, several key insights were obtained:

1. **Top Taxi Companies**: Through analysis, we identified the top-performing taxi companies in the area, providing valuable competitive intelligence for Zuber to consider in its strategic planning.

2. **Popular Neighborhoods**: By analyzing drop-off data, we determined the top 10 neighborhoods where rides are most frequently requested. This information can help Zuber focus its marketing and operational efforts in these high-demand areas.

3. **Impact of Weather**: We investigated the relationship between ride duration and weather conditions. Our analysis revealed that rides are more frequent during favorable weather conditions, suggesting that weather indeed plays a role in ride frequency.

4. **Hypothesis Testing**: We tested a hypothesis regarding the impact of weather on ride frequency, specifically on Saturdays. Contrary to the hypothesis, our analysis indicated that ride performance during Saturdays under different weather conditions was not statistically significant compared to overall trends.

## **Recommendations for Zuber:**

1. **Competitive Strategies**: Zuber should leverage insights about the top-performing taxi companies to inform its competitive strategies, whether through pricing, service quality, or marketing initiatives.

2. **Targeted Marketing**: Given the identified popular neighborhoods, Zuber can tailor its marketing efforts to these areas to attract more customers and increase market share.

3. **Weather-Responsive Operations**: While weather conditions were found to influence ride frequency, Zuber should consider implementing weather-responsive operational strategies, such as dynamic pricing or targeted promotions during inclement weather, to capitalize on fluctuations in demand.

4. **Further Analysis**: Zuber should continue to explore and analyze additional factors that may influence ride patterns, such as time of day, events, or local regulations, to further optimize its service offerings and enhance customer satisfaction.

By leveraging these insights and recommendations, Zuber can make informed decisions to effectively position itself in the competitive ride-sharing market in Chicago.
