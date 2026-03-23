# 🎮 GamePulse — Big Data Pipeline for an Online Gaming Platform

> *Leveling up data engineering, one Delta table at a time.*

## 👾 About the Project

GamePulse is a simulated online gaming platform built to analyze player behaviour, game engagement, and in-game spending patterns. This project implements a full end-to-end big data pipeline using **Databricks** and **PySpark**, following the **medallion architecture** (Bronze → Silver → Gold).

Built as part of **SYST52461 – Big Data Storage and Analysis** at Humber College.

## 👥 Team — Group 6

| Name | GitHub |
|---|---|
| Sara Farshadfar | @username |
| Rodrigo Mayorga Rozo | @username |
| Aprash Jamwal | @aprashjamwal |
| Aniket Shinde | @username |

## 🗂️ Repository Structure

| Notebook | Purpose |
|---|---|
| 01_bronze_data_generation.ipynb | Mock data generation |
| 02_silver_gold_processing.ipynb | Cleaning, joins, aggregations |
| 03_eda_analysis.ipynb | EDA, KPIs, visualizations |

## 🏗️ Medallion Architecture

| Layer | What happens |
|---|---|
| 🥉 Bronze | Raw mock data with intentional quality issues |
| 🥈 Silver | Cleaned, standardized, and correctly typed data |
| 🥇 Gold | Joined and aggregated tables ready for dashboards |

## 📊 Dataset — 4 Tables

| Table | Description |
|---|---|
| players | Demographics — username, age, region, account type |
| games | Game catalog — title, genre, game mode |
| game_sessions | Session logs — duration, score, match outcome |
| purchases | In-game transactions — item name, category, amount spent |

## 🔍 Key Analysis Questions

- Which regions and account types drive the most session activity?
- What games generate the highest engagement?
- How does spending behaviour differ across player segments?
- Are there trends in session activity over time?

*SYST52461 — Humber College, Winter 2026*
