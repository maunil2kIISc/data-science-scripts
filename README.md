# data-science-scripts

This repository contains a small exploratory analysis of the "District - Taluka wise 10 Crore Plantation Status" dataset released by the Forest Department of Maharashtra (as on 08-09-2025).

Data files and notebook
- `Plantation_2.csv` — raw dataset (district/taluka planting statistics).
- `Research_methods_assignment_5.ipynb` — a Jupyter notebook that loads the CSV, performs basic anaysis of the dataset (scatter, boxplots, and a top-20 bar chart).

Dataset source
- Original source: https://www.data.gov.in/resource/district-taluka-wise-10-crore-plantation-status-forest-department-maharashtra-state-08-09

Summary of what this repo does
- Loads `Plantation_2.csv`, coerces numeric fields and strips extra characters (commas, whitespace).
- Visualizes the relationship between planned seedlings and pits dug (scatter plot), inspects distributions with boxplots, and shows the top 20 districts by seedlings planted.

Key observations and quick analysis
- Data cleaning: Several numeric columns contain commas and/or non-numeric values; these are converted to integers where possible and missing values are set to 0 for plotting convenience.
- Outliers: The notebook filters outliers (using the IQR rule) before plotting the scatter and boxplots, which helps make the main trends more visible.
- Planning vs Pits Dug: The scatter plot typically shows a positive relationship — talukas that planned more seedlings also tend to have more pits dug. However, a number of points deviate from this pattern, indicating differences in execution or reporting.
- Distribution: Boxplots for the numeric columns reveal a right-skewed distribution (many talukas with low-to-moderate counts and a few with very high counts). This pattern is common in district-level administrative data where a few large districts/talukas account for most activity.
- Top districts: The top-20 ranking highlights a small set of districts that contributed the largest numbers of seedlings planted; these districts drive a large fraction of the total planted count.

Notes, limitations and next steps
- The notebook treats any row with the District labeled as "Total" (case-insensitive) as an aggregate row and excludes it from district-level charts; this is important to avoid double-counting.
- Some columns may still contain dirty or inconsistent text values (spelling, extra whitespace). For a production analysis, more careful cleaning and validation against authoritative district/taluka lists would be recommended.
- Next steps that would add value:
	- Standardize district/taluka names against an authoritative list.
	- Add per-capita or area-normalized metrics (if population/area data available) to compare planting intensity.
	- Map visualizations (choropleth) to show spatial patterns across districts/talukas.
	- Provide reproducible environment notes (conda/pip requirements) and unit tests for the cleaning helpers.

How to run
1. Open the notebook `Research_methods_assignment_5.ipynb` with Jupyter or VS Code.
2. Ensure you have Python 3.8+ and the packages used in the notebook (pandas, matplotlib). A quick pip install line:

```bash
pip install pandas matplotlib
```

3. Run the notebook cells in order. The first cell reads `Plantation_2.csv` from the repository root.

License & attribution
- Dataset provided by the Government of India / data.gov.in. See the dataset page for licensing details.

If you'd like, I can also add a small `requirements.txt` and a short script to reproduce the notebook plots from the command line.
