# DFB-Pokal Analysis Project

## Overview

This project provides a comprehensive data analysis of the **DFB-Pokal** (German Football Cup) from the 2014-15 to 2023-24 seasons. The study examines whether the DFB-Pokal follows its own rules by analyzing various factors that influence match outcomes when teams from different divisions compete.

## Research Questions

The main research question explored in this project is: **"Does the DFB-Pokal have its own rules?"**

The analysis investigates several key factors:

1. **Team Performance Differences**: Win rates between DFB-Pokal matches vs regular league matches
2. **Team Value Differences**: Impact of squad valuations on match outcomes
3. **Scheduling Pressure**: Effects of fixture congestion and rest days
4. **Squad Rotation**: How lineup changes affect performance
5. **Team Form**: Recent goal-scoring and defensive performance
6. **Home Advantage**: Stadium capacity, atmosphere, and home form effects

## Data Sources

The project scrapes data from **Transfermarkt.de**, collecting:
- Match results and statistics
- Team information and stadium details
- Player data and squad valuations
- Match schedules and fixture lists

## Project Structure

```
├── notebook.ipynb              # Main analysis notebook
├── requirements.txt            # Python dependencies
├── datasets/
│   ├── final_datasets/         # Cleaned and processed data
│   │   ├── cleaned_matches.csv
│   │   ├── cleaned_players.csv
│   │   ├── cleaned_teams.csv
│   │   ├── dfb_matches.csv
│   │   ├── higher_win_cases.csv
│   │   └── lineups.csv
│   ├── players/               # Individual team player data
│   ├── schedules/             # Team schedule data
│   └── teams/                 # Team information and statistics
└── README.md
```

## Key Datasets

### cleaned_matches.csv
Complete match data including:
- Date and time
- Home and away teams
- Scores and attendance
- Competition and season information

### dfb_matches.csv
DFB-Pokal specific matches with:
- Division levels of competing teams
- Round information
- Match outcomes and statistics

### cleaned_teams.csv
Team information including:
- Stadium details (capacity, heating, field dimensions)
- Team links and identifiers

### cleaned_players.csv
Player data containing:
- Position information
- Team affiliations
- Seasonal data

## Installation and Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd DFB-Cup
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the analysis**
   Open `notebook.ipynb` in Jupyter Notebook or VS Code to explore the analysis.

## Dependencies

- `pandas` - Data manipulation and analysis
- `requests` - Web scraping
- `beautifulsoup4` - HTML parsing
- `matplotlib` - Data visualization
- `seaborn` - Statistical data visualization
- `numpy` - Numerical computing
- `scipy` - Statistical analysis
- `lxml` - XML/HTML parser

## Analysis Highlights

### 1. Win Rate Analysis
Compares team performance in DFB-Pokal matches versus regular league matches to identify teams that perform differently in cup competitions.

### 2. Division Disparity Impact
Analyzes outcomes when teams from different divisions (Bundesliga, 2. Bundesliga, 3. Liga, etc.) face each other.

### 3. Schedule Analysis
Examines the impact of:
- Days since last match
- Number of games in recent weeks
- Fixture congestion effects

### 4. Form Analysis
Evaluates team form through:
- Goals scored in last 10 matches
- Goals conceded in last 10 matches
- Recent performance trends

### 5. Home Advantage
Investigates factors such as:
- Stadium capacity and atmosphere
- Home team performance
- Field conditions and dimensions

## Key Findings

The analysis reveals various factors that influence DFB-Pokal outcomes, including:
- Significant differences in team performance between league and cup matches
- Impact of scheduling and fixture congestion on higher-division teams
- Role of team form and recent performance
- Home advantage variations across different division matchups

## Data Coverage

- **Seasons**: 2014-15 to 2023-24
- **Matches**: Over 41,000 total matches analyzed
- **DFB-Pokal Matches**: 664 cup matches specifically
- **Teams**: Comprehensive coverage of German football clubs across all divisions

## Usage

The notebook is structured for step-by-step analysis:

1. **Data Scraping**: Code for collecting data from Transfermarkt
2. **Data Cleaning**: Processing and standardizing the collected data
3. **Exploratory Analysis**: Initial data exploration and visualization
4. **Statistical Analysis**: Hypothesis testing and comparative analysis
5. **Visualization**: Charts and graphs illustrating key findings

## Contributing

This is an academic research project. For suggestions or improvements, please open an issue or submit a pull request.

## License

This project is for educational and research purposes. Please respect Transfermarkt's terms of service when using their data.

## Acknowledgments

- Data sourced from Transfermarkt.de
- Analysis conducted as part of university research 
