# 🏙️ Google 2.5D Buildings – Bulk Downloader (Country-Level)

_Detailed blogpost explaining this GitHub repo and scripts can be read here:_ https://sola.kau.se/deprimap/2025/07/15/google-25d-download/

This repository provides a **Jupyter Notebook-based pipeline** for downloading the full set of `.tif` tiles from Google's Open Buildings 2.5D dataset for one or more countries and selected years (between 2016 and 2023).

Google Earth Engine is limited by export quotas and task sizes, making national-scale downloads challenging. This approach bypasses GEE entirely by downloading public `.tif` files directly using the URLs provided by Google.

Here is the link to the original source on HDX platform by Google Research: https://data.humdata.org/dataset/google-open-buildings-temporal

---

## 📦 What's Included

- `25d data download.ipynb`  
  → Jupyter Notebook to bulk download tiles by ISO3 code and year  
- `urls_part1.zip` and `urls_part2.zip`  
  → Text files (`ISO3_YEAR.txt`) containing one `.tif` URL per line for each country-year combination. Download them, unzip them and create one folder named `urls`. It is uploaded two zip folders due to Github filesize limitations.  
- `country_codes.csv`  
  → Reference CSV listing ISO3 codes and country names for easy lookup   

---

## 🌍 Dataset Overview

The **Google Open Buildings Temporal** dataset includes building-level information such as:

- `fractional_building_count`: Fractional building count per pixel 
- `building_height`: Estimated building height in meters  
- `building_presence`: Confidence layer ranging from 0 to 1

The data is provided at a resolution of 0.5 meters. The `.tif` files are downloaded as three-band raster files with the above-mentioned layers.

Each raster is tiled and publicly hosted as `.tif` files. For more about the dataset, visit:  
👉 https://sites.research.google/gr/open-buildings/temporal

---
## 📋 Notes

- The dataset is very large. Some countries (e.g., Nigeria, India) may exceed 100–200 GB.
- Make sure your disk has sufficient space before launching a batch download.
- If any download fails (due to timeout or network issues), you can re-run the notebook to retry only missing files.
---
## ✅ Use Cases

- Urban change detection
- Slum / informal settlement mapping
- Building height modelling
- Population estimation
  
---

## 🙏 Acknowledgements

- Google Research - https://data.humdata.org/dataset/google-open-buildings-temporal
- DEPRIMAP Project- https://sola.kau.se/deprimap/
  
_This code was developed as part of the DEPRIMAP project for large-scale urban deprivation analysis._

<img width="373" height="110" alt="image" src="https://github.com/user-attachments/assets/a180a6e3-1b60-429d-b0b8-c14a45e4e190" />

