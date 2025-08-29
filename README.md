# GeoAI for Monthly River Discharge in Piedmont (Italy)

**Author:** Arman Mohammadi  
**Result:** Tuned XGBoost with RS drivers (P, NDVI, ET, Soil Moisture, T2m)  
→ **NSE = 0.686**, **R² = 0.686**, **RMSE ≈ 29.5 m³/s** (test period)

---

## 📖 Project overview
This project explores whether **satellite remote sensing** can reproduce monthly discharge at selected Piedmont river stations using **GeoAI** (XGBoost).  
The work combines **Google Earth Engine** (CHIRPS, MODIS NDVI/ET, ERA5-Land SM & T2m) with Python machine learning.

It serves as:
- A reproducible **GeoAI workflow** for hydrology,
- A complement to **trend analysis** of discharge series,
- A portfolio project for **GeoAI in water resources**.

---

## 🗂 Repo structure

piedmont-geoai-discharge/
├─ README.md
├─ LICENSE
├─ requirements.txt
├─ .gitignore
├─ data/ # (not in repo, see below)
│ ├─ discharge_monthly.csv
│ └─ RS_monthly_plus.csv
├─ src/ # Python scripts
│ ├─ train_rf.py
│ ├─ train_xgb.py
│ ├─ tune_xgb.py
│ └─ train_xgb_plus.py
├─ gee/
│ └─ rs_monthly_plus.js # Earth Engine export script
└─ outputs/ # results (kept as examples)
├─ model_report.txt
├─ station_skill.csv
├─ obs_vs_pred.png
└─ feature_importance.png

## 📊 Results

### Example discharge fit
![Observed vs Predicted discharge](outputs/obs_vs_pred.png)

### Feature importance
![Feature importance](outputs/feature_importance.png)

---

## 🧑‍💻 Quick start

```bash
# 1) create environment
python -m venv .venv
source .venv/bin/activate   # (Windows: .venv\Scripts\activate)

# 2) install requirements
pip install -r requirements.txt

# 3) add your data
#   data/discharge_monthly.csv
#   data/RS_monthly_plus.csv

# 4) train model
python src/train_xgb_plus.py

