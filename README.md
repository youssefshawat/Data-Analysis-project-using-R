# 🚴 BikeShare Exploratory Data Analysis

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![R](https://img.shields.io/badge/R-3.4+-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)

## 📋 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** on real-world bikeshare data collected from three major US cities: **Chicago**, **New York**, and **Washington**. The analysis is part of the Udacity "Programming for Data Science with R" Nanodegree program.

### 🎯 Research Questions

The project answers three key questions about bikeshare usage patterns:

| Question | Focus Area | Key Insights |
|----------|-----------|---------------|
| **Q1: Trip Duration** | Travel times by city and user type | Customers take 3x longer trips than Subscribers |
| **Q2: Popular Times** | Monthly, weekly, and hourly patterns | Peak usage in June, weekdays show commute patterns |
| **Q3: Popular Routes** | Most common start/end station combinations | Tourist areas dominate common routes |

---

## 🛠️ Tools & Technologies

### Languages & Environments
- **R** (v3.4+) - Primary analysis language
- **Jupyter Notebook** - Interactive analysis environment

### Key Libraries & Packages
| Package | Purpose |
|---------|---------|
| `ggplot2` | Data visualization (plots & charts) |
| `base R` | Data manipulation and statistics |

### Data Sources
- **Chicago**: Bike share data with user demographics
- **New York**: Bike share data with user demographics
- **Washington**: Bike share data (core metrics only)

---

## 📁 Project Structure

```
Exploratory-Data-Analysis-with-R/
├── 📂 data/                    # Raw bikeshare datasets
│   ├── chicago.csv
│   ├── new_york_city.csv
│   └── washington.csv
│
├── 📂 src/                     # Clean R scripts
│   └── bikeshare_analysis.R    # Refactored analysis script
│
├── 📂 notebooks/               # Jupyter notebooks
│   └── Explore_bikeshare_data.ipynb
│
├── 📂 imgs/                    # Generated visualizations
│   ├── Trip_Duration.png
│   ├── Monthly.png
│   ├── Weekly.png
│   ├── Hourly.png
│   ├── Chicago_Trips.png
│   ├── New_York_Trips.png
│   └── Washington_Trips.png
│
├── 📂 reports/                 # Analysis reports
│   └── (generated reports)
│
├── 📄 README.md               # Project documentation
└── 📄 requirements.txt         # R package dependencies
```

---

## 🚀 How to Run

### Prerequisites
- R (v3.4 or higher)
- RStudio (recommended) or Jupyter with IRkernel

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/Exploratory-Data-Analysis-with-R.git
cd Exploratory-Data-Analysis-with-R
```

2. **Install R packages**
```r
# Install required packages
install.packages("ggplot2")
```

3. **Run the analysis**

**Option A: Using RStudio**
```r
# Source the analysis script
source("src/bikeshare_analysis.R")
```

**Option B: Using Jupyter Notebook**
```bash
# Open the notebook
jupyter notebook notebooks/Explore_bikeshare_data.ipynb
```

**Option C: Using R console**
```bash
Rscript src/bikeshare_analysis.R
```

---

## 📊 Key Findings

### Question 1: Trip Duration Analysis

| Metric | Chicago | New York | Washington |
|--------|---------|----------|------------|
| Median Trip Duration | 11.2 min | 10.2 min | 11.8 min |
| Average Trip Duration | 15.6 min | 15.1 min | 20.6 min |

**Key Insight:** Customers (one-time users) take significantly longer trips than Subscribers:
- **Customers**: 32-44 minutes average (leisure use)
- **Subscribers**: 11-13 minutes average (commute use)

### Question 2: Temporal Patterns

| Pattern | Finding |
|---------|---------|
| **Peak Month** | June - Bikeshare usage increases steadily from January to June |
| **Weekday vs Weekend** | Lower weekend usage in Chicago/NY; Washington shows more balanced usage |
| **Peak Hours** | Morning (7-9 AM) and Evening (5-7 PM) commute peaks |

### Question 3: Popular Routes

| City | Top Route | Count |
|------|-----------|-------|
| Chicago | Lake Shore Dr & Monroe St → Streeter Dr & Grand Ave | 32 |
| New York | E 7 St & Avenue A → Cooper Square & E 7 St | 33 |
| Washington | Jefferson Dr & 14th St SW → Jefferson Dr & 14th St SW | 198 |

---

## 📈 Visualizations Generated

All visualizations are saved in the `/imgs` folder:

| Chart | Description |
|-------|-------------|
| `Trip_Duration.png` | Boxplot comparing trip duration by city and user type |
| `Monthly.png` | Bar chart of monthly trip counts per city |
| `Weekly.png` | Bar chart of weekly trip counts per city |
| `Hourly.png` | Bar chart of hourly trip counts per city |
| `Chicago_Trips.png` | Top 5 most common trips in Chicago |
| `New_York_Trips.png` | Top 5 most common trips in New York |
| `Washington_Trips.png` | Top 5 most common trips in Washington |

---

## 🔍 Data Quality Notes

The dataset includes the following data quality considerations:

### Missing Values Handling
- **Chicago & New York**: Contain `Gender` and `Birth.Year` columns with some missing values
- **Washington**: Does not include `Gender` or `Birth.Year` columns
- All analyses filter appropriately based on data availability

### Data Cleaning Applied
1. Filtering out null/empty values before statistical calculations
2. Converting trip duration from seconds to minutes for readability
3. Removing spurious empty entries from categorical counts

---

## 📝 Code Documentation

The codebase follows clean code principles:

- **Modular Functions**: Reusable helper functions (`two_col_df`, `count_table`, `get_weekday`, etc.)
- **Section Headers**: Clear section dividers with purpose descriptions
- **Inline Comments**: Detailed comments explaining complex operations
- **Consistent Naming**: Descriptive variable and function names

---

## 🎓 Educational Context

This project was developed as part of the **Udacity Programming for Data Science with R Nanodegree**. The goal was to demonstrate proficiency in:

- Data exploration and visualization
- R programming fundamentals
- Statistical analysis techniques
- Creating professional reports and documentation

---

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 👤 Author

Youssef Yasser (Youssef Shawat)
Data Science & AI Student @ِ ANU 

GitHub: github.com/youssefshawat

LinkedIn: www.linkedin.com/inyoussef-shawat-49971939

Watsapp :+20 01284926787

## 🙏 Acknowledgments

- [Udacity](https://www.udacity.com/) - For the Data Science Nanodegree program
- Bike Share companies of Chicago, New York, and Washington for providing the data
