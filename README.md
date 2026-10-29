# MLB All-Star Selection Prediction

Data Wrangling assignment from my Diploma in Data Science (Apr 2026 semester). The goal is to predict whether a position player gets picked for the All-Star Game in a given season, using his batting stats, his profile and how his team did.

Most of the work was putting the data together from four tables: `batting`, `player`, `team` and `all_star`.

- Batting has one row per player per stint, so I grouped it into one row per player-season and dropped players with under 20 games
- Joined in player details, the team's win percentage and the All-Star flag
- Worked out batting average, and age and years of experience from the debut date
- Split into train and test before any cleaning, so missing values, outliers, encoding and scaling are all fitted on the training set only

Only about 1 in 10 player-seasons is an All-Star, so I compared a Logistic Regression model with a baseline that always predicts "not an All-Star". Accuracy is about the same (0.933 vs 0.928), but the baseline never finds a real All-Star and the model finds some. The notebook ends with what I would try next.

## Running it

The CSV files are not included. Put `batting.csv`, `player.csv`, `team.csv` and `all_star.csv` from the History of Baseball dataset in a folder called `csv` next to the notebook, then run all cells.
