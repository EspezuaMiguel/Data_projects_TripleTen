# **Basic Python: Project**

In this project, you will work with data from the entertainment industry. You will study a dataset with records on movies and shows. The research will focus on the “Golden Age” of television, which began in 1999 with the release of _The Sopranos_ and is still ongoing.

The aim of this project is to investigate how the number of votes a title receives from IMDb users impacts its ratings. The assumption is that highly-rated shows (we will focus on TV shows, ignoring movies) released during the “Golden Age” of television also have the most votes.

This project is similar to the tasks you will be getting in your job as a data professional. Many business decisions are initially born as assumptions, your contribution as an expert in the data domain is to answer the question “Did the assumption formulated before the study appear to be true?”


## **Description of the data**

The data is stored in the file `/datasets/movies_and_shows.csv`.

**Description of columns:**



* `'name'` — first and last name of actor (director)
* `'character'` — character played (for actors)
* `'role '` — the person’s contribution to the title (it can be in the capacity either of actor or director)
* `'title '` — title of movie (show)
* `'type '` — show or movie
* `'genres'` — list of genres under which the movie (show) falls
* `'release_year'` — year when the movie (show) was released
* `'imdb_score'` — score on IMDb
* `'imdb_votes'` — votes on IMDb


## **Instructions for completing the project**

A template of a Jupyter Notebook is provided for you where you can write your code, along with descriptions of your analysis. To complete the project, you must fill in every code cell in the template and edit markdown cells where the template asks you to explain your results.

In later sprints, the work will be more independent. This time, to help you get started, we’ll provide a notebook containing:



* The project structure
* Guidelines for analysis
* Conclusions

Your project will consist of three stages:

**Stage 1**: Data overview. The notebook has pre-made cells with instructions for what kind of code to write, as well as text blocks where you can write your observations.

**Stage 2**: Data preprocessing. In this stage, you’ll clean up column names and address missing and duplicate values. Follow the outline provided in the notebook and be sure to write about your observations at the end of this section.

**Stage 3**: Data analysis. This is the meat of your project. Walk through the coding steps needed to evaluate the assumption and comment on your results in the appropriate blocks. Finally, summarize the overall project in the “Conclusion” section which is equal to the “Presenting Results” stage we mentioned in the lessons.

# Conclusion

## Project Overview

The project aimed to investigate the impact of the number of votes on IMDb ratings for TV shows during the "Golden Age" of television. This involved analyzing a dataset containing records on movies and shows, focusing on TV shows released between 1999 and the present. The project simulated real-world tasks by testing hypotheses related to user activity and music preferences in different cities based on the day of the week and time of day.

## Project Execution

### Stage 1: Data Overview
- The dataset was examined to understand its structure and contents.
- Initial observations were made regarding the distribution of data and potential issues such as missing values and duplicates.

### Stage 2: Data Preprocessing
- Column names were cleaned up for easier processing.
- Missing values were replaced with 'unknown' markers, and implicit duplicates in genre names were addressed.
- Observations were made regarding the potential impact of missing values on the analysis.

### Stage 3: Data Analysis
- Three hypotheses were tested:
  1. User activity differs depending on the day of the week and from city to city.
  2. On Monday mornings and Friday evenings, Springfield and Shelbyville residents listen to different genres.
  3. Springfield and Shelbyville listeners have different music preferences, with Springfield favoring pop and Shelbyville favoring rap.

### Hypothesis Testing Results:
1. **User Activity:** Springfield and Shelbyville showed different patterns of user activity depending on the day of the week, confirming the first hypothesis.
2. **Music Genre Preferences:** While there were slight differences in genre preferences between Springfield and Shelbyville on Monday mornings and Friday evenings, the overall top genres were similar in both cities, primarily dominated by pop music. However, the presence of missing values raised concerns about the reliability of the results.
3. **City Preferences:** There was not enough evidence to support the hypothesis that Springfield and Shelbyville have significantly different music preferences. Both cities demonstrated a preference for pop music, with rap not prominently featured in either city's top genres.

## Recommendations
1. **Data Integrity:** Address the issue of missing values to ensure the reliability of future analyses. Investigate the reasons for missing data and implement strategies to minimize its impact.
2. **Continuous Monitoring:** Regularly monitor data quality and refine analysis methodologies to adapt to changing patterns and data trends.
3. **Expanded Analysis:** Explore additional factors that may influence user behavior and music preferences, such as demographic data, geographic location, or time of day.

## Future Improvements
1. **Statistical Hypothesis Testing:** Implement more rigorous statistical hypothesis testing methodologies to validate findings and quantify the significance of observed trends.
2. **Data Augmentation:** Expand the dataset with additional sources of data to enhance the depth and breadth of analysis, providing more comprehensive insights into user behavior and preferences.
3. **Machine Learning Models:** Explore the use of machine learning algorithms to predict user behavior and preferences, enabling more accurate and proactive decision-making based on predictive analytics.

By addressing these recommendations and pursuing future improvements, the project outcomes can be further refined and expanded, ultimately providing valuable insights for decision-making in the entertainment industry.
