# **Exploring Shelter Usage Trends in Toronto**

## **Project Overview**
This repository contains an exploratory data analysis (EDA) of Toronto's shelter system, focusing on shelter occupancy trends throughout 2021. The goal of this analysis is to uncover key patterns in shelter usage and provide insights that may inform policies aimed at addressing homelessness in the city.

### **Research Questions**
This study investigates the following:
1. **Seasonal Trends:** How does shelter occupancy vary across different months? Are there significant differences between warm and cold seasons?
2. **Program Model Differences:** Are occupancy rates significantly different between emergency and transitional shelter programs?
3. **Capacity Type Comparison:** Do programs with room-based capacity exhibit different occupancy characteristics than those with bed-based capacity?

## **Dataset**
The analysis is based on data from the `INF2178_A1_data.xlsx` file, which contains daily occupancy records for shelters across Toronto. The dataset includes the following key variables:
- **Occupancy Date**
- **Program Model** (Emergency or Transitional)
- **Service User Count**
- **Capacity Type** (Bed-based or Room-based)
- **Actual Capacity (Beds & Rooms)**
- **Occupied Capacity (Beds & Rooms)**

### **Data Cleaning & Feature Engineering**
- **Handling Missing Data:** Some columns contained missing values, but they were complementary and did not affect analysis.
- **New Features Added:**
  - **Occupancy Rate (%):** Measures how fully utilized a shelter is at a given time.
  - **Occupancy Month:** Extracted from the date field to analyze trends by month.
  - **Occupancy Season:** Categorized data into Spring, Summer, Fall, and Winter.

## **Exploratory Data Analysis (EDA)**
- **Descriptive statistics**: Summary metrics of shelter usage.
- **Correlation Analysis**: Examined relationships between capacity and occupancy.
- **Occupancy Trends by Season**: Used statistical tests to confirm that occupancy rates are significantly higher in colder months.
- **Comparison of Emergency vs. Transitional Shelters**: Found that emergency shelters have significantly higher occupancy rates.
- **Room-based vs. Bed-based Programs**: Room-based shelters tend to operate at higher occupancy rates than bed-based programs.

## **Key Findings**
- **Colder seasons (Fall & Winter) see higher occupancy rates**, confirming increased demand during harsher weather conditions.
- **Emergency shelters operate at higher occupancy levels** than transitional shelters, highlighting the urgent need for more emergency housing.
- **Room-based shelters tend to have higher occupancy rates** than bed-based shelters, suggesting a potential difference in how space is allocated.

## **Repository Structure**
```
/shelter-usage-trends
│── data/
│   ├── INF2178_A1_data.xlsx         # Raw dataset
│   ├── cleaned_data.csv             # Processed dataset after cleaning
│
│── notebooks/
│   ├── shelter_analysis.ipynb       # Jupyter notebook with full analysis
│
│── reports/
│   ├── shelter_usage_trends.pdf     # Final report summarizing findings
│
│── src/
│   ├── data_cleaning.py             # Data wrangling and preprocessing script
│   ├── eda.py                       # EDA visualizations and statistical tests
│
│── README.md                        # Project documentation
│── requirements.txt                  # Dependencies (Pandas, Matplotlib, Seaborn, SciPy)
│── LICENSE                           # License details (MIT, GPL, etc.)
```

## **Getting Started**
### **Installation & Requirements**
To reproduce the analysis, install the required dependencies using:

```bash
pip install -r requirements.txt
```

### **Running the Analysis**
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/shelter-usage-trends.git
   cd shelter-usage-trends
   ```
2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook notebooks/shelter_analysis.ipynb
   ```
3. View the report in the `/reports/` folder.

## **Future Work**
- Investigate **longitudinal trends** beyond 2021.
- Explore **additional factors** influencing shelter occupancy, such as policy changes or economic conditions.
- Develop **predictive models** to anticipate shelter demand.

## **Contributors**
- **Kevin Nitiema** – Data Analysis, Report Writing, and Visualization
