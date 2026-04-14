# 📊 Rally Performance Analytics (v2.5)

[![Rally Charts](https://img.shields.io/badge/Rally-Analytics-blue)]()
[![Version](https://img.shields.io/badge/version-2.5-green)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)]()

> *"To finish first, first you have to finish."*

A technical framework for extraction, processing, and multi-dimensional visualization of rally timing data — built on the philosophy that **overall results tell the real story**, not individual stage times.

---

## 📖 Table of Contents
- [Philosophy](#philosophy)
- [Analytical Framework](#analytical-framework)
- [Rallies Covered](#rallies-covered)
- [Chart Types](#chart-types)
  - [Position Battles (Bump Charts)](#position-battles-bump-charts)
  - [Performance Dashboards](#performance-dashboards)
  - [Stage Repeats Analysis](#stage-repeats-analysis)
  - [Self Evolution](#self-evolution)
  - [Pace Evolution](#pace-evolution)
  - [Performance Density (Violin Plots)](#performance-density-violin-plots)
- [Greek Championship Data](#greek-championship-data)
- [Color Coding Guide](#color-coding-guide)
- [Data Sources](#data-sources)

---

## 🎯 Philosophy

Rally is not a sprint championship. It is a **risk management competition** across 20+ special stages where the winner is the driver who best balances pace, caution, and car preservation.

Stage wins measure peak speed. Rally wins measure complete performance. They are different skills.

This project focuses on the **big picture** — cumulative gaps, consistency patterns, position evolution, and dispersion analysis — rather than isolated stage results. A driver can win 15 stages and still lose the rally. The data shows why.

---

## 🔬 Analytical Framework

### Normalization
All stage times are normalized to the stage winner (1.0 = stage winner pace). This removes stage length and allows direct comparison across different stages and rallies.

### Key Metrics
- **Pace Index**: Normalized stage time. Values near 1.0 = competitive. Values above 1.1 = significant gap.
- **Cumulative Gap**: Total seconds lost from overall leader, accumulated stage by stage.
- **Self Evolution**: Percentage difference between first and second pass of repeated stages. Negative = faster on second pass (learning). Positive = slower (deterioration or incident).
- **Dispersion**: Statistical spread of pace within a category. Tight distribution = competitive field. Wide distribution = mixed field quality.

### The Learning Curve Question
When a stage is run multiple times, two competing forces act on the times:
- **Learning effect** (makes you faster): Drivers gain knowledge of the road on each pass
- **Deterioration effect** (makes you slower): Gravel stages degrade with each car through, especially on rough surfaces

This is particularly visible in Greek gravel championship data where three-pass stages reveal which effect dominates at each performance level.

---

## 🏁 Rallies Covered

| Series | Rallies | Surface |
|--------|---------|---------|
| **WRC** | Monte Carlo 2026 | Tarmac / Snow mix |
| **WRC** | Sweden 2026 | Snow / Ice |
| **WRC** | Safari Kenya 2026 | Rough gravel / Dirt |
| **WRC** | Croatia 2026 | Tarmac |
| **Greek** | Rally Sprint Attikis 2026 | Gravel |
| **Greek** | Olympiako | Gravel |
| **Greek** | Egio / Lamias | Tarmac |

*Browse the `WRC/` and `Greek/` folders to see all rallies — new rounds added regularly.*

---

## 🖼️ Chart Types

All examples below are from `WRC/04_Croatia/`

---

### Position Battles (Bump Charts)

Shows how driver positions evolve **stage by stage**. Each line = one driver. Lines crossing = position changes. The narrative of who was fighting whom at each moment of the rally is immediately visible.

**Croatia 2026 — Top 20 Overall**
![Top 20 Overall](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/BumpChart_Top20_Overall.png)

**Croatia 2026 — RC2 Top 10 Battle**
![RC2 Top 10](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/BumpChart_RC2_Top10_Battle.png)

> **Reading tip**: A flat horizontal line = dominant, consistent performance. Sudden vertical drop = incident or retirement. Gradual climb = steady recovery or competitors dropping out.

---

### Performance Dashboards

Combined chart pairing **cumulative gap evolution** (top) with **pace index heatmap** (bottom). The heatmap shows *where* time was lost; the gap chart shows *consequence* over the rally.

| RC1 Dashboard | RC2 Dashboard |
|---------------|---------------|
| ![RC1 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC1.png) | ![RC2 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC2.png) |

| RC3 Dashboard | RC4 Dashboard |
|---------------|---------------|
| ![RC3 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC3.png) | ![RC4 Dashboard](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_RC4.png) |

**Top 15 Overall Dashboard**
![Top 15 Overall](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Dashboard_Top15_Overall.png)

> **Note:** The heatmap uses a **logarithmic color scale** so that large outliers (retirements, incidents) do not destroy the color range for the competitive field.

---

### Stage Repeats Analysis

Compares absolute times when the same stage is run twice. Sorted by first-pass time, with both passes shown side by side. Immediately reveals who improved, who was consistent, and who had incidents on the second pass.

![Repeats - Alan, Senj](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Repeats_Alan%20-%20Senj.png)

![Repeats - Beram, Cerovlje](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Repeats_Beram%20-%20Cerovlje.png)

---

### Self Evolution

Measures each driver's **own improvement** across repeated stages. Shows percentage difference between passes:
- **Negative / Green** = faster on second pass (knowledge gained)
- **Positive / Red** = slower on second pass (incident, deterioration, or gap management)

This chart separates genuine learning from stage-condition effects. When an entire column turns red, it indicates a systematic conditions change (weather, road degradation) rather than individual driver issues.

**RC1 - Beram, Cerovlje**
![Self Evolution RC1](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/heatmaps_evolution/Self_Evolution_Beram%20-%20Cerovlje_RC1.png)

---

### Pace Evolution

Tracks each driver's percentage gap to stage winner **consistently across all stages of a repeated route**. Reveals whether a driver's pace relative to the field improves, deteriorates, or holds steady across passes.

**RC1 - Alan, Senj**
![Pace Evolution RC1](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/heatmaps_evolution/Pace_Ev_Alan%20-%20Senj_RC1.png)

**RC3 - Beram, Cerovlje**
![Pace Evolution RC3](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/heatmaps_evolution/Pace_Ev_Beram%20-%20Cerovlje_RC3.png)

---

### Performance Density (Violin Plots)

Statistical distribution of normalized pace across a category. Shows the **competitive structure** of a class:
- **Narrow, tall violin** = tight competitive field, small gaps
- **Wide belly** = large cluster of drivers at similar pace
- **Long tail** = few drivers well off the pace (or incidents)
- **Values below 1.0** = possible due to normalization to class winner; indicates a driver faster than average in their class

| RC1 | RC4 | Overall |
|-----|-----|---------|
| ![RC1 Violin](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/ViolinMatrix_RC1.png) | ![RC4 Violin](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/ViolinMatrix_RC4.png) | ![Overall Violin](https://raw.githubusercontent.com/teneatis/Rally-results-Charts/refs/heads/main/WRC/04_Croatia/Violin_Overall.png) |

---

## 🇬🇷 Greek Championship Data

Greek national and regional championship data is included alongside WRC, enabling direct comparison across performance levels. The Greek data covers multiple categories including modern RC classes and historical groups (Group 2, 3, 4, A5F2, A7F2).

### The Amateur vs Professional Gap

One of the core research questions driving this project: **how large is the performance gap between Greek club-level crews and professional WRC drivers?**

The data reveals a complete performance pyramid:
- WRC RC1 factory teams: 1.0–1.05 normalized pace (extremely tight)
- WRC RC2/RC3: 1.05–1.25 (competitive but wider spread)
- Greek modern classes: varies significantly by category
- Greek historical groups: different baseline entirely
- Greek club level: gaps of 40–97% to stage winner observed

### Three-Pass Learning Curves

Some Greek rally sprints (such as Rally Sprint Attikis) run a single stage three times — SS1, SS2 and SS3 are the same route. This creates a natural experiment with three data points per driver on identical terrain. The Self Evolution charts for Greek data show the interaction between:
- **Learning effect**: drivers gain knowledge with each pass
- **Road deterioration**: gravel stages degrade with each car through

This is particularly visible in rough gravel conditions where the question becomes: *at what performance level does knowledge overcome terrain?*

---

## 🎨 Color Coding Guide

### Pace Index Heatmap (Discrete Bins — Log Scale)

| Color | Meaning | Range |
|-------|---------|-------|
| 🟢 Dark Green | Elite pace | 0.0% – 1.0% gap |
| 🟢 Light Green | Competitive | 1.0% – 3.0% |
| 🟡 Yellow | Moderate gap | 3.0% – 5.0% |
| 🟠 Orange | Significant gap | 5.0% – 10.0% |
| 🔴 Red | Major loss / incident | > 10.0% |
| 🔴 Deep Red | Retirement / superally | > 100% |

### Self Evolution Heatmap

| Color | Meaning |
|-------|---------|
| 🟢 Green | Faster on second pass (learning) |
| ⬜ Neutral | No significant change |
| 🔴 Red | Slower on second pass (incident / deterioration) |

> **Note on superally times**: When a driver retires and restarts under superally rules, they receive a fixed penalty time (5 minutes slower than the category leader per stage). These appear as consistent large red values across multiple crews on the same stage and are administrative times, not actual pace data.

---

## 📂 Data Sources

Results data is collected from publicly available official timing and results pages.
Crew matching uses **participation numbers** as unique identifiers — unambiguous across all sources regardless of name spelling variations.

---

## 📜 License

MIT License — see repository for details.
