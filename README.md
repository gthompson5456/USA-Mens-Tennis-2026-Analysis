# USA-Mens-Tennis-2026-Analysis

This project analyzes the performance of American male tennis players at ATP Masters 1000 tournaments and Grand Slam events during the 2026 season.

The analysis is built in Python and Jupyter Notebook. It downloads and processes match data, identifies matches involving U.S. players, calculates player and match-level statistics, and presents the results through interactive Altair visualizations.

## See "OUTPUTS" folder for all visuals

## Project objectives

The project is designed to:

* Track American men throughout the 2026 Masters 1000 and Grand Slam calendar.
* Create one standardized record for each American player in each match.
* Compare player performance across tournaments, surfaces, rounds, and opponents.
* Evaluate serve performance, break-point performance, rankings, upsets, and match outcomes.
* Analyze deciding sets and tiebreak performance.
* Compare actual match results with ranking-based expectations.
* Preserve dated snapshots so that the season can be analyzed over time.
* Produce tables and charts that can be shared through GitHub.

## Tournaments included

The intended scope includes:

* ATP Masters 1000 events
* Australian Open
* Roland Garros
* Wimbledon
* US Open

Only completed or available 2026 matches involving at least one American male player are included in the player-centric analytical dataset.

## Data source

Match data is obtained from the [TennisMyLife Tennis Match Database](https://stats.tennismylife.org/tennis-match-database).

The notebook downloads the relevant CSV files, combines the available records, validates the data, removes duplicates, and filters the results to the tournaments and players included in the project.

This repository is an independent analytical project and is not affiliated with TennisMyLife, the ATP Tour, or the Grand Slam tournaments.

## How the project works

The notebook follows this general workflow:

1. Configure the analysis year, tournament scope, source files, and output folders.
2. Download the available 2026 match CSV files.
3. Combine historical and current-season records.
4. Standardize column names and data types.
5. Validate required fields and identify missing values.
6. Remove duplicate matches created by overlapping data sources or repeated refreshes.
7. Identify matches involving U.S. male players.
8. Reshape each match into a player-centric format.
9. Calculate match-level and player-level performance measures.
10. Parse match scores for set, deciding-set, and tiebreak analysis.
11. Compare actual results with ranking-based expectations.
12. Generate interactive Altair tables and visualizations.
13. Export processed datasets and dated result snapshots.

## Player-centric dataset

The final dataset contains one row for each American player’s participation in a match.

For example, when two Americans play each other, the match produces two player-centric records—one from each player’s perspective.

The analytical fields include:

* American player
* Opponent
* Win or loss
* Tournament and date
* Surface
* Round
* Match score
* Match duration
* Player and opponent rankings
* Ranking difference
* Aces
* Double faults
* First-serve percentage
* First-serve points won
* Second-serve points won
* Service points won
* Break points saved
* Break points converted
* Sets won and lost
* Tiebreaks played and won
* Deciding-set result
* Ranking-based expected result
* Actual performance compared with expectation

## Analysis features

### Player performance

The notebook summarizes each player’s:

* Matches played
* Wins and losses
* Win percentage
* Performance by surface
* Performance by tournament
* Tournament finishing round
* Results over time

### Serve performance

Serve analysis includes:

* Aces and double faults
* First-serve percentage
* First-serve points won
* Second-serve points won
* Overall service points won
* Break-point save percentage

### Return and break-point performance

The project measures:

* Break-point opportunities
* Break points converted
* Break-point conversion percentage
* Opponent break-point pressure
* Performance in high-leverage situations

### Ranking analysis

Each match compares the American player’s ranking with the opponent’s ranking.

Matches are classified to identify:

* Expected wins
* Expected losses
* Upset victories
* Losses to lower-ranked opponents
* Actual results compared with ranking-based expectations

Ranking-based expectations are intended as an analytical benchmark rather than a calibrated prediction or betting model.

### Score and clutch analysis

The notebook parses match scores from the American player’s perspective to study:

* Sets won and lost
* Straight-set results
* Deciding-set matches
* Deciding-set wins and losses
* Tiebreaks played
* Tiebreaks won and lost
* Tiebreak win percentage

Walkovers, retirements, incomplete scores, and unusual scoring formats may require special handling.

## Visualizations

The visualization section uses Altair to create interactive charts and drill-down views.

Planned or included visualizations cover:

* Win percentage by American player
* Win percentage by surface
* First-serve and second-serve effectiveness
* Wins over higher-ranked opponents
* Tournament performance
* Cumulative win percentage over time
* Deciding-set and tiebreak performance
* Actual results compared with ranking-based expectations

Altair charts can be saved as standalone HTML files for interactive viewing. PNG versions can also be exported for display directly in this README.
