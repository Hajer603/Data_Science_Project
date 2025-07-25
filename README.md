# Data_Science_Project
# 🏠 Real Estate Price Prediction Project (Oman)

## 📌 Objective
The purpose of this project is to collect and analyze real estate listings in Oman, clean the data, engineer useful features, and build machine learning models to predict property sale prices based on key property characteristics.

---

## 🌐 Websites Used
- **Website 1**: [https://www.dubizzle.com.om/en/properties/](https://www.dubizzle.com.om/en/properties/)
- **Website 2**: [https://hilalprp.com.om/](https://hilalprp.com.om/)

---

## 🔄 Data Collection & Cleaning Steps
1. **Web Scraping**:
   - Used Python with `requests`, `BeautifulSoup`, and `pandas` to scrape listing data.
   - Extracted features: property title, city, area, price, number of bedrooms, bathrooms, garage, and listing type.

2. **Data Cleaning**:
   - Removed text units (e.g., "OMR", "SqM") from price and area columns using regex.
   - Converted numeric columns to floats.
   - Filled missing values using median (for numeric data) or mode (for categorical data).
   - Dropped rows with excessive missing information.

---

## 🛠️ Feature Engineering Strategy
- Created new columns such as `price_per_sqm, city,government,total rooms` based on property size.
- Applied label encoding for categorical features (e.g., location,city, listing type and government).
- Normalized numerical features where needed.
- Combined data from two sources into one unified dataset.

---

## 🤖 Modeling Approach
Used Scikit-learn to apply and evaluate different regression models:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**

### Evaluation Metrics:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared Score (R²)

---

## 📊 Results Summary

| Model              | RMSE     | R² Score |
|--------------------|----------|----------|
| Linear Regression  | 0.10     | 0.43     |
| Decision Tree      | 0.02     | 0.98     |
| Random Forest      | 0.01     | 0.99     |

✅ **Random Forest** performed the best, achieving the highest R² and lowest RMSE.

---

## 📂 Project Files
•	Web scraping scripts or notebooks
•	Data cleaning functions
•	Final combined CSV file
•	Feature engineering and modeling code
•	A brief README.md file 


---

## 🚀 Future Enhancements
- Add more features like amenities, location coordinates, or property age.
- Scrape additional websites to expand the dataset.
- Deploy the model as a prediction tool via Flask or Streamlit.

