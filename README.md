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
