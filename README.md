# Football Data Analysis

Three data analysis reports on professional football, built from public data: a team playing style study (Brentford), a season dashboard report (Stade de Reims) and a data-driven recruitment study (replacing Riyad Mahrez). Each report goes from raw data to interpretable visuals and a clear conclusion.

Author: Khalil Moughamir, Computer Science student (Data track), IUT of Reims.

## Contents

| Report | Question | Data | Tools | Report file |
|---|---|---|---|---|
| Brentford FC, playing style | What is Brentford's attacking, defensive and pressing identity in 2025-2026? | Opta | Tableau Public | [PDF](Brentford_Data_Analysis_Khalil_Moughamir.pdf) |
| Stade de Reims, season report | How do players and the team perform, and what tactical signals appear? | FBref (Standard Stats, Scores & Fixtures) | Tableau Public | [PDF](KhalilMoughamir_Reims_DataVisualizationReport_2025-2026.pdf) |
| Replacing Riyad Mahrez | Which profile statistically succeeds Mahrez, at a realistic cost? | FBref, Transfermarkt | Python, Excel | [PDF](Mahrez_Succession_Analysis.pdf) |

---

## 1. Brentford FC: playing style analysis (Premier League, 2025-2026)

49-page visual report on Brentford's identity, organized in six blocks: attacking, chance creation, defense, players, pressing and set pieces. Every chart compares Brentford with the Premier League average and ends with a short written insight.

**Main findings**
- Attack: a selective approach that prioritizes shot quality over shot volume, with a strong conversion rate relative to shot quality. The team scores slightly fewer goals than its expected goals (xG).
- Transition: more than twice the league average share of xG comes from fast breaks, the most distinctive trait of the team.
- Set pieces: a slightly higher share of xG than the league average, a meaningful but not dominant source of chances.
- Defense: the team limits the quality of shots conceded and the share of shots taken inside the box, but concedes slightly more goals than its expected goals against (xGA).
- Pressing: moderately aggressive, with a pressing intensity slightly above the league average and a balanced defensive line.
- Players: attacking output is concentrated around a few players, with Igor Thiago outperforming his xG.

**Metrics used:** xG, xGA, goals vs xG, conversion rate, open play and set piece xG share, transition xG, shots conceded and locations, PPDA, pressing height.

---

## 2. Stade de Reims: season data report (2025-2026)

22-page report with 15 charts, designed to be shared with a technical staff. It combines an individual block and a collective block.

**Individual performance:** goals by player, playing time and attacking impact, contributions per 90 minutes, discipline, starts per player, impact relative to minutes played (under and over-performers).

**Collective and tactical analysis:** team KPIs (35 goals, 1.67 goals per match), workload concentration, main direct contributors, home vs away performance, match-by-match evolution of goals scored and conceded, link between possession and efficiency, results and points per match by formation.

**Takeaway:** the report identifies the key contributors and usage patterns of the squad, and tactical signals such as the home and away context, the possession link and the impact of the formation.

---

## 3. Replacing Riyad Mahrez: multidimensional analysis and recruitment shortlist

29-page study that anticipates the succession of Riyad Mahrez at Al-Ahli by finding a statistically similar, tactically transferable and financially realistic profile.

**Method**
1. Build a proprietary dataset of about 40 left-footed right wingers and wide attacking midfielders, aged 18 to 32, with at least 900 minutes played and a market value up to 25 million euros.
2. Merge advanced metrics (FBref) and market values (Transfermarkt), collected in Excel and exported to CSV, with a reproducible Python pipeline.
3. Select 10 per 90 minute metrics linked to Mahrez's role: expected assists, key passes, progressive passes and carries, expected goals, touches in the box, among others.
4. Normalize the variables, then rank players by cosine similarity to the Mahrez reference profile (Premier League 2022-2023).
5. Validate the ranking visually: PCA projection, creation vs threat and creation vs progression scatter plots, violin plot, boxplot and comparative radars.

**Result:** Luiz Henrique is the closest profile (similarity 0.61), ahead of Kang-in Lee (0.34) and Ritsu Doan (0.26). He is recommended as the priority target for his role continuity, his age and upside, and his tactical transferability. The report also lists the risks: league adaptation and a slightly lower number of touches in the box.

**Limitations:** leagues with incomplete advanced data (Saudi Pro League, Super Lig, Ligue 2, Denmark, Greece) are excluded to keep the dataset consistent. Market value is only a proxy for acquisition cost.

---

## Repository content

The repository contains the three reports as PDF files, to be opened directly from GitHub:

- `Brentford_Data_Analysis_Khalil_Moughamir.pdf`
- `KhalilMoughamir_Reims_DataVisualizationReport_2025-2026.pdf`
- `Mahrez_Succession_Analysis.pdf`

## Skills demonstrated

Data collection and structuring, metric selection and normalization, similarity analysis (cosine similarity, PCA), data visualization with Tableau, analytical storytelling for technical staff.

## Data and usage notes

The underlying data comes from Opta, FBref and Transfermarkt. Raw datasets are not redistributed in this repository. The reports are shared for educational and portfolio purposes.

## Author

Khalil Moughamir
- Portfolio: [khalil-moughamir.vercel.app](https://khalil-moughamir.vercel.app)
- LinkedIn: [linkedin.com/in/khalil-moughamir](https://www.linkedin.com/in/khalil-moughamir)
