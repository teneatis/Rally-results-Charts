# 📊 2026 Rally Performance Analytics Gallery

This repository is a visual data gallery dedicated to the **2026 Rally Season** (WRC, ERC, and more). In Rallying, performance is measured in two distinct ways: individual **Stage Pace** (speed on a specific road section) and **Overall Classification** (the cumulative time across the entire event).

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
* **The Scale:** We use **Dynamic Normalization**. The fastest driver in a group is set at **1.0**. A driver at **1.02** was 2% slower than their category winner.
* **Insight:** A "fat" violin means the field is tightly packed. A "stretched" violin indicates large gaps between the leader and the rest.

#### B. Performance Heatmaps

*Visualizes consistency and raw pace across the entire itinerary.*

![Heatmap](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_Dashboard.png?raw=true)

* **What it shows:** Every stage's percentage gap (%) from the winner.
* **Insight:** Dark green rows show consistent, high-level pace. Red cells instantly highlight a puncture, a spin, or a mechanical issue in a specific stage.

---

### 2. Overall Classification (The Big Picture)

*Focuses on the cumulative battle for the win.*

#### A. Standings Evolution

*The competitive drama of the rally.*

![Evolution](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_Dashboard.png?raw=true)

* **What it shows:** The time gap (in seconds) between competitors and the leader as the rally progresses.
* **Insight:** Crossing lines represent position swaps on the road. A flat line means the driver is matching the leader's pace, while a rising slope indicates time loss.

#### B. Final Event Dispersion

*The final "verdict" at the finish line.*

![Overall Violin](https://github.com/teneatis/Rally-results-Charts/blob/main/WRC/01_Rally_MonteCarlo_2026/01_Rally_MonteCarlo_2026_Overall_Violin.png?raw=true)

* **What it shows:** The performance gaps at the end of the rally for each machinery class.
* **Insight:** The **Red Diamond** represents the group's mean performance. This reveals if a category was dominated by one driver or if it was a tight battle.

---

## 🛠 Methodology

* **Dynamic Normalization:** Comparisons are made strictly within machinery classes (Category RC1, RC2, etc.) to ensure meaningful data.
* **Smart Zoom:** Chart axes automatically adjust to the data's dispersion, providing high-detail views of close battles.
* **Master Data:** Every event is backed by a **Master CSV** containing stage positions, overall standings, and penalty evolution.

---

## 📁 Directory Structure

* `/[Series]/[Rally_Name]/` -> Visual Gallery (PNG Plots)
* `/data/[Series]/[Rally_Name]/` -> Master Data (Timing & Positions CSV) *in a future version*

---

*Disclaimer: Independent statistical analysis based on publicly available timing data.*
