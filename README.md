# Pie Charts VM Notebook

## Overview
This Jupyter Notebook processes and visualizes Virtual Machine (VM) allocation and request data from Excel files. It performs data cleaning, merging, and generates pie charts to provide insights into VM usage.

## Requirements
- Python 3.x
- Jupyter Notebook
- Required Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `pygsheets`
  - `gspread`
  - `oauth2client`

## Files Used
- **RequestFileV2.xlsx**: Contains VM request data.
- **VM allocations.xlsx**: Contains VM allocation data.

## Steps in the Notebook
### 1. Import Libraries
   - Loads necessary Python modules for data processing and visualization.

### 2. Load Data from Excel
   - Reads VM request and allocation data from the respective Excel sheets:
     - "Form responses 1" (Requests)
     - "Production" (Allocations)

### 3. Data Cleaning and Preprocessing
   - Removes extra spaces in VM names.
   - Eliminates rows where VM name is missing.
   - Limits `VM allocations.xlsx` data to 108 rows.
   - Converts numeric columns to object types.
   - Fills missing or empty values with "Unknown".

### 4. Merging Data
   - Joins the two datasets using "VM name" as the key.
   - Keeps only records present in both datasets.

### 5. Function: `BaseExcel()`
   - Opens and reads the `RequestFileV2.xlsx` file.
   - Handles errors if the file is missing.

### 6. Visualization
   - Generates pie charts to visualize VM allocation and requests.

## Usage
- Ensure the required Excel files are available in the specified directory.
- Run the notebook step by step to process and visualize the data.
- Modify the file paths if needed for your system.

## Notes
- Ensure dependencies are installed before running the notebook.
- The dataset is preprocessed to handle missing or incorrect values.
- Adjust visualization parameters as needed for better insights.

## Documentation
- [Pygsheets Documentation](https://pygsheets.readthedocs.io/en/stable/authorization.html)
- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/en/stable/)
- [Project Jupyter Official Website](https://jupyter.org/)
- [IPython and Jupyter Guide](https://ipython.readthedocs.io/en/stable/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html/)


