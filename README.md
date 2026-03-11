# DFB-Pokal Analysis Project

## Overview

This project provides a comprehensive data analysis of the **DFB-Pokal** (German Football Cup) from the 2014-15 to 2023-24 seasons. The study examines whether the DFB-Pokal follows its own rules by analyzing factors that influence match outcomes when teams from different divisions compete.

The repository now includes a unified project notebook that combines teammate and individual work into one end-to-end analysis flow.

## Research Question

The main research question explored in this project is: **"Does the DFB-Pokal have its own rules?"**

The analysis investigates key factors:

1. **Team Performance Differences**: Win rates in DFB-Pokal vs regular league matches
2. **Team Value Differences**: Impact of squad valuation gaps on outcomes
3. **Scheduling Pressure**: Effects of rest time and fixture congestion
4. **Squad Rotation**: Relationship between lineup changes and match results
5. **Team Form**: Recent attacking/defensive performance impact
6. **Home Advantage**: Stadium and hosting effects

## Notebook Workflow

### Primary Notebook (Start Here)
- `project_overview_notebook.ipynb`  
  Combined project notebook for full analysis and presentation.

### Supporting Notebooks
- `Stadiums/Teams&Stadiums.ipynb`  
  Team, stadium, and home-advantage related analysis.
- `matches&lineups/matches&lineups.ipynb`  
  Match and lineup-focused analysis.

### Baseline Notebook
- `notebook.ipynb`  
  Teammate's original core notebook used as the base for the merged overview notebook.

## Data Sources

The project scrapes and processes data from **Transfermarkt.de**, including:
- Match results and schedules
- Team and stadium information
- Player and lineup data
- Competition context and seasonal records

## Project Structure

```text
DFB-Cup/
├── project_overview_notebook.ipynb      # Main combined notebook (recommended)
├── notebook.ipynb                       # Teammate baseline notebook
├── Stadiums/
│   ├── Teams&Stadiums.ipynb             # Stadiums/teams analysis notebook
│   └── Smnr_Teams&Stadiums_cleaned.ipynb
├── matches&lineups/
│   └── matches&lineups.ipynb            # Matches/lineups analysis notebook
├── datasets/
│   ├── final_datasets/
│   │   ├── cleaned_matches.csv
│   │   ├── cleaned_players.csv
│   │   ├── dfb_matches.csv
│   │   ├── final_cleaned_teams.csv
│   │   ├── higher_win_cases.csv
│   │   ├── lineups.csv
│   │   └── teams_stadiums_ratings.csv
│   ├── lineups/
│   │   ├── higher_win_cases.csv
│   │   └── lineups.csv
│   ├── players/
│   ├── schedules/
│   └── teams/
└── requirements.txt
```

## Key Datasets

### `cleaned_matches.csv`
Complete match-level dataset including date, teams, scores, and competition context.

### `dfb_matches.csv`
DFB-Pokal specific matches with division-level matchup information and round context.

### `final_cleaned_teams.csv`
Team-level dataset including stadium and structural team information.

### `cleaned_players.csv`
Player-level attributes linked to clubs and seasons.

### `lineups.csv`
Lineup-level match participation data used for rotation and squad usage analysis.

### `teams_stadiums_ratings.csv`
Team and stadium-derived rating features supporting home-advantage and environment analysis.

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
   Open `project_overview_notebook.ipynb` in Jupyter Notebook or VS Code.

## Dependencies

- `requests` - Data collection from web sources
- `beautifulsoup4` - HTML parsing for scraping
- `pandas` - Data processing and analysis
- `lxml` - HTML/XML parsing backend

## Analysis Highlights

### 1. Win Rate Analysis
Compares team behavior between cup and league contexts.

### 2. Division Disparity Analysis
Evaluates outcomes for cross-division matchups.

### 3. Schedule Pressure Analysis
Measures impact of rest windows and fixture congestion.

### 4. Lineup and Rotation Analysis
Assesses squad usage, lineup changes, and performance effects.

### 5. Team/Stadium Context Analysis
Investigates home conditions, stadium factors, and team-level context.

## Data Coverage

- **Seasons**: 2014-15 to 2023-24
- **Matches**: Over 41,000 total matches analyzed
- **DFB-Pokal Matches**: 664 cup matches
- **Teams**: Broad coverage of German clubs across divisions

## Usage

Use the combined notebook for the full project narrative:

1. Data preparation and integration
2. Cup-vs-league comparative analysis
3. Lineup/scheduling effect analysis
4. Team and stadium context analysis
5. Final findings and visual summaries

For module-level deep dives, use the two supporting notebooks in `Stadiums/` and `matches&lineups/`.

## Contributing

This is an academic research project. For suggestions or improvements, open an issue or submit a pull request.

## License

This project is for educational and research purposes. Please respect Transfermarkt's terms of service when using derived data.

## Acknowledgments

- Data sourced from Transfermarkt.de
- Analysis developed as part of university research
