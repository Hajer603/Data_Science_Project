<img width="406" height="502" alt="image" src="https://github.com/user-attachments/assets/e7cb130e-29da-472e-8301-635dac71c28f" /># Data_Science_Project
# 🏠 Real Estate Data Collection and Cleaning Project

## 📌 Objective

This project simulates a real-world data science task involving:

- Web scraping real estate listings from two Omani websites
- Cleaning and integrating the data
- Performing feature engineering
- (Optional) Building a predictive model for property prices

All project artifacts are included in this repository, organized for clarity, reproducibility, and evaluation.

---

## 🌐 Websites Used

- [Dubizzle Oman](https://www.dubizzle.com.om/en/properties/)
- [Hilal Properties](https://hilalprp.com.om/)

These platforms list properties **for sale** across Oman. Data was collected from both to ensure a diverse and rich dataset.

---

## 🛠️ Project Steps

### 1. Web Scraping

- Scraped key property information:
  - Title
  - Location
  - Price
  - Number of bedrooms & bathrooms
  - Size (sqm)
  - Listing type (e.g., apartment, villa)
- Handled multiple pages and potential dynamic content
- Saved raw data into structured CSV files

> 📁 Output: `dubizzle_raw.csv`, `hilal_raw.csv`

---

### 2. Data Cleaning & Integration

- Removed or imputed missing values
- Standardized location and property type formats
- Removed duplicates
- Merged both datasets into a unified CSV

> 📁 Output: `combined_cleaned_data.csv`

---

### 3. Feature Engineering

- Created new features:
  - `price_per_sqm` = price / size
  - `total_rooms` = bedrooms + bathrooms
  - Encoded categorical variables for modeling
- Scaled numerical features using `MinMaxScaler` and `StandardScaler`

> 📁 Output: `engineered_data.csv`

---

### 4. (Optional) Predictive Modeling

- **Modeling Objective**: Predict property price based on features
- Preprocessing:
  - Train-test split
  - Encoding
  - Scaling
- Implemented and compared:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
- Evaluated models using RMSE and R²

> 📁 Output: `modeling.ipynb` *(optional)*

---

## 🗂️ Repository Structure

├── data/
 dubizzle_raw.csv
 hilal_raw.csv
combined_cleaned_data.csv
│
├── notebooks/
 web_scraping_dubizzle.ipynb
 web_scraping_hilal.ipynb
 modeling.ipynb (optional)
│
├── scripts/
cleaning.py
feature_engineering.py
│
├── README.md
└── requirements.txt
