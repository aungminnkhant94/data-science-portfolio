# Aung Minn Khant - Data Science Portfolio

## About Me

I am Aung Minn Khant (Student ID: MC651192), a postgraduate student at the
University of Macau studying data science, with a focus on data visualization,
exploratory data analysis, and machine learning. This portfolio showcases my
project work and is published with GitHub Pages.

## Technical Skills

- **Languages:** Python, SQL
- **Data analysis:** pandas, NumPy, scikit-learn
- **Visualization:** matplotlib, seaborn, Plotly
- **Tools:** Jupyter Notebook, Git/GitHub, GitHub Pages

## Project Showcase

### Forest Fire Burned-Area Analysis (Montesinho Natural Park)

**Research question:** When and under what weather conditions do the most
damaging forest fires occur in Montesinho Natural Park, Portugal, and how well
do Fire Weather Index (FWI) components relate to the burned area?

![Burned area and fire count by month](assets/monthly_burned_area.png)

**Findings:** Analysis of 517 fires (2000-2003, UCI Forest Fires dataset) shows
that fire damage is heavily concentrated in late summer - August and September
alone account for more than 80% of the total burned area. The largest fires
cluster under hot, low-humidity conditions, and nearly half of all fires burn
less than 1 ha while the largest single fire burned 1,090.8 ha.

![Burned area vs temperature, coloured by humidity](assets/temp_vs_area.png)

The scatter plot above shows that fires burning more than ~100 ha occur almost
exclusively above 20 deg C with relative humidity below 45%, which makes the
seasonal peak easy to explain.

**The modelling twist:** I then benchmarked a Random Forest regressor against a
median baseline to predict log(burned area) from the FWI indices and weather.
The model could not beat the baseline (R2 = -0.01 on a held-out test set) -
even though feature importances confirm that temperature, humidity and the
drought codes carry the most signal. The conclusion: burned area is driven
largely by factors outside the dataset (ignition cause, firefighting response,
terrain), an honest negative result that matches the original research paper.

![Random Forest feature importances](assets/feature_importance.png)

- **Project repository:** [github.com/aungminnkhant94/data-science-project](https://github.com/aungminnkhant94/data-science-project)
- **Status:** Completed

---

*Published with GitHub Pages for CISC7204 Data Visualization, Practice 09.*
