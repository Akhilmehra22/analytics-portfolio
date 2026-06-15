# FIFA 2022 World Cup Data Insights

An analytical deep dive into player and team performance at the 2022 FIFA World Cup using StatsBomb event data -- tracking every pass, shot, and touch across all 64 matches.

## Key Findings

**Messi vs Mbappé:** Both scored 9 goals but through different profiles. Messi generated 7.6 xG across 34 shots -- high volume, high quality. Mbappé generated only 5.0 xG across 32 shots but outscored his model by 4 goals, making him the tournament's most clinical finisher.

**Biggest Wasted Chances:** Jamal Musiala (Germany) accumulated 1.15 xG across 11 shots and scored zero -- the tournament's most wasteful performer among players with at least 5 shots.

**Best Shot Quality:** Argentina generated the highest xG per shot at 0.19, meaning their average shot had a 19% chance of going in. Their attack wasn't just high volume -- it was high quality.

## Tools Used
- Python (pandas, matplotlib, statsbombpy)
- Tableau Public

## Dashboard
[View the interactive dashboard](https://public.tableau.com/app/profile/akhil.mehra7475/viz/FIFAWorldCup2022PlayerAnalysis/2022FIFAWorldCupPlayerPerformance)

## How to Run
1. Clone the repo
2. Install dependencies: `uv pip install pandas matplotlib statsbombpy`
3. Open `fifa/Fifa-exploration.ipynb` in JupyterLab
4. Run all cells