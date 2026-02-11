# Exploratory Data Analysis on Pokémon Stats Dataset

## Overview
This repository contains an **Exploratory Data Analysis (EDA)** project
performed on a Pokémon statistics dataset.  
The goal of this project is to understand the dataset structure, analyze
statistical patterns, identify relationships between features, and extract
meaningful insights using both **static and interactive visualizations**.

---

## Dataset
- **Source:** Kaggle  
- **File:** `pokemon_stats_2025.csv`  
- **Description:**  
  The dataset contains information about Pokémon, including:
  - Physical attributes (height, weight)
  - Battle statistics (HP, attack, defense, special stats, speed)
  - Primary and secondary Pokémon types
  - Base experience values

Missing values occur only in the `type_2` column, indicating single-type Pokémon.

---

## Tools & Libraries Used

The following libraries are listed in `requirements.txt` and are used in this project:

- **NumPy**  
  Used for numerical computations and serves as the foundation for data operations.

- **Pandas**  
  Used for loading, cleaning, manipulating, and analyzing tabular data.

- **Matplotlib**  
  Used for basic plotting and figure configuration.

- **Seaborn**  
  Used for statistical data visualization and enhanced plotting aesthetics.

> **Note:**  
> Interactive visualizations in the notebook are implemented using **Plotly**.  
> If Plotly and related dependencies (`plotly`, `nbformat`, `ipython`) are not
> already installed in your environment, they may need to be installed separately
> to enable interactive charts.

---

## Key Analysis Performed

- Dataset overview and statistical summary
- Missing values analysis
- Univariate analysis (distribution of stats)
- Defense-based outlier detection using IQR method
- Categorical analysis of Pokémon types
- Type-based interactive filtering dashboard
- Bivariate analysis (Attack vs Defense, Speed vs Experience)
- Correlation analysis using heatmaps
- Multivariate analysis using scatter matrix plots

Some visualizations are interactive, allowing:
- Hover-based data inspection
- Zooming and panning
- Type-based filtering
- Dynamic legend toggling

---

## Statistical Enhancement

### Outlier Detection (Defense)

The Interquartile Range (IQR) method was used to detect statistical
outliers in the **Defense** stat:

- Q1 (25th percentile)
- Q3 (75th percentile)
- IQR = Q3 − Q1
- Outliers defined as values outside:
  - Q1 − 1.5 × IQR
  - Q3 + 1.5 × IQR

This helps identify Pokémon with exceptionally strong defensive capabilities.

---

## Key Insights
- The dataset contains **250 Pokémon with 13 attributes**.
- Missing values occur only in `type_2`, indicating single-type Pokémon.
- Strong positive correlation exists between:
  - Attack and Special Attack
  - Defense and Special Defense
- Several Pokémon act as outliers with exceptionally high battle statistics.
- Speed shows a positive relationship with base experience.

---

## How to Run the Project

1. **Clone the repository**
   ```bash
   git clone <repository-url>

2. **Navigate to the project directory**
   ```bash
   cd pokemon-eda

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt

4. **Open the notebook**
   ```bash
   jupyter notebook notebooks/Exploratory_Data_Analysis_Pokemon_Stats.ipynb

5. **Run all cells to view the analysis and visualizations.**



