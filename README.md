# Voter Turnout Analysis - India General Elections

Analysis of voter turnout patterns across 10 Indian constituencies for the 2014, 2019 and 2024 General Elections.

## About This Project

This project examines how voter participation has changed over three election cycles in major Indian cities. I selected 10 constituencies from different states to get a diverse picture of voting behavior across the country.

The main goals were:
- Create a clean dataset from Election Commission reports
- Build visualizations that tell the story of changing turnout
- Design an interactive dashboard for exploring the data

## Project Files

```
├── 01_Data_Exploration.ipynb     # Data cleaning and preparation
├── 02_Visualizations.ipynb       # Charts and graphs
├── 03_Dashboard.ipynb            # Interactive dashboard
├── cleaned_data/
│   ├── curated_voter_turnout_10_constituencies.xlsx
│   ├── curated_voter_turnout_10_constituencies.csv
│   └── [visualization images]
├── dataset/                      # Raw ECI data
├── requirements.txt              # Python dependencies
└── README.md
```

## Constituencies Analyzed

I picked these 10 constituencies to represent different regions:

| Constituency | State |
|-------------|-------|
| New Delhi | NCT of Delhi |
| Mumbai North | Maharashtra |
| Kolkata Dakshin | West Bengal |
| Chennai Central | Tamil Nadu |
| Bangalore South | Karnataka |
| Hyderabad | Telangana |
| Lucknow | Uttar Pradesh |
| Jaipur | Rajasthan |
| Patna Sahib | Bihar |
| Chandigarh | Chandigarh |

## Data Collection

Data comes from the Election Commission of India website (https://www.eci.gov.in/statistical-reports). I used the "PC Wise Voter Turnout" tables from each election year.

For 2014 and 2019 data, gender-wise elector counts weren't directly available, so I calculated them:
```
Electors_Male = Voters_Male / (Turnout_Male / 100)
```

The final dataset has 18 variables:
- 3 categorical: Year, State, Constituency Name
- 15 quantitative: various counts and turnout percentages

## Visualizations

The project includes four main visualizations:

1. **Line Chart** - Shows overall turnout trend from 2014 to 2024
2. **Grouped Bar Chart** - Compares male vs female turnout each year
3. **Heatmap** - Shows turnout by constituency and year
4. **Interactive Chart** - Bokeh-based chart with gender breakdown

Each visualization applies Gestalt principles like proximity (grouping related items), similarity (consistent colors), and continuity (line charts showing flow).

## Dashboard

The dashboard in `03_Dashboard.ipynb` combines all visualizations with a dropdown selector. You can pick any constituency to see its detailed breakdown.

## Running the Code

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebooks in Jupyter and run them in order (01, 02, 03)

## Tools Used

- Python 3.12
- Pandas for data handling
- Matplotlib and Seaborn for static charts
- Bokeh for interactive visualizations
- OpenPyXL for Excel file support

## References

- Election Commission of India: https://www.eci.gov.in/statistical-reports
- Storytelling with Data by Cole Nussbaumer Knaflic
- Course textbook: Data Visualization – Storytelling Using Data

---

Anik Das
