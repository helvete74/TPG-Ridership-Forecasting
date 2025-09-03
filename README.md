# TPG Ridership Forecasting

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Made with Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-scikit--learn-orange)](https://scikit-learn.org/)

Open data–based project applying **Machine Learning** to forecast ridership on Geneva Public Transport (**TPG**).  
This project was carried out as part of the **EPFL Applied Data Science: Machine Learning** program.

---

## 📌 Project Overview
The goal is to predict the **number of passengers** (boardings) on the TPG network,  
both at the **global level** (entire network, daily ridership) and at the **local level** (specific stop & line).  

Key aspects:
- Integration of **TPG open data** (ridership by stop/line/day).
- Enrichment with **calendar features** (weekday, holidays, vacations).
- Addition of **weather data**.
- Comparison of several **ML models** (Baseline, Ridge, Decision Trees, Random Forest, k-NN, Neural Networks).
- Evaluation with standard metrics (**MAE, RMSE, R²**).

---

## 📊 Datasets
Data sources are **not stored** in this repository but referenced here:

- TPG Open Data Portal → [opendata.tpg.ch](https://opendata.tpg.ch)  
- Dataset: *Ridership per day per stop per line* (boardings/alightings)  
- Weather data: [MeteoSwiss / Open-Meteo](https://open-meteo.com/)  

---

## ⚙️ Installation & Environment
A ready-to-use **Anaconda environment file** is provided: [`adsml.yml`](adsml.yml).  

To create the environment:
```bash
conda env create -f adsml.yml
conda activate adsml


