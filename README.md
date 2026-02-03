# Connecticut Single-Family Home Market Analysis (2001-2023)

## 📊 Project Description

This project analyzes over 400,000 single-family home sales transactions in Connecticut from 2001-2023 to identify price trends, regional variations, and the impact of major economic events. The analysis serves as a foundation for future machine learning applications in real estate price prediction.

## 📥 Dataset

**Dataset:** Real Estate Sales 2001-2023 GL  
**Source:** Connecticut Office of Policy and Management via [Data.gov](https://catalog.data.gov/dataset/real-estate-sales-2001-2018)  
**Size:** 1.1+ million transactions, ~130MB

### How to Obtain the Dataset

1. Download from [Data.gov](https://catalog.data.gov/dataset/real-estate-sales-2001-2018)
2. Save as `Real_Estate_Sales_2001-2023_GL.csv`
3. Place in `data/` directory

**Note:** Dataset not included in repository (exceeds 100MB GitHub limit)

## 🚀 How to Run the Project

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Jupyter Notebook or JupyterLab

### Installation Steps

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/ct-housing-analysis.git
cd ct-housing-analysis
```

2. **Create virtual environment (recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies:**
```bash
pip install -r requirements.txt
```

4. **Download dataset** (see instructions above) and place in `data/` folder

5. **Launch Jupyter Notebook:**
```bash
jupyter notebook data_workflow.ipynb
```

6. **Run all cells:** In Jupyter, select "Kernel" → "Restart & Run All"

## 📦 Dependencies
```txt
pandas==2.1.3
numpy==1.26.2
matplotlib==3.10.8
seaborn>=0.12.0
scipy>=1.11.4
jupyter>=1.0.0
```

Install with:
```bash
pip install -r requirements.txt
```

To regenerate requirements.txt:
```bash
pip freeze > requirements.txt
```

## 📁 Repository Structure
```
.
├── data_workflow.ipynb       # Main analysis notebook
├── requirements.txt          # Python dependencies
├── README.md                 # This file
├── module_summary.pdf        # Detailed report with citations
└── data/                     # Dataset folder (not in repo)
    └── Real_Estate_Sales_2001-2023_GL.csv
```

## 🔄 Version Control

This project uses Git with multiple branches:
- `main` - Final version
- `data-cleaning` - Data cleaning development
- `eda` - Exploratory analysis development

## 👤 Author

Shotaro Oyama  
AI Mastery Capstone - Project 1

## 📄 License

Educational project for AI Mastery Capstone program.

---

**For detailed analysis, methodology, and citations, see `module_summary.pdf`**