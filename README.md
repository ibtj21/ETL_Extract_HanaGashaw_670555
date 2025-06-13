# DSA2040_PROJECT_3: Full,Incremental Data Extraction and Transformation

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

This Jupyter Notebook (`etl_extract.ipynb`) demonstrates **full and incremental data extraction transformation** techniques using a simulated hospital admissions dataset. It showcases how to:
### Section_1: Simulated Data Generation  
This notebook begins by generating a **simulated dataset** of hospital admissions spanning 60 days. The dataset includes fields such as patient ID, admission date, hospital name, severity level, and other relevant details.

---

### Section_2: Full Extraction  
A **full extraction** process is implemented to retrieve **all available records** from the generated dataset. This simulates a scenario where the entire data is loaded for the first time or when a complete refresh is required.

---

### Section_3: Incremental Extraction  
The notebook also demonstrates an **incremental extraction** strategy. It filters and retrieves only the **new or updated records** based on a previously stored **timestamp checkpoint**, enabling efficient data updates without redundancy.

#### Checkpoint Management  
A key feature of the incremental process is **checkpoint management**. The notebook reads from a `last_extraction.txt` file that stores the timestamp of the last successful extraction. After each incremental run, this checkpoint is **updated** to ensure that future extractions only include **newly added or modified records** since that time.

---

### Section_4: Transformation – Full Data  
Once the full dataset is extracted, it undergoes several **transformation steps** to prepare the data for analysis. These include:

- **Data Cleaning:** Handling missing values, correcting data types, and removing any duplicates.  
- **Key Restructuring:** Generating **surrogate keys** to uniquely identify records and maintain referential integrity.  
- **Categorization:** Grouping ages into **meaningful categories** such as child, teenager, adult, etc., for easier interpretation and segmentation.

---

### Section_5: Transformation – Incremental Data  
Similarly, the **incrementally extracted data** also undergoes transformation using the same techniques to ensure **consistency with the full dataset**:

- **Data Cleaning:** Ensuring that only valid and clean records are passed on for analysis.  
- **Key Restructuring:** Assigning surrogate keys to new or updated records.  
- **Categorization:** Mapping age values into predefined categories for uniformity.

**Note:**  
The notebook includes **detailed markdown explanations** for each step, making the extraction and transformation process clear, educational, and easy to follow for students and beginners.

---

## Output Screenshots

### 1. Full Extraction Output
![Full Extraction](Output_Screenshoots/Full_Extraction.jpg)

### 2. Incremental Extraction Output
![Incremental Extraction](Output_Screenshoots/Incremental_Extraction.jpg)

### 3. Data Cleaning Output
![Data Cleaning](Output_Screenshoots/Data_Cleaning.jpg)

### 4. Key Restructuring Output
![Key Restructuring](Output_Screenshoots/Key_Restructuring.jpg)

### 4. Categorization Output
![Categorization](Output_Screenshoots/Categorization.jpg)



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
