# 🎮 GamePulse — Big Data Pipeline for an Online Gaming Platform

> *Leveling up data engineering, one Delta table at a time.*

---

## 👾 About the Project

GamePulse is a simulated online gaming platform built to analyze player behaviour, game engagement, and in-game spending patterns. This project implements a full end-to-end big data pipeline using **Databricks** and **PySpark**, following the **medallion architecture** (Bronze → Silver → Gold).

Built as part of **SYST52461 – Big Data Storage and Analysis** at Humber College, Winter 2026.

---

## 👥 Team — Group 6

| # | Name | GitHub |
|---|---|---|
| 1 | Sara Farshadfar | @username |
| 2 | Rodrigo Mayorga Rozo | @username |
| 3 | Aprash Jamwal | @aprashjamwal |
| 4 | Aniket Shinde | @username |

---

## 🏗️ Medallion Architecture

🥉 BRONZE          🥈 SILVER            🥇 GOLD
──────────         ──────────           ──────────
Raw mock     →     Cleaned &      →     Joined &
data               standardized         aggregated

| Layer | What Happens |
|---|---|
| 🥉 Bronze | Raw mock data generated with intentional quality issues — nulls, inconsistent formatting, wrong data types |
| 🥈 Silver | Data is cleaned, standardized, null values handled, and date fields correctly typed |
| 🥇 Gold | Silver tables are joined and aggregated into analysis-ready datasets |

---

## 🗂️ Repository Structure

📁 LevelUp-BigData/
│
├── 📓 notebooks/
│   ├── 01_bronze_data_generation.ipynb    ← Raw mock data generation
│   ├── 02_silver_processing.ipynb         ← Cleaning & standardizing
│   ├── 03_gold_aggregation.ipynb          ← Joins & aggregations
│   └── 04_eda_analysis.ipynb              ← EDA, KPIs & visualizations
│
└── 📄 README.md

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

players ──── player_id ────► game_sessions ◄──── game_id ──── games
│
└──── player_id ────► purchases

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

 *© 2026 Group 6 — SYST52461 Big Data Storage and Analysis*
