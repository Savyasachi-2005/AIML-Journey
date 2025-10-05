# IPL Data Analysis with Pandas

This repository focuses on **exploratory data analysis (EDA)** of Indian Premier League (IPL) matches and ball-by-ball deliveries to **learn and practice Pandas**, with visualizations in **Matplotlib** and **Seaborn** where useful.

## 📹 Learning Resources

**YouTube Playlist:** [Pandas Tutorial Series](https://youtube.com/playlist?list=PLKnIA16_RmvbR85fgbfVRKOiMokUKVupy&si=dPAmRaWZvm5LanrA)

**Pandas Documentation:** [Official Pandas Docs](https://pandas.pydata.org/docs/)
- [User Guide](https://pandas.pydata.org/docs/user_guide/index.html)
- [API Reference](https://pandas.pydata.org/docs/reference/index.html)
- [Getting Started](https://pandas.pydata.org/docs/getting_started/index.html)

All analyses are driven from two CSV files: `matches.csv` and `deliveries.csv`, loaded into DataFrames named `data` and `deliveries` within the notebook [`IPL-analysis.ipynb`](IPL-analysis.ipynb). The project demonstrates **indexing, grouping, reshaping, filtering, and plotting workflows** suitable for beginners and intermediate learners.

---

## Datasets

### `matches.csv`
- **Shape:** 636 rows × 18 columns
- **Content:** Match-level metadata including `id`, `season`, `city`, `date`, `venue`, teams, toss details, result, margin, player_of_match, and umpires.
- **Notes:** Columns like `city`, `winner`, `player_of_match`, `umpire1`, `umpire2` have some missing values; `umpire3` is fully null.

### `deliveries.csv`
- **Shape:** 150,460 rows × 21 columns
- **Content:** Ball-level details including `match_id`, `inning`, `batting_team`, `bowling_team`, `over`, `ball`, `batsman`, `bowler`, dismissal info, and per-ball runs breakdown.
- **Purpose:** Enables fine-grained batting, bowling, and over-phase analysis.

---

## Key Analyses

1. **Team success and participation**
   - Computes most successful teams by wins and total matches played.
   - Highlights top winners (e.g., Mumbai Indians) and frequent participants (e.g., Royal Challengers Bangalore).

2. **Toss decisions**
   - Frequency of toss decisions (`bat` vs `field`) summarized and plotted.

3. **Location filters**
   - Demonstrates filtering by city, e.g., counting all matches in Bangalore and reproducing counts after date filters.

4. **Seasonal winners view**
   - Uses `drop_duplicates('season', keep='last')` to surface the last recorded match per season and inspect winners.

5. **Player stats from deliveries**
   - Aggregates total runs by batsman, runs against specific bowling teams, per-season top run-scorers, and death-overs strike rates.

6. **Sixes by over and team**
   - Pivot table of sixes per over × batting team for heatmap visualizations.

---

## Selected Highlights

- **Top run-scorers by season:**

| Season | Batsman       |
|--------|---------------|
| 2008   | SE Marsh      |
| 2009   | ML Hayden     |
| 2010   | SR Tendulkar  |
| 2011   | CH Gayle      |
| 2012   | CH Gayle      |
| 2013   | MEK Hussey    |
| 2014   | RV Uthappa    |
| 2015   | DA Warner     |
| 2016   | V Kohli       |
| 2017   | DA Warner     |

- **Data cleaning examples:** Handling missing values with `dropna`, `fillna`, forward fill (`ffill`), backward fill (`bfill`).
- **Pandas techniques practiced:** Indexing, selection, sorting, deduplication, column renaming, groupby aggregation, pivoting, and filtering.

---

## Visualizations

- **Bar charts:** Distributions of toss decisions and team wins.
- **Heatmaps:** Sixes per over × batting team to highlight power-hitting patterns.
- **Death-overs analysis:** Filters overs > 15 to compute strike rates with a minimum balls-faced threshold to avoid small-sample noise.

---

## Repository Structure

```
IPL-data-analysis/
│
├── IPL-analysis.ipynb    # Main notebook with EDA, transformations, and plots
└── data/                 # Place matches.csv and deliveries.csv here
```

---

## Getting Started

### Requirements
- Python 3.x
- Pandas
- Matplotlib & Seaborn
- Jupyter Notebook or JupyterLab

### Running the Notebook
1. Launch Jupyter in the project folder:
   ```bash
   jupyter notebook
   ```
2. Open `IPL-analysis.ipynb` and run cells sequentially.

### Installing Jupyter (if not installed)
```bash
pip install notebook
# or for JupyterLab
pip install jupyterlab
```

---

## Learning Focus

Hands-on Pandas workflows: loading CSVs, inspecting dtypes, handling missing data, filtering, aggregating, reshaping, and visualizing.

**Follow along with the [YouTube playlist](https://youtube.com/playlist?list=PLKnIA16_RmvbR85fgbfVRKOiMokUKVupy&si=dPAmRaWZvm5LanrA)** to reinforce API concepts with live coding over IPL datasets, and refer to the [official pandas documentation](https://pandas.pydata.org/docs/) for detailed explanations of functions and methods.

---

## Extend the Analysis

- Add player metrics: boundary percentages, dot-ball rates, dismissal modes.
- Compute bowler economy and strike rates by phase.
- Analyze city/venue-based win patterns and toss→result conditional rates.
- Practice multi-index groupby and normalized crosstabs.