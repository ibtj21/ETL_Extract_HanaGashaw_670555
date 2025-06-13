# DSA2040_PROJECT_3: Full and Incremental Data Extraction

**Author:** Hana Hailemariam Gashaw

---

## Table of Contents
- [Project Description](#project-description)  
- [Objective](#objective)  
- [Tools Used](#tools-used)  
- [Repository Contents](#repository-contents)  
- [Notebook Description](#notebook-description)  
- [Output Screenshots](#output-screenshots)  
- [How to Reproduce](#how-to-reproduce)   
- [License](#license)  

---

## Project Description

This project demonstrates a simple **ETL (Extract, Transform, Load)** pipeline focusing on **full** and **incremental** data extraction and transformation techniques. It uses simulated hospital admissions data to illustrate how to efficiently extract updated records based on a timestamp checkpoint.

---

## Objective

- Generate sample hospital admissions data spanning multiple days.  
- Implement a **full extraction** process to load all data.  
- Implement an **incremental extraction** process that only pulls data updated since the last extraction timestamp.  
- Maintain and update a checkpoint to keep track of the last extraction time.  
- Apply at least three transformation techniques to both full and incremental datasets to prepare them for analysis.  

---

## Tools Used

- **Language & Environment:** Python 3.x (Jupyter Notebook)  
- **Libraries:**  
  - `pandas`  
  - `numpy`  
  - `datetime`  
  - `random`  

---

## Repository Contents

| File                              | Description                                                                 |
|-----------------------------------|-----------------------------------------------------------------------------|
| `hospital_admissions.csv`         | Simulated hospital admissions dataset (CSV); same as the fully extracted data |
| `last_extraction.txt`            | Text file storing the last extraction timestamp                            |
| `etl_extract.ipynb`              | Jupyter Notebook for full and incremental extraction                       |
| `.gitignore`                     | Specifies files/folders ignored by Git                                     |
| `LICENSE`                        | MIT license details                                                        |
| `README.md`                      | Project documentation (this file)                                          |
| `hospital_admissions_incremental.csv` | Simulated hospital admissions dataset extracted starting from a specific time period |
| `transformed_full.csv`           | Transformed hospital admissions dataset                                    |
| `transformed_incremental.csv`    | Transformed incremental data                                               |
| `Output_Screenshoots`            | Screenshots from the results of extraction and transformation              |

---

## Notebook Description

This Jupyter Notebook (`etl_extract.ipynb`) demonstrates **full and incremental data extraction** techniques using a simulated hospital admissions dataset. It showcases how to:
- Generate a **simulated dataset** of hospital admissions for 60 days.  
- Perform a **full extraction** of all records from the generated dataset.  
- Run an **incremental extraction** of only new or updated records since the last checkpoint.  
- Maintain and update the **last extraction timestamp** for efficient future runs.  
- Apply three transformation techniques to both full and incremental datasets to prepare them for analysis, namely:  
  - Data cleaning (e.g., handling missing values and changing data types)  
  - Key restructuring (e.g., generating surrogate keys for better integrity)  
  - Categorization (e.g., grouping ages into categories like child, teenager, etc.)  

**Note:**  
The notebook includes **detailed markdown explanations** for each step, making the extraction and transformation process clear, educational, and easy to follow for students and beginners.

---

## Output Screenshots

### 1. Full Extraction Output
![Full Extraction](Output_Screenshoots/Full_Extraction.jpg)

### 2. Incremental Extraction Output
![Incremental Extraction](Output_Screenshoots/Incremental_Extraction.jpg)

### 3. Updated Last Extraction Timestamp
![Updated Last Extraction](Output_Screenshoots/Updated_last_extraction.jpg)

---

## How to Reproduce

1. **Clone or download this repository.**

2. **Open and run the notebook `etl_extract.ipynb` in Jupyter Notebook or JupyterLab.**

3. **Data Source:**

   - The data is **simulated inside the notebook** for learning and demonstration purposes.  
   - The generated and exported files `hospital_admissions.csv` and `hospital_admissions_incremental.csv` contain admissions with hospital name, severity, timestamps, and other relevant details.

---

## License

This project is licensed under the **MIT License**.  
See the [`LICENSE`](LICENSE) file for more details.
