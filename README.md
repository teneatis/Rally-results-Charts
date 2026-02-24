# 📊 2026 Rally Performance Analytics Gallery

This repository is a visual data gallery dedicated to the **2026 Rally Season**. Rallying is a unique sport where performance is measured in two distinct ways: individual **Stage Pace** (speed on a specific road section) and **Overall Classification** (the cumulative time across the entire event).

This project translates complex timing data into intuitive competitive analytics using **Python** and **Seaborn**.

---

## 🔍 Visual Analysis Guide

To help you navigate the gallery, here is an explanation of the analytical tools provided for each event:

### 1. Stage Performance & Consistency

*Focuses on individual speed tests (Stages).*

#### A. Stage Pace Distribution (Violin Plots)

*The statistical "fingerprint" of a stage's competitiveness.*

![Violin Plot](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_SS5_Violin.png?raw=true)

* **What it shows:** The distribution of times for Category RC1, RC2, and RC3 within a single stage.
* **The Scale:** 1.0 is the fastest driver in the category. 1.02 means 2% slower pace.
* **Insight:** A "fat" violin means the field is tightly packed.

#### B. Performance Heatmaps

*Visualizes consistency across the itinerary.*

![Heatmap](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_Dashboard.png?raw=true)

* **What it shows:** Percentage gap (%) from the winner per stage.
* **Insight:** Instantly reveals consistency or specific time-loss incidents.

---

### 2. Overall Classification (The Big Picture)

*Focuses on the cumulative battle for the win.*

#### A. Final Event Dispersion (Overall Violin)

*The final "verdict" at the finish line.*

![Overall Violin](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_Overall_Violin.png?raw=true)

* **What it shows:** The cumulative performance gaps at the end of the rally.
* **Interpretation:** The **Red Diamond** represents the group's mean performance. It shows if a category was dominated by one driver or was a tight battle.

#### B. Standings Evolution

*The competitive drama of the rally.*

![Evolution](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_Dashboard.png?raw=true)

* **What it shows:** Time gap from the leader as the rally progresses.
* **Insight:** Crossing lines represent position swaps.

---

## 📁 Directory Structure

* `/gallery/[Series]/[Rally_Name]/` -> Visual Gallery (PNG Plots)
* `/data/[Series]/[Rally_Name]/` -> Master Data (Timing & Positions CSV) *in a future version*

---

*Disclaimer: Independent statistical analysis based on publicly available timing data.*
