# One-Way & Two-Way ANOVA with MLB Batting Data

A statistics lab using real MLB data from the [Lahman Baseball Database](https://sabr.org/lahman-database/) to explore hypothesis testing via ANOVA.

📺 **Video walkthrough:** [https://www.youtube.com/watch?v=n_s4Cb0EHuI](#)

## What's Covered

- **One-Way ANOVA** — Does batting average differ by batting handedness (R, L, Switch)?
- **Two-Way ANOVA** — Does batting average differ by handedness *and* birth era, and do they interact?
- Post-hoc analysis (Tukey HSD)
- Diagnostic plots (Q-Q plot, boxplot)
- Interaction visualization

## Data

Uses the [Lahman Baseball Database](https://sabr.org/lahman-database/) (Batting, Fielding, People tables), filtered to:
- Position players only
- Minimum 100 at-bats
- 1980 onward

## Key Results

| Test | p-value | Result |
|---|---|---|
| One-Way ANOVA (Handedness) | 0.0025 | Significant |
| Two-Way ANOVA (Handedness) | 0.00018 | Significant |
| Two-Way ANOVA (Era) | < 0.00001 | Significant |
| Two-Way ANOVA (Interaction) | 0.00054 | Significant |

Left vs. right-handed batters differ significantly, and this gap has narrowed for players born after 1980.

## Tech Stack

Python, pandas, sqlite3, statsmodels, seaborn/matplotlib

## Running It

1. Clone the repo
2. `pip install pandas statsmodels matplotlib seaborn scipy`
3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/dalyas/lahman-baseball-database)
4. Run `lahman-anova.ipynb`
