# Crime Rate Analysis by Region Using Python

## Project Overview
This project analyzes crime rates across different regions using Python. It helps identify crime trends, compare crime categories, and visualize crime statistics using graphs and charts.

The project uses data analysis and visualization techniques to better understand crime patterns and regional differences.

---

# Features
- Region-wise crime analysis
- Crime category comparison
- Year-wise crime trend analysis
- Data visualization using graphs
- Heatmap representation
- Cleaned dataset generation

---

# Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

# Project Structure

```plaintext
Crime-Rate-Analysis/
│
├── crime_analysis.py
├── crime_data.csv
├── requirements.txt
├── README.md
└── cleaned_crime_data.csv
```

---
#coding used
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
crime_data = pd.read_csv('crime_data.csv')

# Display data
print(crime_data.head())

# Total crimes by region
region_crime = crime_data.groupby('Region')['Number_of_Cases'].sum()

# Bar graph
plt.figure(figsize=(10,5))
region_crime.plot(kind='bar', color='red')
plt.title('Crime Rate by Region')
plt.xlabel('Region')
plt.ylabel('Number of Cases')
plt.show()

# Crime type distribution
plt.figure(figsize=(8,5))
sns.countplot(data=crime_data, x='Crime_Type')
plt.title('Crime Type Distribution')
plt.xticks(rotation=45)
plt.show()

# Year-wise crime trend
yearly_crime = crime_data.groupby('Year')['Number_of_Cases'].sum()

plt.figure(figsize=(8,5))
plt.plot(yearly_crime.index, yearly_crime.values, marker='o')
plt.title('Year-wise Crime Trend')
plt.xlabel('Year')
plt.ylabel('Cases')
plt.grid(True)
plt.show()

print("Crime Analysis Completed")

# Dataset Columns

| Column Name | Description |
|-------------|-------------|
| Region | Name of region/state/city |
| Year | Crime record year |
| Crime_Type | Type of crime |
| Number_of_Cases | Total reported cases |
| Population | Population of region |
| Crime_Rate | Crimes per 100,000 people |

---

# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/Crime-Rate-Analysis.git
```

## Open Project Folder

```bash
cd Crime-Rate-Analysis
```

## Install Requirements

```bash
pip install -r requirements.txt
```

---

# Run Project

```bash
python crime_analysis.py
```

---

# Sample Dataset

```csv
Region,Year,Crime_Type,Number_of_Cases,Population,Crime_Rate
Chennai,2022,Theft,1200,8000000,15
Mumbai,2022,Robbery,1500,12000000,18
Delhi,2023,Assault,1700,15000000,20
Bangalore,2023,Cyber Crime,900,9000000,10
Hyderabad,2022,Fraud,1100,10000000,12
```

---

# Output
The project generates:
- Bar charts
- Line graphs
- Crime distribution graphs
- Crime trend analysis

---

# Advantages
- Easy to understand crime patterns
- Useful for statistical analysis
- Helps identify high-crime regions
- Supports data-driven decision making

---

# Future Improvements
- Machine learning crime prediction
- Real-time data integration
- Dashboard using Streamlit
- Map-based visualization

---

# Conclusion
This project demonstrates how Python can be used for crime data analysis and visualization. By analyzing crime statistics region-wise, the project helps understand trends and identify areas with high crime activity.

---

# Author
Adnan Hussain
