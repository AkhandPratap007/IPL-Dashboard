# 🏏 IPL Analytics Dashboard – Power BI

A comprehensive Indian Premier League (IPL) analytics dashboard built in Power BI, leveraging DAX for KPIs and interactive visuals.

---

## 🔍 Features
- Team Performance: Win/Loss, Net Run Rate, runs scored/conceded, season trends
- Player Statistics: Top scorers, wicket-takers, strike rates, consistency
- Match Insights: Toss impact, venue analysis, head-to-head comparisons
- Interactive Filters: Season, team, player, venue, innings, result type

---

## 🧱 Data Modeling
- Star schema  
  - Fact: `Matches`, `Deliveries`  
  - Dimensions: `Teams`, `Players`, `Venues`, `Seasons`
- Proper cardinality and single-direction filters where applicable
- Surrogate keys for stable relationships

---

## 📈 KPIs (examples)
- Total Runs / Wickets / Matches
- Win %,
- Venue Win Bias and Toss Outcome Impact

---

## 🛠️ How to Use
1. Open `IPL-Dashboard.pbix` in Power BI Desktop.
2. Click Transform Data to review queries and schema.
3. Refresh data if you’ve connected to your own CSV/DB source.
4. Use slicers to explore seasons, teams, and players.

---

## 🖼️ Results (Screenshots)

<p align="center">
  <img src="https://github.com/user-attachments/assets/4c854cdd-9a7b-4e48-a42c-b8de8c273805" width="48%" alt="Overview 1"/>
  <img src="https://github.com/user-attachments/assets/aac98f6e-5219-41a3-9f77-474abae9e1b9" width="48%" alt="Overview 2"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/57497db5-5e1c-41aa-8936-4c50ef749098" width="48%" alt="Player/Team Deep Dive"/>
  <img src="https://github.com/user-attachments/assets/aa98a2fb-dc9e-4f5a-9dac-86a0849bb817" width="28%" alt="Mobile/Focused View"/>
</p>

---

## 🚀 Tech Stack
- **Power BI Desktop**
- **Power Query (M)** for ETL
- **DAX** for measures
- Optional: source CSV/DB (matches, deliveries, teams, players)

---


