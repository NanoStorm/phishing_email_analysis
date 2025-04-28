# 💻 Cybersecurity Data Analysis Project

## 📒 Project Overview
This project was completed for CYB333: Security Automation. The objective was to create a cybersecurity-focused data analysis using Python, Jupyter Notebooks, and visualization libraries. 

I created a phishing dataset manually to simulate cybersecurity data. Using Pandas, I explored and analyzed the dataset, then visualized patterns related to phishing URLs and legitimate URLs. This project demonstrates how automation can assist cybersecurity teams in identifying threats faster through data analysis and visual reporting.

---

## 💡 Features
- Custom-created phishing and legitimate URL dataset
- Data loading, exploration, and cleaning using Pandas
- Statistical analysis of URL characteristics:
  - Phishing vs Legitimate URL counts
  - Average URL length comparisons
  - Percentage of IP address usage
  - Percentage of URL shortening usage
- Visualizations using Matplotlib:
  - Bar Graph: Phishing vs Legitimate URLs
  - Pie Chart: Shortened vs Normal URLs

---

## 🛠️ How to Run This Project
   ### Requirements 📋
   - Python 3.x
   - pandas
   - matplotlib
   
1. Make sure you have Python installed.
2. Install the required libraries:
   ```bash
   pip install pandas matplotlib
3. Open the '.ipynb' file in Jupyter Notebook or VS Code.

- View the project notebook [here](./CYB333.ipynb). 

4. Run each cell step-by-step.

---

## 🧩 Code Documentation

This project is organized into clear, beginner-friendly steps, and each code section is fully documented with comments explaining what it does.

Below is a breakdown of the notebook structure and logic:

---

### 1. Import Libraries & Load the Dataset 📚
The project uses two main Python libraries:
- `pandas`: for working with tabular data (loading, exploring, analyzing).
- `matplotlib.pyplot`: for creating graphs and charts to visualize findings.

```python
import pandas as pd
import matplotlib.pyplot as plt
```
The phishing dataset was manually created and saved as a CSV file (phishing_dataset.csv)

```python
data = pd.read_csv('phishing_dataset.csv')
```

- This line reads the CSV file and loads it into a DataFrame called data, which acts like a table in memory.
- We then preview the first few rows using .head() to ensure it loaded correctly.

### 2. Explore the Dataset 🗺️
Several steps are taken to understand the data

```python
data.isnull().sum() # Checks if any data is missing.
data.info() # Shows the data types and how many entries are in each column.
data.describe() # Shows the basic statistics for numeric columns.
```

### 3. Analyze the Dataset 🔍
The project calculates important cybersecurity insights:
- How many phishing vs legitimate URLs exist
- Average URL lengths.
- Percentage of IP address usage.
- Percentage of shortened URLs.

Functions and Logic used:
```python
value_counts() # Counts how many times each unique value appears in a column
groupby() # Groups rows based on column value to calculate statistics for each group separately
.sum() # Adds up the total values in a column
.len() # Measures the total number of entries (rows) in the dataset
```

### 4. Visualize Findings 📊
Two main graphs were created:
- Bar Graph: Phishing vs Legitimate URLs.
- Pie Chart: Shortened vs Normal URLs.

Both visualizations are created using matplotlib.pyplot, with clear titles and labels
