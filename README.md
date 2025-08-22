# ✈️ Flight Price EDA  

## 📌 Project Overview  
This project performs **Exploratory Data Analysis (EDA)** on flight ticket prices to understand the key factors that influence airfare. By cleaning, transforming, and analyzing the dataset, we gain insights into how airline, source, destination, duration, stops, and other variables impact the price of flights.  

---

## 🛠️ Steps Performed  

### 1. **Data Import & Inspection**  
- Imported required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`.  
- Loaded dataset `flight_price.xlsx`.  
- Performed `head()`, `tail()`, `info()`, and `describe()` to understand the structure, missing values, and statistics.  

👉 **Why?** To get a first look at the dataset and identify data types, shape, and potential issues.  

---

### 2. **Feature Engineering**  
- Extracted `Date`, `Month`, `Year` from `Date_of_Journey`.  
- Converted them into integer format for easier handling.  
- Dropped the original `Date_of_Journey` column (redundant after extraction).  

👉 **Why?** Splitting journey date allows temporal analysis and helps ML models later.  

---

### 3. **Arrival & Departure Time Transformation**  
- Cleaned `Arrival_Time` to keep only the time portion.  
- Extracted `Arrival_hour` and `Arrival_min`.  
- Extracted `Dep_hour` and `Dep_min` from `Dep_Time`.  

👉 **Why?** To analyze time-based effects (morning vs evening flights, etc.).  

---

### 4. **Duration Feature Engineering**  
- Cleaned `Duration` column to extract `dur_hour` and `dur_min`.  
- Handled inconsistent values like only hours (`19h`) or only minutes (`45m`).  

👉 **Why?** Flight duration is a key factor in pricing and needs to be standardized into numeric columns.  

---

### 5. **Stops, Airline, and Additional Info**  
- Analyzed `Total_Stops` feature and its relation to price.  
- Studied airline and additional info for categorical distributions.  

👉 **Why?** Different airlines and number of stops heavily affect ticket cost.  

---

### 6. **Exploratory Data Analysis (EDA)**  
- Distribution plots for price.  
- Boxplots and violin plots comparing airlines, stops, and classes against ticket prices.  
- Heatmaps and correlations for numeric features.  

👉 **Why?** To identify patterns, detect outliers, and visualize relationships between features and target variable (`Price`).  

---

## 📊 Key Features in Dataset  

1. **Airline** – Categorical (type of airline)  
2. **Flight** – Flight code  
3. **Source City** – City of departure  
4. **Destination City** – City of arrival  
5. **Departure Time** – Time bins (morning, afternoon, night, etc.)  
6. **Arrival Time** – Time bins  
7. **Stops** – Number of stops (non-stop, 1-stop, 2-stops, etc.)  
8. **Class** – Business / Economy  
9. **Duration** – Total journey time (converted to hours & minutes)  
10. **Days Left** – Derived feature (booking date vs journey date)  
11. **Price** – Target variable  

---

## 📌 Why This EDA Matters  
- Helps understand **pricing dynamics** in the airline industry.  
- Prepares data for further **predictive modeling** (e.g., price prediction).  
- Shows **feature engineering techniques** for handling dates, times, and durations.  

---

## 🚀 Next Steps (if extended)  
- Build regression models to predict ticket price.  
- Try feature encoding (One-Hot Encoding, Target Encoding).  
- Experiment with ML models (Linear Regression, Random Forest, XGBoost).  

---

## 📂 Project Structure  
┣ 📜 flightprice.ipynb # Jupyter notebook with code
┣ 📜 flight_price.xlsx # Dataset (if allowed)
┣ 📜 README.md # Documentation
