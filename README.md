# Activity 1: Task 01

**Dataset Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/501/beijing+multi+site+air+quality+data)

---

## About the Dataset

Here we use the **Beijing Multi-Site Air Quality Dataset**, a real-world hourly air quality monitoring dataset collected across 12 stations in Beijing, China.

The data was compiled as part of a study published in the Royal Society journal examining air quality trends in one of the world's most polluted cities:

> Zhang, S. et al. (2017). *Cautionary tales on air quality improvement in Beijing.* Proceedings of the Royal Society A. https://royalsocietypublishing.org/rspa/article/473/2205/20170457/57438/Cautionary-tales-on-air-quality-improvement-in

---

## Dataset Structure

The dataset structure is as follows:

```
data/
└── PRSA_Data_20130301-20170228/
    ├── PRSA_Data_Aotizhongxin_20130301-20170228.csv
    ├── PRSA_Data_Changping_20130301-20170228.csv
    ├── PRSA_Data_Dingling_20130301-20170228.csv
    ├── PRSA_Data_Dongsi_20130301-20170228.csv
    ├── PRSA_Data_Guanyuan_20130301-20170228.csv
    ├── PRSA_Data_Gucheng_20130301-20170228.csv
    ├── PRSA_Data_Huairou_20130301-20170228.csv
    ├── PRSA_Data_Nongzhanguan_20130301-20170228.csv
    ├── PRSA_Data_Shunyi_20130301-20170228.csv
    ├── PRSA_Data_Tiantan_20130301-20170228.csv
    ├── PRSA_Data_Wanliu_20130301-20170228.csv
    └── PRSA_Data_Wanshouxigong_20130301-20170228.csv
```

### Monitoring Stations

All 12 stations are located across Beijing and its surrounding districts, capturing both urban and suburban air quality levels.

| Station | Area type |
|---|---|
| Aotizhongxin | Urban |
| Changping | Suburban/northern |
| Dingling | Suburban/northern |
| Dongsi | Urban |
| Guanyuan | Urban |
| Gucheng | Urban/western |
| Huairou | Suburban/northeast |
| Nongzhanguan | Urban |
| Shunyi | Suburban/eastern |
| Tiantan | Urban/southern |
| Wanliu | Urban/western |
| Wanshouxigong | Urban |

### Combined Dataset Dimensions

When all 12 files are loaded and combined:

| Metric | Value |
|---|---|
| Total rows | 420,768 |
| Total columns | 18 |
| Stations | 12 |
| Date range | March 2013 – February 2017 |
| Frequency | Hourly |

### Column Reference

| Column | Type | Description |
|---|---|---|
| `No` | int | Row index |
| `year` | int | Year of measurement |
| `month` | int | Month of measurement |
| `day` | int | Day of measurement |
| `hour` | int | Hour of measurement (0–23) |
| `PM2.5` | float | Fine particulate matter ≤ 2.5 µm (µg/m³) |
| `PM10` | float | Coarse particulate matter ≤ 10 µm (µg/m³) |
| `SO2` | float | Sulfur dioxide (µg/m³) |
| `NO2` | float | Nitrogen dioxide (µg/m³) |
| `CO` | float | Carbon monoxide (µg/m³) |
| `O3` | float | Ozone (µg/m³) |
| `TEMP` | float | Temperature (°C) |
| `PRES` | float | Atmospheric pressure (hPa) |
| `DEWP` | float | Dew point temperature (°C) |
| `RAIN` | float | Precipitation (mm) |
| `wd` | str | Wind direction (e.g. NNW, SE) |
| `WSPM` | float | Wind speed (m/s) |
| `station` | str | Station name (added during loading) |

---

## Why we dont use `data.csv` and `test.csv`

These two files contain **stock market price data** — completely unrelated to air quality or Beijing. Both files share the same columns (`Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`) and cover the same date range (July 2018 – June 2020, 503 trading days), but represent two different stocks with different price ranges.


They appear to be leftover files from a separate machine learning exercise on stock price prediction. They contain no pollution measurements, no weather data, no geographic information, and no overlap whatsoever with the Beijing air quality dataset.

For these reasons, `data.csv` and `test.csv` are ignored in all analysis.

---
