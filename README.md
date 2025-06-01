# 🏏 IPL Analytics Dashboard - Power BI

![Power BI Dashboard Screenshot](./"C:\Users\akhand pratap\Pictures\Screenshots\Screenshot 2025-04-20 011049.png") *(Replace with actual screenshot path)*

A comprehensive **Indian Premier League (IPL)** analytics dashboard built with **Power BI**, leveraging DAX for advanced calculations and interactive visualizations.

## 🔍 **Features**
- **Team Performance**: Win/loss ratios, runs scored/conceded, and season trends.
- **Player Statistics**: Top scorers, wicket-takers, strike rates, and consistency analysis.
- **Match Insights**: Toss impact, venue analysis, and head-to-head team comparisons.
- **Interactive Filters**: Dynamic filters by season, team, player, and match type.

## ⚙️ **Technical Implementation**
### **Data Modeling**
- Star schema with fact tables (matches, deliveries) and dimension tables (teams, players, venues).
- Established relationships with proper cardinality and cross-filtering.

### **DAX Measures**
```dax
// Example: Dynamic win percentage by team
Win % = 
DIVIDE(
    COUNTROWS(FILTER(Matches, Matches[Winner] = SELECTEDVALUE(Teams[Team]))),
    COUNTROWS(FILTER(Matches, Matches[Team1] = SELECTEDVALUE(Teams[Team]) || Matches[Team2] = SELECTEDVALUE(Teams[Team]))),
    0
)

// Player strike rate (runs/balls faced)
Strike Rate = 
DIVIDE(
    SUM(Deliveries[Batsman Runs]),
    COUNTROWS(FILTER(Deliveries, Deliveries[Batsman] = SELECTEDVALUE(Players[Player]))),
    0
) * 100
