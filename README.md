# Property Sales Data Analysis & Machine Learning

## Project Overview
This project analyses multi-year residential property sales data (2021–2024) to explore trends in housing prices and property characteristics.  
The workflow focuses on building a clean **Analytics Base Table (ABT)**, performing exploratory data analysis (EDA), and applying machine learning techniques to infer missing property features.

The project demonstrates practical data engineering, data visualisation, and supervised learning skills using Python.

---

## Objectives
- Clean and standardise raw property sales data scraped from online sources  
- Construct a reusable **Analytics Base Table (ABT)** suitable for analysis and modelling  
- Explore relationships between price, location, and structural property features  
- Apply machine learning to predict missing categorical attributes (Garden and Garage)  
- Clearly communicate insights through visualisations and documented analysis  

---

## Dataset
- **Time period:** 2021–2024  
- **Granularity:** One row per property sale  
- **Key features:**  
  - Sale Date  
  - Sale Price  
  - Location  
  - Property Type  
  - Bedrooms, Bathrooms, Stories  
  - Year Built  
  - Garden (Yes / No / Unknown)  
  - Garage (Yes / No / Unknown)

The dataset contains missing values and inconsistent formats, reflecting realistic data quality challenges.

---

## Data Preparation
Key preprocessing steps include:
- Parsing and standardising date formats into pandas `datetime` objects  
- Cleaning numeric fields (e.g. extracting and imputing `Year Built`)  
- Handling missing and inconsistent categorical values  
- Removing redundant columns and validating data types  
- Merging yearly datasets into a single multi-year ABT  

All preprocessing decisions are explained within Jupyter notebooks using Markdown cells.

---

## Exploratory Data Analysis
Exploratory analysis was conducted using **pandas** and **Matplotlib**, including:
- Distribution analysis of sale prices and property attributes  
- Scatter plots examining relationships between price, bedrooms, and bathrooms  
- Grouped aggregations by location, property type, and amenities  
- Temporal analysis to identify trends and seasonality across years  

These visualisations help characterise the housing market and identify key price drivers.

---

## Machine Learning
Two supervised classification models were developed to infer missing categorical data:

### Garden Classifier
- **Model:** Random Forest  
- **Goal:** Predict whether a property has a garden  
- **Outcome:** Very high accuracy due to class imbalance (most properties have gardens), with limited ability to detect rare “No” cases  

### Garage Classifier
- **Model:** Random Forest  
- **Goal:** Predict whether a property has a garage  
- **Outcome:** More balanced performance, indicating garage presence is more strongly linked to measurable features such as price, location, and property type  

Model performance was evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

---

## Challenges
- Handling class imbalance in categorical prediction tasks  
- Significant price variability within the same bedroom or bathroom counts  
- Limited feature set (e.g. no floor area or energy rating data)  

These challenges were discussed and addressed where possible using appropriate modelling and evaluation techniques.

---

## Future Work
Potential extensions of this project include:
- Incorporating additional features such as floor area, lot size, or energy ratings  
- Applying geospatial analysis to study neighbourhood-level price effects  
- Building regression models to predict sale price directly  
- Exploring advanced models (e.g. Gradient Boosting) and hyperparameter tuning  
- Expanding the dataset to include more years or regions  

---

## Technologies Used
- Python  
- pandas, NumPy  
- Matplotlib  
- scikit-learn  
- BeautifulSoup (web scraping)  
- Jupyter Notebook  


---

## Author
Developed as part of a data analytics / machine learning coursework project, demonstrating end-to-end data processing and analysis in a real-world context.

