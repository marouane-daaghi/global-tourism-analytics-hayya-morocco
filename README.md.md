# 🌍 Global Tourism Analytics | Hayya Morocco

> **AI-powered tourism intelligence dashboard** — Exploratory data analysis, forecasting, and market segmentation using UNWTO global outbound tourism data (1995–2030).

---

## 📌 Project Overview

This project delivers end-to-end tourism data analysis for **Hayya Morocco**, a Moroccan travel and tourism company. The goal is to identify the **top outbound tourism source markets**, analyze historical global travel trends, and generate **AI-powered forecasts** to support strategic business decisions.

Built with Python in a Jupyter Notebook environment, with interactive Plotly visualizations and a scikit-learn forecasting model.

---

## 📊 Key Insights Delivered

| Insight | Value |
|--------|-------|
| 🌐 Global Outbound Tourists (2024) | ~1.9M (filtered dataset) |
| 📅 Latest Year in Dataset | 2024 |
| 🥇 Top Source Country | **Germany** |
| 📈 Forecast Horizon | 2025–2030 |

---

## 🗂️ Dataset

- **Source:** [UNWTO — World Tourism Organization](https://www.unwto.org/tourism-statistics/key-tourism-statistics)
- **Indicator:** `OUTB_TRIP_TOTL_TOTL_TOUR` — Total outbound overnight visitor trips
- **Coverage:** 142 countries | 30 years (1995–2024)
- **Format:** CSV with columns: `indicator_code`, `reporter_area_label`, `partner_area_label`, `year`, `value`

> ⚠️ Data is sourced from the official UNWTO statistics portal. Some country values may be estimates.

---

## 📁 Project Structure

```
hayya-morocco-tourism-analytics/
│
├── 📓 notebook.ipynb               # Main analysis notebook
├── 📂 data/
│   └── tourism_data.csv            # UNWTO outbound tourism dataset
├── 📄 requirements.txt             # Python dependencies
├── 📄 README.md                    # Project documentation
└── 📄 .gitignore
```

---

## 🔬 Analysis Pipeline

```
Raw Data (CSV)
     │
     ▼
1. Data Loading & Cleaning
   └── dropna, astype(int), to_numeric(errors='coerce')
     │
     ▼
2. Exploratory Data Analysis (EDA)
   ├── df.describe()
   ├── Global totals & latest year stats
   └── Top 10 source countries (2024)
     │
     ▼
3. Visualizations (Plotly)
   ├── 📈 Global Outbound Tourism Trend (1995–2024)
   ├── 🗺️ Choropleth World Map
   ├── 📊 Top 10 Countries Sending Tourists Abroad
   └── 🎯 Top Tourism Markets to Target
     │
     ▼
4. Forecasting (scikit-learn)
   ├── LinearRegression on yearly trend
   ├── PolynomialFeatures for non-linear capture
   └── Predictions: 2025–2030
     │
     ▼
5. Final Dashboard Chart
   └── Historical + AI Forecast overlay (Plotly)
```

---

## 📈 Visualizations

| Chart | Description |
|-------|-------------|
| Global Outbound Tourism Trend | Line chart with markers (1995–2024) |
| Global Tourism Outbound Map | Choropleth map by country |
| Top 10 Countries (Bar Chart) | Ranked by outbound trips in 2024 |
| AI Forecast 2025–2030 | Linear Regression overlay on historical trend |

All charts are styled with the **Hayya Morocco AI** branding and UNWTO source attribution.

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/hayya-morocco-tourism-analytics.git
cd hayya-morocco-tourism-analytics
```

### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch the notebook
```bash
jupyter lab notebook.ipynb
```

---

## 🧰 Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=flat&logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-5.x-3F4F75?style=flat&logo=plotly)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.5-F7931E?style=flat&logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/JupyterLab-4.x-F37626?style=flat&logo=jupyter)

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, transformation |
| `numpy` | Numerical operations |
| `plotly.express` | Interactive charts & choropleth maps |
| `plotly.graph_objects` | Custom multi-trace visualizations |
| `sklearn.linear_model` | Linear Regression forecasting |
| `sklearn.preprocessing` | PolynomialFeatures |
| `openpyxl` | Excel file support |

---

## 🤖 Forecasting Methodology

The forecast uses a **Linear Regression** model trained on the aggregated global outbound tourist trend from 1995–2024.

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)

# Forecast 2025–2030
future_years = np.arange(2025, 2031).reshape(-1, 1)
predictions = model.predict(future_years)
```

**Limitations:**
- Linear model does not capture COVID-19 shock recovery dynamics perfectly
- No external macroeconomic features included
- Suitable for trend direction, not precise point estimates

---

## 🏢 About

This project was developed for **[Hayya Morocco](https://hayyamorocco.com)** — a Moroccan tourism company leveraging data intelligence to identify high-value international source markets and optimize acquisition strategy.

**Powered by Hayya Morocco AI** | Data Source: UNWTO

---

## 📜 License

This project is licensed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

## 🙋 Author

**Maroaune**  
Data Scientist | Ivegodata Analytics Platform  
📍 Marrakech, Morocco  

[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?style=flat&logo=github)](https://github.com/your-username)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/your-profile)

---

*⭐ If you found this project useful, consider starring the repository!*
