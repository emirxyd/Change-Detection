# Uzaktan-Alg-lama-ve-De-i-im-Analizi-Change-Detection-
Proje; 10 yıllık arazi kullanımı değişimi (Land Use/Cover Change), Sentinel-2 verileri, QDA (Quadratic Discriminant Analysis) ile makine öğrenmesi sınıflandırması, Sieve gürültü filtresi, Sankey diyagramı ve Markov Zinciri ile 2035 Projeksiyonu gibi ileri seviye teknikleri barındırıyor.
# 🌍 Land Cover Change Detection & Future Projection (2015–2025–2035) using Sentinel-2 & QDA

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=flat-square&logo=python)
![QGIS](https://img.shields.io/badge/QGIS-3.x-green?style=flat-square&logo=qgis)
![Sentinel-2](https://img.shields.io/badge/Data-Sentinel--2%20L2A-orange?style=flat-square)
![Machine Learning](https://img.shields.io/badge/ML-Quadratic%20Discriminant%20Analysis-red?style=flat-square)

An end-to-end Geospatial Data Science & Remote Sensing project analyzing land use and land cover (LULC) changes in the Muğla region (Turkey) over a 10-year period (2015–2025) and modeling future trends for 2035 using Markov Chain Projections.

---

## 📌 Project Overview

Muğla experienced significant ecological transformations due to massive forest fires in 2021 and ongoing urban expansion. This study employs **Post-Classification Comparison (PCC)** on multi-temporal **Sentinel-2 L2A satellite imagery** (10m spatial resolution) to map, quantify, and project environmental degradation and recovery.

### Key Highlights:
* **Multi-Temporal Analysis:** 10-year change detection (Dec 2015 vs. Dec 2025) across 9 distinct land cover classes.
* **Supervised Machine Learning:** Applied **Quadratic Discriminant Analysis (QDA)** for pixel-level classification.
* **Post-Processing Pipeline:** Integrated a custom **Sieve Filter (GDAL/Rasterio)** to remove "salt-and-pepper" noise and isolate genuine land transitions (>2,000 m²).
* **Future Predictive Modeling:** Implemented a **Markov Chain Transition Matrix** to simulate land cover dynamics for the year **2035**.

---

## 📊 Key Findings & Transition Statistics

* **Wildfire Impact Identified:** Analysis quantified **~19,367 hectares** of forest loss transitioned directly into bare soil/burnt land between 2015 and 2025 due to wildfires.
* **Natural Reforestation & Recovery:** **14,448 hectares** shifted from bare soil back to forest cover, indicating active reforestation and natural succession.
* **Bare Soil Expansion:** The "Soil/Bare Land" class experienced the highest overall net gain (+10,000+ ha).

```text
2015–2025 Transition Matrix (Sample Metrics in Hectares):
- Forest -> Forest (Unchanged): ~182,168 ha
- Forest -> Bare Soil (Burnt/Degraded): ~19,367 ha
- Bare Soil -> Forest (Recovered): ~14,448 ha
