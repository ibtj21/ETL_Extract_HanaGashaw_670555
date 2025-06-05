# DSA2040_PROJECT_1: Full and Incremental Data Extraction

## Table of Contents
- [Project Description](#project-description)  
- [Objective](#objective)  
- [Tools](#tools)  
- [Repository Contents](#repository-contents)  
- [How to Use](#how-to-use)  
- [ETL Process Design](#etl-process-design)  
- [Reflection & Discussion](#reflection--discussion)  
- [Collaborators / Team Members](#collaborators--team-members)  
- [License](#license)  

---

## Project Description

This project demonstrates a simple **ETL (Extract, Transform, Load)** pipeline focusing on **full** and **incremental** data extraction techniques. It uses simulated hospital admissions data to illustrate how to efficiently extract updated records based on a timestamp checkpoint.

---

## Objective

- Generate sample hospital admissions data spanning multiple days.
- Implement a **full extraction** process to load all data.
- Implement an **incremental extraction** process that only pulls data updated since the last extraction timestamp.
- Maintain and update a checkpoint to keep track of the last extraction time.

---

## Tools

- **Language & Environment:** Python 3.x (Jupyter Notebook)

- **Libraries:**
  - pandas
  - numpy
  - datetime
  - random  

---

## Repository Contents

| File                  | Description                                  |
|-----------------------|----------------------------------------------|
| `hospital_admissions.csv` | Simulated hospital admissions dataset (CSV) |
| `last_extraction.txt`      | Text file storing the last extraction timestamp |
| `data_extraction.py`       | Python script for full and incremental extraction |
| `README.md`                | Project documentation (this file)              |

---

## How to Use

1. Clone the repository.  
2. Run `data_extraction.py` to generate the simulated data and perform full and incremental extractions.  
3. The script will save `hospital_admissions.csv` and update `last_extraction.txt` accordingly.  
4. Modify `last_extraction.txt` to simulate incremental extraction from different points in time.

---

## ETL Process Design

- **Extract**: Load data from the CSV file; simulate full and incremental extraction using timestamp filtering.  
- **Transform**: Filter records updated after the last checkpoint.  
- **Load**: Save the latest timestamp to `last_extraction.txt` to be used in the next incremental extraction.  

The incremental extraction reduces processing by pulling only new or updated records since the last extraction.

---

## Reflection & Discussion

- Using a timestamp checkpoint for incremental extraction improves efficiency by avoiding redundant data processing.  
- Simulated data enables testing without relying on live databases.  
- The approach is scalable and applicable to many real-world ETL scenarios.  
- Future improvements can include automating checkpoint management and integrating with database systems.

---

## Collaborators / Team Members

- Your Name

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
