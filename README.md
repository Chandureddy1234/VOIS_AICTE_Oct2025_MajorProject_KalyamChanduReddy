# Netflix Content Trends Analysis# Netflix Content Trends Analysis



This notebook-driven project analyzes the Netflix catalogue (7,789 titles, 11 columns) to surface content trends for strategic decision-making. It focuses on how Movies vs. TV Shows, genres, countries, ratings, talent, and durations have evolved so that stakeholders can optimize acquisition, production, and product experiences.This notebook-driven project analyzes the Netflix catalogue (7,789 titles, 11 columns) to surface content trends for strategic decision-making. It focuses on how Movies vs. TV Shows, genres, countries, ratings, talent, and durations have evolved so that stakeholders can optimize acquisition, production, and product experiement.
## Environment
- Python 3.12 (tested)

- Key libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `pycountry`, `networkx`, `python-dateutil`- Python 3.12 (tested)

Install everything with:

Install everything with:

```bash

python -m pip install pandas numpy matplotlib seaborn plotly pycountry networkx python-dateutil```bash

```python -m pip install -r requirements.txt  # if you maintain a requirements file

# or install ad-hoc when prompted by the notebook's bootstrap cell

> The first notebook cell automatically installs the core analysis packages if they are missing, keeping the workflow reproducible on a clean machine.```



## How to run> The first notebook cell automatically installs the core analysis packages if they are missing, keeping the workflow reproducible on a clean machine.



1. Open `netflix_content_trends_analysis.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.## How to run

2. Run all cells from top to bottom (the notebook is idempotent and handles output directories).

3. On completion you will find:1. Open `netflix_content_trends_analysis.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.

   - `outputs/netflix_cleaned.csv` (clean dataset)2. Run all cells from top to bottom (the notebook is idempotent and handles output directories).

   - Aggregation tables such as `titles_by_year.csv`, `top_genres_overall.csv`, `top_countries.csv`3. On completion you will find:

   - Visualization assets (`fig_*.png` and Plotly HTML files)   - `outputs/netflix_cleaned.csv` (clean dataset)

   - `outputs/run_summary.json` capturing run metadata   - Aggregation tables such as `titles_by_year.csv`, `top_genres_overall.csv`, `top_countries.csv`

   - Visualization assets (`fig_*.png` and Plotly HTML files)


## Key insights```



- **Growth plateau after 2019:** Content additions accelerated through 2019 before stabilizing, implying a shift from quantity to quality.## Key insights

- **International surge:** India, South Korea, Spain, and Japan provide a large share of newer titles, validating continued localization investments.

- **Genre clusters:** Dramas, International content, and Comedies dominate; genre co-occurrence heatmaps reveal bundle-friendly combinations (e.g., International Romantic Dramas).- **Growth plateau after 2019:** Content additions accelerated through 2019 before stabilizing, implying a shift from quantity to quality.

- **Talent long tail:** A handful of directors supply a disproportionate share of titles, making them critical partners for renewals.- **International surge:** India, South Korea, Spain, and Japan provide a large share of newer titles, validating continued localization investments.

- **Maturity skew:** TV-MA titles dominate the catalogue, highlighting an opportunity to bolster family-friendly programming.- **Genre clusters:** Dramas, International content, and Comedies dominate; genre co-occurrence heatmaps reveal bundle-friendly combinations (e.g., International Romantic Dramas).

- **Duration nuances:** Documentaries and stand-up specials trend shorter (~70–80 minutes), while Action & Adventure pushes beyond 115 minutes, impacting engagement strategies.- **Talent long tail:** A handful of directors supply a disproportionate share of titles, making them critical partners for renewals.

- **Maturity skew:** TV-MA titles dominate the catalogue, highlighting an opportunity to bolster family-friendly programming.

## Assumptions & notes- **Duration nuances:** Documentaries and stand-up specials trend shorter (~70–80 minutes), while Action & Adventure pushes beyond 115 minutes, impacting engagement strategies.



- When `release_year` is missing, the pipeline derives it from `date_added`; decisions based on release recency should treat this as an approximation.## Assumptions & notes

- Missing director, cast, and country fields are filled with `"Unknown"` while preserving counts via engineered features.

- Genre, cast, and country lists are exploded for aggregation, so duplicated records represent intentional multi-tag relationships, not data errors.- When `release_year` is missing, the pipeline derives it from `date_added`; decisions based on release recency should treat this as an approximation.

- The notebook saves plots to disk instead of embedding full-resolution images to keep the file size manageable.- Missing director, cast, and country fields are filled with `"Unknown"` while preserving counts via engineered features.

- Genre, cast, and country lists are exploded for aggregation, so duplicated records represent intentional multi-tag relationships, not data errors.
- The notebook saves plots to disk instead of embedding full-resolution images to keep the file size manageable.

## Next steps (optional)

- Extend the analysis with engagement metrics (views, completion rates) if available to connect supply with demand.
- Parameterize the notebook via Papermill or Airflow for scheduled monthly refreshes.
- Add automated tests or linting if the pipeline evolves into a larger analytics codebase.
- Update the PowerPoint deck with refreshed visuals for executive presentations.
