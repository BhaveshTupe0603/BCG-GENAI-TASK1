# 📊 BCG Gen-AI Job Simulation: Financial Data Analysis for AI-Powered Chatbot

This repository contains the solution to a simulated project by **BCG's Gen-AI Virtual Experience Program**. The task involves **manual extraction** of key financial figures from SEC filings for **Microsoft, Tesla, and Apple**, followed by **data-driven analysis** using Python (`pandas` in Jupyter Notebook) to generate insights that can help build an **intelligent financial chatbot**.

---

## 🧠 Objective

To extract and analyze key financial data from **10-K filings** of leading tech companies over the last **three fiscal years**, and derive insights using Python — forming a foundation for building an **AI-powered financial assistant**.

---

## 🗂️ Task Overview

### ✅ Step 1: Data Extraction

- **Companies**: Microsoft, Tesla, Apple  
- **Source**: [SEC EDGAR Database](https://www.sec.gov/edgar.shtml)  
- **Filing Type**: 10-K Annual Reports  
- **Years Covered**: 2023, 2022, 2021 (or latest 3 years available)  
- **Extracted Metrics**:
  - Total Revenue
  - Net Income
  - Total Assets
  - Total Liabilities
  - Cash Flow from Operating Activities

> 📋 Data was compiled manually and saved as `financial_data.csv` for analysis.

---

### ✅ Step 2: Setting Up Jupyter Notebook

1. **Install Jupyter Notebook**
   ```bash
   pip install notebook
   ```

2. **Launch Jupyter**
   ```bash
   jupyter notebook
   ```

3. Create a new notebook for analysis and documentation.

---

### ✅ Step 3: Python-Based Analysis

Using `pandas`, the notebook performs the following:

**Load the cleaned data:**
```python
import pandas as pd
df = pd.read_csv('financial_data.csv')
```

**Calculate Year-over-Year (YoY) growth:**
```python
df['Revenue Growth (%)'] = df.groupby('Company')['Total Revenue'].pct_change() * 100
df['Net Income Growth (%)'] = df.groupby('Company')['Net Income'].pct_change() * 100
df['Asset Growth (%)'] = df.groupby('Company')['Total Assets'].pct_change() * 100
df['Liability Growth (%)'] = df.groupby('Company')['Total Liabilities'].pct_change() * 100
df['Operating Cash Flow Growth (%)'] = df.groupby('Company')['Cash Flow from Operating Activities'].pct_change() * 100
```

**Summarize insights** using descriptive statistics, grouping, and markdown explanations.

---

### ✅ Step 4: Documentation and Output

**Documentation**: Clear explanations provided using markdown cells inside the notebook, including methodology, trends, and strategic implications.

**Exported Files:**

- `financial_analysis.ipynb` (Jupyter Notebook)
- `financial_analysis.pdf` (Notebook exported as PDF)
- `financial_data.csv` (Cleaned data used in the analysis)

---

## 📈 Sample Insights

- **Microsoft** maintained consistent revenue and net income growth over the three years.
- **Tesla** showed rapid growth in revenue but volatile net income due to high R&D and operational expansion.
- **Apple** had stable asset and cash flow performance, indicating mature financial efficiency.

---

## 🛠️ Tools Used

- Python 3.x  
- Jupyter Notebook  
- pandas  
- Manual data entry (Excel to CSV)

---

## 📁 File Structure

```
📦BCG-Financial-Analysis
├── financial_data.csv
├── financial_analysis.ipynb
└── README.md
```

---

## 🧾 License

This project is part of a virtual simulation and is intended for educational purposes under fair use.

---

## 🙋 Contact

For any queries or feedback, feel free to raise an issue or connect on LinkedIn.
