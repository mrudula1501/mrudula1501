<div align="center">

<h1>Hi, I'm Mrudula 👋</h1>

<p><strong>ML Engineer · Data Scientist · MS Data Science @ University at Buffalo</strong></p>

<p>
I build end-to-end machine learning systems — from messy raw data to deployed models that make real decisions.<br/>
My work spans healthcare AI, time series forecasting, financial ML, and multi-agent LLM systems.
</p>

<p>
<a href="https://mrudula1501.github.io/"><img src="https://img.shields.io/badge/Portfolio-%23000000.svg?style=for-the-badge&logo=firefox&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/dmrudula/"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:mrudulad25@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

</div>

<br/>

---

## 🏆 Hackathon Win

> **UB Hacking 2024** — out of 87 teams

🥇 **Best Use of AI/ML** — OpenAI Sponsor Prize &nbsp;&nbsp;|&nbsp;&nbsp; 🥈 **2nd Place Overall** &nbsp;&nbsp;|&nbsp;&nbsp; 💡 **Most Innovative Architecture**

Built a production-grade multi-agent trading system in 24 hours. Judges called it *"genuinely novel — mirrors how real trading desks operate."*

---

## 🔬 What I've Built

<details open>
<summary><b>🧠 Alzheimer's Disease Detection</b> &nbsp;·&nbsp; Healthcare AI &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/alzheimers-detection">View Repo →</a></summary>

<br/>

Early Alzheimer's detection from MRI scans using a **CNN + SVM hybrid pipeline**. The CNN handles complex spatial feature extraction from brain scans; the SVM provides robust classification with strong generalization on limited medical data.

**Pipeline:**
```
MRI Image  →  Preprocessing  →  CNN Feature Extraction  →  SVM Classifier  →  AD / MCI / CN
```

| Metric | Result |
|--------|--------|
| Classification Accuracy | **92%** |
| Classes | AD · MCI · Cognitively Normal |
| Deployment | Flask REST API for real-time inference |

**Stack:** `Python` `TensorFlow` `Keras` `Scikit-learn` `Flask`

</details>

---

<details open>
<summary><b>📈 Synapse Street</b> &nbsp;·&nbsp; Multi-Agent LLM System &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/Synapse-Street">View Repo →</a></summary>

<br/>

Three coordinated **GPT-4 agents** — Data, Analysis, and Execution — share a Qdrant vector memory and vote on every trade signal. A weighted consensus engine resolves disagreements. High-consensus signals (all 3 agents agree) hit **78% win rate**.

**Architecture:**
```
Market Data + News + SEC Filings
        ↓
  Qdrant Vector Memory (Ada-002 embeddings)
        ↓
  ┌──────────────┬──────────────┬──────────────┐
  │  Data Agent  │Analysis Agent│Execution Agent│
  └──────────────┴──────┬───────┴──────────────┘
                        ↓
              Consensus Engine (LangGraph)
                        ↓
                 BUY / SELL / HOLD
```

| Metric | Result |
|--------|--------|
| Backtest Return | **+42.8%** vs 24.5% buy & hold |
| High-Consensus Win Rate | **78%** |
| Sharpe Ratio | **1.8** vs 1.2 baseline |
| Max Drawdown | **-12%** vs -18% baseline |

**Stack:** `LangGraph` `GPT-4` `Qdrant` `PySpark` `Backtrader` `Streamlit`

</details>

---

<details open>
<summary><b>🦠 Foodborne Illness Forecasting</b> &nbsp;·&nbsp; Public Health · Time Series &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/Foodborne-Illness-Forecasting">View Repo →</a></summary>

<br/>

**Ensemble forecasting system** predicting foodborne illness outbreaks 4 weeks in advance using CDC surveillance data. Stacks Prophet (seasonality), ARIMA (short-term), and Random Forest (feature-heavy) under an XGBoost meta-learner. PELT changepoint detection flags structural breaks — like the -40% reporting drop during COVID-19.

**Pipeline:**
```
CDC NORS + FDA CORE + Weather + Census
        ↓
  Apache Airflow (Daily ETL)
        ↓
  Feature Engineering (lag features, seasonality, geospatial)
        ↓
  Prophet + ARIMA + Random Forest  →  XGBoost Meta-Learner
        ↓
  4-Week Forecast  →  Outbreak Alert (if > 2σ)
```

| Metric | Result |
|--------|--------|
| MAPE | **10.5%** |
| Outbreak Detection Sensitivity | **100%** — zero missed outbreaks |
| Lead Time | **4 weeks** advance warning |
| Estimated Annual Impact | 200+ lives, $50M+ cost savings if deployed |

**Stack:** `Prophet` `ARIMA` `XGBoost` `ruptures` `Airflow` `Streamlit`

</details>

---

<details open>
<summary><b>💳 Fraud Detection ML</b> &nbsp;·&nbsp; Financial ML &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/fraud-detection-ml">View Repo →</a></summary>

<br/>

Fraud detection on **6.3 million transactions** where only 0.129% are fraudulent. Solving extreme class imbalance with SMOTE + cost-sensitive learning, then stacking XGBoost and LightGBM under a meta-learner. Optimized for **F2-Score** (recall-weighted) because missing fraud costs more than a false alarm. SHAP explanations make every prediction auditable.

**Pipeline:**
```
6.3M Transactions  →  Feature Engineering  →  SMOTE  →  XGBoost + LightGBM
        ↓                                                        ↓
  Fraud Score (0–1)  ←  XGBoost Meta-Learner  ←  Stacking Ensemble
        ↓
  Alert if Score > 0.7  →  Case Management
```

| Metric | Result |
|--------|--------|
| ROC-AUC | **0.9992** |
| Recall | **94%** — catches 94 out of 100 fraud cases |
| Precision | **96%** |
| F2-Score | **0.945** |

**Stack:** `XGBoost` `LightGBM` `imbalanced-learn` `SHAP` `Flask` `Docker`

</details>

---

<details open>
<summary><b>🚕 RoutePulse</b> &nbsp;·&nbsp; Distributed Big Data &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/RoutePulse">View Repo →</a></summary>

<br/>

Distributed ML pipeline processing **3.5M+ NYC taxi trips** on a 5-node Hadoop + Spark cluster. Three models: Logistic Regression for payment-type prediction, Naive Bayes for tip forecasting, and DBSCAN for anomaly detection (ghost trips, fare fraud). Achieves **linear scalability** — doubling nodes halves processing time.

| Model | Task | Accuracy |
|-------|------|----------|
| Logistic Regression | Payment type prediction | **91%** |
| Naive Bayes | Tip range prediction | **78%** |
| DBSCAN | Ghost trip / fraud detection | 1.8% anomaly rate flagged |

**Stack:** `PySpark` `Hadoop HDFS` `MLlib` `Docker Compose`

</details>

---

<details open>
<summary><b>⛓️ DeFi Analytics</b> &nbsp;·&nbsp; Blockchain & Databases &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/DeFi-Analytics">View Repo →</a></summary>

<br/>

Relational database system for Ethereum DeFi risk assessment. BCNF-normalized PostgreSQL schema over **10K+ token transfer records** sourced from Google BigQuery. Strategic indexing delivers 50–60% query speedup. Detects 4 suspicious pattern types: large transfers, wallet concentration, velocity spikes, and circular flows.

| Metric | Value |
|--------|-------|
| Normalization | BCNF |
| Query Speedup | 50–60% with indexing |
| Risk Patterns Detected | 4 types |
| Data Integrity | 7 FK constraints · 3 domain checks |

**Stack:** `PostgreSQL` `Python` `Google BigQuery` `Pandas`

</details>

---

## 🛠️ Skills

**Machine Learning & AI**
`Scikit-learn` `XGBoost` `LightGBM` `TensorFlow` `Keras` `PyTorch` `SHAP` `LIME`
`LangGraph` `LangChain` `OpenAI API` `Qdrant` `RAG Pipelines`

**Data Engineering**
`Apache Spark` `Hadoop HDFS` `Airflow` `Pandas` `NumPy` `SQL` `PostgreSQL` `BigQuery`

**Time Series**
`Prophet` `ARIMA` `statsmodels` `pmdarima` `ruptures (PELT)`

**Deployment & Infrastructure**
`Flask` `FastAPI` `Docker` `Streamlit` `AWS` `GitHub Actions`

---

## 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=mrudula1501&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true"/>
&nbsp;&nbsp;
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mrudula1501&layout=compact&theme=tokyonight&hide_border=true"/>

</div>

---

<div align="center">

**Open to full-time ML Engineering · Data Science · Data Engineering roles**<br/>
Let's connect → [linkedin.com/in/dmrudula](https://www.linkedin.com/in/dmrudula/) · [mrudulad25@gmail.com](mailto:mrudulad25@gmail.com)

</div>
