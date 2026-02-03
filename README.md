# Connecticut Single-Family Home Market Analysis (2001-2023)

A comprehensive data analysis project examining over two decades of residential real estate transactions in Connecticut, with a focus on price trends, regional variations, and the impact of major economic events.

## 📊 Project Overview

This project analyzes 400,000+ single-family home sales transactions from Connecticut (2001-2023) to uncover patterns in the housing market. The analysis explores how prices changed over time, regional price differences, the relationship between assessed and market values, and seasonal patterns in real estate activity.

**Key Research Questions:**
1. How have single-family home prices in Connecticut evolved from 2001 to 2023?
2. What impact did major economic events (2008 Financial Crisis, COVID-19 Pandemic) have on housing prices?
3. Are there significant regional differences in price trends across Connecticut towns?
4. What is the relationship between assessed property values and actual sale prices?
5. Do seasonal patterns exist in home sales and pricing?

## 🎯 Project Goals

This project serves as the foundation for the AI Mastery Capstone series by:
- Building a clean, reproducible data workflow
- Demonstrating professional data science practices
- Establishing a dataset ready for future machine learning applications
- Documenting insights that inform predictive modeling strategies

## 📁 Repository Structure
```
ct-housing-analysis/
├── notebooks/
│   └── DataWorkFlow.ipynb          # Main analysis notebook
├── data/
│   └── Real_Estate_Sales_2001-2023_GL.csv  # Dataset (not included - see instructions below)
├── README.md                        # This file
├── requirements.txt                 # Python dependencies
└── .gitignore                      # Git ignore rules
```

## 📥 Dataset

This project uses the **Real Estate Sales 2001-2023 GL** dataset from the Connecticut Office of Policy and Management.

**Source:** [Data.gov - Connecticut Real Estate Sales](https://catalog.data.gov/dataset/real-estate-sales-2001-2018)

**Size:** ~130MB (1.1+ million transactions)

### How to Obtain the Dataset

1. Visit the [Data.gov dataset page](https://catalog.data.gov/dataset/real-estate-sales-2001-2018)
2. Click **"Download"** and select the CSV format
3. Save the file as `Real_Estate_Sales_2001-2023_GL.csv`
4. Place it in the `data/` directory of this project

**Note:** The dataset is not included in this repository due to its size (>100MB GitHub limit).

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone this repository:**
```bash
   git clone https://github.com/yourusername/ct-housing-analysis.git
   cd ct-housing-analysis
```

2. **Create a virtual environment (recommended):**
```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies:**
```bash
   pip install -r requirements.txt
```

4. **Download the dataset** (see instructions above) and place it in `data/`

5. **Launch Jupyter Notebook:**
```bash
   jupyter notebook notebooks/DataWorkFlow.ipynb
```

## 📦 Dependencies
```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0
```

Install all dependencies with:
```bash
pip install -r requirements.txt
```

## 🔍 Analysis Workflow

The notebook follows a structured data science workflow:

1. **Introduction** - Project context and research questions
2. **Data Loading** - Initial dataset inspection and quality assessment
3. **Data Cleaning** - Filtering, outlier removal, feature engineering
4. **Exploratory Data Analysis** - Price trends, regional patterns, relationships
5. **Visualizations** - Time series plots, distributions, heatmaps
6. **Key Findings** - Summary of insights and limitations
7. **Future Work** - Implications for AI/ML applications
8. **References** - Data sources and methodological citations

## 🎨 Key Visualizations

The analysis includes 5 main visualizations:

1. **Time Series Analysis:** Median home prices from 2001-2023 with economic event markers
2. **Price Distribution:** Histogram showing the distribution of sale prices
3. **Regional Comparison:** Box plots comparing prices across top Connecticut towns
4. **Assessment vs. Market:** Scatter plot of assessed values vs. actual sale prices
5. **Seasonality Heatmap:** Transaction volume by month and year

## 📈 Major Findings

- **40% price growth** from 2001-2023, with significant volatility during economic crises
- **2008 Financial Crisis:** ~13% price decline over 5 years
- **COVID-19 Pandemic:** ~19% price increase from 2019-2023
- **Regional variation:** 2-3x price differences between Connecticut towns
- **Assessment gap:** Homes consistently sell for 1.5-2x their assessed value
- **Strong seasonality:** June-August peak sales, winter lows

## 🤖 Future AI/ML Applications

This workflow establishes the foundation for:

- **Price Prediction Models:** Regression models using temporal and geographic features
- **Time Series Forecasting:** ARIMA/LSTM models for price trend prediction
- **Market Segmentation:** Clustering similar towns or property types
- **Anomaly Detection:** Identifying unusual transactions or market conditions

## 🛠️ Technologies Used

- **Python** - Primary programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib & Seaborn** - Data visualization
- **Jupyter Notebook** - Interactive development environment
- **Git & GitHub** - Version control

## 📝 Version Control

This project demonstrates professional Git practices:

- Multiple meaningful commits documenting development progress
- Feature branches for data cleaning, EDA, and visualization work
- Clear commit messages describing changes
- Proper `.gitignore` to exclude data files and system files

## 🎓 Academic Context

This project is part of the **AI Mastery Capstone** series. It focuses on building robust data workflows that serve as the foundation for subsequent projects in:

- Machine Learning
- Deep Learning
- Generative AI
- Agentic AI Systems

## 📚 References

**Data Source:**  
State of Connecticut Office of Policy and Management. (2023). *Real Estate Sales 2001-2023 GL*. Data.gov. https://catalog.data.gov/dataset/real-estate-sales-2001-2018

**Key References:**  
- Case, K. E., & Shiller, R. J. (1989). The efficiency of the market for single-family homes. *American Economic Review*, 79(1), 125-137.
- McKinney, W. (2010). Data structures for statistical computing in Python. *Proceedings of the 9th Python in Science Conference*, 56-61.

See the notebook's References section for complete citations.

## 👤 Author

Shotaro Oyama 

AI Mastery Capstone - Project 1: Data Workflow

## 📄 License

This project is created for educational purposes as part of the AI Mastery Capstone program.

Dataset: Public domain (U.S. Government work)

## 🤔 Reflection Questions

### 1. Bias Awareness: Data Cleaning and Bias

**Question:** Where could poor data cleaning introduce bias into this analysis or future ML models?

**Answer:**

Poor data cleaning in this project could introduce several types of bias:

#### Selection Bias
- **Outlier removal:** Using town-year IQR method removes ~4% of transactions. While this eliminates obvious errors, it may disproportionately affect rapidly appreciating neighborhoods or unique luxury properties, underrepresenting these market segments
- **Single-family focus:** Filtering only single-family homes (35% of dataset) excludes condos, multi-family properties, and commercial real estate, limiting insights about the complete housing market

#### Temporal Bias
- **Missing data patterns:** If municipalities have inconsistent reporting during economic downturns, our crisis impact analysis could be skewed
- **Assessment lag:** Properties with outdated assessments (>5 years) may introduce systematic bias if revaluation practices differ across wealthy vs. lower-income areas

#### Geographic Bias
- **Small town representation:** Towns with few transactions (<20 per year) use global statistics in our IQR method, potentially missing local market dynamics
- **Sample size imbalance:** Towns like Hartford (8,000+ sales) vs. small towns (100 sales) create uneven representation in regional analysis

#### Assessment-Based Bias
- **Systematic under-assessment:** Our finding that homes sell for 1.5-2x assessed value could perpetuate existing inequities if assessment practices systematically undervalue certain neighborhoods
- **Non-market transactions:** Despite filtering ratios <0.5, family transfers and distressed sales may remain, potentially biasing price predictions downward

#### Mitigation Strategies
1. **Documentation:** Clear documentation of all filtering decisions with explicit rationale
2. **Sensitivity analysis:** Test model performance with different outlier thresholds
3. **Stratified validation:** Ensure models perform equitably across price ranges, towns, and time periods
4. **Bias auditing:** Regular checks for disparate impact across demographic groups (when such data becomes available)

---

### 2. ML Workflow Changes

**Question:** How would your workflow change if you were preparing this data for a machine learning model?

**Answer:**

#### Additional Data Processing Steps

**Feature Engineering:**
- **Temporal features:** Create lag features (previous year's median price by town), rolling averages (3-month, 6-month), year-over-year growth rates
- **Geographic features:** Distance to employment centers, coastal proximity, town median income (from external sources), school district ratings
- **Interaction features:** Town × Year, Month × Town (capture seasonal patterns by location)
- **Derived features:** Price per square foot (if property size data available), days on market, assessment accuracy (sale/assessed ratio)

**Categorical Encoding:**
- **Town encoding:** 170 towns require careful handling:
  - Target encoding (mean price by town) for tree-based models
  - One-hot encoding for linear models (creates 169 dummy variables)
  - Embeddings for neural networks (reduce to 16-32 dimensions)
- **Temporal encoding:** Cyclical encoding for month (sin/cos transformation) to capture seasonality

**Data Splitting Strategy:**
- **Temporal split:** Critical for time series data
  - Training: 2001-2019 (prevents data leakage)
  - Validation: 2020-2021 (hyperparameter tuning)
  - Test: 2022-2023 (final evaluation)
- **Stratified sampling:** Ensure representation across:
  - Price ranges (low, medium, high, luxury)
  - Towns (major cities vs. small towns)
  - Seasons (account for cyclical patterns)

**Scaling and Normalization:**
- **StandardScaler:** For linear models and neural networks
- **Log transformation:** For right-skewed price distribution (improves model performance)
- **Robust scaling:** For features with outliers (assessed value, sale amount)

**Missing Value Strategy:**
- **Imputation:** KNN imputation for missing property characteristics
- **Indicator variables:** Create "missing" flags as additional features
- **Domain-informed:** Use median imputation for numerical, mode for categorical

**Class Imbalance:**
- **Price range distribution:** If predicting price bins, handle imbalance with:
  - SMOTE for synthetic minority samples
  - Class weights in loss

## 🙏 Acknowledgments

- Connecticut Office of Policy and Management for providing the dataset
- Data.gov for hosting public datasets
- The Python data science community for excellent open-source tools

---

**Last Updated:** February 2026
