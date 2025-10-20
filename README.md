# Netflix-DataCleaning
Cleaned and standardized Netflix Movies &amp; TV Shows dataset for analysis.
# Netflix Dataset - Data Cleaning

## Overview
This project focuses on **cleaning the Netflix Movies and TV Shows dataset** from Kaggle. The dataset was standardized, missing values handled, and columns cleaned for future analysis.

## Dataset
- File: `netflix_titles.csv`
- Source: [Kaggle - Netflix Movies and TV Shows](https://www.kaggle.com/shivamb/netflix-shows)

## Data Cleaning Steps
1. **Column Name Standardization**
   - Removed leading/trailing spaces
   - Converted to lowercase
   - Replaced spaces with underscores
   - Removed special characters

   Example:
   ```python
   df.columns = (
       df.columns.str.strip()
                 .str.lower()
                 .str.replace(' ', '_')
                 .str.replace(r'[^\w_]', '', regex=True)
   )
