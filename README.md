# Pandas Data Analysis Exercises

## Overview

This repository contains a comprehensive set of exercises designed to develop practical skills in data manipulation and analysis using Pandas, a fundamental library in the Python data science ecosystem. These exercises simulate real-world data analysis tasks you might encounter as a data analyst at a multinational energy company.

## Role Context

**Scenario**: You are a data analyst working for a multinational energy company. Your team is responsible for analyzing various datasets to improve operational efficiency and customer service. Your deliverables should include clean, efficient code with clear explanations suitable for both technical team members and non-technical executives.

## Learning Objectives

- Master core Pandas functionality for data manipulation
- Work with real-world datasets
- Handle missing values effectively
- Perform data cleaning and transformation
- Conduct basic statistical analysis
- Create DataFrames from various data sources
- Understand the relationship between Pandas, NumPy, SciPy, Matplotlib, and Scikit-learn

## Prerequisites

- Python 3.9 or higher
- Understanding of basic Python programming
- Familiarity with NumPy (helpful but not required)

## Environment Setup

### Required Libraries

- **Python**: 3.9+
- **NumPy**: Latest stable version
- **Pandas**: 1.0.1+ (latest recommended)
- **Jupyter**: For interactive development

### Installation

#### Option 1: Using virtualenv

```bash
# Create virtual environment
python -m venv ex00

# Activate virtual environment
# On Windows:
ex00\Scripts\activate
# On macOS/Linux:
source ex00/bin/activate

# Install required packages
pip install pandas numpy jupyter
```

#### Option 2: Using conda

```bash
# Create conda environment
conda create -n ex00 python=3.9 pandas numpy jupyter

# Activate environment
conda activate ex00
```

## Exercise Structure

### Exercise 0: Environment and Libraries
**Objective**: Set up your Python development environment with all required libraries.

**Tasks**:
- Create a virtual environment named `ex00`
- Install Pandas, NumPy, and Jupyter
- Verify installation

### Exercise 1: Your First DataFrame
**Objective**: Learn to create basic Pandas objects using different methods.

**Tasks**:
- Create a DataFrame from a NumPy array
- Create a DataFrame from Pandas Series
- Work with the following structure:
  ```
  	color	list	number
  1	Blue	[1, 2]	1.1
  3	Red	[3, 4]	2.2
  5	Pink	[5, 6]	3.3
  7	Grey	[7, 8]	4.4
  9	Black	[9, 10]	5.5
  ```
- Print column types and first value types

### Exercise 2: Electric Power Consumption
**Objective**: Manipulate real-world energy consumption data.

**Dataset**: [Individual Household Electric Power Consumption](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)

**Tasks**:
1. Delete columns: `Time`, `Sub_metering_2`, `Sub_metering_3`
2. Set `Date` as the index
3. Create a `update_types()` function to update DataFrame types
4. Use `describe()` for data overview
5. Remove rows with missing values
6. Transform `Sub_metering_1`: `(x+1)*0.06`
7. Filter rows where `Date >= 2008-12-27` and `Voltage >= 242`
8. Print the 88,888th row
9. Find the date with maximum `Global_active_power`
10. Sort by `Global_active_power` (desc) and `Voltage` (asc)
11. Calculate daily average of `Global_active_power`

### Exercise 3: E-commerce Purchases
**Objective**: Analyze e-commerce transaction data with minimal guidance.

**Dataset**: E-commerce Purchases

**Questions to Answer**:
1. How many rows and columns?
2. Average Purchase Price?
3. Highest and lowest purchase prices?
4. How many English ('en') language users?
5. How many people have "Lawyer" as job title?
6. AM vs PM purchase distribution?
7. Top 5 most common job titles?
8. Purchase price for Lot "90 WT"?
9. Email for credit card: 4926535242672853?
10. American Express users with purchases > $95?
11. Credit cards expiring in 2025?
12. Top 5 email providers?

### Exercise 4: Handling Missing Values
**Objective**: Learn proper techniques for handling missing data.

**Key Concepts**:
- Understanding types of missing data (MCAR, MAR, MNAR)
- Different imputation strategies
- When to drop vs. fill missing values

**Tasks**:
1. Drop the `flower` column
2. Fill missing values with different strategies:
   - `sepal_length` → mean
   - `sepal_width` → median
   - `petal_length`, `petal_width` → 0
3. Fill missing values using `fillna()` with median
4. **Bonus Questions**:
   - Why is filling with 0 or mean sometimes problematic?
   - Find the special row in the dataset

## Resources

### Recommended Reading
- **Primary Resource**: Chapter 5 of "Python for Data Analysis" by Wes McKinney (40 pages)
- [Pandas Official Documentation](https://pandas.pydata.org/docs/)
- [Missing Data Types Article](https://stefvanbuuren.name/fimd/sec-MCAR.html)

### Additional Resources
- NumPy Documentation
- Matplotlib for visualizations
- Scikit-learn for machine learning integration

## Best Practices

1. **Code Quality**:
   - Write clean, readable code
   - Use meaningful variable names
   - Comment complex operations

2. **Documentation**:
   - Explain your methodology
   - Document assumptions
   - Create clear visualizations

3. **Presentation**:
   - Prepare insights for technical and non-technical audiences
   - Create concise summaries
   - Support findings with data

## Tips for Success

- Take time to understand Pandas concepts deeply rather than rushing through exercises
- Experiment with different approaches to solve problems
- Use Jupyter notebooks for interactive exploration
- Refer to the official documentation when stuck
- Practice explaining your findings clearly

## Project Structure

```
pandas-exercises/
│
├── README.md
├── requirements.txt
├── notebooks/
│   ├── exercise_0_setup.ipynb
│   ├── exercise_1_dataframes.ipynb
│   ├── exercise_2_power_consumption.ipynb
│   ├── exercise_3_ecommerce.ipynb
│   └── exercise_4_missing_values.ipynb
│
├── data/
    ├── household_power_consumption.txt
    ├── ecommerce_purchases.csv
    └── missing_values_dataset.csv
```

## Troubleshooting

**Common Issues**:
- **Import errors**: Ensure virtual environment is activated
- **Version conflicts**: Use compatible library versions
- **Memory errors with large datasets**: Consider using `chunksize` parameter
- **Encoding issues**: Specify encoding when reading files (e.g., `encoding='utf-8'`)

## Contributing

Feel free to submit improvements, bug fixes, or additional exercises through pull requests.

## License

This educational material is provided for learning purposes.

---

**Note**: These exercises are designed to build foundational skills that will be essential throughout your data science journey. Pandas proficiency is crucial for data preprocessing, feature engineering, and exploratory data analysis.

Happy Learning! 🐼📊