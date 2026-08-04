# 📊 Car Sales Data Cleaning & Processing (Pandas Project)

This repository contains the data cleaning workflow and transformation steps applied to a raw *Car Sales / Auction Dataset* using Python's pandas library.

---

## 🛠️ Data Cleaning Workflow & Steps Applied 

### 1. Initial Assessment & Column Renaming
* *Inspection:* Identified null values across multiple categorical and numerical attributes (e.g., Make, Model, Transmission, Condition).
* *Standardization:* Renamed all column headers to proper *Title Case* (data.rename()) for consistency.

---

### 2. Missing Value Imputation (Handling NaNs)
* *Categorical Imputation:* Categorical columns (Transmission, Make, Model, Trim, Body, Color, Interior) were filled with "Unknown".
* *Numerical Imputation:* Missing values in numerical attributes (Condition, Odometer, Mmr, Sellingprice) were imputed using column *medians* to avoid skewness from outliers.
* *Critical Record Removal:* Rows missing key identifiers like Vin and Saledate were dropped (dropna()).

---

### 3. Data Type Formatting & Typecasting
* *Datetime Conversion:* Parsed raw string dates in Saledate into standardized datetime64[ns, UTC] objects using pd.to_datetime().
* *Typecasting:* Explicitly cast Odometer to int64.

---

### 4. Text Case Standardization & Anomaly Cleanup
* *Upper Case:* Applied .str.upper() to structural codes (Vin, State).
* *Title Case:* Applied .str.title() to textual attributes (Make, Model, Trim, Body, Seller, Color, Interior).
* *Lower Case:* Lowercased values in Transmission.
* *Anomaly Handling:* Cleaned invalid entries in State by capping text lengths.

---

## 📁 Output Dataset
The cleaned, ready-for-analysis dataset was exported as:
* cleaned_car_prices.csv

---

## 🧰 Tech Stack Used
* *Language:* Python
* *Library:* pandas
* *Environment:* Jupyter Notebook / Anaconda 
