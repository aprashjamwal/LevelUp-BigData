# 🎮 GamePulse - Big Data Pipeline for an Online Gaming Platform

> *Leveling up data engineering, one Delta table at a time.*

---

## 👾 About the Project

GamePulse is a simulated online gaming platform built to analyze player behaviour, game engagement, and in-game spending patterns. This project implements a full end-to-end big data pipeline using **Databricks** and **PySpark**, following the **medallion architecture** (Bronze → Silver → Gold).

Built as part of **SYST52461 – Big Data Storage and Analysis**, Winter 2026.

---

## 👥 Team: Group 6

| # | Name | GitHub |
|---|---|---|
| 1 | Xian Qin | @enzo-qin |
| 2 | Rodrigo Mayorga Rozo | @rodrimayorga19-hash |
| 3 | Aprash Jamwal | @aprashjamwal |
| 4 | Aniket Shinde | @aniketqxp |

---

## 🏗️ Medallion Architecture

| Layer | Description |
|---|---|
| 🥉 **Bronze** | Raw mock data generated with intentional quality issues - nulls, inconsistent formatting, wrong data types |
| 🥈 **Silver** | Data is cleaned, standardized, null values handled, and date fields correctly typed |
| 🥇 **Gold** | Silver tables are joined and aggregated into analysis-ready datasets for dashboards and EDA |

---

## 🗂️ Repository Structure

| Notebook | Layer | Purpose |
|---|---|---|
| `01_bronze_data_generation.ipynb` | 🥉 Bronze | Raw mock data generation |
| `02_silver_processing.ipynb` | 🥈 Silver | Cleaning & standardizing |
| `03_gold_aggregation.ipynb` | 🥇 Gold | Joins & aggregations |
| `04_eda_analysis.ipynb` | 📊 EDA | KPIs & visualizations |

---

## 📊 Dataset — 4 Tables

| Table | Description | Key Columns |
|---|---|---|
| `players` | Player demographics and account info | player_id, username, age, region, account_type |
| `games` | Game catalog | game_id, title, genre, game_mode |
| `game_sessions` | Session logs per player per game | session_id, player_id, game_id, duration, score, outcome |
| `purchases` | In-game transactions per player | purchase_id, player_id, item_name, category, amount_spent |

---

## 🔗 Table Relationships

| Foreign Key | From Table | To Table |
|---|---|---|
| `player_id` | `game_sessions` | `players` |
| `player_id` | `purchases` | `players` |
| `game_id` | `game_sessions` | `games` |

---

## 🔍 Key Analysis Questions

- 🌍 Which regions and account types drive the most session activity?
- 🕹️ What games generate the highest player engagement?
- 💰 How does spending behaviour differ across player segments?
- 📈 Are there trends in session activity and revenue over time?

---

## 🛠️ Tech Stack

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apache-spark&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD8?style=flat&logo=databricks&logoColor=white)

---

## 🤝 Team Contributions

All team members collaboratively contributed to every stage of the project, including data generation, data processing, analysis, and visualization. While each member took primary responsibility for specific components, all members participated in reviewing, testing, and refining the entire pipeline.

Primary responsibilities were distributed as follows:

- **Xian Qin**  
  Led the development of the Bronze layer (data generation), and contributed to Silver cleaning and overall testing.

- **Rodrigo Mayorga Rozo**  
  Led the Silver layer (data cleaning and transformation), and assisted with Gold aggregation and debugging.

- **Aprash Jamwal**  
  Led the Gold layer and EDA analysis, and contributed to Silver processing and data validation.

- **Aniket Shinde**  
  Led dashboard development and visualization, and contributed to EDA and report writing.

All members actively reviewed each other’s code, contributed improvements, and ensured consistency across the Bronze, Silver, and Gold layers.

---

*© 2026 Group 6 - SYST52461 Big Data Storage and Analysis*
