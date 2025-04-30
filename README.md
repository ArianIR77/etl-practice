# Simple ETL Pipeline for Car Data

This project is a basic **Extract, Transform, Load (ETL)** pipeline implemented in Python. It reads vehicle data from multiple file formats — CSV, JSON, and XML — performs a simple transformation (rounding prices), and writes the cleaned dataset to a single CSV file. The process is also logged with timestamps in a log file.

---

## 🧰 Technologies Used

- Python 3
- pandas
- xml.etree.ElementTree
- glob
- datetime

---

## 📁 Input File Formats

The script can process:
- `.csv` files with car data
- `.json` files in line-delimited format
- `.xml` files structured with `<car>` elements

All formats must include:
- `car_model`
- `year_of_manufacture`
- `price`
- `fuel`

---

## ⚙️ How the Pipeline Works

1. **Extract**:
   - Scans the current folder for all `.csv`, `.json`, and `.xml` files
   - Reads and combines their data into a single DataFrame

2. **Transform**:
   - Rounds all `price` values to two decimal places

3. **Load**:
   - Outputs the transformed data to `transformed_data.csv`

4. **Logging**:
   - Each phase is logged with a timestamp in `log_file.txt`

---

## ▶️ How to Run

Make sure your working directory contains your input files. Then run:
bash
python your_script_name.py
Replace `your_script_name.py` with the name of your Python file (e.g., `etl_script.py`).

---

## 📌 Output Files

- `transformed_data.csv`: Final cleaned dataset
- `log_file.txt`: Log file with ETL progress and timestamps

---

## 📬 Author

**Arian Moslehikhah**  
[GitHub](https://github.com/ArianIR77)
