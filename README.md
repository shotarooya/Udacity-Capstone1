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

## 🙏 Acknowledgments

- Connecticut Office of Policy and Management for providing the dataset
- Data.gov for hosting public datasets
- The Python data science community for excellent open-source tools

---

**Last Updated:** February 2026
