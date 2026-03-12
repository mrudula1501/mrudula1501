<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=3&section=header"/>

<br/>

# Mrudula Deshmukh

### ML Engineer &nbsp;·&nbsp; Data Scientist &nbsp;·&nbsp; MS Data Science @ University at Buffalo

<br/>

*I build end-to-end ML systems — from raw messy data to deployed models that make real decisions.*  
*Healthcare AI · Time Series Forecasting · Financial ML · Multi-Agent LLM Systems*

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-24243e?style=for-the-badge&logo=safari&logoColor=a78bfa)](https://mrudula1501.github.io/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-24243e?style=for-the-badge&logo=linkedin&logoColor=a78bfa)](https://www.linkedin.com/in/dmrudula/)
[![Email](https://img.shields.io/badge/Email-24243e?style=for-the-badge&logo=gmail&logoColor=a78bfa)](mailto:mrudulad25@gmail.com)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=3&section=header"/>

</div>

<br/>

## &nbsp;What I've Built

<br/>

<details open>
<summary><b>&nbsp;🧠 &nbsp;Alzheimer's Disease Detection</b> &nbsp;·&nbsp; Healthcare AI &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/alzheimers-detection">View Repo →</a></summary>
<br/>

Early Alzheimer's detection from MRI scans using a **CNN + SVM hybrid pipeline**. The CNN handles complex spatial feature extraction from brain scans; the SVM provides robust classification with strong generalization on limited medical data.

```
MRI Image  →  Preprocessing  →  CNN Feature Extraction  →  SVM Classifier  →  AD / MCI / CN
```

| Metric | Result |
|--------|--------|
| Classification Accuracy | **92%** |
| Classes | AD · MCI · Cognitively Normal |
| Deployment | Flask REST API for real-time inference |

**Stack:** &nbsp;`Python` &nbsp;`TensorFlow` &nbsp;`Keras` &nbsp;`Scikit-learn` &nbsp;`Flask`

<br/>
</details>

---

<details open>
<summary><b>&nbsp;📈 &nbsp;Synapse Street</b> &nbsp;·&nbsp; Multi-Agent LLM System &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/Synapse-Street">View Repo →</a></summary>
<br/>

Three coordinated **GPT-4 agents** — Data, Analysis, and Execution — share a Qdrant vector memory and vote on every trade signal. A weighted consensus engine resolves disagreements. High-consensus signals (all 3 agents agree) hit a **78% win rate**.

```
Market Data + News + SEC Filings
          ↓
  Qdrant Vector Memory (Ada-002 embeddings)
          ↓
  ┌─────────────┬─────────────┬─────────────┐
  │ Data Agent  │Analysis Agent│Execution Agent│
  └─────────────┴──────┬──────┴─────────────┘
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

**Stack:** &nbsp;`LangGraph` &nbsp;`GPT-4` &nbsp;`Qdrant` &nbsp;`PySpark` &nbsp;`Backtrader` &nbsp;`Streamlit`

<br/>
</details>

---

<details open>
<summary><b>&nbsp;🦠 &nbsp;Foodborne Illness Forecasting</b> &nbsp;·&nbsp; Public Health · Time Series &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/Foodborne-Illness-Forecasting">View Repo →</a></summary>
<br/>

**Ensemble forecasting system** predicting foodborne illness outbreaks 4 weeks in advance using CDC surveillance data. Stacks Prophet, ARIMA, and Random Forest under an XGBoost meta-learner. PELT changepoint detection flags structural breaks — including the -40% reporting anomaly during COVID-19.

```
CDC NORS + FDA CORE + Weather + Census
          ↓
  Airflow ETL  →  Feature Engineering
          ↓
  Prophet + ARIMA + Random Forest  →  XGBoost Meta-Learner
          ↓
  4-Week Forecast  →  Outbreak Alert ( > 2σ )
```

| Metric | Result |
|--------|--------|
| MAPE | **10.5%** |
| Outbreak Detection Sensitivity | **100%** — zero missed outbreaks |
| Advance Warning | **4 weeks** |

**Stack:** &nbsp;`Prophet` &nbsp;`ARIMA` &nbsp;`XGBoost` &nbsp;`ruptures` &nbsp;`Airflow` &nbsp;`Streamlit`

<br/>
</details>

---

<details open>
<summary><b>&nbsp;💳 &nbsp;Fraud Detection ML</b> &nbsp;·&nbsp; Financial ML &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/fraud-detection-ml">View Repo →</a></summary>
<br/>

Fraud detection on **6.3 million transactions** where only 0.129% are fraudulent. Solves extreme class imbalance with SMOTE + cost-sensitive learning, then stacks XGBoost and LightGBM under a meta-learner. Optimized for **F2-Score** because missing fraud costs more than a false alarm. SHAP explanations make every prediction auditable.

```
6.3M Transactions  →  Feature Engineering  →  SMOTE
          ↓
  XGBoost  +  LightGBM  →  Stacking Meta-Learner
          ↓
  Fraud Score (0–1)  →  Alert if > 0.7
```

| Metric | Result |
|--------|--------|
| ROC-AUC | **0.9992** |
| Recall | **94%** |
| Precision | **96%** |
| F2-Score | **0.945** |

**Stack:** &nbsp;`XGBoost` &nbsp;`LightGBM` &nbsp;`imbalanced-learn` &nbsp;`SHAP` &nbsp;`Flask` &nbsp;`Docker`

<br/>
</details>

---

<details open>
<summary><b>&nbsp;🚕 &nbsp;RoutePulse</b> &nbsp;·&nbsp; Distributed Big Data &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/RoutePulse">View Repo →</a></summary>
<br/>

Distributed ML pipeline processing **3.5M+ NYC taxi trips** on a 5-node Hadoop + Spark cluster. Three models run in parallel — payment-type classification, tip prediction, and DBSCAN anomaly detection for ghost trips. Achieves **linear cluster scalability**.

| Model | Task | Result |
|-------|------|--------|
| Logistic Regression | Payment type classification | **91% accuracy** |
| Naive Bayes | Tip range prediction | **78% accuracy** |
| DBSCAN | Ghost trip / fraud detection | 1.8% anomaly rate flagged |

**Stack:** &nbsp;`PySpark` &nbsp;`Hadoop HDFS` &nbsp;`MLlib` &nbsp;`Docker Compose`

<br/>
</details>

---

<details open>
<summary><b>&nbsp;⛓️ &nbsp;DeFi Analytics</b> &nbsp;·&nbsp; Blockchain & Databases &nbsp;·&nbsp; <a href="https://github.com/mrudula1501/DeFi-Analytics">View Repo →</a></summary>
<br/>

Relational database system for Ethereum DeFi risk assessment. BCNF-normalized PostgreSQL schema over **10K+ token transfer records** from Google BigQuery. Strategic indexing delivers 50–60% query speedup. Detects 4 suspicious pattern types: large transfers, wallet concentration, velocity spikes, and circular flows.

| Metric | Value |
|--------|-------|
| Normalization | BCNF |
| Query Speedup | **50–60%** with indexing |
| Risk Patterns Detected | 4 types |
| Data Integrity | 7 FK constraints · 3 domain checks |

**Stack:** &nbsp;`PostgreSQL` &nbsp;`Python` &nbsp;`Google BigQuery` &nbsp;`Pandas`

<br/>
</details>

<br/>

---

## &nbsp;Skills

<br/>

**Machine Learning & AI**&nbsp;&nbsp;&nbsp;
`Scikit-learn` `XGBoost` `LightGBM` `TensorFlow` `Keras` `PyTorch` `SHAP`
`LangGraph` `LangChain` `OpenAI API` `Qdrant` `RAG Pipelines`

**Data Engineering**&nbsp;&nbsp;&nbsp;
`Apache Spark` `Hadoop HDFS` `Airflow` `Pandas` `NumPy` `SQL` `PostgreSQL` `BigQuery`

**Time Series**&nbsp;&nbsp;&nbsp;
`Prophet` `ARIMA` `statsmodels` `pmdarima` `ruptures (PELT)`

**Deployment**&nbsp;&nbsp;&nbsp;
`Flask` `FastAPI` `Docker` `Streamlit` `AWS`

<br/>

---

## &nbsp;GitHub Stats

<div align="center">
<br/>

<img height="170" src="https://github-readme-stats.vercel.app/api?username=mrudula1501&show_icons=true&theme=midnight-purple&hide_border=true&count_private=true&include_all_commits=true&title_color=a78bfa&icon_color=a78bfa&text_color=ffffff&bg_color=0d1117"/>
&nbsp;&nbsp;
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mrudula1501&layout=compact&theme=midnight-purple&hide_border=true&title_color=a78bfa&text_color=ffffff&bg_color=0d1117"/>

<br/><br/>

</div>

---

<div align="center">

**Open to full-time roles in ML Engineering · Data Science · Data Engineering**

[linkedin.com/in/dmrudula](https://www.linkedin.com/in/dmrudula/) &nbsp;·&nbsp; [mrudulad25@gmail.com](mailto:mrudulad25@gmail.com)

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0f0c29,50:302b63,100:24243e&height=3&section=footer"/>

</div>
