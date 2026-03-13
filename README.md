# Save The Cat? Assessing the Ability to Predict Global Box Office Based on Adherence to Story Structure

**Winner of Michael F. Dacey Award for Most Outstanding Senior Thesis** | Brett Toban

## Abstract

Given an increasingly risk-averse entertainment industry, research into the financial
impact of story structure is highly needed. While there has been much literary scholarship
about story structure, very little research has been produced using mathematical modeling
to estimate financial output. This paper seeks to determine if adherence to the beat
structure from Blake Snyder’s Save The Cat! (2005) can be used to predict global box
office. Using two Ordinary Least Squares models and a Random Forest regression, the
study looks at a sample of 51 films evaluated for beat adherence by Anthropic’s LLM
Claude 3.7 Sonnet. The models fail to find a statistically significant relationship between
deviations from Snyder’s beats and financial output. Outliers rooted in existing
intellectual properties dominated the box office, showing that brand recognition appears
to be a much greater factor than story structure. We conclude that story structure alone
cannot be used to predict global box office.


## Repository Structure

```
Thesis/
├── Analysis/
│   ├── combined_summary_tables.Rmd   # R Markdown: summary stats + model tables
│   └── thesis2.Rproj                 # RStudio project file
├── Data/
│   ├── summary_stats.csv             # Descriptive statistics (n=51)
│   ├── save_the_cat_beat_pages.csv   # Framework's expected beat page ranges
│   ├── model1_ols_avg_deviation.csv  # OLS results: average deviation model
│   ├── model2_ols_all_beats.csv      # OLS results: all 15 beats model
│   └── rf_feature_importance.csv     # Random forest feature importance
├── Outputs/
│   ├── figure1.png                   # Visualization 1
│   ├── figure2.png                   # Visualization 2
│   └── *.tex                         # LaTeX-formatted regression tables
└── TobanThesis.pdf                   # Full thesis document
```

## Reproducing the Analysis

Open `Analysis/thesis2.Rproj` in RStudio, then knit `Analysis/combined_summary_tables.Rmd`. Required packages:

```r
install.packages(c("readr", "kableExtra", "dplyr", "tidyr"))
```
