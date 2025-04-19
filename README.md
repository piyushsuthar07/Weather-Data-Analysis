# Weather-Data-Analysis
# 🌦️ Weather Data Analysis using Python & Pandas

## 📌 Project Overview

This project involves performing **Exploratory Data Analysis (EDA)** on a weather dataset using **Python and Pandas**. The goal was to extract insights, perform data cleaning, and answer specific analytical questions related to weather conditions.

---

## 🛠️ Tools & Libraries Used

- Python
- Pandas

---

## 📂 Step 1: Import the Dataset

```python
import pandas as pd

data = pd.read_csv("file.csv")
print(data)

📊 Step 2: Initial Data Exploration

data.head()              # View first 5 rows
data.shape               # Shape of the dataset
data.index               # Index info
data.columns             # Column names
data.dtypes              # Data types of each column
data["Weather"].unique() # Unique weather conditions
data["Weather"].nunique()# Total number of unique weather types
data["Weather"].count()  # Count of non-null values
data["Weather"].value_counts() # Frequency of each weather condition
data.info()              # Dataset summary
🌬️ Find All Unique Wind Speeds
data["Wind Speed_km/h"].unique()
data["Wind Speed_km/h"].nunique()
🌞 Find All Instances of Clear Weather
python
Copy
Edit
# Using value_counts
data["Weather"].value_counts()

# Using filtering
data[data["Weather"] == "Clear"]

# Using groupby
data.groupby("Weather").get_group("Clear")
🌪️ Count Times When Wind Speed Was Exactly 4 km/h
python
Copy
Edit
data[data["Wind Speed_km/h"] == 4]
🧱 Check for Null Values
python
Copy
Edit
data.isnull().sum()
data.notnull().sum()
🏷️ Rename Column: "Weather" to "Weather Condition"
python
Copy
Edit
data.rename(columns={"Weather": "Weather Condition"}, inplace=True)
📏 Mean of Visibility
python
Copy
Edit
data.Visibility_km.mean()
🧪 Standard Deviation of Pressure
python
Copy
Edit
data.Press_kPa.std()
💧 Variance of Relative Humidity
python
Copy
Edit
data["Rel Hum_%"].var()
❄️ Find All Instances When Snow Was Recorded
python
Copy
Edit
# Using exact match
data[data["Weather"] == "Snow"]

# Using string match
data[data["Weather"].str.contains("Snow")]
🔍 Find Instances with Wind Speed > 24 km/h and Visibility = 25 km
python
Copy
Edit
data[(data["Wind Speed_km/h"] > 24) & (data["Visibility_km"] == 25)]
📈 Find Min, Max, and Mean for Each Weather Condition
python
Copy
Edit
data.groupby("Weather").mean()
data.groupby("Weather").min()
data.groupby("Weather").max()
✅ Conclusion
This project helped me strengthen my understanding of:

Data Cleaning & Exploration

Data Filtering and Grouping

Statistical analysis using Pandas

It’s a great beginner project to get hands-on with real-world datasets using Python.

📌 Author
Piyush Suthar
Aspiring Data Analyst | Video Editor | Content Creator

# Feel free to fork, clone, and suggest improvements!
