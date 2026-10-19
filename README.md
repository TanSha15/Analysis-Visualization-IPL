# IPL 2022 Exploratory Data Analysis (EDA)

## Project Overview

The Indian Premier League (IPL) is a professional Twenty20 cricket league in India featuring franchise teams representing different cities. This project focuses on Exploratory Data Analysis (EDA) of IPL 2022 match-level data to identify patterns, analyze team performance, evaluate individual player contributions, and understand factors associated with match outcomes.

Using Python and its data analysis libraries, this project explores match results, toss decisions, batting and bowling performances, winning margins, and venue statistics to derive meaningful insights from the IPL 2022 season.

## Project Objectives

- Analyze match wins across all participating teams.
- Examine toss decisions and their relationship with match outcomes.
- Compare victories achieved by runs and wickets.
- Identify players with the most Player of the Match awards.
- Analyze top individual batting performances.
- Evaluate bowling performances using wickets taken.
- Identify venues that hosted the most matches.
- Investigate the largest winning margins and best bowling figures.
- Create visualizations to communicate findings effectively.

## Dataset Description

The dataset, `IPL.csv`, contains match-level information from IPL 2022.

| Property | Details |
|---|---|
| Dataset | IPL.csv |
| Season | IPL 2022 |
| Total Matches | 74 |
| Total Columns | 20 |
| Missing Values | None in the original dataset |
| Data Type | Match-level cricket data |

### Important Columns

| Column | Description |
|---|---|
| `match_id` | Unique identifier for each match |
| `date` | Date on which the match was played |
| `venue` | Stadium where the match took place |
| `team1` | First participating team |
| `team2` | Second participating team |
| `stage` | Stage of the tournament |
| `toss_winner` | Team that won the toss |
| `toss_decision` | Decision to bat or field |
| `first_ings_score` | First innings total score |
| `first_ings_wkts` | Wickets lost in the first innings |
| `second_ings_score` | Second innings total score |
| `second_ings_wkts` | Wickets lost in the second innings |
| `match_winner` | Team that won the match |
| `won_by` | Victory method: runs or wickets |
| `margin` | Winning margin |
| `player_of_the_match` | Player awarded Player of the Match |
| `top_scorer` | Player with the highest individual score in the match |
| `highscore` | Highest individual score recorded in the match |
| `best_bowling` | Bowler with the best recorded bowling performance |
| `best_bowling_figure` | Bowling figures in wickets-runs format |

## Technologies and Libraries

- **Python** – Programming language for data analysis.
- **Pandas** – Data loading, manipulation, grouping, and aggregation.
- **NumPy** – Numerical computations and data operations.
- **Matplotlib** – Data visualization and chart creation.
- **Seaborn** – Statistical visualization and comparative analysis.
- **Jupyter Notebook** – Interactive environment for executing code and documenting findings.

## Project Workflow

### 1. Data Loading

Imported the required Python libraries and loaded the IPL 2022 dataset using Pandas.

### 2. Data Inspection

Examined the dataset using `head()`, `info()`, and `shape` to understand its structure, data types, and dimensions.

### 3. Data Quality Assessment

Checked for missing values using `isnull().sum()`. The original dataset contains no missing values across its 20 columns.

### 4. Exploratory Data Analysis

Performed descriptive analysis and created visualizations to investigate team performance, toss decisions, player statistics, bowling figures, and venue distributions.

### 5. Insight Generation

Used grouping, aggregation, sorting, and filtering to answer cricket-related analytical questions and identify notable trends.

## Key Analysis and Findings

### 1. Team Performance

Gujarat recorded the highest number of match wins in the dataset, followed by Rajasthan.

| Team | Matches Won |
|---|---:|
| Gujarat | 12 |
| Rajasthan | 10 |
| Bangalore | 9 |
| Lucknow | 9 |
| Delhi | 7 |
| Punjab | 7 |
| Kolkata | 6 |
| Hyderabad | 6 |
| Chennai | 4 |
| Mumbai | 4 |

A horizontal bar chart was used to compare the number of wins across teams.

### 2. Toss Decision Trends

Analyzed how frequently teams chose to bat or field after winning the toss. A count plot was used to visualize the distribution of toss decisions.

### 3. Toss Winner vs. Match Winner

Approximately **48.65% of matches** were won by the team that also won the toss.

This suggests that winning the toss did not automatically translate into winning the match during the analyzed season.

### 4. Winning Methods

Compared matches won by runs with matches won by wickets. A count plot was used to examine the distribution of the two victory methods and understand how teams secured their wins.

### 5. Player of the Match Awards

Kuldeep Yadav received the highest number of Player of the Match awards in the dataset, with four awards.

Other notable performers included:

- **Kuldeep Yadav:** 4 awards
- **Jos Buttler:** 3 awards
- Several other players received 2 awards each.

A horizontal bar chart was used to compare individual award counts.

### 6. Top Individual Batting Performances

Jos Buttler had the highest aggregated `highscore` value in the analysis, with 651, followed by Quinton de Kock with 377.

These values represent the sum of the `highscore` column grouped by `top_scorer`. They should not be interpreted as official season batting totals without validating the underlying records.

### 7. Best Bowling Performances

Bowling figures were analyzed by extracting the wickets component from `best_bowling_figure`.

| Bowler | Bowling Figures |
|---|---|
| Yuzvendra Chahal | 5/40 |
| Umran Malik | 5/25 |
| Wanindu Hasaranga | 5/18 |
| Jasprit Bumrah | 5/10 |

Jasprit Bumrah recorded the best figures among these performances, taking five wickets for 10 runs.

### 8. Venue Analysis

Wankhede Stadium in Mumbai hosted the highest number of matches in the dataset.

| Venue | Matches |
|---|---:|
| Wankhede Stadium, Mumbai | 21 |
| Dr DY Patil Sports Academy, Mumbai | 20 |
| Brabourne Stadium, Mumbai | 16 |
| Maharashtra Cricket Association Stadium, Pune | 13 |
| Eden Gardens, Kolkata | 2 |
| Narendra Modi Stadium, Ahmedabad | 2 |

A bar chart was used to compare the number of matches played at each venue.

### 9. Highest Victory Margin by Runs

Chennai recorded the largest victory by runs in the dataset, winning by **91 runs**.

This result was identified by filtering matches won by runs and sorting them by winning margin.

### 10. Highest Individual Score

Quinton de Kock recorded the highest individual score in the dataset, scoring **140 runs**.

### 11. Best Bowling Figures

The best bowling figures identified in the dataset were Jasprit Bumrah's **5 wickets for 10 runs (5/10)**.

The analysis also identified three other five-wicket performances by Yuzvendra Chahal, Umran Malik, and Wanindu Hasaranga.

## Visualizations

The project includes the following visualizations:

- Bar chart of match wins by team.
- Count plot of toss decisions.
- Count plot of victory methods.
- Horizontal bar chart of Player of the Match awards.
- Bar chart of aggregated high scores by batter.
- Horizontal bar chart of bowling wickets aggregated by bowler.
- Bar chart of matches played at each venue.

These visualizations make it easier to compare teams, identify outstanding individual performances, and understand patterns in the tournament data.

## How to Run the Project

### Prerequisites

- Python 3.x
- Jupyter Notebook
- IPL 2022 dataset (`IPL.csv`)

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
