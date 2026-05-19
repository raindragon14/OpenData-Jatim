# OpenData-Jatim

**East Java economic analysis — Composite Risk Score, XGBoost surrogate model, and LLM-powered policy narratives.**

Selected as **Finalist** in the **Jatim Datathon 2025** (Open Data Analytics Competition) organized by Dinas Kominfo Jatim, Google, AWS, and Western Sydney University — competing against 76 teams across East Java universities.

---

## Highlights

| Metric | Value |
|--------|-------|
| Competition | Jatim Datathon 2025 — Finalist |
| Macro variables | 15+ (PDRB, MSME growth, poverty, inflation, etc.) |
| Dimensionality reduction | PCA → Composite Risk Score |
| Validation | Spearman correlation **0.9182** (p < 0.0001) against NPL |
| Surrogate model | XGBoost — **R² = 0.9669** with SHAP/LIME interpretation |
| Deployment | Streamlit web app + Tableau dashboard |
| LLM integration | Translates numerical risk outputs into policy narratives |

---

## Repository Structure

```
├── data/          # Source datasets
├── models/        # Trained XGBoost models
├── notebooks/     # Jupyter notebooks (EDA, PCA, modeling)
├── app.py         # Streamlit web app
└── main.py        # Data pipeline entry point
```

---

Built with Python, XGBoost, PCA, SHAP, and Streamlit. Licensed under MIT.
