# Data Science Scripts

This repository contains a small exploratory analysis of the "District - Taluka wise 10 Crore Plantation Status" dataset released by the Forest Department of Maharashtra (as on 08-09-2025).

Data files and notebook
- `Plantation_2.csv` — raw dataset (district/taluka planting statistics).
- `Research_methods_assignment_5.ipynb` — a Jupyter notebook that loads the CSV, performs basic anaysis of the dataset (scatter, boxplots, and a top-20 bar chart).

Dataset source
- Original source: https://www.data.gov.in/resource/district-taluka-wise-10-crore-plantation-status-forest-department-maharashtra-state-08-09

Summary of what this repo does
- Loads `Plantation_2.csv`, coerces numeric fields and strips extra characters (commas, whitespace).
- Visualizes the relationship between planned seedlings and pits dug (scatter plot), inspects distributions with boxplots, and shows the top 20 districts by seedlings planted.

Observations and quick analysis
- No. of pits dug shows a linear trend for majority of the districts, although in some districts participants directly planted the seeds without digging up.
- After looking at the box plot, median for no. of seedling is around, No. of pits dug, and No. of seedling planted are ~1,00,000, ~75,000, and ~60,000 respectively.
- Top 20 districts with highest seedling counts are as follows: 'Chandrapur', 'Ahilyanagar', 'Gadchiroli', 'Nashik', 'Beed', 'Dharashiv', 'Akola', 'Solapur', 'Yavatmal', 'Gondia', 'Jalgaon', 'Nanded', 'Raigad', 'Palghar', 'Amravati', 'Nagpur', 'Chhatrapati Sambhajinagar', 'Pune', 'Buldhana', and 'Latur'.

How to run
 - Ensure you have Python 3.8+ and the packages used in the notebook (pandas, matplotlib). A quick pip install line:

```bash
pip install pandas matplotlib
```
<img width="1189" height="889" alt="9bd2e566-056e-4cda-a853-fccca9864fa3" src="https://github.com/user-attachments/assets/872cb7fb-b85f-4076-8df5-fe7f4454415b" />
<img width="1189" height="889" alt="d98f0db0-6178-4db1-bbfa-15e4009f4abb" src="https://github.com/user-attachments/assets/81a98099-ec14-4ee5-bba6-c8319a258c61" />
<img width="1990" height="989" alt="bb825c8f-4520-4747-858b-cb5854b6f565" src="https://github.com/user-attachments/assets/a482b16c-c132-41a6-a05b-1853fea4ca3e" />
