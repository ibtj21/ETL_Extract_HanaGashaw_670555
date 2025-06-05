# ETL Extract Lab

**Author:** Hana Hailemariam Gashaw
**Student ID:** 670555 

---

## 📘 Description

This Jupyter Notebook (`etl_extract.ipynb`) demonstrates **full and incremental data extraction** techniques using a simulated hospital admissions dataset. It showcases how to perform:

- ✅ Full extraction of all records from the CSV file.
- 🔄 Incremental extraction of only new or updated records since the last extraction time.
- 🕒 Managing and updating the extraction checkpoint for efficient future retrieval.

📒 **Note**:  
The notebook includes **complete documentation** with **markdown explanations** at each step, making it easy to follow and understand the ETL process, even for beginners.


---

## Tools Used

- **Language & Environment:** Python 3.x (Jupyter Notebook)  
- **Libraries:** pandas, numpy, datetime, random

---

## How to Reproduce

1. **Clone or download this repository.**

2. **Run the notebook `etl_extract.ipynb` in Jupyter Notebook or JupyterLab:**

   - The notebook generates a simulated hospital admissions dataset.
   - It performs a full data extraction from the CSV.
   - It demonstrates incremental extraction using a timestamp checkpoint stored in `last_extraction.txt`.
   - The extraction checkpoint updates after each run to track new or updated records.

3. **Data Source:**

   - The data is simulated within the notebook for demonstration purposes.
   - The dataset `hospital_admissions.csv` contains 60 days of hospital admission records with varying severity levels.

---

## 📸 Output Screenshots

### ✅ 1. Full Extraction Output
![Full Extraction](Output_Screenshoots/Full_Extraction.jpg)

### 🔄 2. Incremental Extraction Output
![Incremental Extraction](Output_Screenshoots/Incremental_Extraction.jpg)

### 🕒 3. Updated Last Extraction Timestamp
![Updated Last Extraction](Output_Screenshoots/Updated_last_extraction.jpg)





## Repository Contents

| File                    | Description                                      |
|-------------------------|------------------------------------------------|
| `hospital_admissions.csv` | Simulated hospital admissions dataset (CSV)    |
| `last_extraction.txt`      | Text file storing the last extraction timestamp |
| `etl_extract.ipynb`        | Jupyter Notebook for full and incremental extraction |
| `.gitignore`               | Git ignore file                                  |
| `LICENSE`                  | License information                              |
| `README.md`                | Project documentation (this file)                |
