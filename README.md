# PM2.5 Concentration Dashboard

## 📌 Project Overview

This project analyzes the Annual Mean Concentrations of Fine Particulate Matter (PM2.5) in urban areas, using the WHO dataset. The goal is to study global air pollution trends, assess compliance with WHO air quality guidelines, and classify countries by health risk and data certainty.

## 📂 Dataset

**Source**: WHO Global Health Observatory

**Indicator**: Mean particulates (PM2.5) in urban areas (µg/m³)

**Columns**:

```DIM_TIME```: Year of observation

```GEO_NAME_SHORT```: Country name

```RATE_N```: Mean PM2.5 estimate (µg/m³)

```RATE_NL```: Lower bound of uncertainty

```RATE_NU```: Upper bound of uncertainty

Other metadata (indicator IDs, country codes, etc.)

## 🔎 Analysis Performed
**1. Risk Classification (2019 Baseline)**

- Computed average PM2.5 for each country in 2019.

- Classified countries into Low, Medium, High Risk using WHO Interim Targets:

  - _Low Risk_ → PM2.5 ≤ 15 µg/m³

  - _Medium Risk_ → 15 < PM2.5 ≤ 35 µg/m³

  - _High Risk_ → PM2.5 > 35 µg/m³

This provides a clear picture of which countries face the greatest air pollution risks.

**2. Uncertainty Analysis**

- Computed uncertainty width

- Computed relative uncertainty (%)

- Classified data certainty levels:

  - _High Certainty_ → Relative uncertainty ≤ 20%

  - _Medium Certainty_ → 20–40%

  - _Low Certainty_ → > 40%

This helps identify regions where estimates are more reliable vs less reliable.

**3. Compliance with WHO Guidelines**

- WHO guideline for annual PM2.5 = 5 µg/m³.

- Since no country in the dataset meets this, we compared against WHO Interim Targets (15, 25, 35 µg/m³).

- Analysis shows how many countries fall into each interim category.

## 📊 Key Insights (so far)

No country meets the 5 µg/m³ guideline; even the cleanest country averages ~5.3.

Many countries fall in the Medium Risk (15–35 µg/m³) range.

Countries with very high PM2.5 (above 35 µg/m³) are flagged as High Risk.

Data certainty varies — some regions (e.g., Africa) have wider uncertainty intervals compared to Europe/North America.

## ⚙️ Tools Used

**PowerBI** for visualization.

**Power Query** for data transformation.
