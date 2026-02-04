# EGFR Dose–Response and Bioactivity Analysis

![EGFR IC50 Histogram](plots/EGFR_IC50_hist_positive.png)

---

## Overview

This project analyzes **Epidermal Growth Factor Receptor (EGFR)** bioactivity data from ChEMBL, focusing on IC50 values of small-molecule inhibitors. The analysis identifies the most potent compounds, visualizes their experimental variability, and provides dose–response insights—directly relevant to **anticancer therapeutics** and **drug discovery research**.

The project demonstrates **data cleaning, aggregation, and visualization skills** in Python, emphasizing preparation and analysis of biomedical datasets, which is essential for MSc-level research in **Applied Biomedicine**.

---

## Dataset

- **Source:** [ChEMBL Bioactivity Database](https://www.ebi.ac.uk/chembl/)  
- **Type:** IC50 measurements (nM) for compounds tested against EGFR  
- **Columns used:**  
  - `Molecule ChEMBL ID` – unique compound identifier  
  - `Molecule Name` – optional, if available  
  - `Value` – IC50 measurement in nM  

> Only numeric and positive IC50 values were considered to ensure meaningful bioactivity analysis.

---

## Skills Demonstrated

- **Data handling:** Cleaning, converting, and validating bioactivity data using **pandas**  
- **Statistical analysis:** Computing mean IC50 per compound, counting measurements, summarizing experimental variability  
- **Data visualization:** Plotting IC50 distribution and dose–response trends with **matplotlib**, including logarithmic scales for pharmacologically relevant insights  
- **Biological interpretation:** Identifying most potent compounds and potential drug candidates based on IC50 trends  

---

## Analysis Steps

1. **Load and inspect dataset** – Read CSV and preview columns.  
2. **Clean IC50 values** – Remove missing or non-numeric entries.  
3. **Compute mean IC50 per compound** – Aggregate experimental measurements to get overall potency.  
4. **Count measurements per compound** – Assess reliability of results.  
5. **IC50 distribution histogram** – Visualize the spread of compound potencies.  
6. **Top 5 compounds trend plot** – Highlight the most potent candidates and their experimental variability.  
7. **Save cleaned dataset** – Output for further downstream analysis.

---

## Key Insights

- The **most potent EGFR inhibitors** (mean IC50 in nM) identified in this dataset:

| Compound ID      | Mean IC50 (nM) |
|-----------------|----------------|
| CHEMBL574059     | 0.38           |
| CHEMBL574058     | 0.39           |
| CHEMBL304271     | 450            |
| CHEMBL5094480    | 900            |
| CHEMBL5087815    | 920            |

- The IC50 histogram illustrates that most compounds fall within the low nanomolar range, indicating strong inhibitory potential.  
- Top 5 trend plots reveal experimental variability, highlighting compounds with consistent high potency—valuable for drug candidate prioritization.

---

## Plots

1. **EGFR IC50 Histogram** – Distribution of compound potencies:  
   `plots/EGFR_IC50_hist_positive.png`  

2. **Top 5 Compounds IC50 Trend (log scale)** – Dose–response visualization:  
   `plots/top5_ic50_trend_positive.png`  

> Plots saved as **300 dpi** for professional, portfolio-ready presentation.

---

## How to Run

```bash
python analysis.py
