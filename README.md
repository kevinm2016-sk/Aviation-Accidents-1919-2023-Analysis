# Aviation Accidents – Exploratory Data Analysis

**Tools:** Python, Pandas, NumPy, Matplotlib, GeoPandas — Google Colab  
**Program:** Master in Data Analytics – ProfessionAI

---

## What's this about

This project is an exploratory analysis of a dataset containing ~24,000 aviation accident records. It was built as part of my Data Analytics Master at ProfessionAI and was my first time working with Pandas and Matplotlib properly.

The goal was to answer 5 questions about aviation safety — plus a bonus world map visualization.

---

## Dataset

CSV file with ~23,967 records covering global aviation accidents. Columns include: date, country, aircraft type, operator, fatalities, and more.

**Cleaning steps applied:**
- Converted `fatalities` to numeric, filled nulls with 0
- Parsed dates and extracted weekday names
- Identified and investigated duplicates — majority were Netherlands records, treated as ignorable
- Dropped duplicates, nulls, and reset index → final clean dataset: ~21,000+ rows

---

## The 5 questions

**Q1 — Which country has the most accidents?**  
USA leads by a large margin, accounting for over 40% of the top 10 countries. Russia and UK follow.

**Q2 — Which days of the week are most dangerous?**  
Weekdays (especially Thu–Fri) see more incidents than weekends. Sunday is the safest day — likely because there's simply less air traffic.

**Q3 — Safest operators in the top 10 countries?**  
For each of the 10 most accident-prone countries, I filtered operators with zero total fatalities — a rough proxy for "safest" within their market.

**Q4 — Which aircraft type caused the most deaths?**  
The Douglas C-47A (DC-3) tops the list with 5,600 fatalities — though this reflects its widespread historical use more than inherent danger. More modern aircraft appear further down.

**Q5 — How did incidents change after 9/11?**  
There's a visible drop in 2001 at the 9/11 marker, but the trend had already been declining through the late 1990s. Post-2001 incidents stabilized at a lower level (~200/year), suggesting a combination of regulatory tightening and reduced traffic.

---

## Bonus – World map

Used GeoPandas with a Natural Earth shapefile to plot accident frequency by country as a choropleth map. Required some manual country name matching (e.g. "United States of America" → "USA") to join with the dataset.

---

## Files

- `progetto_disastri_aerei.ipynb` — full notebook (runs on Google Colab)
- `aviation-accidents.csv` — source dataset (needs to be in Google Drive if running the notebook)

---

*Part of my ongoing Data Analytics portfolio. More projects coming.*
