# Netflix Exploratory Data Analysis (EDA)

## Project Overview
This project involves a comprehensive Exploratory Data Analysis (EDA) and data cleaning pipeline on a Netflix dataset. The goal is to prepare raw, unstructured data for deeper analysis by handling missing values, standardizing formats, and transforming complex, nested columns into structured formats suitable for relational mapping.

## Tech Stack
* **Python**
* **Pandas** (Data manipulation and cleaning)
* **NumPy** (Numerical operations)
* **Seaborn / Matplotlib** (Data visualization)

## Key Steps Performed
1. **Data Quality Audit:** 
   * Evaluated the dataset for shape (8807 rows, 12 columns), data types, and missing values across key features like `director`, `cast`, `country`, and `date_added`.
2. **Data Cleaning:** 
   * Handled null values by imputing 'Unknown' to preserve data integrity for future analysis.
   * Standardized string formatting by stripping trailing and leading whitespaces.
3. **Deep Cleaning & Transformation:**
   * **List Unpacking:** Columns such as `director`, `cast`, `country`, and `listed_in` (genres) contained multiple comma-separated values. These were split into lists and exploded into individual rows to create normalized relationship tables (`title_director`, `title_cast`, `title_country`, `title_genre`).
   * **Duplicate Removal:** Identified and dropped duplicate entries created during the explosion process to maintain an accurate 1:1 mapping.
4. **Feature Engineering:**
   * Converted `date_added` from string format to standard Pandas `datetime` objects.
   * Extracted specific temporal features: `added_year`, `added_month`, and `added_month_name`.
   * Parsed the `duration` column to extract numerical values, separating them into `movie_duration_min` for movies and `tv_seasons` for TV shows.

## Insights & Visualizations
* Analyzed the distribution of content types, revealing that Netflix's catalog consists of approximately 69.6% Movies and 30.4% TV Shows.
* Mapped content growth over the years, tracking the volume of titles added annually to the platform.
