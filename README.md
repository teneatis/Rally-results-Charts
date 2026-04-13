# 📊 Rally Performance Analytics (v2.5)

[![Rally Charts](https://img.shields.io/badge/Rally-Analytics-blue)]()
[![Version](https://img.shields.io/badge/version-2.5-green)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)]()

A technical framework for extraction, processing, and multi-dimensional visualization of rally timing data.

---

## 📖 Table of Contents
- [Rallies Covered](#rallies-covered)
- [Chart Examples (Croatia 2026)](#chart-examples-croatia-2026)
  - [Position Battles (Bump Charts)](#position-battles-bump-charts)
  - [Performance Dashboards](#performance-dashboards)
  - [Stage Repeats Analysis](#stage-repeats-analysis)
  - [Performance Density (Violin Plots)](#performance-density-violin-plots)
  - [Pace Evolution](#pace-evolution)
  - [Self Evolution](#self-evolution)
- [Color Coding Guide](#color-coding-guide)

---

## 🏁 Rallies Covered

| Series | Rallies |
|--------|---------|
| **WRC** | Monte Carlo 2026 / Sweden 2026 / Safari 2026 / Croatia 2026 |
| **Greek** | Egio / Lamias / Olympiakos / Rally Attikis 2026 |

*Browse the `WRC/` and `Greek/` folders to see all rallies – new ones added regularly.*

---

## 🖼️ Chart Examples (Croatia 2026)

All examples below are from `WRC/04_Croatia/`

---

### Position Battles (Bump Charts)

Shows how driver positions evolve stage by stage. Each line = a driver. Lines crossing = position changes.

**Top 20 Overall**
![Top 20 Overall](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/BumpChart_Top20_Overall.png)

**RC2 Top 10 Battle**
![RC2 Top 10](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/BumpChart_RC2_Top10_Battle.png)

---

### Performance Dashboards

Heatmap (% gap to class leader) + classification evolution (cumulative seconds).

| RC1 Dashboard | RC2 Dashboard |
|---------------|---------------|
| ![RC1 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC1.png) | ![RC2 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC2.png) |

| RC3 Dashboard | RC4 Dashboard |
|---------------|---------------|
| ![RC3 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC3.png) | ![RC4 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC4.png) |

**Top 15 Overall Dashboard**
![Top 15 Overall](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_Top15_Overall.png)

> **Note:** If any dashboard image does not load, please refresh or check that the file exists in the repository. GitHub's raw content may sometimes rate-limit large images.

---

### Stage Repeats Analysis

Compares first vs second pass of same stage.

![Repeats - Alan, Senj](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Repeats_Alan%20-%20Senj.png)

![Repeats - Beram, Cerovlje](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Repeats_Beram%20-%20Cerovlje.png)

---

### Performance Density (Violin Plots)

Statistical view of field competitiveness. Wide belly = tight competition. Long tail = large gaps.

| RC1 | RC4 | Overall |
|-----|-----|---------|
| ![RC1 Violin](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/ViolinMatrix_RC1.png) | ![RC4 Violin](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/ViolinMatrix_RC4.png) | ![Overall Violin](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Violin_Overall.png) |

---

### Pace Evolution

Tracks percentage gap consistency across all stages.

**RC1 - Alan, Senj**
![Pace Evolution RC1](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/heatmaps_evolution/Pace_Ev_Alan%20-%20Senj_RC1.png)

**RC3 - Beram, Cerovlje**
![Pace Evolution RC3](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/heatmaps_evolution/Pace_Ev_Beram%20-%20Cerovlje_RC3.png)

---

### Self Evolution

Measures driver's own improvement across repeated stages. Negative (green) = faster on second pass (learning curve).

**RC1 - Beram, Cerovlje**
![Self Evolution RC1](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/heatmaps_evolution/Self_Evolution_Beram%20-%20Cerovlje_RC1.png)

---

## 🎨 Color Coding Guide

| Color | Meaning | Range |
|-------|---------|-------|
| 🟢 Dark Green | Elite pace | 0.0% – 1.5% gap |
| 🟡 Yellow/Orange | Moderate deviation | 1.5% – 6.0% |
| 🔴 Red | Significant loss | > 10.0% |
| 🟣 Purple | Performance regression | Positive value |
| 🟢 Green (Efficiency) | Learning curve | Negative value |

---

## 📜 License

MIT License – see repository for details.

**Version 2.5** | Updated April 2026
