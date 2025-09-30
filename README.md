# DFB-Pokal Analysis Project

## Overview

This project provides a comprehensive data analysis of the **DFB-Pokal** (German Football Cup) from the 2014-15 to 2023-24 seasons. The study examines whether the DFB-Pokal follows its own rules by analyzing various factors that influence match outcomes when teams from different divisions compete, culminating in a predictive machine learning model.

## Research Questions

The main research question explored in this project is: **"Does the DFB-Pokal have its own rules?"**

The analysis investigates several key factors:

1. **Team Performance Differences**: Win rates between DFB-Pokal matches vs regular league matches
2. **Team Form Analysis**: Impact of recent performance on match outcomes
3. **Scheduling Pressure**: Effects of fixture congestion and rest days
4. **Division Disparities**: Cross-division match outcome patterns
5. **Predictive Modeling**: Machine learning approach to upset prediction
6. **Statistical Significance**: Hypothesis testing and regression analysis

## Data Sources

The project scrapes data from **Transfermarkt.de**, collecting:
- Match results and statistics
- Team information and stadium details
- Player data and squad valuations
- Match schedules and fixture lists

## Project Structure

```
├── notebook.ipynb                          # Main analysis notebook
├── requirements.txt                        # Python dependencies
├── DFB_Pokal_Comprehensive_Report.md      # Detailed findings report
├── datasets/
│   ├── final_datasets/                     # Cleaned and processed data
│   │   ├── cleaned_matches.csv            # All match data
│   │   ├── cleaned_players.csv            # Player information
│   │   ├── cleaned_teams.csv              # Team details
│   │   ├── dfb_matches.csv                # DFB-Pokal specific matches
│   │   ├── higher_win_cases.csv           # Upset analysis data
│   │   └── lineups.csv                    # Match lineups
│   ├── players/                           # Individual team player data
│   ├── schedules/                         # Team schedule data
│   └── teams/                             # Team information
├── figures/                               # Generated visualizations
│   ├── performance_evaluation.png         # Model performance plots
│   ├── confusion_matrix_final.png         # Classification results
│   ├── roc_curve_final.png               # ROC analysis
│   └── calibration_final.png             # Model calibration
├── presentations/                         # Project presentations
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

- `pandas>=1.3.0` - Data manipulation and analysis
- `numpy>=1.21.0` - Numerical computing
- `scikit-learn>=1.0.0` - Machine learning algorithms
- `matplotlib>=3.3.0` - Data visualization
- `seaborn>=0.11.0` - Statistical data visualization
- `requests>=2.25.0` - Web scraping
- `beautifulsoup4>=4.9.0` - HTML parsing
- `lxml>=4.6.0` - XML/HTML parser

## Analysis Highlights

### 1. Exploratory Data Analysis
- **Win Rate Comparison**: DFB-Pokal vs regular league performance
- **Division Analysis**: Cross-division match outcome patterns
- **Temporal Trends**: Seasonal and historical upset patterns
- **Home Advantage**: Stadium effects and geographical factors

### 2. Statistical Analysis
- **Form Metrics**: Recent performance indicators (last 10 games)
- **Schedule Impact**: Rest days and fixture congestion effects
- **T-tests and Significance**: Statistical validation of findings
- **Distribution Analysis**: Pattern identification in upsets

### 3. Machine Learning Model
- **Logistic Regression**: Predictive model for upset probability
- **Feature Engineering**: Advanced interaction terms
- **Cross-Validation**: Leave-one-season-out validation
- **Performance Metrics**: AUC, accuracy, and calibration analysis

### 4. Key Features Analyzed
- **Team Form Differences**: Recent performance gaps
- **Attacking Form**: Goal-scoring trends
- **Defensive Form**: Defensive stability metrics
- **Schedule Pressure**: Rest days and recent game load
- **Interaction Effects**: Combined feature impacts

## Key Findings

### Statistical Insights
- **Upset Rate**: Lower division teams win approximately 27.5% of cross-division matches
- **Form Impact**: Recent performance significantly influences upset probability
- **Schedule Effects**: Fixture congestion affects higher-division teams differently
- **Seasonal Consistency**: Upset patterns remain relatively stable across seasons

### Machine Learning Results
- **Model Performance**: Achieved meaningful predictive accuracy with AUC > 0.6
- **Feature Importance**: Defensive form and schedule interactions show significant impact
- **Cross-Validation**: Robust performance across different seasons
- **Interaction Effects**: Combined features provide better predictions than individual metrics

### DFB-Pokal's "Own Rules"
The analysis confirms that the DFB-Pokal indeed operates under different dynamics than regular league play, with measurable factors contributing to its reputation as an "upset-friendly" tournament.

## Data Coverage

- **Temporal Scope**: 2014-15 to 2023-24 seasons (10 years)
- **Total Matches**: Over 41,000 matches analyzed
- **DFB-Pokal Focus**: 664 cup matches with detailed analysis
- **Cross-Division Matches**: 149 matches used for machine learning model
- **Teams**: Comprehensive coverage across all German football divisions
- **Features**: 5 base features + 4 interaction terms for modeling

## Usage

The notebook is structured for comprehensive analysis:

1. **Data Collection**: Automated scraping from Transfermarkt.de
2. **Data Preprocessing**: Cleaning and standardization of raw data
3. **Exploratory Analysis**: Statistical summaries and initial visualizations
4. **Form Analysis**: Team performance metrics and trend analysis  
5. **Schedule Analysis**: Rest days and fixture congestion impact
6. **Statistical Testing**: Hypothesis testing and significance analysis
7. **Machine Learning**: Predictive modeling with logistic regression
8. **Model Evaluation**: Performance assessment and validation
9. **Results Interpretation**: Statistical and practical significance

### Running the Analysis

```bash
# Install dependencies
pip install -r requirements.txt

# Open the main notebook
jupyter notebook notebook.ipynb
# or
code notebook.ipynb  # for VS Code
```

### Reproducing Results

The notebook is designed to be fully reproducible. All data processing steps are included, and the analysis can be run from start to finish. Pre-processed datasets are available in the `datasets/final_datasets/` directory for quick access.

## Methodology

### Data Collection
- **Source**: Transfermarkt.de web scraping
- **Scope**: German football teams across all divisions
- **Period**: 10 seasons (2014-15 to 2023-24)
- **Validation**: Data cleaning and consistency checks

### Feature Engineering
- **Team Form**: Points earned in last 10 matches
- **Attacking Form**: Goals scored in recent games
- **Defensive Form**: Goals conceded metrics
- **Schedule Pressure**: Rest days and fixture density
- **Interaction Terms**: Combined feature effects

### Machine Learning Approach
- **Algorithm**: Logistic Regression with regularization
- **Validation**: Leave-One-Season-Out Cross-Validation
- **Features**: 5 base + 4 interaction terms (9 total)
- **Target**: Binary classification (upset vs expected result)
- **Preprocessing**: StandardScaler normalization

### Statistical Methods
- **Hypothesis Testing**: Welch's t-tests for group comparisons
- **Significance Testing**: 95% confidence intervals
- **Effect Sizes**: Practical significance assessment
- **Distribution Analysis**: Pattern identification and validation

## Contributing

This is an academic research project. For suggestions or improvements, please open an issue or submit a pull request.

## License

This project is for educational and research purposes. Please respect Transfermarkt's terms of service when using their data.

## Acknowledgments

- Data sourced from Transfermarkt.de
- Analysis conducted as part of university research 
