# 📊 Data Sources for TPG Ridership Forecasting

This repository does **not** include raw data files, as they are large and remain the property of their original providers.  
Instead, this document lists the sources and instructions to retrieve them.

---

## 🚌 TPG Ridership Data
- **Provider:** Transports Publics Genevois (TPG) – Open Data Portal  
- **Portal:** [https://opendata.tpg.ch](https://opendata.tpg.ch)  
- **Main dataset used:**  
  - *Montées par arrêt par ligne par jour*  
  - Contains daily passenger boardings per stop and per line.  

**Access via API:**  
- Base URL: `https://tpg.opendatasoft.com/api/explore/v2.1/catalog/datasets`  
- Example dataset IDs:  
  - `arrets` → stop identifiers  
  - `montees-par-arret-par-ligne` → daily boardings per stop/line  

**Note:** Some historical data (e.g., 2021) has been archived by TPG in 2025.

---

## 🌦️ Weather Data
- **Provider:** [Open-Meteo](https://open-meteo.com/)  
- **Data used:**  
  - Daily and hourly weather conditions for Geneva (temperature, precipitation, weather codes).  
- **Coordinates of Geneva:**  
  - Latitude: `46.2022`  
  - Longitude: `6.1457`  

---

## 📅 Calendar Data
- **Provider:** [Python Holidays library](https://pypi.org/project/holidays/)  
- **Subset:** Swiss public holidays (canton Geneva, `holidays.CH(subdiv='GE')`).  

---

## 💾 Zenodo Archive (for reproducibility)
To simplify access and avoid repeated API calls, a subset of the TPG ridership data (2021–2025) and weather data has been archived on **Zenodo**:

- [Zenodo Record – TPG Ridership & Weather (2021–2025)](https://zenodo.org/records/16880747)  

**Files included:**
- `arrets.csv` – TPG stops metadata  
- `frequentations_all.<year>.csv` – Ridership (2021–2025, split per year)  
- `frequentations_ligne12.csv` – Subset for line 12  
- `meteo_daily.csv`, `meteo_hourly.csv` – Weather data  

---

## ⚠️ Usage & Licensing
- **Data License:** The TPG datasets are provided under the conditions of their Open Data portal.  
- **Reminder:** Do not redistribute raw datasets in your own repositories. Instead, reference the official sources or the Zenodo archive above.  

---

✉️ For questions about TPG data, please refer to the [TPG Open Data Contact Form](https://opendata.tpg.ch/pages/accueil/).
