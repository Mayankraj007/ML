# Prediction of winner of FIFA World Cup football matches using  the historical statistics. The prediction should be for  2022 and 2026 World Cups

Abstract: FIFA World Cup Match Outcome Prediction Using Historical Data and Poisson Model
This report presents the development of a data-driven approach to predict FIFA World Cup match outcomes, leveraging historical match data, player statistics, and predictive modeling techniques. The project integrates datasets containing match results, fixtures, and player attributes to analyze trends, build forecasts, and generate outcome predictions using statistical modeling.

Data Cleaning and Preparation
The project involved the utilization of three primary datasets:

Historical Match Data: Capturing match outcomes from previous FIFA World Cups, including information such as the teams involved, match scores, and dates.
Fixture Data: Featuring upcoming World Cup match fixtures.
Supplementary Match Data: Providing additional match records for missing or incomplete data.
Key preprocessing steps included:

Handling Missing Data: Missing records were addressed by removing incomplete entries and augmenting the dataset with external data sources.
Deduplication: Duplicate rows were dropped to avoid skewed results.
Standardization: Team names were stripped of extra spaces and standardized.
Score Normalization: Scores were cleaned and split into separate HomeGoals and AwayGoals columns, facilitating further analysis.
Dataset Transformation
After cleaning the dataset, the following transformations were applied:

Splitting the score column into HomeGoals and AwayGoals.
Introducing a new column TotalGoals to represent the combined goals from both teams.
Renaming columns for clarity, ensuring uniformity across datasets.
Historical Match Analysis
The dataset’s integrity was confirmed by cross-referencing match counts with official FIFA records (e.g., 18 matches from 1930 and 64 matches from 2018). An example analysis focused on Turkey’s performance in specific World Cups (1954 and 2002) to highlight the usefulness of this approach for team performance evaluation.

Player Data Analysis
Player statistics were incorporated to measure team performance. Players from competing national teams were analyzed, and injured or absent players (e.g., Benzema, Mané, Aguero) were excluded for real-world accuracy. Player attributes such as overall rating, potential, value, and wage were assessed to determine each team's strength.

A ranking was generated based on player ratings, highlighting the top teams by average player performance. The top five teams—Spain, Portugal, England, Brazil, and France—emerged as having the strongest squads.

Model and Predictive Strategies
The Poisson Regression Model was chosen as the primary method for predicting match outcomes. This model is widely used for sports predictions, particularly football, due to its suitability for modeling the distribution of rare events (such as goals in football matches).

Poisson Model Overview:

The model assumes that the number of goals scored by a team follows a Poisson distribution.
The model uses historical data to estimate the average number of goals a team is expected to score in a match, depending on factors like team strength, opposition strength, home advantage, and historical goal-scoring trends.
Key Strategies Used:

Data-Driven Model Construction: Historical match outcomes, goals scored, and player attributes formed the foundation of the Poisson model. Home and away goals were treated as separate variables to ensure precision in prediction.
Feature Engineering: Key features such as home advantage, team strength, and player performance were integrated into the model. Player data such as average overall rating provided a proxy for team strength.
Team Performance Scaling: The model scaled team performance using average player attributes and past performance in World Cups, accounting for injured or absent players to ensure realistic predictions.
Goal Expectancy Calculation: The Poisson model was applied to calculate the expected number of goals for each team in a given match, allowing for probability distributions to predict match outcomes (win, draw, loss).
Results and Insights
The Poisson regression approach allowed for the estimation of the likelihood of different match outcomes, such as:

Win probabilities for each team based on their goal-scoring history.
Expected number of goals in future fixtures, leveraging both historical match data and current player statistics.
Conclusion
By combining a comprehensive data cleaning and preparation process with Poisson regression modeling, this project successfully developed a predictive system for FIFA World Cup match outcomes. The results of the model can be further refined with advanced machine learning techniques or additional features, aiming to improve accuracy in forecasting future match results. The analysis of historical trends and player attributes provided a strong foundation for predicting the future outcomes of World Cup matches.
