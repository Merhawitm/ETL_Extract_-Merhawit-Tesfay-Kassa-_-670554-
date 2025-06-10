# ETL Extract Lab

 Merhawit Tesfay
**Student ID:** 670554 

---

## Description

This project demonstrates the difference between **Full Extraction** and **Incremental Extraction** as part of an ETL (Extract, Transform, Load) process. The dataset used is a **synthetic product review dataset** generated using Python, containing 60 records over 60 days.

The notebook performs the following:

1. **Full Extraction** – Loads all available data from the CSV file.
2. **Incremental Extraction** – Loads only records updated since a previously stored timestamp.
3. **Timestamp Update** – Updates the checkpoint time after a successful incremental load.

---

## Tools Used

- Python
- pandas
- numpy
- Jupyter Notebook
- datetime

---

## Project Structure

etl_extract.ipynb
→ Jupyter notebook containing the code for full and incremental extraction.

custom_data.csv
→ Synthetic dataset of product reviews generated using Python.

last_extraction.txt
→ Stores the timestamp of the last incremental extraction.

.gitignore
→ Configuration file to prevent unnecessary files (e.g., cache, logs) from being pushed to GitHub.

README.md
→ This file — explains the purpose, usage, and structure of the project.


---

##  How to Reproduce

1. **Clone or download** the repository from GitHub.
2. Open `etl_extract.ipynb` in **Jupyter Notebook** or **JupyterLab**.
3. Run all cells in order.
   - This will generate `custom_data.csv`.
   - Simulate a past extraction time.
   - Perform full and incremental extractions.
   - Update `last_extraction.txt` after successful extraction.
4. You’ll see printed outputs showing how many rows were extracted in each mode.

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


---
### Submission
This project is submitted as part of:
DSA 2040A - LAB 3 US 2025: Take-Home Lab – Practicing Extraction in ETL


