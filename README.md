# Climate and Air Quality Analysis — Ancona, Italy

## Project Overview

This project explores air pollution and meteorological conditions in **Ancona, Italy**, using Python-based data cleaning, exploratory data analysis (EDA), and visualizations. The goal is to identify patterns in pollutant concentrations across times of day, seasons, monitoring stations, and weather conditions, and discuss their potential relevance to public health.

The analysis is **descriptive and exploratory**: it does not establish that air pollution caused particular health outcomes.

## Project Objectives

- Compare pollutant levels at **8:00 AM and 5:00 PM**.
- Examine seasonal variation in air pollution.
- Explore relationships between weather variables and pollutant concentrations.
- Compare pollutant levels across monitoring stations.
- Investigate monthly patterns in ozone and fine particulate matter.
- Translate findings into practical monitoring and public-health recommendations.

## Dataset

The source dataset contains **500 records and 17 original columns**, including:

| Category | Variables |
| --- | --- |
| Time and location | `Date`, `Latitude`, `Longitude`, `station_name` |
| Air pollutants | `NO2`, `O3`, `PM10`, `PM2.5` |
| Weather and environment | `Wind-Speed (U)`, `Wind-Speed (V)`, `Dewpoint Temp`, `Soil Temp`, `Total Percipitation`, `Vegitation (High)`, `Vegitation (Low)`, `Temp`, `Relative Humidity` |

The dataset retains its original columns after cleaning. Any additional time or wind-speed features used in charts are calculated temporarily during analysis rather than added to the exported cleaned dataset.

## Tools and Methods

- **Python and Jupyter Notebook** for analysis and documentation
- **Pandas and NumPy** for data processing
- **Matplotlib and Seaborn** for visualization
- **Pearson correlation** for exploratory weather–pollution relationships

### Analysis Workflow

1. **Extract:** Load and inspect the original CSV dataset.
2. **Transform:** Check data types, convert dates, handle invalid dates, and remove duplicate records as appropriate.
3. **Load:** Save the cleaned dataset for subsequent analysis.
4. **Explore:** Compare pollutants by time, season, station, and month; examine meteorological correlations.
5. **Interpret:** Summarize observations, limitations, and recommendations.

## Visualizations

The notebook contains five main visual analyses:

1. **8 AM vs. 5 PM:** Mean concentrations of NO₂, O₃, PM₁₀, and PM₂.₅.
2. **Seasonal boxplots:** Distribution of the four pollutants across seasons.
3. **Correlation heatmap:** Relationships between selected weather variables and pollutants.
4. **Monitoring-station comparison:** Average NO₂ and PM₂.₅ by station.
5. **Monthly trends:** O₃ and PM₂.₅ over the sampled months.

## Selected Findings

- Average **O₃** was higher in the sampled **5 PM** observations (approximately **73.50**) than in the **8 AM** observations (approximately **49.53**). The sample sizes differed, so this is not a paired comparison.
- **Summer O₃** averaged approximately **77.08** in the analyzed sample.
- **Relative humidity and O₃** showed a negative Pearson correlation of approximately **−0.50**.
- The highest average **NO₂** among the compared stations was observed at **Falconara Scuola** (approximately **21.54**).
- The highest average **PM₂.₅** among the compared stations was observed at **Chiarvalle** (approximately **19.17**).

*Values are descriptive results from the analyzed sample; pollutant units and relevant regulatory averaging periods should be verified before comparing them with air-quality standards.*

## Public Health Relevance

The findings can help inform questions about when and where additional air-quality monitoring may be useful. Potential actions include closer attention to ozone during warmer periods, investigation of station-level differences, and clearer communication of air-quality conditions to communities.

The project does **not** contain patient-level hospital data and cannot quantify disease risk or establish causal health effects.

## Repository Files

| File | Purpose |
| --- | --- |
| `Ancona_Climate_AirQuality_Analysis.ipynb` | Python notebook containing the workflow, charts, and interpretations |
| `Ancona_Italy_Climate_Report.csv` | Original dataset |
| `Ancona_Cleaned_Dataset.csv` | Cleaned dataset |
| `Ancona_Air_Quality_Technical_Report.docx` | Written technical report |
| `Ancona_Public_Health_Team_08_Improved_Cover.pptx` | Project presentation |

*Some filenames may vary slightly in the repository; use the actual filenames shown on GitHub.*

## How to Run the Analysis

1. Clone or download this repository.
2. Install Python and Jupyter Notebook (or open the notebook in VS Code).
3. Install the required Python packages:

   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

4. Open `Ancona_Climate_AirQuality_Analysis.ipynb`.
5. Ensure the notebook's CSV input path points to the downloaded dataset.
6. Run the notebook cells **from top to bottom**.

## Limitations

- The dataset is a **500-row sample**, not a continuous full monitoring record.
- Observation counts differ between some groups, including the two times of day.
- Associations and correlations do not demonstrate causation.
- No individual exposure histories or patient health outcomes are included.
- Pollutant measurement units, monitoring methods, and averaging periods require confirmation for formal standards-based assessment.

## Conclusion

This project demonstrates an end-to-end exploratory data analysis workflow for understanding air-quality patterns in Ancona. The results highlight differences by time, season, and monitoring location and provide a starting point for further environmental and public-health investigation.
