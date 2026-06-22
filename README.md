# IPL Data Visualization Dashboard (2008–2024)

**Course:** IFT 533 – Data Visualization and Reporting for IT  
**Professor:** Prof. Asmaa Elbadrawy  
**Team:** Bhavy Patel · Harsh Ramanik Shah · Pooja Kondath · Rishi Nikunjkumar Shah


### **Dashboard URL:** https://public.tableau.com/app/profile/bhavy.patel8319/viz/ipl_dashboard_17821614830350/Dashboard1?publish=yes
---

## Overview

An interactive Tableau dashboard analyzing the Indian Premier League (IPL) from 2008 to 2024. Built on ball-by-ball and match-level data, it surfaces player performance, team strategies, toss impact, and venue trends for cricket analysts, team coaches, fantasy sports users, and researchers.

## Dataset

**IPL Complete Dataset (2008–2024)** sourced from [Kaggle](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020)

| File | Contents |
|------|----------|
| `matches.csv` | Match-level data — venues, teams, toss, result, Player of the Match |
| `deliveries.csv` | Ball-by-ball data — batter, bowler, runs, extras, dismissals |

## Project Phases

### Phase 1 — Planning
- Dataset selection and justification
- Identification of target dashboard users (analysts, coaches, journalists, fantasy players, students)
- 14 analytical questions the dashboard should answer
- Column-level data dictionary for both CSVs

### Phase 2 — Decision Making
- **Visualization tool:** Tableau (primary) + Python/Pandas for preprocessing
- **Preprocessing pipeline:**
  - Merged `matches.csv` and `deliveries.csv` on match ID
  - Dropped unused columns (city, venue, umpires, fielder, etc.)
  - Categorized overs into Powerplay (1–6), Middle (7–15), Death (16–20)
  - Derived batting-first vs. chasing flags from toss outcome logic
  - Aggregated runs, economy, wickets per player/match/season

### Phase 3 — Final Dashboard
- 10 visualizations covering player achievements, team performance, bowling analytics, and match strategy
- Interactive filters: season, team, player search, batting-strategy toggle
- Focused on 2022–2024 seasons for the most recent trends

## Dashboard Components

| # | Question | Chart Type |
|---|----------|------------|
| 1 | Which player won the most Player of the Match awards? | Bar Chart (Top 10) |
| 2 | Average win margin (runs & wickets) per team | Grouped Bar Chart |
| 3 | Team performance: batting first vs. chasing | Stacked Bar Chart |
| 4 | Win % when choosing to bat or field after toss | Pie Chart |
| 5 | Player performance: Powerplay vs. Death overs | Line Chart |
| 6 | Most wickets in death overs (16–20) | Bar Chart |
| 7 | Batters consistently scoring 30+ runs | Bar Chart |
| 8 | Most economical bowlers (last 3 seasons) | Scatter Plot |
| 9 | Best performers in Super Over matches | Bar Chart |
| 10 | Correlation: toss decision vs. match outcome | Stacked Bar Chart |

## Repository Structure

```
ipl-data-visualization/
├── dashboard/
│   └── ipl_dashboard.twbx       # Tableau workbook (open in Tableau Desktop/Public)
├── reports/
│   ├── phase1-planning.docx
│   ├── phase2-decision-making.docx
│   └── phase3-final-dashboard.docx
└── planning/
    └── mural-planning-board.pdf  # Visual planning board (dataset overview, preprocessing, dashboard layout)
```

## How to Open the Dashboard

1. Download [Tableau Public](https://public.tableau.com/en-us/s/download) (free)
2. Open `dashboard/ipl_dashboard.twbx`
3. Use the season, team, and player filters to explore the data
