---
layout: page
title: COVID-19 Data Visualization Dashboard
description: Dynamic COVID-19 data dashboard built with Google Looker Studio and Python
img: assets/img/COVID-19 Data Visualization Dashboard.png
importance: 4
category: data science
---
- **View Dashboard:** [Link to Dashboard](https://lookerstudio.google.com/reporting/fa7dfe82-9962-4792-85dc-8224df83c175)
- **View GitHub Repository:** [Link to Repository](https://github.com/joe8606/Covid19_lookerstudio_project.git)
- **View Medium Article:**[Link to Article](https://medium.com/@joe528491/i-completed-a-data-science-assessment-got-a-verbal-offer-and-walked-away-part-1-869698f19032)

## Tools & Technologies
**Technologies:** Python · pandas · Google Looker Studio · Google Sheets · CDC COVID Dataset · Jupyter Notebook  
**Concepts:** Data Visualization · Dashboard Design · Data Pipeline · Real-time Analytics

## Overview
This project presents a dynamic COVID-19 data dashboard built with Google Looker Studio, powered by a CDC dataset processed in Python. The goal is to enable interactive visualization of COVID-19 trends by integrating real-world data into a streamlined and easily updateable pipeline.

## Objectives
- Retrieve and clean raw COVID-19 data from CDC's open API.
- Prepare time-series data with proper formatting, missing value handling, and sorting.
- Connect the cleaned dataset to Looker Studio via Google Sheets to support real-time visual exploration.

## Methodology
**Data Source:** U.S. CDC open dataset containing daily case, death, and hospitalization metrics.

**Data Cleaning in Python:**
- Parsed dates and sorted records chronologically.
- Handled missing values and ensured consistent column formatting.
- Exported the processed data to Google Sheets for visualization.

**Dashboard Design:**
- Built an interactive dashboard in Looker Studio.
- Included key indicators such as daily cases, cumulative deaths, and moving averages.
- Implemented filters for state selection, time range, and metric comparison.

## Results
The resulting dashboard enables users to explore U.S. COVID-19 statistics in a clear and flexible format, powered by a lightweight yet automated Python-to-Google Sheets pipeline.

<div style="text-align: center; margin: 2rem 0;">
  <iframe width="100%" height="600" src="https://lookerstudio.google.com/embed/reporting/fa7dfe82-9962-4792-85dc-8224df83c175/page/1M" frameborder="0" style="border:0" allowfullscreen></iframe>
</div>





