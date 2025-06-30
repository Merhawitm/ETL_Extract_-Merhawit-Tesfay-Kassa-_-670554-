# ETL Extract & Transform Lab

 **Name**  Merhawit Tesfay
**Student ID:** 670554 

---

## Description

This project demonstrates the difference between **Full Extraction** and **Incremental Extraction** as part of an ETL (Extract, Transform, Load) process. The dataset used is a **synthetic product review dataset** generated using Python, containing 60 records over 60 days.

The notebook performs the following:

1. `etl_extract.ipynb`:  
   - Performs full and incremental extraction from a sample dataset
   - Saves outputs to `transformed_full.csv` and `transformed_incremental.csv`

2. `etl_load.ipynb`:  
   - Loads the transformed data into a structured format (SQLite databases)
   - Saves `full_data.db` and `incremental_data.db` into the `loaded_data/` directory
---

## Tools Used

- Python
- pandas
- numpy
- Jupyter Notebook
- datetime

---

## Project Structure

├── etl_extract.ipynb
├── etl_load.ipynb
├── custom_data.csv
├── transformed_full.csv
├── transformed_incremental.csv
├── last_extraction.txt
├── .gitignore
├── README.md
└── loaded_data/
├── full_data.db
└── incremental_data.db

---

##  How to Reproduce

1. **Clone or download** the repository from GitHub.
. Open `etl_extract.ipynb` in **Jupyter Notebook** or **JupyterLab**.
. Run all cells in order.
   - This will generate `custom_data.csv`.
   - Simulate a past extraction time.
   - Perform full and incremental extractions.
   - Update `last_extraction.txt` after successful extraction.
. You’ll see printed outputs showing how many rows were extracted in each mode.
Clarified that the notebook also performs transformations after extraction.

# 2. Run the Notebooks
Open the project in VS Code or JupyterLab

Run etl_extract.ipynb to:

Simulate full & incremental extraction

Save CSV outputs

Run etl_load.ipynb to:

Load CSVs into SQLite databases

Preview data

# 3. Check Output Files
Extracted CSVs:
transformed_full.csv, transformed_incremental.csv

Loaded SQLite DBs:
loaded_data/full_data.db, loaded_data/incremental_data.db
---

##  Dataset Info

- **Fields**:
  - `review_id`: Unique review identifier
  - `product`: Product type (e.g., Laptop, Phone)
  - `rating`: Review rating (1–5)
  - `review_date`: Date of the review
  - `last_updated`: Timestamp used for incremental logic

- **Record Count**: 60 synthetic entries (1 per day)



### Full Extraction
![image](https://github.com/user-attachments/assets/2386337e-0208-452d-b997-5ef6eb2500a0)

### Incremental Extraction

![image](https://github.com/user-attachments/assets/69c720e5-78e7-47b9-b739-5a72d831ef36)


## Example Output

```text
Extracted 60 rows fully.
Extracted 39 rows incrementally since 2025-04-20 12:00:00.
Updated last_extraction.txt to 2025-05-31 22:15:00

## Transformation Section
Entirely new section added, which includes:

A short explanation of the three required transformation techniques:

Cleaning (remove duplicates)

Enrichment (add rating_category)

Structural (convert review_date to datetime)

Output files generated:
transformed_full.csv and transformed_incremental.csv

---



