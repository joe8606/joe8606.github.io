---
layout: page
title: E-Commerce Price Tracking System
description: Automated system to track product prices on Wayfair using web scraping and GitHub Actions
img: assets/img/ecommerce_tracking.png
importance: 1
category: data science
---
## Tools & Technologies
**Technologies:** Python · BeautifulSoup · Selenium · pandas · requests · GitHub Actions  
**Concepts:** CI/CD · Web Scraping · Data Pipeline · Automation · Version Control · Scheduled Tasks

## Overview
This project builds an automated system to track product prices on Wayfair. It integrates web scraping, data cleaning, and GitHub Actions to continuously collect and version pricing data for downstream analysis.
<img src="/assets/img/Ecommerce_workflow.png" alt="workflow" style="width:125%; display:block; margin:auto;">

## Objectives
- Extract product details (name, price, availability) from Wayfair using Python-based scraping tools.
- Clean and structure the data into usable formats.
- Automate the scraping and updating workflow with hourly scheduling via GitHub Actions.

## Methodology
**Web Scraping:** Used requests and BeautifulSoup to parse static pages and Selenium for dynamic content and pagination.

**Data Cleaning:** Parsed nested HTML structures, handled missing fields, standardized currency formats, and exported clean datasets.

**Automation with GitHub Actions:**
- Configured a cron job (0 */1 * * *) to trigger the workflow every hour.
- Installed dependencies, ran the scraper, and committed updated CSVs to the dat/ directory in the repository.
- Managed credentials securely through GitHub Secrets for proxy authentication.
<img src="/assets/img/web_scraping.png" alt="workflow" style="width:125%; display:block; margin:auto;">

<img src="/assets/img/tracking_analysis.png" alt="workflow" style="width:125%; display:block; margin:auto;">


## Results
The system automatically collects product price and availability data every hour and stores timestamped CSV files. This enables long-term price trend analysis, discount tracking, and potential integration with alert systems or dashboards.

- **View GitHub Repository:** [Link to Repository](https://github.com/joe8606/wayfair_product_price_tracker.git)
- **View full slides(PDF):**[Link to Slides](https://github.com/joe8606/wayfair_product_price_tracker/blob/main/data%20wrangling%20presentation%20group%201.pdf)
