# Synthea Healthcare Data Analysis

This repository contains the documentation and outputs of a data cleaning and preparation task performed on **synthetic healthcare data generated using Synthea**. The datasets include patient-level information across domains such as personal details, medical encounters, allergies, medications, and diagnoses.  

The main objective was to **clean, structure, and standardize the datasets** to make them suitable for further analytical use.

---

## 📑 Contents of the Report
1. **Introduction** – Purpose and scope of the project  
2. **Cleaning Summary for Each Dataset**  
   - patients.csv  
   - encounters.csv  
   - allergies.csv  
   - conditions.csv  
   - medications.csv  
3. **Tools & Techniques Used**  
4. **Final Cleaned Dataset Details**  
5. **Conclusion**

---

## 🧹 Data Cleaning Summary

### patients.csv
- Dropped unnecessary/sensitive columns: `prefix`, `suffix`, `maiden`, `drivers`, `passport`
- Standardized column names to lowercase with underscores
- Converted `birthdate` and `deathdate` to datetime  
- Casted `zip` as string to preserve leading 0s  
- No duplicates found  
- **Final Shape:** `1171 rows × 19 columns`

### encounters.csv
- Standardized column names  
- Converted `start`, `stop` to datetime  
- Removed duplicate records  
- **Final Shape:** `4970 rows × 9 columns`

### allergies.csv
- Standardized column names  
- Allowed nulls in `end` (ongoing allergies)  
- Converted `start`, `stop` to datetime  
- Removed duplicates  
- **Final Shape:** `1491 rows × 6 columns`

### conditions.csv
- Standardized column names  
- Allowed nulls in `stop`  
- Converted `start`, `stop` to datetime  
- Removed duplicates  
- **Final Shape:** `4899 rows × 6 columns`

### medications.csv
- Standardized column names  
- Allowed nulls in `stop`  
- Converted `start`, `stop` to datetime  
- Removed duplicates  
- **Final Shape:** `2104 rows × 6 columns`

---

## ⚙️ Tools & Techniques Used
- **Programming Language:** Python  
- **Libraries:** pandas, numpy, datetime  
- **Environment:** Jupyter Notebook  
- **File Format:** CSV  

---

## 📂 Final Cleaned Datasets
| Dataset        | Rows | Columns | Cleaned Filename          |
|----------------|------|---------|---------------------------|
| patients.csv   | 1171 | 19      | `cleaned_patients.csv`    |
| encounters.csv | 4970 | 9       | `cleaned_encounters.csv`  |
| allergies.csv  | 1491 | 6       | `cleaned_allergies.csv`   |
| conditions.csv | 4899 | 6       | `cleaned_conditions.csv`  |
| medications.csv| 2104 | 6       | `cleaned_medications.csv` |

---

## ✅ Conclusion
All five datasets from Synthea were successfully cleaned and standardized.  
- Unnecessary columns removed  
- Consistent naming conventions applied  
- Data types corrected  
- Duplicates removed  

The cleaned datasets are now **ready for exploratory analysis, dashboarding, and modeling**.  
Each step has been carefully documented to ensure **data consistency and integrity**.
