## **Project description**

You work for the online store Ice, which sells video games all over the world. User and expert reviews, genres, platforms (e.g. Xbox or PlayStation), and historical data on game sales are available from open sources. You need to identify patterns that determine whether a game succeeds or not. This will allow you to spot potential big winners and plan advertising campaigns.

In front of you is data going back to 2016. Let’s imagine that it’s December 2016 and you’re planning a campaign for 2017.

(The important thing is to get experience working with data. It doesn't really matter whether you're forecasting 2017 sales based on data from 2016 or 2017 sales based on data from 2016.)

The dataset contains the abbreviation ESRB. The Entertainment Software Rating Board evaluates a game's content and assigns an age rating such as Teen or Mature.

## Conclusion

In this project, I worked for the online store Ice, which sells video games worldwide. The dataset available contained user and expert reviews, genres, platforms (e.g., Xbox or PlayStation), and historical data on game sales, spanning back to 2016. The goal was to identify patterns that determine whether a game succeeds or not, enabling the identification of potential big winners and the planning of advertising campaigns for 2017.

### Data Analysis:

- Utilizing the open-source dataset up to 2016, we conducted a comprehensive analysis to understand the performance and behavior of the video games industry.
- Hypothesis tests were performed to compare the performance of different genres and platforms, confirming that certain genres and platforms exhibited similar market performance.
- The analysis revealed that the top platforms for game demand were PS4, PS3, XOne, 3DS, and X360.
- Action, Shooter, Sports, Role-Playing, and Miscellaneous were identified as the genres with the highest sales.
- Games with ratings of M, E, T, and E10+ were found to have the highest demand.

### Version 2 (V2) Update:

- After refining the analysis to focus on sales data from 2013 onwards, a clear trend in platform discontinuity was observed, leading to the exclusion of data prior to 2013 for prediction calculations.
- Hypothesis testing results indicated that the genres of Action and Sports were significantly different in performance.

### Recommendations:

1. **Focus on High-Demand Platforms and Genres**: Ice should prioritize stocking games for platforms like PS4, PS3, XOne, 3DS, and X360, as well as genres such as Action, Shooter, Sports, Role-Playing, and Miscellaneous to maximize sales potential.

2. **Targeted Marketing Strategies**: Develop targeted advertising campaigns tailored to the preferences of the identified target audience for each genre and platform.

3. **Continuous Monitoring and Analysis**: Regularly update the analysis to adapt to changing market trends and consumer preferences, ensuring that Ice remains responsive to shifts in the video game industry landscape.

4. **Enhanced Data Quality Assurance**: Implement measures to ensure data accuracy and completeness, particularly regarding user and expert reviews and sales data, to improve the reliability of future analyses and predictions.

By implementing these recommendations, Ice can position itself strategically to capitalize on emerging opportunities and drive sustained growth in the competitive video game market.

### **Instructions for completing the project**

**Step 1. Open the data file and study the general information**

File path:

_/datasets/games.csv_ .[ Download dataset](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/moved_games.csv)

**Step 2. Prepare the data**



* Replace the column names (make them lowercase).
* Convert the data to the required types.
* Describe the columns where the data types have been changed and why.
* If necessary, decide how to deal with missing values:
    * Explain why you filled in the missing values as you did or why you decided to leave them blank.
    * Why do you think the values are missing? Give possible reasons.
    * Pay attention to the abbreviation TBD (to be determined). Specify how you intend to handle such cases.
* Calculate the total sales (the sum of sales in all regions) for each game and put these values in a separate column.

**Step 3. Analyze the data**



* Look at how many games were released in different years. Is the data for every period significant?
* Look at how sales varied from platform to platform. Choose the platforms with the greatest total sales and build a distribution based on data for each year. Find platforms that used to be popular but now have zero sales. How long does it generally take for new platforms to appear and old ones to fade?
* Determine what period you should take data for. To do so, look at your answers to the previous questions. The data should allow you to build a prognosis for 2017.
* Work only with the data that you've decided is relevant. Disregard the data for previous years.
* Which platforms are leading in sales? Which ones are growing or shrinking? Select several potentially profitable platforms.
* Build a box plot for the global sales of all games, broken down by platform. Are the differences in sales significant? What about average sales on various platforms? Describe your findings.
* Take a look at how user and professional reviews affect sales for one popular platform (you choose). Build a scatter plot and calculate the correlation between reviews and sales. Draw conclusions.
* Keeping your conclusions in mind, compare the sales of the same games on other platforms.
* Take a look at the general distribution of games by genre. What can we say about the most profitable genres? Can you generalize about genres with high and low sales?

**Step 4. Create a user profile for each region**

For each region (NA, EU, JP), determine:



1. The top five platforms. Describe variations in their market shares from region to region.
2. The top five genres. Explain the difference.
3. Do ESRB ratings affect sales in individual regions?

**Step 5. Test the following hypotheses**:

—Average user ratings of the Xbox One and PC platforms are the same.

—Average user ratings for the Action and Sports genres are different.

Set the _alpha_ threshold value yourself.

Explain:

—How you formulated the null and alternative hypotheses

—What significance level you chose to test the hypotheses, and why

**Step 6. Write a general conclusion**

Format: Complete the task in the Jupyter Notebook. Insert the programming code in the _code_ cells and text explanations in the _markdown_ cells. Apply formatting and add headings.


### **Data description**

—_Name_

—_Platform_

—_Year_of_Release_

—_Genre_

—_NA_sales_ (North American sales in USD million)

—_EU_sales_ (sales in Europe in USD million)

—_JP_sales_ (sales in Japan in USD million)

—_Other_sales_ (sales in other countries in USD million)

—_Critic_Score_ (maximum of 100)

—_User_Score_ (maximum of 10)

—_Rating_ (ESRB)

Data for 2016 may be incomplete.
