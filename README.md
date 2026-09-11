# 📊 OpenData-Jatim

**East Java economic intelligence platform** — Composite Risk Score modeling, XGBoost surrogate models with full interpretability, and LLM-powered policy narratives. Built for real-world decision making.

![Jatim Datathon 2025](https://img.shields.io/badge/Jatim%20Datathon%202025-FINALIST-FF6B35?style=flat-square&logo=trophy&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-0067A8?style=flat-square&logo=xgboost&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![PCA](https://img.shields.io/badge/PCA-9C27B0?style=flat-square&logo=python&logoColor=white)

---

## 🎯 Overview

OpenData-Jatim transforms 15+ macroeconomic indicators into actionable intelligence for East Java's economic planning. The system combines statistical rigor with modern ML to deliver models that are both **accurate** and **interpretable**.

Selected as **Finalist** in the **Jatim Datathon 2025**, competing against 76 teams from across East Java universities, organized by Dinas Kominfo Jatim, Google, AWS, and Western Sydney University.

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    Data Sources                          │
│  (PDRB, MSME, Poverty, Inflation, Investment, etc.)     │
└──────────────────────┬──────────────────────────────────┘
                       │
                       ▼
              ┌─────────────────┐
              │   Data Pipeline  │
              │  (Cleaning, EDA) │
              └────────┬────────┘
                       │
                       ▼
         ┌────────────────────────────┐
         │   PCA & Feature Engineer   │
         │  → Composite Risk Score    │
         └────────┬───────────────────┘
                  │
          ┌───────┴───────┐
          ▼               ▼
  ┌──────────────┐  ┌───────────────┐
  │  XGBoost     │  │  SHAP/LIME   │
  │  Surrogate   │  │  (Explain    │
  │  Model       │  │  Ability)    │
  └──────┬───────┘  └───────┬───────┘
         │                  │
         ▼                  ▼
  ┌──────────────────────────────────┐
  │   Validation & Interpretation    │
  │  Spearman ρ = 0.9182 vs NPL     │
  │  R² = 0.9669 on surrogate       │
  └────────┬─────────────────────────┘
           │
     ┌─────┴──────┐
     ▼            ▼
┌────────┐  ┌──────────┐
│Streamlit│  │ Tableau  │
│  App    │  │Dashboard │
└────────┘  └──────────┘
     │
     ▼
  LLM Integration: Numerical outputs → Policy narratives
```

---

## 📈 Key Results

| Metric | Value | Significance |
|--------|-------|-------------|
| **Validation Correlation** | Spearman ρ = **0.9182** | Validated against real NPL data (p < 0.0001) |
| **Model Accuracy** | R² = **0.9669** | XGBoost surrogate model performance |
| **Macro Variables** | **15+** | PDRB, MSME growth, poverty, inflation, investment, etc. |
| **Competition** | **Finalist** / 76 teams | Jatim Datathon 2025 — Top tier |
| **Interpretability** | SHAP + LIME | Full model transparency for stakeholders |

---

## 🚀 Quick Start

### Prerequisites
- Python ≥ 3.9
- pip / poetry
- (Optional) Docker for isolated environment

### Installation

```bash
# Clone the repository
git clone https://github.com/raindragon14/OpenData-Jatim.git
cd OpenData-Jatim

# Install dependencies
pip install -r requirements.txt

# Run the data pipeline
python main.py

# Launch the Streamlit dashboard
streamlit run app.py
```

### Docker (Alternative)

```bash
docker-compose up --build
```

---

## 📂 Repository Structure

```
OpenData-Jatim/
├── data/                    # Source datasets and processed features
│   ├── raw/                 # Raw CSV/Excel sources
│   └── processed/           # Cleaned and feature-engineered data
├── models/                  # Trained models and model artifacts
│   ├── *.csv               # Model outputs and predictions
│   └── Dashboard_Data*     # Dashboard-ready datasets
├── notebooks/               # Jupyter notebooks (EDA, PCA, modeling)
├── app.py                   # Streamlit web application
├── main.py                  # Data pipeline entry point
└── README.md                # This file
```

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Data Processing** | pandas, NumPy | Data cleaning, transformation |
| **Dimensionality Reduction** | PCA | Feature extraction from 15+ macro variables |
| **ML Modeling** | XGBoost | Surrogate model with high accuracy |
| **Interpretability** | SHAP, LIME | Model explanation for stakeholders |
| **Validation** | SciPy | Statistical testing (Spearman correlation) |
| **Visualization** | Streamlit, Tableau | Interactive dashboards & reports |
| **LLM Integration** | OpenAI API | Policy narrative generation from data |
| **Environment** | Docker, pip | Reproducible setup |

---

## 🔬 Methodology

1. **Data Collection**: Gather 15+ macroeconomic indicators from official East Java statistics
2. **Exploratory Data Analysis**: Identify patterns, correlations, and data quality issues
3. **Dimensionality Reduction**: PCA to create Composite Risk Score from correlated variables
4. **Model Training**: XGBoost trained on historical data, validated against NPL (Non-Performing Loan)
5. **Interpretation**: SHAP values explain feature contributions; LIME provides local explanations
6. **Narrative Generation**: LLM translates numerical risk scores into human-readable policy narratives
7. **Deployment**: Streamlit web app + Tableau dashboard for stakeholders

---

## 🏆 Competition Journey

> **Jatim Datathon 2025** — Open Data Analytics Competition
> Organized by: Dinas Kominfo Jatim · Google · AWS · Western Sydney University
> Competing against 76 teams from East Java universities — **Finalist**

---

## 📊 Dashboard Preview

The project includes two presentation layers:
- **Streamlit App**: Interactive web app for model exploration
- **Tableau Dashboard**: Executive-level visualizations for decision makers

---

## 📬 Contact & Attribution

Built by **Muhammad Reihan Pandanarang**

- 📧 [Email](mailto:reihan@raindragon14.dev)
- 💼 [LinkedIn](https://linkedin.com/in/mreihanpandanarang)
- 🌐 [Website](https://reihanpandanarang.my.id)

---

<div align="center">

*License: MIT — See [LICENSE](LICENSE) for details*

*"Data is the new oil, but only if you refine it."*

</div>
