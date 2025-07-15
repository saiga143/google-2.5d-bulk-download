# 🏙️ Google 2.5D Buildings – Bulk Downloader (Country-Level)

This repository provides a **Jupyter Notebook-based pipeline** for downloading the full set of `.tif` tiles from Google's Open Buildings 2.5D dataset for one or more countries and selected years (between 2016 and 2023).

Google Earth Engine is limited by export quotas and task sizes, making national-scale downloads challenging. This approach bypasses GEE entirely by downloading public `.tif` files directly using the URLs provided by Google.

Here is the link to the original source on HDX platform by Google Research: https://data.humdata.org/dataset/google-open-buildings-temporal

---

## 📦 What's Included

- `download_google_25d.ipynb`  
  → Jupyter Notebook to bulk download tiles by ISO3 code and year  
- `urls/`  
  → Text files (`ISO3_YEAR.txt`) containing one `.tif` URL per line for each country-year combination  
- `country_codes.csv`  
  → Reference CSV listing ISO3 codes and country names for easy lookup   

---

## 🌍 Dataset Overview

The **Google Open Buildings Temporal** dataset includes building-level information such as:

- `building_height`: Estimated building height in meters  
- `fractional_building_count`: Fractional building count per pixel  
- `building_presence`: Confidence layer ranging from 0 to 1

The data is provided at a resolution of 0.5 meters

Each raster is tiled and publicly hosted as `.tif` files. For more about the dataset, visit:  
👉 https://sites.research.google/gr/open-buildings/temporal

---
## 🙏 Acknowledgements

https://sola.kau.se/deprimap/

<img width="373" height="110" alt="image" src="https://github.com/user-attachments/assets/a180a6e3-1b60-429d-b0b8-c14a45e4e190" />

